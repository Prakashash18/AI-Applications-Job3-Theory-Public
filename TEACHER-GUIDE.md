# Teacher Guide — Job 3 Animated Data Augmentation

## Suggested timing: 60–75 minutes

| Time | Slides | Teaching purpose |
|---|---:|---|
| 0–6 min | 1–3 | Connect to the Job 2 CNN lesson and introduce the “AI Photographer” story. |
| 6–12 min | 4–5 | Establish the new-photo problem and define one transformation in plain language. |
| 12–25 min | 6–10 | Watch flip, rotation, zoom/crop, lighting, contrast and noise; apply the label-preserving rule. |
| 25–34 min | 11–14 | Use the playground and random generator, reveal one-to-many views, then introduce the term data augmentation. |
| 34–44 min | 15–18 | Place augmentation in the pipeline; distinguish training from validation; explore split ratios and the baseline. |
| 44–58 min | 19–27 | Read curves, diagnose overfitting, decode the Keras layers, explain dropout and compare results. |
| 58–75 min | 28–35 | Predict a new image, interpret confidence, prepare the two Job Sheet investigations and complete the exit ticket. |

## Critical teaching sequence

### Before slide 14

Avoid leading with the phrase **data augmentation**. Use these sentences instead:

- “The computer is pretending to take another photo.”
- “The picture changed, but the flower did not.”
- “This is one controlled change to the image.”

After students can explain the process, slide 14 supplies the formal name.

### The repeated question

Ask this on every transformation slide:

> What changed in the picture, and what stayed the same in the meaning?

Expected answer:

- The pixels, framing, orientation or lighting changed.
- The label stayed **sunflower**.

## How to use the animated section

### Slides 4–5: problem and definition

Let the changing test image run. Ask “Still sunflower?” several times. On slide 5, define a transformation as **one controlled change**, not as a mathematical operation.

### Slides 6–9: one change at a time

Do not discuss all transformations together. For each one:

1. Watch the motion.
2. Describe it in ordinary language.
3. Check that the label remains valid.
4. Reveal the Keras layer name where applicable.

### Slide 10: safe versus too far

Use the class rule:

> Change the view. Keep the answer.

A transformation becomes unsafe when important evidence is removed or the resulting image is unrealistic for the task.

### Slide 11: Transformation Playground

Invite students to choose the next button. After every click, ask them to state the visible change before reading the code label.

Suggested sequence:

1. Original
2. Flip
3. Rotate
4. Zoom
5. Darker
6. Noise
7. Random

### Slide 12: Random Transformation Generator

The image changes automatically until the button is clicked. Read the generated recipe aloud. Emphasise that **random means sampled within chosen limits**, not unlimited or careless change.

### Slides 13–14: one-to-many and formal term

On slide 13, count how many real photos were stored: one. Wait for the six training views to appear. Then move to slide 14 and ask students to define data augmentation in their own words.

## Graph-reading scaffold

Use the same four questions for every accuracy/loss graph:

1. What happens to training accuracy or loss?
2. What happens to validation accuracy or loss?
3. Is the train–validation gap becoming larger or smaller?
4. What does that suggest about performance on new images?

Do not accept “training accuracy is high” as sufficient evidence of a good model.

## Likely misconceptions

| Misconception | Correction prompt |
|---|---|
| “A transformation changes the flower into a new class.” | What changed: the view or the flower identity? |
| “Data augmentation takes new real photographs.” | How many real photos were stored on the factory slide? |
| “Random means any possible change.” | What ranges and safety rule control the random values? |
| “More extreme augmentation is always better.” | Is the correct label still reliable and is the result realistic? |
| “The validation set should be changed too.” | Training is the practice bench; validation is the stable check bench. |
| “Dropout changes the image.” | Augmentation acts on input images; dropout acts inside the network. |
| “High training accuracy proves the model is good.” | Which curve represents held-out examples? |
| “97% confidence means guaranteed correct.” | Can the model assign a high score to a wrong class? |

## Job Sheet investigation prompts

For the 90/10, 80/20 and 70/30 comparison, keep these constant:

- model architecture
- random seed
- epoch count
- image size and batch size
- augmentation settings

Record validation accuracy, validation loss, curve stability and the train–validation gap.

For the rose, daisy and tulip tests, record:

- actual flower
- predicted class
- confidence
- whether the prediction was correct
- a possible reason for a low-confidence or incorrect result

## Exit-ticket expected ideas

1. A transformation is one controlled change to an image.
2. A safe transformation keeps the correct label valid.
3. Data augmentation creates varied training views from existing data.
4. Augmentation helps the model generalise to new photos.
5. Validation evidence—not training accuracy alone—shows whether learning transfers.
