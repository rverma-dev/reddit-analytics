# Project Overview
You are building a reddit analytics platform, where users can get analytics of different sub reddits, where they can see top contents & see category of posts;

You will be using NextJS 15, shadcn, tailwind, Lucid icon

# User Stories for Reddit Analytics Platform
## **1. See List of Available Subreddits & Add New Subreddits**

### **US-1.1**: View List of Subreddits
- **Description**: As a user, I want to see a list of all available subreddits on the platform so that I can browse and select the ones I’m interested in.
- **Acceptance Criteria**:
  - Display a paginated list of subreddits.
  - Each subreddit should show its name, description, and number of posts analyzed. 
  - Each subreddit name should be clickable, leading me to its detailed page  
  - Include a search bar to filter subreddits by name.

### **US-1.2**: Add New Subreddit
- **Description**: As a user, I want to add a new subreddit to the platform so that I can analyze its data.
- **Acceptance Criteria**:
  - Provide an "Add Subreddit" button.
  - Validate the subreddit name (ensure it exists on Reddit).
  - Add the subreddit to the list and start fetching its data in the background.

### **US-1.3**: Loading State for Adding Subreddit
- **Description**: As a user, I want to see a loading state when a new subreddit is being added so that I know the platform is processing my request.
- **Acceptance Criteria**:
  - Show a spinner or progress bar while the subreddit is being added.
  - Display a success or error message once the subreddit is added or fails.

---

## **2. Subreddit Page**

### **US-2.1**: View Subreddit Page
- **Description**: As a user, I want to view a dedicated page for a subreddit so that I can see its analytics and top content.
- **Acceptance Criteria**:
  - Display subreddit name, description, and statistics (e.g., total posts, active users, growth rate).
  - Show tabs for "Top Posts," "Top Comments," and "Themes."

### **US-2.2**: Key Metrics Summary
- **Description**: As a user, I want to see a summary of key metrics for a subreddit so that I can quickly understand its performance.
- **Acceptance Criteria**:
  - Display metrics like total posts, comments, upvotes, and engagement rate.
  - Show a graph of activity over time (e.g., posts per day).

### **US-2.3**: Filter Posts by Date Range
- **Description**: As a user, I want to filter posts by date range so that I can analyze data for a specific period.
- **Acceptance Criteria**:
  - Add a date picker to filter posts and comments.
  - Update the analytics and metrics based on the selected date range.

---

## **3. Fetch Reddit Posts Data in "Top Posts" & Fetch Reddit Comments Data in "Top Comments" for Each Post**

### **US-3.1**: View Top Posts
- **Description**: As a user, I want to see the top posts in a subreddit so that I can understand what content performs best.
- **Acceptance Criteria**:
  - Fetch and display the top posts based on upvotes, comments, or engagement.
  - Show post title, author, upvotes, comments, and publication date.

### **US-3.2**: View Top Comments for Each Post
- **Description**: As a user, I want to see the top comments for each post so that I can understand user engagement.
- **Acceptance Criteria**:
  - Fetch and display the top comments for each post.
  - Show comment author, upvotes, and text.

### **US-3.3**: Sort Top Posts
- **Description**: As a user, I want to sort top posts by different criteria (e.g., upvotes, comments, date) so that I can customize my analysis.
- **Acceptance Criteria**:
  - Add sorting options (e.g., "Most Upvoted," "Most Comments," "Newest").
  - Update the list dynamically based on the selected sorting option.

---

## **4. Analyze Reddit Posts Data in "Themes"**

### **US-4.1**: View Post Themes
- **Description**: As a user, I want to see a breakdown of post themes in a subreddit so that I can understand the main topics of discussion.
- **Acceptance Criteria**:
  - Use NLP to categorize posts into themes (e.g., "Technology," "Politics," "Entertainment").
  - Display a pie chart or bar graph showing the distribution of themes.

### **US-4.2**: Explore Posts by Theme
- **Description**: As a user, I want to click on a theme to see related posts so that I can dive deeper into a specific topic.
- **Acceptance Criteria**:
  - Make themes clickable.
  - Display a list of posts that belong to the selected theme.

### **US-4.3**: Sentiment Analysis for Themes
- **Description**: As a user, I want to see the sentiment analysis for each theme so that I can understand the overall tone of discussions.
- **Acceptance Criteria**:
  - Show sentiment scores (positive, negative, neutral) for each theme.
  - Display a sentiment distribution graph.

---

## **5. Ability to Add New Theme Categories**

### **US-5.1**: Add New Theme
- **Description**: As a user, I want to add a new theme category so that I can customize the analysis for my needs.
- **Acceptance Criteria**:
  - Provide an "Add Theme" button.
  - Allow users to define a new theme name and keywords.
  - Update the theme analysis to include the new category.

### **US-5.2**: Edit or Delete Themes
- **Description**: As a user, I want to edit or delete existing theme categories so that I can refine my analysis.
- **Acceptance Criteria**:
  - Provide an "Edit" and "Delete" option for each theme.
  - Allow users to update theme names or keywords.
  - Reflect changes in the theme analysis immediately.

### **US-5.3**: Confirmation for Deleting Themes
- **Description**: As a user, I want to see a confirmation prompt before deleting a theme so that I can avoid accidental deletions.
- **Acceptance Criteria**:
  - Show a confirmation dialog when deleting a theme.
  - Only delete the theme if the user confirms.

---

## **Additional Enhancements**

### **US-6.1**: Export Analytics Data
- **Description**: As a user, I want to export analytics data (e.g., top posts, themes) as a CSV file so that I can use it for external reporting.
- **Acceptance Criteria**:
  - Add an "Export" button for each section (e.g., top posts, themes).
  - Generate and download a CSV file with the relevant data.

### **US-6.2**: Email Notifications
- **Description**: As a user, I want to receive email notifications when new data is available for a subreddit so that I can stay updated.
- **Acceptance Criteria**:
  - Allow users to subscribe to email notifications for specific subreddits.
  - Send an email when new posts or comments are analyzed.

### **US-6.3**: Compare Multiple Subreddits
- **Description**: As a user, I want to see a comparison of multiple subreddits so that I can analyze their performance side by side.
- **Acceptance Criteria**:
  - Allow users to select multiple subreddits for comparison.
  - Display a comparison chart for metrics like engagement, themes, and growth.


## 1. See list of available subreddits & Add New Subreddits
### Story 1: View List of Tracked Subreddits
**As a** Logged-in user  
**I want to** view a list of subreddits I’m currently tracking  
**So that** I can quickly navigate to each subreddit’s analytics  

**Acceptance Criteria:**
- **Given** I am logged in  
  **When** I go to the “Dashboard” or “Home” screen  
  **Then** I should see a list of subreddits I am already tracking  
- **And** each subreddit name should be clickable, leading me to its detailed page  

### Story 2: Add a New Subreddit
**As a** Logged-in user  
**I want to** add a new subreddit by specifying its name/URL  
**So that** I can begin fetching and analyzing its data  

**Acceptance Criteria:**
- **Given** I am on the “Add Subreddit” form/page  
  **When** I enter a valid subreddit name (e.g. `r/technology`)  
  **Then** the system should verify the subreddit exists  
  **And** add it to my tracked list  
- **If** the subreddit does not exist,  
  **Then** I should receive an error message  

## 2. Subreddit Page
### Story 1: View Subreddit Overview
**As a** Logged-in user  
**I want to** navigate to a selected subreddit’s page  
**So that** I can see top posts, top comments, and other relevant analytics  

**Acceptance Criteria:**
- **Given** I have clicked on a subreddit in my tracked list  
  **When** the subreddit page loads  
  **Then** I should see an overview that includes:
  - Subreddit name and description (if available)
  - A summary of recent or top posts (titles, upvote counts, etc.)
  - Basic metrics like number of active users, average engagement, etc.

### Story 2: Filter Posts by Time Range
**As a** Logged-in user  
**I want to** filter displayed subreddit posts (e.g. last 24 hours, last week, last month)  
**So that** I can narrow my analytics to a specific timeframe  

**Acceptance Criteria:**
- **Given** I am on the subreddit page  
  **When** I select a time range (e.g. “Past Week”)  
  **Then** only posts from that timeframe should display in the “Top Posts” section  
- **And** analytics (e.g. average upvote count) should recalculate accordingly  

## 3. Fetch Reddit Posts Data in "Top Posts" / Fetch Reddit Comments Data in "Top Comments" for Each Post
### Story 1: Fetch and Display Top Posts
**As a** System  
**I want to** retrieve the most popular posts from a subreddit via the Reddit API  
**So that** I can display them in the “Top Posts” section for users  

**Acceptance Criteria:**
- **Given** a subreddit is tracked  
  **When** the system queries the Reddit API for that subreddit’s top posts  
  **Then** it should store essential data (post title, author, upvotes, etc.) in a database  
- **And** the “Top Posts” component should display these results in descending order of popularity  

### Story 2: Fetch and Display Top Comments for Each Post
**As a** System  
**I want to** retrieve the top comments from each post via the Reddit API  
**So that** users can see the most engaged comments at a glance  

**Acceptance Criteria:**
- **Given** a user expands a post to view comments  
  **When** the system queries the Reddit API for that post’s top-level comments  
  **Then** it should store the comment text, author, upvotes, etc. in a database  
- **And** the “Top Comments” section should display the top N comments in descending order of popularity  

### Story 3: Handle Large Data Volumes Efficiently
**As a** System  
**I want to** implement caching or pagination for both top posts and top comments  
**So that** the user experience remains fast even for subreddits with high activity  

**Acceptance Criteria:**
- **Given** a subreddit with a large volume of posts/comments  
  **When** a user requests top posts or expands comments  
  **Then** the system should handle the data via pagination, caching, or background jobs  
- **And** the user should see results with minimal load times  

## 5. Analyze Reddit Posts Data in "Themes"
### Story 1: Categorize Posts by Theme
**As a** Logged-in user  
**I want to** see each post assigned to a theme category (e.g. “News,” “Discussion,” “Help Request”)  
**So that** I can quickly understand the types of content dominating the subreddit  

**Acceptance Criteria:**
- **Given** the system has a set of pre-defined theme categories  
  **When** a new post is fetched  
  **Then** the system should attempt to match it to one of the theme categories based on keywords or metadata  
- **And** if no theme is applicable, the post remains uncategorized or is flagged for manual review  

### Story 2: View Theme Analytics (Charts/Reports)
**As a** Logged-in user  
**I want to** view the distribution of posts by theme  
**So that** I can gauge which topic areas are most active or popular  

**Acceptance Criteria:**
- **Given** I am on the subreddit’s analytics page  
  **When** I open the “Themes” tab  
  **Then** I should see a chart/graph showing how many posts belong to each theme  
- **And** I should be able to filter by date range or sort by popularity  

## 6. Ability to Add New Theme Categories
### Story 1: Create New Theme Categories
**As a** Logged-in user  
**I want to** add a new theme category (e.g. “Memes”)  
**So that** I can classify relevant posts under that new theme  

**Acceptance Criteria:**
- **Given** I have admin or appropriate permissions  
  **When** I navigate to the “Manage Themes” section and provide a new theme name  
  **Then** the system should add this theme to the list of available categories  

### Story 2: Manage Categorization Logic
**As a** Logged-in user with admin permissions  
**I want to** define rules/keywords to automatically categorize posts under the new theme  
**So that** posts can be automatically filtered without manual intervention  

**Acceptance Criteria:**
- **Given** a new or existing theme  
  **When** I set up keywords or specific post attributes  
  **Then** the system should apply these rules when it fetches new posts  
- **If** the rules match a post’s title or content, the post is automatically categorized  

### Story 3: Edit or Delete Existing Theme Categories
**As a** Logged-in user with admin permissions  
**I want to** edit or delete a theme category  
**So that** I can keep theme definitions up-to-date  

**Acceptance Criteria:**
- **Given** there is a list of existing themes  
  **When** I select a theme to edit  
  **Then** I can update the theme’s name or associated rules  
- **And** if I choose to delete the theme, all posts labeled under that theme become “uncategorized” or are moved to a default category  

# Doc

# Current File Structure