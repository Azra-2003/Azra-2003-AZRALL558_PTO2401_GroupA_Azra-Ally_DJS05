# DJS05 Project Brief: Building a Redux-Inspired Store for a Tally App

## Redux-Inspired Tally Counter
This project implements a simple Redux-inspired store to manage the state of a tally counter. 

It allows for state updates through actions like adding, subtracting, and resetting the count, and provides a mechanism for subscribers to respond to state changes.

## How to Run

Ensure you have Node.js installed on your system.

Save the provided JavaScript code in a file named store.js.

Run the JavaScript file in your terminal using Node.js:

## bash

node store.js

You should see console output reflecting the initial state and the changes as actions are dispatched to update the state.

## Approach

Store Creation: A createStore function is defined to encapsulate the store logic. The store manages the state, handles dispatching actions, and allows subscribers to listen for state updates.

Reducer: The tallyReducer function manages updates to the count state based on the action dispatched. It processes ADD, SUBTRACT, and RESET actions, while returning the current state for unknown actions.

Subscription: A subscribe method allows listeners to register callback functions that are invoked whenever the state changes, providing a simple way to react to state updates in real-time.

Scenarios: Four scenarios are tested in the code:

Initial State: Logs the starting value of the counter.

Increment: Adds two to the counter.

Decrement: Subtracts one from the counter.

Reset: Resets the counter to zero.

# Challenges Faced

Understanding Reducer Logic: One challenge was ensuring the reducer function correctly handles all defined actions (ADD, SUBTRACT, and RESET). Ensuring that unknown actions default to returning the current state was crucial to preventing unwanted state mutations.

Subscription Handling: Managing the subscription system to ensure that subscribers were notified of every state change without unnecessary updates posed a small challenge. The solution was to properly manage the list of listeners and filter them out correctly upon unsubscription.


