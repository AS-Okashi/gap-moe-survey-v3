# Gap Moe Survey Modification

Implement:
- Display original + 7 variant images.
- Add cards with data-part:
  color, pattern, material, silhouette, exposure, season, accessory
- Save selected value as gapFactor.
- Prepare placeholder image names:
images/original.png
images/color.png
images/pattern.png
images/material.png
images/silhouette.png
images/exposure.png
images/season.png
images/accessory.png

JavaScript:

document.querySelectorAll('.selectable').forEach(card=>{
 card.onclick=()=>{
  document.querySelectorAll('.selectable').forEach(c=>c.classList.remove('selected'));
  card.classList.add('selected');
  window.surveyData=window.surveyData||{};
  surveyData.gapFactor=card.dataset.part;
 };
});
