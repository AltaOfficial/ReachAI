# 🚀 ReachAI

<div align="center">
  
  **AI-powered Twitter/X outreach automation platform that scales your DM campaigns across multiple accounts**
  
  <img width="2940" height="1594" alt="image" src="https://github.com/user-attachments/assets/61f25163-510d-4713-ab6a-e99e675295ab" />

  [Live Demo (Preview build. Payment is in test mode—use Stripe test card numbers only.)](https://reachai-top-git-preview-jaedon-farrs-projects.vercel.app/)
  
  > 🔒 **Note:** The actual repository is private. This README showcases the project's architecture, features, and development journey.
  
</div>
<div align="center">
  <img src="assets/reachai-hero.gif" alt="ReachAI Demo" width="100%"/>
</div>

## 📦 Technologies

* `Frontend`: Next.js 15.2.4, React 19, TypeScript, Tailwind CSS
* `UI Libraries`: Radix UI, shadcn/ui, Framer Motion
* `Data Tables`: TanStack Table
* `Backend`: Node.js 22, Express.js, Socket.io
* `Database`: MongoDB Atlas, Mongoose
* `Real-time`: WebSockets, Server-Sent Events
* `Scheduling`: node-cron for automated tasks
* `Authentication`: Clerk
* `Payments`: Stripe
* `Monitoring`: Sentry
* `Integrations`: Twitter/X API, SMSPVA, Svix webhooks
* `Deployment`: Vercel (Frontend), Railway (Backend)

## 🦄 Features

<div align="center">
  <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/af400513-e995-463f-8d67-8122c5e8aeb0" />
</div>

**Core Features:**
* **Automated DM Campaigns**: Send personalized direct messages at scale across multiple Twitter accounts
* **Multi-Account Management**: Coordinate campaigns across numerous accounts from one dashboard
* **Real-time Conversation Tracking**: Monitor all conversations and responses with live WebSocket updates
* **Campaign Analytics**: Track performance metrics like open rates, response rates, and conversions
* **Profile Scraping & Interactions**: Automated profile discovery and engagement
* **Subscription Management**: Full SaaS model with Stripe integration for billing and payments

**Planned Enhancements:**
* **AI-Powered Messaging**: GPT-based personalized messaging that learns from your communication style or follows custom scripts
* **Content Automation**: Automated reposting capabilities
* **Twitter Blue Automation**: Subscription process automation up to Stripe checkout
* **Follower Marketplace**: Buy followers using platform credits
* **Custom Metrics**: User-defined tracking metrics with export to spreadsheets
* **Multi-Platform Support**: Expand to LinkedIn, Instagram, and WhatsApp

## 🎯 Why I Built This

In today's fast-paced digital landscape, social media outreach is essential for businesses, creators, and marketers. However, manual outreach on platforms like X/Twitter is inefficient, time-consuming, and difficult to scale.

**The problem:**
* Manual DM outreach takes hours per day
* Difficult to track conversations across multiple accounts
* No way to measure campaign effectiveness
* Response rates suffer from poor timing and personalization

**The solution:** Build ReachAI to automate and optimize outreach marketing, enabling users to focus on engagement and conversions rather than repetitive tasks. The goal is to cut down manual messaging time by over 90%.

## 👩🏽‍🍳 The Process

### Defining Core Features & Design

<div align="center">
  <img width="2940" height="694" alt="image" src="https://github.com/user-attachments/assets/f53a54f8-d60d-4ef7-b949-5e4d7ade16d7" />
  <a href="https://www.figma.com/design/iExAV1IhimRFpXGeW36c7f/ReachAi.Top-Website?node-id=0-1&t=v4ijC4gtgtmNy3Sd-1" target="_blank">Take a closer look</a>
</div>

Since this was my first major web application, I started by designing the entire interface in Figma before writing any code. This helped me understand what I was building and included:
- Campaign management dashboard
- Real-time conversation tracking interface
- Balance/billing page with Stripe integration
- Home page and onboarding flow

The visual planning was crucial for someone with limited web dev experience at the time.

### Choosing the Tech Stack

#### **Frontend Stack**

<table>
<tr>
<td><strong>Technology</strong></td>
<td><strong>Category</strong></td>
<td><strong>Used in MVP?</strong></td>
<td><strong>Reason</strong></td>
</tr>
<tr>
<td><strong>Next.js 15.2.4</strong></td>
<td>Framework</td>
<td>✅ Yes</td>
<td>Server-side rendering for better performance and SEO</td>
</tr>
<tr>
<td><strong>React 19</strong></td>
<td>UI Library</td>
<td>✅ Yes</td>
<td>Component-based architecture for maintainable code</td>
</tr>
<tr>
<td><strong>TypeScript</strong></td>
<td>Language</td>
<td>✅ Yes</td>
<td>Type safety prevents bugs and improves developer experience</td>
</tr>
<tr>
<td><strong>Tailwind CSS</strong></td>
<td>Styling</td>
<td>✅ Yes</td>
<td>Rapid UI development with utility-first classes</td>
</tr>
<tr>
<td><strong>Radix UI + shadcn/ui</strong></td>
<td>Component Library</td>
<td>✅ Yes</td>
<td>Accessible, customizable component primitives</td>
</tr>
<tr>
<td><strong>Framer Motion</strong></td>
<td>Animation</td>
<td>✅ Yes</td>
<td>Smooth animations for better UX</td>
</tr>
<tr>
<td><strong>TanStack Table</strong></td>
<td>Data Tables</td>
<td>✅ Yes</td>
<td>Powerful data table for campaign management (steep learning curve!)</td>
</tr>
<tr>
<td><strong>Socket.io Client</strong></td>
<td>Real-time</td>
<td>✅ Yes</td>
<td>Real-time updates for conversations and metrics</td>
</tr>
<tr>
<td><strong>Clerk</strong></td>
<td>Auth</td>
<td>✅ Yes</td>
<td>Authentication and user management</td>
</tr>
<tr>
<td><strong>Stripe</strong></td>
<td>Payments</td>
<td>✅ Yes</td>
<td>Subscription billing and payments</td>
</tr>
<tr>
<td><strong>Sentry</strong></td>
<td>Monitoring</td>
<td>✅ Yes</td>
<td>Error tracking and performance monitoring</td>
</tr>
</table>

#### **Backend Stack**

<table>
<tr>
<td><strong>Technology</strong></td>
<td><strong>Category</strong></td>
<td><strong>Used?</strong></td>
<td><strong>Reason</strong></td>
</tr>
<tr>
<td><strong>Node.js 22</strong></td>
<td>Runtime</td>
<td>✅ Yes</td>
<td>JavaScript runtime for backend services</td>
</tr>
<tr>
<td><strong>Express.js</strong></td>
<td>Framework</td>
<td>✅ Yes</td>
<td>Lightweight web framework for APIs</td>
</tr>
<tr>
<td><strong>TypeScript</strong></td>
<td>Language</td>
<td>🔄 In Progress</td>
<td>Currently migrating from JavaScript for better type safety</td>
</tr>
<tr>
<td><strong>NestJS</strong></td>
<td>Framework</td>
<td>📋 Planned</td>
<td>Better structure as backend grows (inspired by Spring Boot experience)</td>
</tr>
<tr>
<td><strong>MongoDB Atlas</strong></td>
<td>Database</td>
<td>✅ Yes</td>
<td>Cloud database for campaigns, users, metrics (8 Mongoose models)</td>
</tr>
<tr>
<td><strong>Mongoose</strong></td>
<td>ODM</td>
<td>✅ Yes</td>
<td>Object modeling for MongoDB</td>
</tr>
<tr>
<td><strong>Socket.io</strong></td>
<td>Real-time</td>
<td>✅ Yes</td>
<td>WebSocket server for bidirectional real-time updates</td>
</tr>
<tr>
<td><strong>node-cron</strong></td>
<td>Scheduling</td>
<td>✅ Yes</td>
<td>Scheduled tasks for campaign automation</td>
</tr>
</table>

### Technical Challenges I Faced

#### 1. TanStack Table Learning Curve

<div align="center">
  <img width="2940" height="1602" alt="image" src="https://github.com/user-attachments/assets/8ed6cd22-e6cf-4915-b762-4ea6aa2884a6" />
</div>

**The Problem:** Coming from limited web dev experience, understanding TanStack Table was extremely difficult. The documentation wasn't beginner-friendly, and I couldn't figure out why the table wasn't rendering at all.

**The Solution:** After days of debugging, I finally discovered it was literally **one missing parameter in a function**. One word. That single missing argument was causing the entire table to fail. This experience taught me the importance of carefully reading function signatures and understanding exactly what each library expects.
```typescript
// The issue was something like this:
// Wrong (missing 'data' parameter):
const table = useReactTable({
  columns,
  getCoreRowModel: getCoreRowModel(),
});

// Correct:
const table = useReactTable({
  columns,
  data: campaigns, // This one missing parameter broke everything!
  getCoreRowModel: getCoreRowModel(),
});
```

#### 2. Next.js Server Actions Can't Handle Long-Running Tasks

**The Problem:** When I started the project, I didn't understand that Next.js Server Actions have strict time limits and aren't designed for long-running background processes. I initially tried to run the entire campaign automation (scraping thousands of followers, filtering, sending DMs) within Server Actions, which would timeout or fail unpredictably.

**The Solution:** Had to split the architecture into two separate servers:
- **Next.js (Frontend)**: Handles UI, auth, and simple database queries
- **Express Backend**: Handles long-running campaign execution, Twitter API calls, and background task scheduling

The campaign execution now runs asynchronously on the Express server, using MongoDB change streams to monitor for status changes. This taught me the fundamental difference between serverless functions (short-lived, stateless) and traditional servers (long-running, stateful).
```javascript
// What I tried (doesn't work for long tasks):
// app/actions/runCampaign.js
'use server'
export async function runCampaign(campaignId) {
  // This times out after 60 seconds in serverless
  for (let i = 0; i < 10000; i++) {
    await scrapFollowers();
    await sendDMs();
  }
}

// What actually works:
// Backend/index.js
app.post('/modifycampaign', async (req, res) => {
  res.send({success: true}); // Respond immediately
  
  // Run async in background
  campaignRunner({campaign, campaignId}).catch(console.error);
});
```

#### 3. Twitter's Proprietary x-client-transaction-id Header

**The Problem:** Twitter's GraphQL API requires a custom `x-client-transaction-id` header that changes with every request. Without this header, API calls are rejected. The header generation algorithm was completely undocumented and obfuscated in Twitter's frontend JavaScript.

**The Discovery Process:**
1. Noticed API calls failing with 403 errors despite valid auth tokens
2. Inspected network traffic in browser DevTools and found the `x-client-transaction-id` header
3. Realized the header value changed with every single request (not a static token)
4. Found an existing solution online that had reverse-engineered the algorithm
5. Needed to adapt it for my Node.js backend

**The Solution:** Used Claude to port an existing Python implementation to JavaScript. The algorithm involves SVG animation parsing, cubic interpolation, transformation matrices, SHA-256 hashing, and XOR encoding. Honestly, I don't fully understand the math behind it - the code is dense and confusing. But it works, and for an MVP, that's what mattered.
```javascript
// The actual function - I understand the high-level flow but not the math
async function generateClientTransactionId({ path, method }) {
  // 1. Fetch Twitter's home page to get verification key
  const homePage = await handleXMigration(session);
  
  // 2. Get the obfuscated JavaScript file
  const ondemandFileUrl = getOndemandFileUrl(homePage);
  const ondemandFile = await fetch(ondemandFileUrl);
  
  // 3. Parse animation data (this part is a black box to me)
  const clientTransaction = new ClientTransaction(
    homePage,
    ondemandFile
  );
  
  // 4. Generate the transaction ID (magic happens here)
  const transactionId = await clientTransaction.generateTransactionId(
    method,
    path
  );
  
  return transactionId;
}
```

**What I Actually Learned:**
- **You don't need to understand everything to ship**: Sometimes it's okay to use code you don't fully understand, especially for an MVP. The perfect can be the enemy of the good.
- **Leverage existing solutions**: Someone smarter than me already solved this problem. Rather than spending weeks reverse-engineering it myself, I found their solution and adapted it.
- **AI as a translation tool**: Using Claude to port Python to JavaScript was incredibly effective - it handled the syntax conversion while preserving the complex logic I didn't understand.
- **When to dive deep vs. when to move on**: I could've spent a month understanding cubic bezier curves and transformation matrices, but that wouldn't have gotten users. Knowing when to treat something as a black box is a valuable skill.

This taught me an important lesson about pragmatism in engineering: shipping a working product is more valuable than deeply understanding every line of code, especially when you're working alone on an MVP.

#### 4. Headless Login Reliability Issues

**The Problem:** When logging into Twitter accounts in headless mode (without a browser UI), sometimes login randomly fails. Even switching to headful mode doesn't help for that account, but a different account logs in fine. When sending DMs at scale, Twitter eventually kicks the account out (not a ban, just forced logout). When trying to log back in, the system struggles.

**Current Status:** This is still an ongoing challenge. I suspect it's related to Twitter's spam detection algorithms.

**Workarounds I'm exploring:**
- Rotating accounts more frequently to avoid detection
- Adding random delays between actions to mimic human behavior
- Implementing behavior pattern randomization
- Using residential proxies instead of datacenter IPs
- Session persistence improvements

## 📚 What I Learned

### 🔧 Technical Skills

* **Pragmatic Problem Solving**: When Twitter's API needed a proprietary `x-client-transaction-id` header, I found an existing Python implementation online and used Claude to port it to JavaScript. I don't fully understand the math (cubic interpolation, transformation matrices), but I learned it's okay to use code as a black box when shipping an MVP. Understanding when to dig deep vs. when to move on is valuable.

* **Real-time Systems Architecture**: Implementing WebSockets for live campaign updates taught me about bidirectional communication, state synchronization across clients, and handling concurrent connections at scale.

* **Serverless vs. Traditional Backend**: Learning the hard way that Next.js Server Actions can't handle long-running processes forced me to understand the difference between serverless functions (short-lived, stateless) and traditional servers (long-running, stateful). This led to splitting the architecture into Next.js for UI and Express for background processing.

* **API Reverse Engineering**: Learned to work with undocumented APIs by inspecting network traffic in DevTools, finding existing solutions online, and adapting them to my stack.

* **Scale Considerations**: Managing multiple accounts, rate limits, and concurrent operations taught me about queuing systems, job scheduling, and the importance of retry logic with exponential backoff.

* **Database Modeling**: Designing 8 interconnected Mongoose models (Users, Campaigns, Conversations, Accounts, Tasks, Metrics, Proxies, Offersets) taught me about data relationships, indexing for performance, and avoiding N+1 queries.

* **TypeScript Migration Strategy**: Learning to gradually migrate a JavaScript codebase to TypeScript showed me the value of types in catching bugs early and improving code maintainability.

### 🎯 Project Management

* **Solo Development Reality**: Building everything alone without AI tools (started before modern AI coding assistants were mature) made the backend unstructured. Now that AI tools are available, restructuring will be easier, but dealing with messy JavaScript code is a challenge.

* **Technical Debt Costs**: Starting with JavaScript and later wanting TypeScript/NestJS taught me the importance of choosing the right architecture early, even with a steeper learning curve.

* **MVP vs. Perfect**: Learning to focus on core features that prove the concept (DM automation, campaign management) rather than building everything at once.

* **School-Life Balance**: Juggling a major project with coursework taught me realistic time management and the importance of sustainable development pace.

### 💼 Business Lessons

* **Platform Risk**: Building on unofficial APIs means your platform can break at any time. Always have monitoring, fallback strategies, and be prepared to adapt quickly.

* **Real Users Matter**: Solo testing only reveals so much. Planning to onboard test users to validate features and find real-world issues before scaling.

* **Proof of Concept First**: Goal is to get paying clients using the MVP to prove the business model works before building advanced features.

### 🧠 Technical Highlights

<div align="center">
  <img width="2940" height="1602" alt="image" src="https://github.com/user-attachments/assets/4ed23aa6-a3f5-4f74-90ba-6a4ab6ceaf93" />
</div>

* **Real-time WebSocket System**: Built a scalable Socket.io server that handles multiple concurrent campaigns, broadcasting updates to connected clients with minimal latency

* **Automated Job Scheduling**: Implemented node-cron based system for campaign execution, message queuing, and account rotation

* **Multi-Account Orchestration**: Created a system that coordinates actions across multiple Twitter accounts while respecting rate limits and mimicking human behavior patterns

* **Campaign Analytics Pipeline**: Built visualizations that process real-time metrics from MongoDB and display engagement trends, response rates, and conversion data

## 💭 Current State & Future Vision

### Where It Is Now
This is currently an **active MVP development project**. The core automation works, but there's significant work remaining:
- Backend needs restructuring (unorganized JavaScript → TypeScript/NestJS)
- Limited testing (personal account only, ~500 DMs sent)
- No scalability testing with multiple accounts or high volume
- No real users yet (planning to onboard test users soon)

### The Vision
The goal is to launch an MVP, get initial paying clients, and prove the concept works. Once validated with real users making real money, I'll focus on:
- Restructuring the backend for maintainability
- AI-powered messaging capabilities
- Multi-platform support (LinkedIn, Instagram, WhatsApp)
- Advanced analytics and optimization features
- Enterprise-grade scalability and reliability

This is a long-term project that I'm committed to seeing through, balancing it with school and other commitments.

## 🛠️ Development Tools

* **Cursor AI** – AI-powered IDE (adopted later in development)
* **Figma** – Complete UI/UX design and prototyping
* **MongoDB Compass** – Database management and query optimization
* **Postman/Insomnia** – API testing and debugging Twitter endpoints
* **Sentry** – Production monitoring and error tracking
* **Chrome DevTools** – Reverse engineering Twitter's network requests

---

<div align="center">
  
Built with ❤️ by Jaedon Farr

<p align="center">
  Readme created with the help of claude <img width="20" height="20" alt="Claude AI" src="https://github.com/user-attachments/assets/ccb8345f-6f6c-455e-8246-d15297f725fb" style="vertical-align: middle;" />
</p>

[Portfolio](https://jaedonfarr.vercel.app) • [LinkedIn](https://linkedin.com/in/jaedonfarr) • [GitHub](https://github.com/altaofficial)

</div>
