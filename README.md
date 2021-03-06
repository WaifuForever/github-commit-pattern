# Github-Commit-Patterns
Principles and patterns intended to standardize github commits.

## Why and when you should commit changes?


## What are the benefits of standardizing commits?

## Commmit Pattern:

Let's split commits in 5 differents types:

### Fix
  When you solve a previously or not identified issue
  ```
  git commit -m "fix: user controller index function"
  ```
 
  
### Add
  When you add a new feature into your project
  ```
  git commit -m "add: user controller sign-up function"
  ```
  
### Remove
  When you remove a feature, comments or function from your project, you use a remove commit.
  
  All remove commits refer to a remove action, you just need to detail what you deleted from the code.
   ```
  git commit -m "remove: like function"
  ```
  
  ```
  git commit -m "remove: blank spaces inside list function"
  
  ```
 
### Update
  When you make minor changes in the code, such as changing variables name, changing loop logic
  ```
  git commit -m "update: page url"
  ```
  You can especify your action adding a verb on it 
  
  ```
  git commit -m "update: send custom return for empty list"
  ```
  
  ```
  git commit -m "update: rename user products property"
  ```
  
### Refactor
  When you make major changes in the code, such as remaking all the logic in particular file or feature;
  ```
  git commit -m "refactor: profile page layout"
  ```

## Documenting issues
  When you identify a issue in the code and you're not capable do solve this in the moment.
  Every unsolved issue needs to be documented somewhere, you can keep this inside readme.md or another file.   
 
  Example:
  ```
  {
  "001" : send duplicated user_id back to the client"
  }
  
  ```
  
  if you still not solve this issue and want to send another commits you should do as shown:
  
  ```
  git commit -m "add: user controller delete function [001]"
  ```
  
  always inform if the documented issue is solved or not in the current commit  
  if all documented issues are solved you can type empty square brackets [] or just omit them

  ```
  git commit -m "add: user controller delete function []"
  ```
  
  also right:
  ```
  git commit -m "add: user controller delete function"
  ```
  
  Never delete a documented issue from the file where you are store them, this is way you will always know which fixed or unfixed issues are in the commit

## On progress commits // Broken features
  If you are adding a new feature into your project, and you couldn't finish it. You can register your progress inside the commit as shown:
  
  ```
  git commit -m "add: user middleware valid delete !!"
  ```
  
  ```
  git commit -m "add: user middleware valid delete 2/?"
  ```
  
  ```
  git commit -m "add: user middleware valid delete 3/3"
  ```
    
  Let's suppose you're struggling to implemeting a certain function and don't want to delay the project development. 
  You can commit the unfinished/broken feature as complete and add a issue.
  
  ```
  git commit -m "add: user middleware valid delete !!"
  ```
  Commiting unfinished feature as complete.
  ```
  git commit -m "fix: user middleware valid delete"
  ```
  
  Adding a issue.
  ```
  {
  "003" : user middleware valid delete does not validate req.query"
  }
  
  ```
  
  Please remember to report the unresolved issue in all upcoming commits until you have this fixed.


## Conventions
  Always use Present, ask "what does this commit do?" then read the answer: "update: product findone() middleware"
  ```
  git commit -m "update: use cors":
  ```
  
  ```
  git commit -m "update: send manga status back to the client"
  ```
  
  Using text inside commit:
  ```
  git commit -m "add: 'admin/index' route"
  ```

