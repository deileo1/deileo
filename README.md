<html>
<script>

    const vocabulary = {
            words: {
                word0: {
                    original: "Wassup",
                    translation: "Salut"
                },
                word1: {
                    original: "Bye",
                    translation: "Larevedere"
                },
                word2: {
                    original: "Programer",
                    translation: "Programist"
                },
            },
            
            wordsCount: 3
        }
        
    const notificationMessages = {
        start: {
          hello: "Hello man u can learn english. Good LUCK!"
        },
        result: {
            finishSucces: "Bine. Good result!",
            finishUnsucces: "Bine. dar trebuie mai bine"
        }
    }

    const settings = {
        correctAnswersMinPercent: 50
    }

    const result = {
        correctAnswersCount: 0
    }

    // -----------

    alert(notificationMessages.start.hello)

    const userAnswer0 = prompt(vocabulary.words.word0.original); // 0
    window.prompt(userAnswer0 === vocabulary.words.word0.translation);
    if (userAnswer0 === vocabulary.words.word0.translation) {
        result.correctAnswersCount = result.correctAnswersCount + 1;
    }

    const userAnswer1 = prompt(vocabulary.words.word1.original); // 1
    window.prompt(userAnswer1 === vocabulary.words.word1.translation);
    if (userAnswer1 === vocabulary.words.word1.translation) {
        result.correctAnswersCount = result.correctAnswersCount + 1;
    }

    const userAnswer2 = prompt(vocabulary.words.word2.original); // 2
    window.prompt(userAnswer2 === vocabulary.words.word2.translation);
    if (userAnswer2 === vocabulary.words.word2.translation) {
        result.correctAnswersCount = result.correctAnswersCount + 1;
    }

    const userCorrectAnswersPercent = result.correctAnswersCount / vocabulary.wordsCount.wordsCount * 100;

    if (userCorrectAnswersPercent > settings.correctAnswersMinPercent) {
        alert(notificationMessages.result.finishSucces);
    } else {
        alert(notificationMessages.result.finishUnsucces);
    }


</script>
</html>
