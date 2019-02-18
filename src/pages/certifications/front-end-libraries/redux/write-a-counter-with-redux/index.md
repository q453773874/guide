---
title: Write a Counter with Redux
---
## Write a Counter with Redux

This is a stub. <a href='https://github.com/freecodecamp/guides/tree/master/src/pages/certifications/front-end-libraries/redux/write-a-counter-with-redux/index.md' target='_blank' rel='nofollow'>Help our community expand it</a>.

<a href='https://github.com/freecodecamp/guides/blob/master/README.md' target='_blank' rel='nofollow'>This quick style guide will help ensure your pull request gets accepted</a>.

<!-- The article goes here, in GitHub-flavored Markdown. Feel free to add YouTube videos, images, and CodePen/JSBin embeds  -->
const INCREMENT = 'INCREMENT'; // define a constant for increment action types
const DECREMENT = 'DECREMENT'; // define a constant for decrement action types


const counterReducer = (state = 0,action) => {

    switch (action.type) {
        case DECREMENT:
            return state - 1
        case INCREMENT:
            return state + 1
        default:
            return state
    }
}

const incAction = (state) => {
    return {
        type:INCREMENT
    }
}

const decAction = (state) => {
    return {
        type:DECREMENT
    }
}

const store = Redux.createStore(counterReducer); 
// define the Redux store here, passing in your reducers

store.dispatch(incAction())
console.log(store.getState())
store.dispatch(decAction())
console.log(store.getState())
