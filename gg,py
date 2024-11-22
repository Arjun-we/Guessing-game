import streamlit as st
import random
st.title("Number Guessing Game")
st.write("Guess a number between 1 and 100!")

if "target_number" not in st.session_state:
    st.session_state.target_number = random.randint(1, 100)

user_guess = st.number_input("Enter your guess:", min_value=1, max_value=100, step=1, key="guess")

if st.button("Check Guess"):
    target = st.session_state.target_number
    if user_guess < target:
        st.write("Too low! Try again.")
    elif user_guess > target:
        st.write("Too high! Try again.")
    else:
        st.success("Congratulations! You guessed the correct number!")
        # Reset the game
        st.session_state.target_number = random.randint(1, 100)
        st.write("A new number has been generated. Try again!")

if st.button("Reset Game"):
    st.session_state.target_number = random.randint(1, 100)
    st.write("Game reset! Guess a new number.")