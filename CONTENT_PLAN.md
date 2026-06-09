# Convo Documentation Content Plan

> **Note (June 2026):** This plan predates the Convo → Humanize rebrand and the June 2026 feature update (segments & quotas, emotion analysis, supercuts, exporting). Kept for historical reference; paths and branding below are outdated.

> **Purpose:** Actionable content plan for docs.useconvo.ai (Mintlify). Based on competitor audit (Conveo, Listen Labs, Outset) and Convo codebase feature audit.
>
> **Date:** March 2026
>
> **Priority key:** P0 = launch blocker | P1 = launch week | P2 = fast follow

---

## 1. Proposed Navigation Structure (docs.json)

```json
{
  "navigation": {
    "tabs": [
      {
        "tab": "Guides",
        "groups": [
          {
            "group": "Getting Started",
            "pages": [
              "introduction",
              "quickstart",
              "key-concepts"
            ]
          },
          {
            "group": "Creating Studies",
            "pages": [
              "studies/ai-study-builder",
              "studies/manual-editor",
              "studies/discussion-guide",
              "studies/screener",
              "studies/welcome-screen",
              "studies/interview-settings",
              "studies/versioning-and-lifecycle"
            ]
          },
          {
            "group": "Recruitment",
            "pages": [
              "recruitment/overview",
              "recruitment/prolific-integration",
              "recruitment/bring-your-own-participants",
              "recruitment/panel-builder",
              "recruitment/scheduling-rounds",
              "recruitment/applicant-funnel"
            ]
          },
          {
            "group": "Live Sessions",
            "pages": [
              "sessions/how-ai-moderation-works",
              "sessions/participant-experience",
              "sessions/video-check",
              "sessions/stimulus-presentation",
              "sessions/monitoring-sessions"
            ]
          },
          {
            "group": "Analysis & Insights",
            "pages": [
              "analysis/running-analysis",
              "analysis/summary-tab",
              "analysis/deep-dive",
              "analysis/responses",
              "analysis/themes",
              "analysis/participant-analysis"
            ]
          },
          {
            "group": "Video Clips & Sharing",
            "pages": [
              "clips/auto-generated-clips",
              "clips/study-trailer",
              "clips/sharing-and-exports"
            ]
          },
          {
            "group": "Explore (AI Chat)",
            "pages": [
              "explore/overview",
              "explore/asking-questions",
              "explore/charts-and-citations"
            ]
          },
          {
            "group": "Workspace & Team",
            "pages": [
              "workspace/settings",
              "workspace/team-management",
              "workspace/roles-and-permissions"
            ]
          }
        ]
      },
      {
        "tab": "Resources",
        "groups": [
          {
            "group": "Best Practices",
            "pages": [
              "resources/writing-great-discussion-guides",
              "resources/screener-best-practices",
              "resources/maximizing-show-rates",
              "resources/getting-better-insights"
            ]
          },
          {
            "group": "Troubleshooting",
            "pages": [
              "resources/troubleshooting",
              "resources/faq"
            ]
          },
          {
            "group": "Platform",
            "pages": [
              "resources/security-and-privacy",
              "resources/changelog"
            ]
          }
        ]
      }
    ],
    "global": {
      "anchors": [
        {
          "anchor": "App",
          "href": "https://app.useconvo.ai",
          "icon": "arrow-up-right-from-square"
        },
        {
          "anchor": "Changelog",
          "href": "/resources/changelog",
          "icon": "clock-rotate-left"
        }
      ]
    }
  }
}
```

**Total: 38 pages** (vs. Conveo's 28, Outset's 22)

---

## 2. Page-by-Page Plan

---

### TAB: Guides

---

#### GROUP: Getting Started

---

##### Page: Introduction
- **File:** `introduction.mdx`
- **Priority:** P0
- **Description:** Welcome page explaining what Convo is and who it's for.
- **Content outline:**
  - What is Convo (AI-moderated focus groups, not 1:1 interviews -- differentiate)
  - Who it's for (UX researchers, product managers, marketers)
  - What makes Convo different (AI moderator "Peggy," multi-participant sessions, auto analysis)
  - How the docs are organized (guide readers to the right section)
  - Quick links: Quickstart, AI Study Builder, How AI Moderation Works
- **Media:** Hero illustration or product screenshot showing a live session
- **Word count:** Short (300-500)

---

##### Page: Quickstart — Run Your First Study in 15 Minutes
- **File:** `quickstart.mdx`
- **Priority:** P0
- **Description:** End-to-end tutorial that walks a new user through creating, launching, and analyzing their first study.
- **Content outline:**
  - Prerequisites (signed up, workspace created)
  - Step 1: Create a study with the AI Study Builder (describe goals, let AI generate guide)
  - Step 2: Review the discussion guide (moments, probes, priorities)
  - Step 3: Add a screener (optional, keep simple for first study)
  - Step 4: Set up recruitment (Prolific panel or share a link)
  - Step 5: Launch a recruitment round
  - Step 6: Sessions run automatically -- what to expect
  - Step 7: Run analysis and review the summary
  - Step 8: Explore findings with AI Chat
  - What to do next (links to deeper docs)
- **Media:**
  - Screenshot: AI Study Builder chat interface
  - Screenshot: Discussion guide with moments
  - Screenshot: Recruitment round launch
  - Screenshot: Analysis summary tab
  - GIF or short video: The full flow (optional, high-effort)
- **Word count:** Long (1000+)
- **Strategic note:** Neither Conveo nor Outset has a true first-study walkthrough. This is the single highest-impact page.

---

##### Page: Key Concepts
- **File:** `key-concepts.mdx`
- **Priority:** P0
- **Description:** Glossary of Convo-specific terminology so users share a common vocabulary.
- **Content outline:**
  - Study (the top-level container)
  - Discussion Guide / Moments (the ordered list of topics)
  - Probes (follow-up questions within a moment)
  - Stimulus (media shown during a moment)
  - Screener (qualification questionnaire)
  - Panel (a set of recruitment filters on Prolific)
  - Recruitment Round (a scheduled batch of sessions)
  - Peggy (the AI moderator)
  - Director Agent (secondary AI that monitors and adapts)
  - Explore (AI chat for post-study Q&A)
  - Study Trailer (auto-generated highlight reel)
  - Applicant funnel stages: New, Screener, Video check, Qualified, Signed up, Joined
  - Study lifecycle: Draft, Active, Completed, Archived
- **Media:** Diagram showing study lifecycle states
- **Word count:** Medium (500-1000)

---

#### GROUP: Creating Studies

---

##### Page: AI Study Builder
- **File:** `studies/ai-study-builder.mdx`
- **Priority:** P0
- **Description:** How to use Convo's chat-based AI builder to generate a complete study from a research goal or existing guide.
- **Content outline:**
  - What the AI builder does (5-step chat flow, powered by Claude)
  - Starting from scratch: describe your research goals
  - Starting from an existing guide: upload your document
  - How the live artifact preview works
  - Reviewing and editing the generated study
  - When to use the AI builder vs. the manual editor
  - Tips for writing effective prompts for the builder
- **Media:**
  - Screenshot: AI builder chat interface with example prompt
  - Screenshot: Live artifact preview showing generated discussion guide
  - Screenshot: Transition from builder to editor
- **Word count:** Medium (500-1000)

---

##### Page: Manual Study Editor
- **File:** `studies/manual-editor.mdx`
- **Priority:** P0
- **Description:** Reference guide for the form-based study editor and all its sections.
- **Content outline:**
  - Editor overview (Basic Info, Discussion Guide, Interview Settings, Welcome Screen, Screener tabs)
  - Basic Info fields (title, description, objectives)
  - Interview Settings (duration, participant count, any configurable options)
  - Welcome Screen configuration
  - Navigating between sections
  - Saving and activating
- **Media:**
  - Screenshot: Editor with each section tab highlighted
  - Screenshot: Basic Info form
- **Word count:** Medium (500-1000)

---

##### Page: Discussion Guide (Moments)
- **File:** `studies/discussion-guide.mdx`
- **Priority:** P0
- **Description:** How to structure your discussion guide using moments, probes, priorities, and stimuli.
- **Content outline:**
  - What is a moment (a topic/question block in the guide)
  - Anatomy of a moment: script, priority, goals, probes, stimulus
  - Setting priority levels (Low / Medium / High) -- how this affects moderation
  - Writing effective scripts (what the AI moderator will say/ask)
  - Goals / signal detection (what you want to learn from this moment)
  - Adding probes (follow-up questions the moderator can ask)
  - Attaching stimuli (URL and description for images/videos)
  - Ordering moments and auto-calculated durations
  - Best practices: how many moments, how to balance depth vs. breadth
- **Media:**
  - Screenshot: A well-structured moment with all fields filled
  - Screenshot: Moment list showing ordering and durations
  - Diagram: How priority affects time allocation
- **Word count:** Long (1000+)
- **Strategic note:** Conveo has good stimuli docs. Match or exceed that quality. Convo's "moments" concept is unique -- explain it thoroughly.

---

##### Page: Screener
- **File:** `studies/screener.mdx`
- **Priority:** P1
- **Description:** How to build a screener to qualify participants before they join sessions.
- **Content outline:**
  - What the screener does and when participants see it
  - Adding sections and questions
  - Question types: Multiple choice, Open text, Number, Yes/No
  - Question settings: required, allow multiple selections, selection limits, randomize options
  - Per-option disqualification (auto-reject based on answers)
  - Screener strategy: keep it short, focus on must-have criteria
- **Media:**
  - Screenshot: Screener builder with a multi-question screener
  - Screenshot: Disqualification option configuration
- **Word count:** Medium (500-1000)

---

##### Page: Welcome Screen
- **File:** `studies/welcome-screen.mdx`
- **Priority:** P2
- **Description:** How to customize the welcome screen participants see before joining.
- **Content outline:**
  - What the welcome screen is
  - Customization options
  - Best practices for setting expectations
- **Media:** Screenshot of welcome screen editor and participant-facing view
- **Word count:** Short (300-500)

---

##### Page: Interview Settings
- **File:** `studies/interview-settings.mdx`
- **Priority:** P2
- **Description:** Reference for configuring session duration, participant count, and other session parameters.
- **Content outline:**
  - Available settings
  - Recommended configurations for different study types
  - How settings affect the AI moderator's behavior
- **Media:** Screenshot of settings panel
- **Word count:** Short (300-500)

---

##### Page: Versioning & Study Lifecycle
- **File:** `studies/versioning-and-lifecycle.mdx`
- **Priority:** P1
- **Description:** How study drafts, active versions, and the study lifecycle work.
- **Content outline:**
  - Study states: Draft, Active, Completed, Archived
  - What you can/can't edit in each state
  - Versioning: editing an active study creates a draft version
  - Activating a draft version (replaces the current active version)
  - Discarding a draft
  - Archiving completed studies
- **Media:** Diagram of study lifecycle state machine
- **Word count:** Medium (500-1000)

---

#### GROUP: Recruitment

---

##### Page: Recruitment Overview
- **File:** `recruitment/overview.mdx`
- **Priority:** P0
- **Description:** Overview of Convo's two recruitment paths and how the participant funnel works.
- **Content outline:**
  - Two options: Prolific integration or Bring Your Own participants
  - When to use each
  - The applicant funnel: New -> Screener -> Video check -> Qualified -> Signed up -> Joined
  - How each stage works at a high level
  - Link out to detailed pages
- **Media:**
  - Diagram: Applicant funnel with all stages
- **Word count:** Medium (500-1000)

---

##### Page: Prolific Integration
- **File:** `recruitment/prolific-integration.mdx`
- **Priority:** P0
- **Description:** How to recruit participants through Prolific's panel directly from Convo.
- **Content outline:**
  - What is Prolific and why Convo integrates with it
  - Connecting your Prolific account (if applicable)
  - How Convo publishes studies to Prolific
  - Automated messaging: RSVP confirmations, reminders, no-show follow-ups
  - Prolific-specific considerations (approval, rejection, bonus payments)
- **Media:**
  - Screenshot: Prolific panel configuration in Convo
- **Word count:** Medium (500-1000)

---

##### Page: Bring Your Own Participants
- **File:** `recruitment/bring-your-own-participants.mdx`
- **Priority:** P0
- **Description:** How to recruit participants using a direct shareable link.
- **Content outline:**
  - When to use BYO (existing customer panels, internal research, specific communities)
  - Getting and sharing the direct link
  - What participants experience (signup flow: welcome -> screener -> video check -> contact info -> calendar)
  - Tracking applicants through the funnel
- **Media:**
  - Screenshot: Direct link sharing UI
  - Screenshot: Participant-facing signup flow
- **Word count:** Medium (500-1000)

---

##### Page: Panel Builder
- **File:** `recruitment/panel-builder.mdx`
- **Priority:** P1
- **Description:** How to configure Prolific panel filters, sample sizes, and rewards.
- **Content outline:**
  - What a panel is (a filtered segment of Prolific participants)
  - Setting demographic and behavioral filters
  - Setting sample size and reward amount
  - Eligible pool indicator (how to interpret it)
  - Creating multiple panels per study (e.g., different demographics)
- **Media:**
  - Screenshot: Panel builder with filters applied and pool indicator
- **Word count:** Medium (500-1000)

---

##### Page: Scheduling Recruitment Rounds
- **File:** `recruitment/scheduling-rounds.mdx`
- **Priority:** P1
- **Description:** How to schedule, launch, pause, and manage recruitment rounds.
- **Content outline:**
  - What is a recruitment round (a batch of scheduled sessions)
  - Creating a round: setting date/time, number of slots
  - Launching a round
  - Pausing and resuming
  - Managing multiple rounds
  - Join window management
- **Media:**
  - Screenshot: Round scheduling interface
  - Screenshot: Active round with participant status
- **Word count:** Medium (500-1000)

---

##### Page: Applicant Funnel
- **File:** `recruitment/applicant-funnel.mdx`
- **Priority:** P1
- **Description:** Detailed breakdown of each applicant stage and how to manage participants through the funnel.
- **Content outline:**
  - Stage-by-stage breakdown:
    - New: participant clicked link / accepted Prolific study
    - Screener: answering qualification questions
    - Video check: AI-powered A/V quality validation
    - Qualified: passed screener + video check
    - Signed up: confirmed contact info and session time
    - Joined: actually entered the session
  - Viewing and filtering applicants by stage
  - Common drop-off points and what to do about them
- **Media:**
  - Screenshot: Applicant list with funnel stage filters
- **Word count:** Medium (500-1000)

---

#### GROUP: Live Sessions

---

##### Page: How AI Moderation Works
- **File:** `sessions/how-ai-moderation-works.mdx`
- **Priority:** P0
- **Description:** Technical and practical explanation of how Convo's AI moderator runs live multi-participant sessions.
- **Content outline:**
  - Meet Peggy: Convo's AI moderator (warm but direct personality)
  - The technology stack: Claude for reasoning, Deepgram for speech-to-text, ElevenLabs/Cartesia for text-to-speech
  - Session stages: Waiting Room -> Intro -> Discussion -> Conclusion -> Ended
  - How Peggy follows the discussion guide (moments, priorities, probes)
  - The Director Agent: a secondary AI that monitors the session and can restructure the discussion mid-session if needed
  - Multi-participant handling: speaker identification, turn management
  - Real-time transcription with speaker ID
  - How stimuli are presented during sessions
  - What happens if something goes wrong (participant drops, audio issues)
- **Media:**
  - Diagram: Session stages flow
  - Diagram: AI moderation architecture (simplified -- Peggy + Director + participant)
  - Screenshot: Active session view (if there's an observer/monitor view)
- **Word count:** Long (1000+)
- **Strategic note:** This is Convo's core differentiator. No competitor documents their AI moderation in depth. Go deep here -- researchers want to understand what's happening under the hood so they can trust the tool.

---

##### Page: Participant Experience
- **File:** `sessions/participant-experience.mdx`
- **Priority:** P0
- **Description:** What participants see and experience from signup through the end of a session.
- **Content outline:**
  - The full participant journey: link/Prolific -> Welcome screen -> Screener -> Video check -> Contact info -> Calendar -> Join page -> Session -> End
  - What the join page looks like (device settings, echo detection)
  - What a live session feels like for the participant
  - How Peggy introduces herself and the topic
  - How stimuli appear on the participant's screen
  - Session conclusion and what happens after
- **Media:**
  - Screenshot: Participant join page
  - Screenshot: Participant in-session view
  - Screenshot: Stimulus display from participant perspective
- **Word count:** Medium (500-1000)
- **Strategic note:** Useful for researchers who want to preview the experience before recruiting. Neither Conveo nor Outset documents this well.

---

##### Page: Video & Audio Check
- **File:** `sessions/video-check.mdx`
- **Priority:** P1
- **Description:** How Convo's AI-powered video/audio quality check works and why it matters.
- **Content outline:**
  - What the video check evaluates: face visibility, lighting, background, microphone quality
  - Why it exists (data quality -- ensure clear audio for transcription)
  - The 3-attempt limit
  - What participants see during the check
  - Common failure reasons and guidance for participants
- **Media:**
  - Screenshot: Video check pass/fail screen
- **Word count:** Short (300-500)

---

##### Page: Stimulus Presentation
- **File:** `sessions/stimulus-presentation.mdx`
- **Priority:** P1
- **Description:** How to configure and present images and videos to participants during specific moments.
- **Content outline:**
  - What stimuli are (images, videos shown during discussion)
  - Attaching a stimulus to a moment (URL + description)
  - Supported formats
  - How and when the stimulus appears during the session
  - Tips for effective stimulus use (file size, resolution, context)
- **Media:**
  - Screenshot: Stimulus configuration in moment editor
  - Screenshot: Stimulus as displayed to participants
- **Word count:** Medium (500-1000)

---

##### Page: Monitoring Sessions
- **File:** `sessions/monitoring-sessions.mdx`
- **Priority:** P2
- **Description:** How to monitor live and completed sessions, view transcripts, and review session data.
- **Content outline:**
  - Viewing session status (in progress, completed)
  - Session details: transcript, participant list, logs
  - Real-time transcript with speaker identification and timestamps
  - Audio recordings
  - Session performance metrics
- **Media:**
  - Screenshot: Session details page with transcript
- **Word count:** Medium (500-1000)

---

#### GROUP: Analysis & Insights

---

##### Page: Running Analysis
- **File:** `analysis/running-analysis.mdx`
- **Priority:** P0
- **Description:** How to trigger Convo's AI analysis pipeline and what to expect.
- **Content outline:**
  - When to run analysis (after sessions are complete)
  - How to trigger analysis (manual trigger)
  - Analysis pipeline stages: Pending -> Preparing -> Analyzing -> Generating clips -> Complete
  - How long it takes (set expectations)
  - What gets generated: summary, deep dive, responses, themes, clips, trailer
- **Media:**
  - Screenshot: Analysis trigger button and progress indicator
- **Word count:** Short (300-500)

---

##### Page: Summary Tab
- **File:** `analysis/summary-tab.mdx`
- **Priority:** P0
- **Description:** How to read and use the AI-generated study summary with metrics, decisions, and findings.
- **Content outline:**
  - Overview section
  - Metrics cards: participant count, consensus rate, debates
  - Per-objective decisions: verdict, confidence level, evidence, pulls/pushes, quotes, recommendations
  - Key findings
  - Agreements and debates
  - Emergent insights (things the AI found that weren't in your guide)
  - Auto-generated charts
  - How to interpret confidence levels
- **Media:**
  - Screenshot: Full summary tab overview
  - Screenshot: A decision card with verdict, confidence, and evidence
  - Screenshot: Auto-generated chart
- **Word count:** Long (1000+)
- **Strategic note:** Outset has ZERO analysis docs. Conveo has some but not at this depth. This is a massive gap to fill. Go very detailed here.

---

##### Page: Deep Dive
- **File:** `analysis/deep-dive.mdx`
- **Priority:** P1
- **Description:** How to use the moment-by-moment deep dive analysis view.
- **Content outline:**
  - What the deep dive shows (analysis broken down by each moment)
  - Navigating between moments
  - How to drill into specific topics
  - Connecting deep dive findings to summary-level conclusions
- **Media:**
  - Screenshot: Deep dive view for a single moment
- **Word count:** Medium (500-1000)

---

##### Page: Responses
- **File:** `analysis/responses.mdx`
- **Priority:** P1
- **Description:** How to view and compare individual participant responses organized by moment.
- **Content outline:**
  - What the responses view shows
  - Filtering by participant or moment
  - Comparing responses across participants for the same question
  - Using responses for quote-mining and report building
- **Media:**
  - Screenshot: Responses tab with participant responses
- **Word count:** Medium (500-1000)

---

##### Page: Theme Analysis
- **File:** `analysis/themes.mdx`
- **Priority:** P1
- **Description:** How to explore cross-cutting themes with quotes and filters.
- **Content outline:**
  - What theme analysis is (AI-identified patterns across all sessions)
  - How themes are generated
  - Viewing quotes associated with each theme
  - Filtering themes by objective, moment, or participant
  - Using themes for synthesis and reporting
- **Media:**
  - Screenshot: Theme list with quote count
  - Screenshot: Theme detail with quotes and filters
- **Word count:** Medium (500-1000)

---

##### Page: Participant Analysis
- **File:** `analysis/participant-analysis.mdx`
- **Priority:** P2
- **Description:** How to review individual participant engagement metrics and contributions.
- **Content outline:**
  - Per-participant metrics: engagement level, word count, turns, decision influence
  - Viewing participant quotes
  - Identifying dominant vs. quiet participants
  - Using participant analysis for recruitment quality assessment
- **Media:**
  - Screenshot: Participant analysis view
- **Word count:** Medium (500-1000)

---

#### GROUP: Video Clips & Sharing

---

##### Page: Auto-Generated Clips
- **File:** `clips/auto-generated-clips.mdx`
- **Priority:** P0
- **Description:** How Convo automatically generates video clips highlighting key moments from sessions.
- **Content outline:**
  - What auto-generated clips are (AI identifies key moments, creates short video clips)
  - How clips are generated (part of the analysis pipeline, enhanced via Mux)
  - Browsing and previewing clips
  - How clips connect to analysis findings
  - Using clips in presentations and stakeholder communication
- **Media:**
  - Screenshot: Clips gallery
  - Screenshot: Individual clip player
- **Word count:** Medium (500-1000)
- **Strategic note:** Neither Conveo nor Outset documents anything like this. Major differentiator.

---

##### Page: Study Trailer
- **File:** `clips/study-trailer.mdx`
- **Priority:** P0
- **Description:** How Convo auto-generates a shareable highlight reel from your study's best moments.
- **Content outline:**
  - What a study trailer is (auto-generated highlight reel)
  - How it's generated (AI selects clips, assembles into a coherent reel)
  - Previewing your trailer
  - Sharing via public URL (no authentication required for viewers)
  - Use cases: stakeholder buy-in, team alignment, executive summaries
- **Media:**
  - Screenshot: Trailer preview
  - Screenshot: Share dialog with public URL
- **Word count:** Medium (500-1000)
- **Strategic note:** Completely unique to Convo. No competitor has anything like this. Highlight it prominently.

---

##### Page: Sharing & Exports
- **File:** `clips/sharing-and-exports.mdx`
- **Priority:** P1
- **Description:** How to export analysis results and share findings with stakeholders.
- **Content outline:**
  - PDF export of analysis summary
  - Sharing study trailers via public link
  - Who can access shared content (public links require no auth)
  - Tips for presenting findings to stakeholders
- **Media:**
  - Screenshot: Export/share options
  - Screenshot: PDF export preview
- **Word count:** Short (300-500)

---

#### GROUP: Explore (AI Chat)

---

##### Page: Explore Overview
- **File:** `explore/overview.mdx`
- **Priority:** P0
- **Description:** Introduction to Convo's AI-powered chat interface for querying study findings.
- **Content outline:**
  - What Explore is (conversational Q&A about your study data)
  - When to use it (after analysis is complete)
  - What it can do: answer questions, search transcripts, generate charts, cite specific clips/participants
  - Confidence indicators (how sure the AI is about its answers)
  - Multiple conversations per study
  - Suggested questions to get started
- **Media:**
  - Screenshot: Explore chat interface with a sample question and answer
  - Screenshot: Confidence indicator on a response
- **Word count:** Medium (500-1000)
- **Strategic note:** Listen Labs has a "Research Agent" but doesn't document it well. Conveo and Outset have nothing comparable. Document this thoroughly.

---

##### Page: Asking Questions
- **File:** `explore/asking-questions.mdx`
- **Priority:** P1
- **Description:** Tips and examples for getting the most out of Explore's conversational interface.
- **Content outline:**
  - Types of questions that work well:
    - Summary questions ("What did participants think about X?")
    - Comparison questions ("How did reactions differ between groups?")
    - Quote-finding ("Find quotes about pricing concerns")
    - Pattern questions ("Were there any surprising findings?")
  - Uploading files for additional context
  - Managing multiple conversations
  - Using suggested questions as starting points
- **Media:**
  - Screenshot: Example questions and AI responses
- **Word count:** Medium (500-1000)

---

##### Page: Charts & Citations
- **File:** `explore/charts-and-citations.mdx`
- **Priority:** P2
- **Description:** How Explore generates charts and cites specific clips and participants in its answers.
- **Content outline:**
  - How chart generation works (AI creates visualizations from study data)
  - How citations work (links to specific clips, participants, transcript segments)
  - Clicking through citations to source material
  - Using generated charts in reports
- **Media:**
  - Screenshot: AI-generated chart in Explore
  - Screenshot: Citation linking to a clip
- **Word count:** Short (300-500)

---

#### GROUP: Workspace & Team

---

##### Page: Workspace Settings
- **File:** `workspace/settings.mdx`
- **Priority:** P1
- **Description:** How to configure your workspace name, company context, and other settings.
- **Content outline:**
  - Renaming your workspace
  - Setting company context (used by AI for better moderation and analysis)
  - Deleting a workspace (irreversible, warnings)
  - Multi-workspace support
- **Media:**
  - Screenshot: Workspace settings page
- **Word count:** Short (300-500)

---

##### Page: Team Management
- **File:** `workspace/team-management.mdx`
- **Priority:** P1
- **Description:** How to invite team members and manage your workspace team.
- **Content outline:**
  - Inviting members via email
  - Viewing current team members
  - Changing member roles
  - Removing members
- **Media:**
  - Screenshot: Team management page
- **Word count:** Short (300-500)

---

##### Page: Roles & Permissions
- **File:** `workspace/roles-and-permissions.mdx`
- **Priority:** P2
- **Description:** Reference for the Owner, Admin, and Member roles and what each can do.
- **Content outline:**
  - Role definitions: Owner, Admin, Member
  - Permissions matrix (table format):
    - Create/edit/delete studies
    - Manage team members
    - Workspace settings
    - Invite new members
    - Delete workspace
  - How to change roles
  - Transferring ownership
- **Media:** None needed (table is sufficient)
- **Word count:** Short (300-500)

---

### TAB: Resources

---

#### GROUP: Best Practices

---

##### Page: Writing Great Discussion Guides
- **File:** `resources/writing-great-discussion-guides.mdx`
- **Priority:** P1
- **Description:** Research-backed advice for structuring discussion guides that produce actionable insights.
- **Content outline:**
  - How many moments to include (and why)
  - Setting the right priority mix (not everything can be High)
  - Writing scripts the AI moderator will deliver naturally
  - Crafting effective probes
  - Using goals/signal detection to focus the AI
  - Balancing structure vs. flexibility
  - Common mistakes and how to avoid them
  - Example: a well-structured 6-moment guide (annotated)
- **Media:** Annotated screenshot of an example discussion guide
- **Word count:** Long (1000+)
- **Strategic note:** Conveo has good guide-writing docs. Match their quality and add Convo-specific advice (moments, priorities, Director Agent behavior).

---

##### Page: Screener Best Practices
- **File:** `resources/screener-best-practices.mdx`
- **Priority:** P2
- **Description:** How to write screeners that effectively qualify participants without creating drop-off.
- **Content outline:**
  - Keep it short (ideal number of questions)
  - Use disqualification options strategically
  - Avoid leading questions
  - Balance specificity vs. recruitment pool size
  - When to use open-text vs. multiple choice
- **Media:** None
- **Word count:** Medium (500-1000)

---

##### Page: Maximizing Show Rates
- **File:** `resources/maximizing-show-rates.mdx`
- **Priority:** P2
- **Description:** Tactics for reducing no-shows and maximizing the number of participants who actually join sessions.
- **Content outline:**
  - How automated Prolific messaging helps (RSVP, reminders, no-show follow-ups)
  - Optimal scheduling (days of week, times of day)
  - Reward amount guidance
  - Over-recruiting strategy (invite more than you need)
  - BYO: communication tips for your own participant panels
  - How the video check affects show rates (set expectations upfront)
- **Media:** None
- **Word count:** Medium (500-1000)
- **Strategic note:** Outset has 8 recruitment articles. This page consolidates the most valuable advice into one actionable guide.

---

##### Page: Getting Better Insights
- **File:** `resources/getting-better-insights.mdx`
- **Priority:** P2
- **Description:** Tips for study design and analysis workflow that lead to higher-quality, more actionable insights.
- **Content outline:**
  - Setting clear objectives before building your guide
  - Using the right number of participants
  - How priority levels affect depth of discussion
  - Making the most of the analysis pipeline
  - Using Explore to go beyond the summary
  - Combining clips + themes for stakeholder presentations
- **Media:** None
- **Word count:** Medium (500-1000)

---

#### GROUP: Troubleshooting

---

##### Page: Troubleshooting
- **File:** `resources/troubleshooting.mdx`
- **Priority:** P1
- **Description:** Solutions for common issues users encounter.
- **Content outline:**
  - Session issues:
    - Participant can't join (browser permissions, firewall)
    - Audio echo detected on join page
    - Participant dropped mid-session
  - Recruitment issues:
    - Low eligible pool on Prolific
    - Participants failing video check repeatedly
    - Low show rates
  - Analysis issues:
    - Analysis stuck in "Preparing" or "Analyzing" state
    - Clips not generating
  - General:
    - Can't edit an active study (need to create a draft version)
    - Invited team member didn't receive email
  - Contact support link
- **Media:** None
- **Word count:** Long (1000+)
- **Strategic note:** Zero competitors have troubleshooting docs. Easy win.

---

##### Page: FAQ
- **File:** `resources/faq.mdx`
- **Priority:** P1
- **Description:** Answers to the most common questions about Convo.
- **Content outline:**
  - How many participants can be in a session at once?
  - Can I observe sessions in real time?
  - What languages does Convo support?
  - How long does analysis take?
  - Can I edit my discussion guide after launching a study?
  - How does Convo ensure data quality?
  - What happens if a participant has technical issues?
  - Is my data secure?
  - Can I use Convo for 1:1 interviews or only focus groups?
  - How does the AI moderator handle off-topic responses?
- **Media:** None (use Mintlify's Accordion component)
- **Word count:** Medium (500-1000)
- **Strategic note:** No competitor has an FAQ in their docs. Use Mintlify's accordion component for clean presentation.

---

#### GROUP: Platform

---

##### Page: Security & Privacy
- **File:** `resources/security-and-privacy.mdx`
- **Priority:** P1
- **Description:** Overview of how Convo handles data security, privacy, and compliance.
- **Content outline:**
  - Data storage and encryption
  - Where data is hosted (cloud provider, region)
  - Audio/video recording storage (S3, presigned URLs -- no permanent public access)
  - Third-party services and their roles:
    - Deepgram (transcription)
    - ElevenLabs/Cartesia (text-to-speech)
    - Mux (video processing)
    - LiveKit (real-time video)
    - Anthropic/Claude (AI moderation and analysis)
  - Data retention policies
  - Participant data handling
  - GDPR/privacy considerations
  - How to request data deletion
  - Contact for security questions
- **Media:** None
- **Word count:** Medium (500-1000)
- **Strategic note:** No competitor has a security page. Enterprise buyers and institutional researchers will look for this. Even a basic page signals maturity.

---

##### Page: Changelog
- **File:** `resources/changelog.mdx`
- **Priority:** P2
- **Description:** Running log of new features, improvements, and fixes.
- **Content outline:**
  - Use Mintlify's changelog/update format
  - Most recent updates first
  - Each entry: date, title, description, category tag (New / Improved / Fixed)
  - Start with 3-5 entries covering recent notable features
  - Commit to updating at least biweekly
- **Media:** Feature screenshots for major releases
- **Word count:** Ongoing (start with Medium)
- **Strategic note:** No competitor maintains a changelog. This signals active development and builds trust. Low effort to maintain once the template is set.

---

## 3. Priority Summary

### P0 -- Launch Blockers (14 pages)

These pages must exist before the docs site goes live.

| # | Page | Group |
|---|------|-------|
| 1 | Introduction | Getting Started |
| 2 | Quickstart | Getting Started |
| 3 | Key Concepts | Getting Started |
| 4 | AI Study Builder | Creating Studies |
| 5 | Manual Study Editor | Creating Studies |
| 6 | Discussion Guide (Moments) | Creating Studies |
| 7 | Recruitment Overview | Recruitment |
| 8 | Prolific Integration | Recruitment |
| 9 | Bring Your Own Participants | Recruitment |
| 10 | How AI Moderation Works | Live Sessions |
| 11 | Participant Experience | Live Sessions |
| 12 | Running Analysis | Analysis & Insights |
| 13 | Summary Tab | Analysis & Insights |
| 14 | Auto-Generated Clips | Video Clips & Sharing |
| 15 | Study Trailer | Video Clips & Sharing |
| 16 | Explore Overview | Explore (AI Chat) |

**Estimated total for P0: ~12,000-15,000 words**

### P1 -- Launch Week (14 pages)

Ship within the first week after launch.

| # | Page | Group |
|---|------|-------|
| 1 | Screener | Creating Studies |
| 2 | Versioning & Study Lifecycle | Creating Studies |
| 3 | Panel Builder | Recruitment |
| 4 | Scheduling Rounds | Recruitment |
| 5 | Applicant Funnel | Recruitment |
| 6 | Video & Audio Check | Live Sessions |
| 7 | Stimulus Presentation | Live Sessions |
| 8 | Deep Dive | Analysis & Insights |
| 9 | Responses | Analysis & Insights |
| 10 | Theme Analysis | Analysis & Insights |
| 11 | Sharing & Exports | Video Clips & Sharing |
| 12 | Asking Questions | Explore (AI Chat) |
| 13 | Workspace Settings | Workspace & Team |
| 14 | Team Management | Workspace & Team |
| 15 | Writing Great Discussion Guides | Best Practices |
| 16 | Troubleshooting | Troubleshooting |
| 17 | FAQ | Troubleshooting |
| 18 | Security & Privacy | Platform |

### P2 -- Fast Follow (8 pages)

Ship within 2-3 weeks after launch.

| # | Page | Group |
|---|------|-------|
| 1 | Welcome Screen | Creating Studies |
| 2 | Interview Settings | Creating Studies |
| 3 | Monitoring Sessions | Live Sessions |
| 4 | Participant Analysis | Analysis & Insights |
| 5 | Charts & Citations | Explore (AI Chat) |
| 6 | Roles & Permissions | Workspace & Team |
| 7 | Screener Best Practices | Best Practices |
| 8 | Maximizing Show Rates | Best Practices |
| 9 | Getting Better Insights | Best Practices |
| 10 | Changelog | Platform |

---

## 4. Strategic Notes

### Where Convo Can Differentiate From Competitors in Docs

1. **First-study quickstart tutorial (vs. everyone).** No competitor has a true end-to-end walkthrough. The Quickstart page is the single highest-ROI page in this plan. Make it excellent.

2. **AI moderation transparency (vs. everyone).** Researchers need to trust the AI moderator before they'll use it for real research. The "How AI Moderation Works" page should go deeper than any competitor -- explain the Director Agent, how priorities affect behavior, how probes work in practice. This builds credibility.

3. **Analysis documentation (vs. Outset).** Outset has zero analysis docs in their help center. Convo's analysis pipeline (summary, deep dive, themes, participant analysis) is a major selling point -- document every tab thoroughly.

4. **Video clips and study trailer (vs. everyone).** Completely unique. No competitor documents anything like auto-generated clips or a shareable highlight reel. These features sell themselves once people understand them.

5. **Explore / AI Chat (vs. everyone).** Listen Labs has a "Research Agent" but barely documents it. Conveo and Outset have nothing comparable. Show researchers what's possible with concrete example questions and responses.

6. **Troubleshooting and FAQ (vs. everyone).** Zero competitors have either. Low effort, high trust signal.

7. **Security & Privacy page (vs. everyone).** No competitor has one. Enterprise and academic buyers check for this. Even a basic page removes a sales objection.

8. **Changelog (vs. everyone).** No competitor maintains one. Signals active development. Start it at launch and commit to regular updates.

### Template Recommendations

Adopt Conveo's successful page template pattern. Each non-reference page should include:

- **Overview** -- 2-3 sentences on what this feature does and why it matters
- **Step-by-step instructions** -- numbered, with screenshots
- **Pro tips** -- callout boxes with expert advice (use Mintlify's `<Tip>` component)
- **Quick reference** -- summary table or bullet list at the bottom for returning users
- **What's next** -- links to related pages

### Mintlify Features to Use

- **`<Tip>`, `<Warning>`, `<Info>` callouts** -- for pro tips, gotchas, and context
- **`<Accordion>` groups** -- for FAQ page
- **`<Steps>` component** -- for all step-by-step instructions
- **`<Card>` groups** -- for the Introduction page's quick links
- **`<Frame>` component** -- for all screenshots (adds consistent border/shadow)
- **Tabs component** -- for pages that cover multiple paths (e.g., Prolific vs. BYO)
- **LLMs.txt** -- add it (Conveo has it, easy to generate from Mintlify)

### Content Production Order

Within each priority tier, write pages in this order to maximize impact:

**P0 batch 1 (core flow):**
1. Introduction
2. Key Concepts
3. Quickstart
4. AI Study Builder
5. Discussion Guide

**P0 batch 2 (recruitment + sessions):**
6. Recruitment Overview
7. Prolific Integration
8. Bring Your Own Participants
9. How AI Moderation Works
10. Participant Experience

**P0 batch 3 (analysis + differentiators):**
11. Manual Study Editor
12. Running Analysis
13. Summary Tab
14. Auto-Generated Clips
15. Study Trailer
16. Explore Overview

---

## 5. Estimated Totals

| Metric | Count |
|--------|-------|
| Total pages | 38 |
| P0 pages | 16 |
| P1 pages | 18 |
| P2 pages | 10 |
| Estimated total word count | 22,000 - 28,000 |
| Screenshots/media needed | ~45-55 |
| Diagrams needed | ~5-6 |
