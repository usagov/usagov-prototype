---
layout: topic
title: U.S. Passports
permalink: /passport/
image: /assets/img/about.jpg
---

## U.S. Passports

American Citizens need a U.S. passport to enter and exit the United States. Here you can learn everything you need to apply, renew, replace, or quickly get a passport. Or, to see everything, [find all of information about U.S. Passports.](#relatedTopicsSection)

### Most Popular

Choose from our most popular topics and your coices will appear below

<form id="filters" action="" class="usa-form">      
  <fieldset class="usa-fieldset">      
    <div class="usa-checkbox">
      <input type="checkbox" name="subtopics" id="renew" value="Renewing a Passport" class="usa-checkbox__input"/>
      <label for="renew" class="usa-checkbox__label">Renewing a Passport</label>
    </div>
    <div class="usa-checkbox">
      <input type="checkbox" name="subtopics" id="apply" value="Applying for the first time" class="usa-checkbox__input"/>
      <label for="apply" class="usa-checkbox__label">Applying for the first time</label>
    </div>
    <div class="usa-checkbox">
      <input type="checkbox" name="subtopics" id="expediate" value="Getting a passport quickly" class="usa-checkbox__input"/>
      <label for="expediate" class="usa-checkbox__label">Getting a passport quickly</label>
    </div>
    <div class="usa-checkbox">
      <input type="checkbox" name="subtopics" id="minors" value="Passports for minors" class="usa-checkbox__input"/>
      <label for="minors" class="usa-checkbox__label">Passports for minors</label>
    </div>  
  </fieldset>      
</form>

<script>

function updateFilteredResults(){
  var selectedTags=[];
  var checked = document.querySelectorAll('#filters [name="subtopics"]:checked');
  Array.prototype.forEach.call(checked, function(el, i){
    selectedTags.push(el.id);
  });
  
  var topics = document.querySelectorAll('#filterResultsSection .topic');
  var anyMatches=false;
  Array.prototype.forEach.call(topics, function(el, i){
    var topicTags = el.getAttribute("data-tags").split(" ");
    console.log(topicTags);
    var match = topicTags.some(function (v) {
      return selectedTags.indexOf(v) >= 0;
    });
    if(match){
      el.classList.remove("unrelated");
      anyMatches=true;
    }else{
      el.classList.add("unrelated");
    }
  });
  if(anyMatches){
    document.querySelectorAll('#filterResultsSection .emptySet')[0].classList.add("hidden");
  }else{
    document.querySelectorAll('#filterResultsSection .emptySet')[0].classList.remove("hidden");
  }
}

var filters = document.querySelectorAll('#filters [name="subtopics"]');
Array.prototype.forEach.call(filters, function(el, i){
  el.addEventListener("change", function(){
    updateFilteredResults();
  });
});
document.addEventListener('DOMContentLoaded', function(event) {
  updateFilteredResults();
})


</script>



