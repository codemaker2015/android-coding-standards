# Android Coding Standards

## Table of contents

* [Code](#code)
    * [Style](#style)
    * [Indentation](#indentation)
    * [Line length](#line-length)
    * [Whitespace](#whitespace)
    * [Imports](#imports)
* [XML](#xml)
    * [Indentation](#indentation)
    * [Structure](#structure)
    * [Id names](#id-names)
    * [Example](#example)
* [Documentation](#documentation)
    * [Javadoc](#javadoc)
    * [Comments](#comments)
* [Version control](#version-control)
    * [Commits](#commits)
    * [Branching](#branching)
    * [Review](#review)
    * [Comments](#comments)

## Code
#### Style
Follow the official Android code style guidelines: [http://source.android.com/source/code-style.html](http://source.android.com/source/code-style.html)

[Importance of coding standards and best practices in software development](https://codemaker2015.medium.com/importance-of-coding-standard-and-best-practices-in-software-development-ac667a80254d)

#### Indentation
Use 4 spaces per indentation level and no tabs.

#### Line Length
Stick within the 120 char line limit. Use line breaks to split up code according to the style guidelines.

#### Whitespace
Code should not have any trailing whitespace to avoid creating unnecessary diff issues. Please setup your IDE to remove these as a save action.

#### Imports
Please setup your IDE to remove all unused imports as a save action.

## XML

#### Indentation
Use 4 spaces per indentation level and no tabs.
Each attribute should appear on its own line.

#### Structure
XML tags should be ordered as follows: 'xmlns' first, then id, then layout_width and layout_height then alphabetically. 

Add a space between the closing slash and the final attribute. 

Eg. ```android:textSize="10dp" />```

#### IDE Auto format

Automatic formatting rules for our coding standards are stored in an Android Studio file inside the root of this repository. Please use File > Import Settings and select [android_studio_settings.jar](https://github.com/codemaker2015/android-coding-standards/blob/master/android_studio_settings.jar) to ensure you get the same rules.

#### Id names
Layout resource ids should use the following naming convention where possible:<br/>
```<layout name>_<object type>_<object name>```<br/>
Eg.
```
friends_listview_icon
friends_item_imageview_follow_icon
```

#### Example
Given a layout called login.xml:
```
<?xml  version="1.0"  encoding="utf-8"?> 
<LinearLayout 
    xmlns:android="http://schemas.android.com/apk/res/android" 
    android:layout_width="match_parent" 
    android:layout_height="match_parent"
    android:orientation="vertical" > 

    <!-- Avatar icon -->
    <ImageView
        android:id="@+id/login_imageview_avatar" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" />
</LinearLayout> 
```

## Documentation

#### Javadoc
Any new classes that are committed must include a class descriptor Javadoc along with:
```@author name@address.com```

Eg: ```@author codemaker2015@gmail.com```

Javadoc any public methods, variables and constants. Javadoc private methods where beneficial.

#### Comments
Use in-line commenting to help the next developer who might be editing your code, even if it seems obvious now. Inline comments should appear on the line above the code your are commenting.
Comment XML View elements using ```<!-- Comment -->```.

## Version control

#### Commits
You should break up commits into smaller, related changes so it’s clear what bugs or features you’re fixing or adding.

Commit often to break down how much work you need to do between commits and make it easier for your team members to review your code.

Write clear commit messages and should be a max of 50 characters and separated from the body of your code by a blank line.

#### Branching
Follow a branching plan to track different lines of development, avoid merge conflicts, prevent overwriting of existing changes, and avoid lost updates.

#### Review

Test and review before you commit to make sure your code works as expected and doesn’t conflict with other changes made by other developer.

#### Comments

No commented out code must be committed unless you have a very good reason that is clearly described in a comment by the code you are ommitting.



