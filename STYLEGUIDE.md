# Clerk Docs Styleguides

These are the guidelines we use to write our docs.

## 1. Write with consistency

### 1.1 Use American English

Clerk is an American company and the epicenter of our development community is located in America's tech community. For that reason, we use the American flavor of English (as opposed to British English).

#### Do

> You might not realize it, but you can change the colors of your Clerk components with global CSS.

#### Don't 

> You might not realise it, but you can change the colours of your Clerk components with global CSS.

### 1.2 Hyphens? Spaces? Neither!

Tech has created many new words by associating two words with each other like "front end" and "web site." On a long enough timeline, these migrate to hyphenated forms: "web site" became "web-site." And finally they become concatenated words: "website." We use the concatenated forms.

#### Do

> Frontend and fullstack developers often build websites with React.

#### Don't 

> Front-end and full stack developers often build web-sites with React.

### 1.3 When mentioning a documented component, function, etc, multiple times on a page, link to the reference documentation on the first mention of that item.

#### Do

> The [`currentUser()`](https://clerk.com/docs/references/nextjs/current-user) helper will return the [`User`](https://clerk.com/docs/references/javascript/user/user) object of the currently active user. The following example userse the `currentUser()` helper to access the `User` object for the authenticated user.

#### Don't 

> The [`currentUser()`](https://clerk.com/docs/references/nextjs/current-user) helper will return the [`User`](https://clerk.com/docs/references/javascript/user/user) object of the currently active user. The following example userse the [`currentUser()`](https://clerk.com/docs/references/nextjs/current-user) helper to access the [`User`](https://clerk.com/docs/references/javascript/user/user) object for the authenticated user.

## 2. Write for clarity

### 2.1 “You” is the reader; "Clerk" is Clerk

Clerk is the entity writing these docs and providing these services. The learner is the person consuming these things and building their own projects. To distinguish between the two and write with clarity, we refer to the learner with "you/your/yours." We objectively refer to Clerk as "Clerk," not "we/us/our/ours."

#### Do

> Clerk's `<ClerkProvider />` provides active session and user context to Clerk's hooks and other components. Import it into your app by adding `import { ClerkProvider } from '@clerk/nextjs'` at the top of your file.

#### Don't 

> Our `<ClerkProvider />` provides active session and user context to our hooks and other components. Let's import it into our app by adding `import { ClerkProvider } from '@clerk/nextjs'` at the top of the file.

### 2.2 "Users" are people logging in/out with Clerk. "Developers" are the audience we’re writing for.

People building with clerk are building for other people to make it clear whether we are talking about the builder or their users, we call builders "developers" and the peoeple they are building for "users."

#### Do

> Clerk helps developers overcome as many challenges as possible without additional configuration. This ensures their users have a secure, safe session.

#### Don't

> Clerk helps users overcome as many challenges as possible without additional configuration. This ensures their users have a secure, safe session.

### 2.3 Shorter is better.

Write short sentences. Short sentences are easier for both human and robots to translate. Concise writing is understandable writing. Look for commas that string together different thoughts. These are often good places to shorten and clarify content.

#### Do

> Clerk is now installed and mounted in your application. You can decide which pages are public or require authentication to access.

#### Don't

> Now that Clerk is installed and mounted in your application, you can decide which pages are public and which should require authentication to access.

### 2.4 Avoid gerunds (-ing words)

English gerunds ("-ing" words like "running") turn verbs into nouns ("run" becomes "running"). This makes the sentence sound passive ("They run" becomes "they are running") and makes it harder to translate. Use an active voice as much as possible and avoid these words.

#### Do

> How to use a routing library with Clerk

#### Don't

> Using a routing library with Clerk

### 2.5 Use task and outcome-based headings and titles that use verbs.

Tell the learner what they will learn from diving into the content. 

#### Do

> How to read session and user data

> How user sessions and user data work

Clearly explains what information the learner will find, helping them decide which to choose.

#### Don't

> User session and user data

Obscure. Doesn't convey whether this is the conceptual or task-based content the learner is looking for. They may pass over it or look briefly, then bounce out. This increases friction.

### 2.6 Lead with location; end with action.

When learners are performing an order of operations, it helps for them to start with _where_ they need to be to perform the action.

#### Do

> In your Next.js project's root folder, open your `.env.local file`.

The learner navigates to the project folder first, opens the file second.

#### Don't

> Open your `.env.local file` in your Next.js project's folder.

The learner must remember the file they need to open before finding out which folder to navigate to. This uses more mental energy.

### 2.7 Avoid colloquialisms

English speakers my find themselves using phrases like "

#### Do

> Something that is difficult for someone new to programming may not be for a senior engineer.

#### Don't

> Something that is difficult for someone new to programming may be child's play for a senior engineer.

Some learners may not have heard this expression before. It may be difficult for machine translation as well.

## 3. Write to include people

### 3.1 Do not assume proficiency

Avoid using language that assumes someone's level of proficiency. Something that is difficult for someone new to programming may not be difficult for a senior engineer. This language can inadvertently alienate or insult a learner. Avoid words like "just," "easy," "simple," "senior," "hard."

#### Do

> You can authenticate your app with Clerk in three steps. Install Clerk with `npm install @clerk/nextjs`, add your environment keys, and then wrap your app in `<ClerkProvider />`, and add [control components](https://clerk.com/docs/components/overview). Visit our [Quickstarts](https://clerk.com/docs/quickstarts/overview) for a step-by-step guide written for your framework.

#### Don't

> It's easy to authenticate your app with Clerk! Just install Clerk with `npm install @clerk/nextjs`, add your environment keys, wrap your app in `<ClerkProvider />`, and simply add [control components](https://clerk.com/docs/components/overview).

### 3.2 Avoid pop culture references

It's tempting to use things that are familiar to us to explain things to others—our favorite TV shows, books, and memes are entertaining and rich sources of metaphors. However, they assume a shared context between author and reader. A joke that mainstream American audiences understand may be completely misunderstood to a learner in Chile.

#### Do

```js
const updateUser = async () => {
  await user.update({
    firstName: "John",
    lastName: "Doe",
  });
};
```

#### Don't

```js
const updateUser = async () => {
  await user.update({
    firstName: "Twilight",
    lastName: "Sparkle",
  });
};
```

This assumes the learner is familiar with the cartoon _My Little Pony: Friendship is Magic,_ which is irrelevant.

### 3.3 Use "they/them/theirs" pronouns

For many years it was common to write with "he/him/his" pronouns in English technical documentation. But pronouns are difficult to translate into some languages. Gendering learners also sends the message that some genders are "default"—and this might not be the learner's gender. We use the neutral "they/them/theirs" pronouns.

#### Do

> When the user logs out using the button, they will be taken to the login page.

#### Don't

> When he logs out using the button, he will be taken to the login page.

### 3.4 Avoid "click"

"Click" is an outdated term that assumes the learner is using a mouse. But learners may be navigating by touchscreen, keyboard, or assistive technology. Often there are better words than "click"—like "select" and "open".

#### Do

> Open the **Settings tab.**

> Select the **Google** social connection.

#### Don't

> Click the **Settings tab.** 

> Click the **Google** social connection.

## 4. Write for code

### 4.1 Use monospace fonts for code, commands, file names, copy-ables, and URLs; use bold for menus, and other UI copy.

#### Do

> In your Clerk Dashboard, go to **User & Authentication > [Social Connections](https://dashboard.clerk.com/last-active?path=user-authentication/social-connections)** and open the **Settings** tab.

> In your browser, open [`http://localhost:3000/`](http://localhost:3000/).

#### Don't

> In your [Clerk Dashboard](https://dashboard.clerk.com/), go to `User & Authentication > Social Connections` and open the "Settings tab."

> In your browser, open [`http://localhost:3000/`](http://localhost:3000/).

### 4.2 Use carets to help users navigate menus; 

Use carets to nest operations of the same type like menu navigation.

#### Do

> In your [Clerk Dashboard](https://dashboard.clerk.com/), go to **User & Authentication > Social Connections** and open the **Settings tab.**

#### Don't

> In your [Clerk Dashboard](https://dashboard.clerk.com/), go to **User & Authentication**, click on **Social Connections**, and open the **Settings tab.**


### 4.3 Write compliant JSON: no single quotes, no comments

Conform to the [JSON standard](https://www.json.org/json-en.html):

* Key names are enclosed in double quotes (`"`)
* Values are between double quotes (`"`), not single quotes (`'`)
* No comments, neither `//` nor `/* */`

#### Do

> This is the user's primary email address in the User object

```json
{
  "email": "{{user.primary_email_address}}"
}
```

#### Don't

```json
{
	// this is the user's primary email address in the User object
  email: '{{user.primary_email_address}}'
}
```
 
### 4.4 Use 2-space indents for code blocks

We use 2-space indents to conserve horizontal space in code blocks.

#### Do

```js
export const config = {
  matcher: ['/((?!.+\\.[\\w]+$|_next).*)', '/', '/(api|trpc)(.*)'],
};
```

#### Don't

```js
export const config = {
    matcher: ['/((?!.+\\.[\\w]+$|_next).*)', '/', '/(api|trpc)(.*)'],
};
```

### 4.5 Authentication states should be hyphenated and bold.

Clerk authentication states **signed-in**, **signed-out**, and **unknown** should be hyphenated and bold to distinguish them from general states of being.

#### Do

> Once you have a **signed-in** user, you need to give them a way to sign out.

#### Don't

> Once you have a signed-in user, you need to give them a way to sign out.

### 4.6 Group like with like under tabs

When presenting things in a series of tabs, ensure that similar things are grouped together. 

#### Do

![App Router and Pages Router exist as two tabs, side by side.](/public/images/styleguide/clerk_uncrowded-tabs.png)

Next.js is a platform with two different implementations grouped underneath it.

#### Don't

![App Router and Pages Router are sitting alongside other very different methods of retrieving data.](/public/images/styleguide/clerk_crowded-tabs.png)

Next.js's two implementations are given equal weight to the other members of the tab bar. Someone unfamiliar with Next.js may become confused, and the ever growing tab bar is harder to navigate at smaller sizes.