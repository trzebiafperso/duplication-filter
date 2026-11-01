ce skill normalisera les commits git selon les règles suivante:
- le message devra rester la forme "<type>s(<scope>): <message>"
- le type devra être l'un des suivant: feat, fix, chore, !feat
- !feat sera utilisé dans le cadre de breaking change, un changement nécessitant une modification de la part des consommateurs pour conserver un fonctionnement identique, une refonte majeure de la configuration, une modification profonde du fonctionnement de l'application
- feat sera utilisé pour l'ajout d'une nouvelle fonctionnalité
- fix sera utilisé pour la correction d'un bug
- chore sera utilisé pour toute autre modification n'impactant pas le code
- le scope est optionnel
- le scope rependra le fin du nom de la branche, après le dernier "/" si la branche est nommée avec des "/" (ex: feat/mon-scope, fix/mon-scope, chore/mon-scope)
- le message devra être en anglais, et commencer par une majuscule, ce sera une description de la modification apportée, et devra être rédigé à l'infinitif

Les commits seront atomiques, c'est à dire qu'ils ne devront contenir qu'une seule modification, et ne pas contenir de modification de code et de documentation dans le même commit.
les tests unitaire s devront être inclus dans le commit de la modification du code, et ne pas être dans un commit séparé.

Les commandes seront lancé depuis git bash, il est installé dans C:\Program Files\Git\bin\bash.exe
les commandes git seront lancés depuis le répertoire de travaille du projet, et non depuis le répertoire .github/skills/conventional-commit
une fois le commit réalisé en local celui-ci sera pushé sur le répertoire.
les corrections apportées a une modification déjà seront commité avec le code d'origin via un fixup. les modification sur du code non impacté par la branche se feront dans un nouveau commit.

un rebase interactif avec --autosquash sera utilisé afin de regrouper les commits. en cas de conflit, me le notifier ete attendre mon intervention avant de pousuivre le process.

si aucune session git n'est active, utilise gh pour te connecter a github.