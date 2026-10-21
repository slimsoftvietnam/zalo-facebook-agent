---
name: zalo-facebook-agent
description: Prepare or carry out user-requested Facebook posts and personal Zalo outreach, gathering the purpose, source material, target, and voice for each task.
metadata:
  short-description: Prepare Facebook posts and Zalo messages interactively
---

# Facebook & Zalo Agent

Support two separate workflows: Facebook publishing and personal Zalo outreach. Treat every request as a new task with its own goal, source material, audience, and channel/destination. Use the persistent SlimAI brand voice in [`references/brand_voice.md`](references/brand_voice.md) by default; a voice or sample the user supplies for a task overrides it for that task. Do not assume that example products, audiences, schedules, contact lists, or trackers from earlier runs apply again.

Use [`references/brand_voice.md`](references/brand_voice.md) as the persistent default voice, and [`references/gioi-han.md`](references/gioi-han.md) for operating boundaries. Historical PEAS/task-card examples do not fix the product, lead list, calendar, platform account, or tracker for future requests.

## Required intake for every task

Before drafting a post or message, first inspect any calendar, sheet, source document, or browser context the user identified. Treat information already present there as provided by the user; do not ask for it again. Ask only for required details still missing or unclear after checking those sources. Make sure the task establishes:

1. **Purpose:** what the content or outreach should achieve, who it is for, and any desired response/action.
2. **Source material:** the approved content, brief, facts, offer, links, images, or other documents the content should rely on. Ask the user to attach or link the relevant material; do not silently reuse sample files from a previous run.
3. **Target and destination:** for Zalo, the intended recipient(s) and supplied/verified contact details; for Facebook, the profile/page or named group(s), and any audience constraints. For a group the user asks the agent to discover, first confirm the topic/audience and check the group's public rules before preparing a post for it.
4. **Voice/reference:** use the persistent SlimAI voice by default. If the user supplies a different brand voice or post/message/template sample, use it for that task. Ask only if the user indicates another brand and its voice is unclear, or if supplied references conflict.

Ask for missing items together in one concise question when practical. When the user provides the information for a post/message and their instruction clearly means to publish/send it, do so as soon as the purpose, source, target/destination, and content are clear; do not add a separate approval round. If the user asks to draft, review, or hold, do not publish/send.

## Browser-first execution

- Publish Facebook posts and send personal Zalo messages through the in-app browser available in the current tool (such as Codex, Claude Code, or another tool with an in-app browser), even if a native sender tool is available. Use the browser session already open and logged in; do not switch to a separate desktop browser or native app for these actions.
- Before composing, verify the visible Facebook profile/Page or Zalo account. Use the identity already active in the in-app browser unless the user names a different one. Do not switch to another profile/Page on your own. If the active identity cannot be determined or conflicts with the user's stated destination/sender, stop and ask once before acting.
- If the in-app browser is not logged in, open the official Facebook or Zalo login page there and pause so the user can complete sign-in. Do not enter or request passwords or verification codes. Resume only after the user signals that sign-in is complete.
- Use the calendar's referenced image or media when one is listed. Resolve the named asset from the calendar's source or linked Drive location. Do not replace an available source image with a generated image. If the named asset cannot be retrieved, ask before substituting another visual.
- Every Facebook post must include an image. If the calendar or source identifies an image, retrieve and attach that exact asset in the in-app browser; do not publish the post text-only or replace the available source image with a generated image. If the named asset cannot be retrieved, stop and ask how to proceed.
- If no image is supplied or referenced, ask whether there is a preferred visual style and request a reference image before creating one. If the user has no style/reference to follow, create an image that fits the post content and brand voice, then attach it to the Facebook post.
- After publishing/sending, verify the result in the browser and provide the direct post/message link when the platform exposes one.

## 1. Đăng bài Facebook

### Flow

1. Inspect the calendar/source the user identifies and extract the purpose, intended audience, copy, destination(s), timing, media, and voice/template. Do not ask again for details the calendar already contains. A content calendar is a task source only when the user supplies or identifies it for this task; it is not a permanent input or standing authorization.
2. Check that the source supports the claims and that the copy, image, and date fit the stated objective. Every Facebook post needs an image: retrieve the exact calendar/source asset when listed. If no image is listed, ask for style and a reference image before creating one; when the user has no reference, create a fitting image. Preserve approved material unless the user requests adaptation. Ask only for unresolved required details; do not invent or substitute a calendar asset silently.
3. Confirm the exact profile/page and group destinations. Publish to groups only when the user specifies them or clearly asks the agent to identify relevant ones for this task. Check each group's visible rules and context; skip destinations where promotional/educational posts are prohibited or the rules are unclear.
4. When the user's instruction and supplied source clearly request publication, publish promptly with the required image to the settled destination through the in-app browser. Verify that both the text and image appear in the published post. Verify each destination separately. A group post awaiting moderation is pending, not published.
5. Update a tracker only if the user supplies or identifies one for this task. Preserve unrelated data, record each destination/result and timestamp, and verify the update. If no tracker is supplied, report the outcome in the conversation.

### Facebook writing

Apply the supplied brand voice or sample. Keep the post aligned with the stated purpose, audience, and source material. Use clear paragraphs and a relevant CTA only when it serves the brief. Avoid unsupported claims, hype, and unnecessary changes to approved copy.

## 2. Gửi tin nhắn Zalo cá nhân — tiếp cận người nhận

### Flow

1. Collect the purpose of the outreach, the source material (brief, offer, facts, or sample), each intended recipient and exact supplied contact identifier, the sender identity, and the brand voice/template. A lead sheet from a previous task is only an example unless the user supplies or identifies it again.
2. Check that each person and contact channel are within the user's stated scope and suitable for the stated purpose. Use only supplied identifiers to look up a profile. Verify identity against available name/context; ambiguous matches, shared/company accounts, or hotlines are not verified personal recipients. Ask if identity cannot be resolved.
3. Draft a message tailored to verified context in the requested voice. Use only claims supported by the current source material. Do not reuse an earlier product/course, company signal, email, or template as a standing offer. If the source does not establish a relevant company/person context, omit personalization rather than guessing. When addressing the recipient as “anh/chị”, refer to the sender as “em” consistently throughout the message. Follow the first-message order in [`references/brand_voice.md`](references/brand_voice.md): verified signal about the recipient first, then sender and offer, then the direct question, then a fallback asking for the right contact when relevant.
4. Show the exact recipient and message for review unless the user explicitly authorized sending that specific content/action. Never send to people outside the named/supplied scope. Respect refusals and opt-outs; do not send follow-ups unless newly requested.
5. Send authorized messages through Zalo in the in-app browser, verifying the visible recipient and sender before sending. If the user asks for a friend request as part of the task, follow the requested sequence and attempt a message only when the user has authorized it and Zalo permits it. Stop on a privacy restriction, platform limit, warning, or error; do not bypass or automatically retry.
6. Update a tracker only if the user supplies or identifies one for this task. Record lookup confidence, friend-request/message outcome, timestamp, and blocker accurately, then verify the update. Otherwise, report results in the conversation.

## Shared operating boundaries

- Never invent the purpose, audience, recipient, channel, source facts, approval state, or brand rules. Ask when required information is missing or conflicting.
- Distinguish composing from publishing/sending. A calendar date, draft, or sample alone is not permission to act; follow a clear current instruction to publish/send and do not insert an extra approval round after the user has provided the requested information.
- Do not delete content/messages, block people, change account settings, bypass platform controls, or retry failed actions automatically.
- Follow any user-supplied limits and platform restrictions. If an applicable limit is missing and action would depend on it, ask or stop the affected action.
- Do not use LinkedIn or another platform unless the user requests it.

## Example-only project files

The `references/brand_voice.md` guide is the persistent user-supplied SlimAI default for this skill. Any campaign data from prior examples—including products, contact lists, content calendars, and trackers—must not be assumed current or reused without the user identifying it for that task.
