### DISC Studio Week 3: GitHub Basics Practice

Today, we're going to learn how to use basic GitHub commands such as `add`, `commit`, `push`, and `branch`.

Suppose, we're creating a web application that uses JavaScript on the frontend & we want to create a file that contains various helper functions. In particular, we'll create files called `Assets.js` and `Date.js` that contain functions that do the following behavior:

* Capitalize a string
  * Ref: https://flexiple.com/javascript/javascript-capitalize-first-letter/
* Compute the range of a numerical array (the maximum minus minimum element)
  * Ref: https://www.geeksforgeeks.org/find-the-min-max-element-of-an-array-using-javascript/
* Return the current date of the month in numerical format (e.g. today is October 20th, so we'd return 10/20)
  * Refs: https://www.w3schools.com/jsref/jsref_getmonth.asp, https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/getDate

And the function calls will perform the following behavior:
  * capitalize("test") --> "Test"
  * range([0, 9, 3, 2, -1]) --> 10
  * currentDate() --> "10/20" (return string)

We'll do so in the following steps:

1. Create a new file called `Assets.js` and implement the `capitalize(...)` function, described above.
2. In your terminal, type `git status`. This will show which files have been modified / created since the last commit.
3. Add the changes locally on your machine by type `git add`. This essentially tracks and picks on the changes you have made since the last commit.
4. To prepare to push the changes to our remote repository, type, `git commit -m "Implement capitalize function"`. This takes the changes we've tracked locally and gets ready to push them to our remote repository.
5. Finally, type `git push origin main`, which will now push these local changes to the `main` branch on our remote repository.
6. Implement the function `range(...)` in the `Assets.js` file & repeat steps 3-5 (with an appropriate commit message).

Next, we'll practice using branches, which we just discussed on the slides. Suppose we want our final function `currentDate(...)` to go in a separate file called `Date.js` as our previous two functions. This function will be used in separate parts of our application than the previous two functions, so we want to create a different branch for the sake of [modularity](https://www.geeksforgeeks.org/modular-approach-in-programming/).

7. First, create a new local branch called `dateTime` by typing `git branch dateTime main`. This create a new `dateTime` branch off of our `main` branch.
8. Implement the `currentDate(...)` function in the `Date.js` file and repeat steps 3 and 4 (again, with an appropriate commit message).
9. Now, when you're ready to push, instead of pushing to the remote `main` branch, we want to push to a new remote branch called `dateTime`, which we can do via: `git push -u origin dateTime`.
