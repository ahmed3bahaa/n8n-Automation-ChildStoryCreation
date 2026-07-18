# Workflow Overview

The workflow generates a child-friendly storybook from a short request.

## Input

The webhook expects:

```json
{
  "character": "Main character description",
  "setting": "Where the story happens",
  "theme": "Lesson, mood, or moral",
  "email": "Recipient email address"
}
```

## Main Stages

1. **Webhook**  
   Receives the story request at `/generate-image`.

2. **Set**  
   Normalizes the incoming body fields: `character`, `setting`, `theme`, and `email`.

3. **Parser**  
   Uses OpenAI to label and structure the request values.

4. **Split**  
   Uses OpenAI to write exactly five scenes. Each scene is expected to be 3-5 sentences.

5. **scene split**  
   Splits the five-scene story into individual scene items.

6. **Image generation/compression**  
   Generates images for scenes and prepares image binaries for storybook assembly.

7. **Scene-image-align**  
   Pairs each scene with its matching image.

8. **binary-to-html**  
   Builds the HTML storybook layout.

9. **pdf.call**  
   Converts the HTML storybook into a PDF file.

10. **Send Email**  
    Sends the generated PDF to the submitted email address.

11. **Google Drive / Google Drive1**  
    Stores or organizes the generated file in Google Drive.

## Output

The intended user-facing output is an emailed PDF storybook containing:

- Five short scenes.
- Scene titles.
- Story text.
- Scene images.

## Notes

- The workflow is inactive in the repository template.
- Credentials must be reconnected after import.
- Generated content quality depends on prompt tuning and chosen models.
