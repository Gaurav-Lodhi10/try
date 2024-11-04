<div align="center">
  <br />
  <img src="https://github.com/Gaurav-Lodhi10/try/blob/master/public/main.png" alt="architect">   
  <img src="https://github.com/Gaurav-Lodhi10/try/blob/master/public/auth.png" alt="architect">
  <img src="https://github.com/Gaurav-Lodhi10/try/blob/master/public/room.png" alt="architect">
  <img src="https://github.com/Gaurav-Lodhi10/try/blob/master/public/real.png" alt="architect">
  <img src="https://github.com/Gaurav-Lodhi10/try/blob/master/public/tag.png" alt="architect">
  <img src="https://github.com/Gaurav-Lodhi10/try/blob/master/public/edit.png" alt="architect">
  <img src="https://github.com/Gaurav-Lodhi10/try/blob/master/public/account.png" alt="architect">
  <br />
<h3 align="center">Startup Directory Platform</h3>

  
</div>

## 📋 <a name="table">Table of Contents</a>

1. 🤖 [Introduction](#introduction)
2. ⚙ [Tech Stack](#tech-stack)
3. 🔋 [Features](#features)
4. 🤸 [Quick Start](#quick-start)

## <a name="introduction">🤖 Introduction (File Sharing Web App)</a>

## Project Overview

**Project Name:** CodeBuddy-(Devinder)  
**Purpose:** Devinder is a platform designed to help developers connect for pair programming. Users can create rooms where they can share their screens, collaborate, and discuss coding issues with other developers in real-time. Codebuddy includes features for live video chat, screen sharing, room creation with tags, and filtering options for easier navigation.

## <a name="tech-stack">⚙ Tech Stack</a>

- React 19
- Next.js 15
- Drizzle ORM
- PostgreSQl
- TailwindCSS
- TypeScript
- NextAuth
- Get Stream
- Docker
- ShadCN

## <a name="features">🔋 Features</a>

👉 Uses **NextAuth** for Google-based sign-in, allowing users to securely log in and manage their sessions.

👉 **Room Creation and Management:**  
   - Users can create rooms with a description, tags, and a GitHub repository link.  
   - Each room can have associated tags (e.g., TypeScript, Next.js, Drizzle ORM), enabling   easy discovery by others.

👉 ***Tag-Based Filtering:**  
   - Users can filter rooms based on specific tags, allowing them to join relevant rooms quickly.

👉 **Edit and Delete Functionality:**  
   - Room details can be updated, and users can delete rooms or even their accounts, which removes all associated data.
👉  **Account Management:**  
   - Users have the option to delete their account, which removes all related data, including created rooms.

## Workflow

1. **User signs in with Google.**
2. **User creates a room** with details and optional GitHub repo link.
3. **User searches for rooms** by tags or filters rooms in the browse section.
4. **Participants join the room** for live video chat, screen sharing, and code collaboration.
5. **User can edit or delete the room** or delete their account and related data.
## <a name="quick-start">🤸 Quick Start</a>

Follow these steps to set up the project locally on your machine.

*Prerequisites*

Make sure you have the following installed on your machine:

- [Git](https://git-scm.com/)
- [Node.js](https://nodejs.org/en)
- [npm](https://www.npmjs.com/) (Node Package Manager)

*Cloning the Repository*

bash
git clone https://github.com/Gaurav-Lodhi10/try.git

*Installation*

Install the project dependencies using npm:

bash
npm install



Set up Project:</br>
Create a new file named .env.local in the root of your project and add the following content:</br>
   - Create a Supabase project and configure the storage bucket.</br>
   - Add your Supabase keys in a .env.local file:</br>
     bash</br>
     DATABASE_URL="REPLACE ME WITH THE REAL URL OF YOUR POSTGRES DATABASE"</br>
     GOOGLE_CLIENT_ID=""</br>
     GOOGLE_CLIENT_SECRET=""</br>
     NEXTAUTH_SECRET="make_this_something_secret"</br>
     NEXT_PUBLIC_GET_STREAM_API_KEY=""</br>
     GET_STREAM_SECRET_KEY=""</br>
     NEXTAUTH_URL=http://localhost:3000</br>

*Running the Project*

bash
npm run dev


Open [http://localhost:3000](http://localhost:5000) in your browser to view the project.



<details>


css
@import url("https://fonts.googleapis.com/css2?family=Work+Sans:ital,wght@0,100..900;1,100..900&display=swap");

@tailwind base;
@tailwind components;
@tailwind utilities;

@layer base {
    :root {
        --radius: 0.5rem;
    }
}

@layer utilities {
    .flex-between {
        @apply flex justify-between items-center;
    }

    .text-30-extrabold {
        @apply text-[30px] font-extrabold text-white;
    }

    .text-30-bold {
        @apply text-[30px] font-bold text-black;
    }

    .text-30-semibold {
        @apply font-semibold text-[30px] text-black;
    }

    .text-26-semibold {
        @apply font-semibold text-[26px] text-black;
    }

    .text-24-black {
        @apply text-[24px] font-black text-black;
    }

    .text-20-medium {
        @apply font-medium text-[20px] text-black;
    }

    .text-16-medium {
        @apply font-medium text-[16px] text-black;
    }

    .text-14-normal {
        @apply font-normal text-sm text-white-100/80;
    }

    .pink_container {
        @apply w-full bg-primary min-h-[530px] pattern flex justify-center items-center flex-col py-10 px-6;
    }

    .tag {
        @apply bg-secondary px-6 py-3 font-work-sans font-bold rounded-sm uppercase relative tag-tri;
    }

    .heading {
        @apply uppercase bg-black px-6 py-3 font-work-sans font-extrabold text-white sm:text-[54px] sm:leading-[64px] text-[36px] leading-[46px] max-w-5xl text-center my-5;
    }

    .sub-heading {
        @apply font-medium text-[20px] text-white max-w-2xl text-center break-words;
    }

    .section_container {
        @apply px-6 py-10 max-w-7xl mx-auto;
    }

    .card_grid {
        @apply grid md:grid-cols-3 sm:grid-cols-2 gap-5;
    }

    .card_grid-sm {
        @apply grid sm:grid-cols-2 gap-5;
    }

    .no-result {
        @apply text-black-100 text-sm font-normal;
    }

    /* profile */
    .profile_container {
        @apply w-full pb-10 pt-20 px-6 max-w-7xl mx-auto lg:flex-row flex-col flex gap-10;
    }

    .profile_card {
        @apply w-80 px-6 pb-6 pt-20 flex flex-col justify-center items-center bg-primary border-[5px] border-black shadow-100 rounded-[30px] relative z-0 h-fit max-lg:w-full;
    }

    .profile_title {
        @apply w-11/12 bg-white border-[5px] border-black rounded-[20px] px-5 py-3 absolute -top-9 after:absolute after:content-[''] after:-top-1 after:right-0 after:-skew-y-6 after:bg-black after:-z-[1] after:rounded-[20px] after:w-full after:h-[60px] before:absolute before:content-[''] before:-bottom-1 before:left-0  before:-skew-y-6 before:w-full before:h-[60px] before:bg-black  before:-z-[1] before:rounded-[20px] shadow-100;
    }

    .profile_image {
        @apply rounded-full object-cover border-[3px] border-black;
    }

    /* idea details */
    .divider {
        @apply border-dotted bg-zinc-400 max-w-4xl my-10 mx-auto;
    }

    .view_skeleton {
        @apply bg-zinc-400 h-10 w-24 rounded-lg fixed bottom-3 right-3;
    }

    /* navbar */
    .avatar {
        @apply p-0 focus-visible:ring-0 bg-none rounded-full drop-shadow-md !important;
    }

    .dropdown-menu {
        @apply w-56 border-[5px] border-black bg-white p-5 rounded-2xl !important;
    }

    .login {
        @apply border-[5px] py-4 border-black bg-white text-black relative shadow-100 font-work-sans font-medium hover:shadow-none transition-all duration-500 !important;
    }

    /* searchform */
    .search-form {
        @apply max-w-3xl w-full min-h-[80px] bg-white border-[5px] border-black rounded-[80px] text-[24px] mt-8 px-5 flex flex-row items-center gap-5;
    }

    .search-input {
        @apply flex-1 font-bold placeholder:font-semibold placeholder:text-black-100 w-full h-auto outline-none;
    }

    .search-btn {
        @apply size-[50px] rounded-full bg-black flex justify-center items-center !important;
    }

    /* startupcard */
    .startup-card {
        @apply bg-white border-[5px] border-black py-6 px-5 rounded-[22px] shadow-200 hover:border-primary transition-all duration-500 hover:shadow-300 hover:bg-primary-100;
    }

    .startup-card_date {
        @apply font-medium text-[16px] bg-primary-100 px-4 py-2 rounded-full group-hover:bg-white-100;
    }

    .startup-card_desc {
        @apply font-normal text-[16px] line-clamp-2 my-3 text-black-100 break-all;
    }

    .startup-card_img {
        @apply w-full h-[164px] rounded-[10px] object-cover;
    }

    .startup-card_btn {
        @apply rounded-full bg-black-200 font-medium text-[16px] text-white px-5 py-3 !important;
    }

    .startup-card_skeleton {
        @apply w-full h-96 rounded-[22px] bg-zinc-400;
    }

    /* startupform */
    .startup-form {
        @apply max-w-2xl mx-auto bg-white my-10 space-y-8 px-6;
    }

    .startup-form_label {
        @apply font-bold text-[18px] text-black uppercase;
    }

    .startup-form_input {
        @apply border-[3px] border-black px-5 py-7 text-[18px] text-black font-semibold rounded-full mt-3 placeholder:text-black-300 !important;
    }

    .startup-form_textarea {
        @apply border-[3px] border-black p-5 text-[18px] text-black font-semibold rounded-[20px] mt-3 placeholder:text-black-300 !important;
    }

    .startup-form_error {
        @apply text-red-500 mt-2 ml-5;
    }

    .startup-form_editor {
        @apply mt-3 border-[3px] border-black text-[18px] text-black font-semibold placeholder:text-black-300 !important;
    }

    .startup-form_btn {
        @apply bg-primary border-[4px] border-black rounded-full p-5 min-h-[70px] w-full font-bold text-[18px] !important;
    }

    /* view */
    .view-container {
        @apply flex justify-end items-center mt-5 fixed bottom-3 right-3;
    }

    .view-text {
        @apply font-medium text-[16px] bg-primary-100 px-4 py-2 rounded-lg capitalize;
    }

    .category-tag {
        @apply font-medium text-[16px] bg-primary-100 px-4 py-2 rounded-full;
    }

    .pattern {
        background-image: linear-gradient(
                to right,
                transparent 49.5%,
                rgba(251, 232, 67, 0.2) 49.5%,
                rgba(251, 232, 67, 0.6) 50.5%,
                transparent 50.5%
        );
        background-size: 5% 100%;
        background-position: center;
        background-repeat: repeat-x;
    }

    .tag-tri {
        @apply before:content-[''] before:absolute before:top-2 before:left-2 before:border-t-[10px] before:border-t-black before:border-r-[10px] before:border-r-transparent after:content-[''] after:absolute after:bottom-2 after:right-2 after:border-b-[10px] after:border-b-black after:border-l-[10px] after:border-l-transparent;
    }

</detail>
