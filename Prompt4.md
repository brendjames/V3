# General Development Rules

You should do task-based development. For every task, you should write the tests, implement the code, and run the tests to make sure everything works. 

Read from the README.md file to understand the project requirements and the features you need to implement. This is VITAL to your success.

Start with the first feature and work your way down the list.

Create a ToDo list in the project's memory file and update it as you complete tasks.

## Retain Memory

There will be a memory file for every project.Create a memory.md file and use it. 

The memory file will contain the state of the project, and any notes or relevant details you'd need to remember between chats.

Keep it up to date based on the project's current state. 

Do not annotate task completion in the memory file. It will be tracked in the to-do list.

## Update development guidelines

If necessary, update the development guidelines to reflect anything you've learned while working on the project.

I'll help you add a social media aspect to your social project. This would be a great enhancement to make the platform more engaging and interactive. Let me suggest some features and implementation approaches:

## Social Media Features for  Finance

Here are some social features that would work well with your stock trading platform:

### 1. User Profiles
Add personalized profiles where users can showcase their investment performance, trading style, and bio.

### 2. Friend/Follow System
Allow users to follow others whose trading strategies they admire.

### 3. Activity Feed
Create a feed where users can see recent trades and portfolio changes from people they follow.

### 4. Trading Groups/Communities
Enable users to create or join investment clubs where they can discuss strategies.

### 5. Trade Sharing
Let users share their successful (or unsuccessful) trades with commentary.

### 6. Leaderboards
Show top performers based on portfolio growth percentage.

### 7. Comments and Reactions
Allow users to comment on trades or react with emojis.

Let's start implementing these features. First, let's examine the database structure we'll need to add:I've examined your Flask application and can now provide detailed implementation suggestions for adding social media features to your C$50 Finance project.

## Implementation Plan for Social Features

Based on your existing code structure, here's how we can implement social media capabilities:

### 1. Database Structure Additions

First, we'll need to add new tables to your database:

- **profiles** - Store user profile information
- **followers** - Track who follows whom
- **posts** - Allow users to share trade ideas or portfolio updates
- **comments** - Enable commenting on posts
- **likes** - Store reactions to posts
- **groups** - Create investment communities
- **group_members** - Track group membership

### 2. New Routes to Implement

Let's add these routes to your Flask application:

1. `/profile` - View and edit user profiles
2. `/profile/<username>` - View other users' profiles
3. `/feed` - Social activity feed showing followed users' activities
4. `/follow/<username>` - Follow another user
5. `/unfollow/<username>` - Unfollow a user
6. `/post/new` - Create new posts about trades or investment ideas
7. `/post/<post_id>` - View a specific post with comments
8. `/groups` - View available investment groups
9. `/group/<group_id>` - View a specific group
10. `/leaderboard` - Display top performing users

### 3. Profile Enhancement

First, let's enhance the user registration to include profile details. Here's what we can do:

1. Expand the users table to include bio, profile picture, privacy settings
2. Create a new profile page that showcases:
   - Portfolio performance charts
   - Recent trading activity
   - Investment philosophy/bio
   - Followers/following count
   - Achievement badges based on trading success

### 4. Frontend Changes

We'll need to add new templates and modify your layout to include:
- A social feed section on the homepage
- Navigation links for social features
- User profile components
- Post creation and commenting interfaces

### 5. Trade Sharing Feature

This would be a killer feature - when users make trades, they can optionally share them with comments about their strategy, creating content for the social feed.

## Next Steps

Here's how I recommend getting started:

1. First, let's modify your database schema to add the social tables
2. Then implement the user profile enhancements
3. Add the follow/follower system
4. Build the activity feed showing trades from followed users
5. Implement posting, comments, and reactions
6. Add groups and leaderboards

