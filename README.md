PannaPalat AI Video Maker (v1, mock AI)

A simple web app that turns one story idea into a Shorts production package: story, character reference, 8 scenes, image prompts, video prompts, Bengali/Hindi narration, subtitles (.srt) and a downloadable project .zip. It works offline and needs no API key.

How to run

Easiest: open index.html in Chrome (double-click it on a computer; on Android, copy the folder to your phone and open index.html with Chrome).

Optional local server: in this folder run python3 -m http.server 8000, then open http://localhost:8000

Files
index.html – the page
style.css – mobile-friendly look (also supports dark mode)
app.js – connects the buttons to the results
mockAI.js – fake "AI" using templates (replace this later)
exporter.js – builds the project folder and .zip
Important

The text is template-based: your idea is saved and shown, but the mock story does not truly understand it yet. Prompts are only prompts; no images, videos or voices are generated.

Next step: real AI

Replace MockAI.buildProject() with a call to your own small server that talks to an AI service. Keep API keys on that server, never in these files. Check free limits first; paid services only with your OK.

v2 additions
Tabs: Story & Prompts, Editing Plan, YouTube SEO.
Character Card: edit name, age, appearance, clothes, hairstyle, personality. It is saved on your device and the same sentence is used in every image prompt.
Story controls: 30/40/60/90 seconds (scenes = seconds / 5) and 8 genres.
Export zip: story.txt, character.txt, scene-prompts.txt, narration.txt, subtitles.srt, editing-plan.json, youtube-seo.txt, sound_plan.txt, project.json.
Longer videos (60s/90s) repeat story beats as silent cutaway shots; genre changes the mood and music cues, not the mock story text.
