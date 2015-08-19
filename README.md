# opentour-se.github.io
OpenTour Pages


var scores = {"F": {}, "P": {}};
for (var hole = 1; hole < 19; hole++) {
  scores.F[hole] = [];
  scores.P[hole] = [];
}
$.each($(".inTable tr"), function (i, round) {
 var course = $(round).children()[1].innerHTML;
 for (var hole = 1; hole < 19; hole++) {
   var index = hole + 1;
   if (hole > 9) { index++; }
    var scoreText = $(round).children()[index].innerHTML;
   if (scoreText == "") continue;
   scores[course][hole].push(scoreText);
 }
});