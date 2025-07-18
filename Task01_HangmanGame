import random

words = ['cursor', 'hangman', 'vscode', 'collab', 'game']
word = random.choice(words)
guessed_letters = []
attempts = 6

print("Welcome to Hangman Game")
print(" _ " * len(word))

while attempts > 0:
    guess = input("Guess a letter: ").lower()

    if len(guess) != 1 or not guess.isalpha():
        print("Write one alphabet only!")
        continue

    if guess in guessed_letters:
        print("This letter is already chosen. Guess another letter!")
        continue

    guessed_letters.append(guess)

    if guess in word:
        print("Correct guess!")
    else:
        attempts -= 1
        print(f"Wrong! {attempts} attempts left.")

    displayed_word = " ".join([letter if letter in guessed_letters else "_" for letter in word])
    print(displayed_word)

    if "_" not in displayed_word:
        print(f"Congratulations! 🎉 The correct word is: {word}")
        break

else:
    print(f"Game Over! The correct word was: {word}")
