# AI Applications Job 3 Theory — Animated Data Augmentation

A self-contained, left-to-right HTML lesson deck for ITE vocational students studying **AI Applications (EC53302FP)**.

The lesson is built around one concrete explanation:

> The computer pretends to take more photos from one existing photo.

Students watch each image change before learning the technical terms **transformation** and **data augmentation**.

## Files

- `index.html` — complete 35-slide lesson deck.
- `TEACHER-GUIDE.md` — pacing, prompts and teaching sequence.
- `preview.png` — title-slide preview.
- `.nojekyll` — allows GitHub Pages to serve the static files directly.

No framework, build command, external font or image file is required. The flowers are generated as inline SVG graphics.

## Main interactive features

- Automatic flip, rotation, zoom, brightness, contrast and noise demonstrations.
- A **Transformation Playground** with Original, Flip, Rotate, Zoom, Darker, Contrast, Noise and Random buttons.
- A **Random Transformation Generator** that creates a new recipe and view automatically or when clicked.
- A sequential **one-photo-to-many-views factory** animation.
- Interactive 90/10, 80/20 and 70/30 training/validation split.
- Self-marking concept checks.
- Training and validation curve explanations.
- Teacher notes, slide overview, keyboard navigation, swipe navigation and URL deep links.

## Lesson progression

1. Bridge from the Job 2 cat/CNN lesson.
2. Show why one neat photo is not enough.
3. Define a transformation as one controlled image change.
4. Animate flip, rotation, zoom/crop, brightness, contrast and noise.
5. Establish the rule: **change the view, keep the answer**.
6. Let students operate the playground and random generator.
7. Reveal the formal term **data augmentation** only after the visual idea is understood.
8. Connect augmentation to the training pipeline, validation split, overfitting and dropout.
9. Read the Keras code, compare curves and predict new flower images.
10. Complete the Job Sheet ratio and new-image investigations.

## Controls

- `←` / `→`, Page Up / Page Down: move between slides.
- Swipe horizontally on touch screens.
- `Home` / `End`: first or last slide.
- `T`: show or hide teacher prompts.
- `O`: open the slide overview.
- URL hashes such as `#11`: deep-link to a slide.

## Publish with GitHub Pages

1. Create a repository such as `AI-Applications-Job3-Theory`.
2. Upload the contents of this folder to the root of the `main` branch.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select `main` and `/(root)`, then save.

The expected URL is:

`https://<username>.github.io/AI-Applications-Job3-Theory/`

## Editing the deck

The whole lesson is inside `index.html`.

- Search for `<section class="slide"` to edit slide content.
- Edit the variables under `:root` to change the theme.
- Add another slide inside `#track`; the counter, dots and overview update automatically.
- Add an instructor prompt with `<aside class="teacher-note">...</aside>`.
- Search for `ANIMATED CONCEPT SCAFFOLD` to edit the new animations.
- Search for `playgroundVisual` or `randomStage` to edit the interactive demonstrations.

## Job Sheet alignment

The deck retains the supplied Job Sheet sequence and terminology:

- Objective: increase the diversity of the training dataset.
- Transformations: flipping, rotating, cropping/scaling, brightness, contrast and noise.
- Part 1: create the dataset, configure the baseline CNN, train and plot accuracy/loss.
- Part 2: use `RandomFlip`, `RandomRotation`, `RandomZoom`, inspect generated views, add `Dropout(0.2)` and retrain.
- Part 3: load a new flower image, predict, apply softmax and report the class confidence.
- Investigations: compare 90/10, 80/20 and 70/30 splits; test rose, daisy and tulip images.

## Practical note

The Job Sheet screenshot contains `test_url = "https://.zip"`, which is a placeholder rather than a usable image address. Replace it with a valid flower-image URL or a local file path during the practical.
