# Hackathon Details

:star: Awarded Most Wanted (First Place) at CatHacks XII, the University of Kentucky's annual hackathon. :star:

[Devpost Link](https://cathacks-xii.devpost.com/)

# Inspiration

We built Nora around a very human problem: a lot of older adults live alone, and the people who love them cannot always check in every day. Families want peace of mind, but existing options are often too reactive, too expensive, or too complicated for seniors to use consistently.

We wanted to create something that feels warm instead of clinical. Nora is designed to make daily check-ins as simple as answering a phone call, while giving guardians a clearer picture of how their loved one is doing.

# What it does

Nora is an AI voice companion for seniors. It places gentle, scheduled phone calls to check in, ask how someone is feeling, and surface useful context like mood, discomfort, reminders, and plans for the day.

On the family side, Nora gives guardians a dashboard where they can set up a loved one’s profile, manage call schedules, trigger a manual call, and review call history, transcripts, and summaries. The goal is to reduce the burden on families while still keeping them meaningfully informed.

A big part of the experience is accessibility: the senior does not need to download an app or learn a new interface. They just answer the phone.

# How we built it

We built Nora as a full-stack web app using Next.js, React, and Tailwind CSS for the frontend experience. For authentication, protected routes, and database access, we used Supabase. That gave us a clean way to manage guardian accounts, senior profiles, call records, schedules, and onboarding flows.

For the voice experience, we used Vapi to initiate and manage outbound calls. We connected that to Supabase Edge Functions so we could trigger manual calls, run scheduled calls, and pass structured context into the assistant prompt. We also built logic around scheduling, time zones, reminders, and storing call activity so the dashboard stays useful after the conversation ends.

On the product side, we designed Nora to support both guardian-led onboarding and senior self-setup, because real families do not all follow the same care workflow.

# Challenges we ran into

One of the hardest parts was making the experience feel trustworthy. A voice product for seniors cannot sound rushed, robotic, or confusing. We had to think carefully about pacing, wording, and what kind of prompt design would make Nora feel calm and clear.

Scheduling was another challenge. Daily check-ins sound simple until you account for time zones, repeat days, missed calls, and how to reliably trigger voice calls from a real app architecture.

We also had to balance warmth with safety. A companion product has to feel personal, but it also needs clear boundaries around reminders, wellbeing questions, and situations that may require escalation.

# Accomplishments that we're proud of

We’re proud that Nora is not just a concept deck. We built a working product with authentication, onboarding, a scheduling system, manual outbound calling, and a dashboard for reviewing care activity.

We’re also proud of the accessibility of the experience. The most important user in this product, the senior, does not need to be fluent with smartphones or apps. That design choice shaped the entire project.

Finally, we’re proud that Nora feels intentional. From the tone of the voice assistant to the calm visual design of the dashboard, we tried to build something that respects older adults instead of treating them like a technical edge case.

# What we learned

We learned that building for care is different from building for convenience. Small product decisions, like how a reminder is phrased or how a check-in summary is presented, carry a lot more emotional weight in this context.

We also learned how much real-world complexity hides inside “simple” features. Scheduling recurring calls, connecting voice infrastructure to a web app, and designing a flow that works for both seniors and guardians forced us to think across product, engineering, and trust all at once.

Most of all, we learned that good AI experiences are not just about model capability. They are about clarity, empathy, and designing around the real habits of the people using the product.

# What's next for Nora

Our next step is to make Nora more proactive and more personalized over time. We want to improve summaries, better identify changes in routine or wellbeing across multiple calls, and give guardians clearer insight into trends instead of just single check-ins.

We also want to expand the safety layer with stronger escalation flows, notifications, and contact management, while continuing to keep the senior experience simple. Longer term, we see Nora becoming a dependable daily companion that helps families stay connected before a small concern becomes a crisis.
