# Snapshots dans VirtualBox

## Qu'est-ce qu'un Snapshot ?

Un **snapshot** est une sauvegarde de l'état d'une machine virtuelle (VM) à un moment donné. Cela permet de capturer l'état de la VM, y compris sa mémoire vive, ses paramètres et ses disques virtuels, afin de pouvoir y revenir ultérieurement. C'est une fonctionnalité utile lorsque vous effectuez des changements risqués ou des tests, vous permettant de revenir à une version stable si quelque chose tourne mal.

## Pourquoi utiliser des Snapshots ?

- **Sauvegarde d'état** : Avant d'effectuer des mises à jour, installations ou modifications risquées, prenez un snapshot pour pouvoir restaurer la machine en cas de problème.
- **Faciliter les tests** : Vous pouvez prendre plusieurs snapshots à différentes étapes d'un processus pour revenir rapidement à un état antérieur.
- **Gestion des versions** : Gardez des versions spécifiques d'une machine pour différents environnements ou étapes de développement.

## Comment créer un Snapshot dans VirtualBox ?

1. **Ouvrir la VM** : 
   - Lancez la machine virtuelle dans VirtualBox.

2. **Prendre un Snapshot** :
   - Allez dans le menu **Machine** et sélectionnez **Prendre un instantané** (ou **Take Snapshot** si vous êtes en anglais).
   - Donnez un nom à votre snapshot et, si nécessaire, ajoutez une description pour expliquer l'état ou le contexte du snapshot.

3. **Vérification** :
   - Pour voir la liste des snapshots, ouvrez l'onglet **Snapshots** situé dans le coin supérieur droit de la fenêtre de la VM dans VirtualBox.

## Comment restaurer un Snapshot ?

1. **Ouvrir l'onglet Snapshots** :
   - Dans VirtualBox, sélectionnez la VM puis cliquez sur l'onglet **Snapshots**.

2. **Restaurer un Snapshot** :
   - Sélectionnez le snapshot auquel vous voulez revenir.
   - Cliquez sur **Restaurer** (ou **Restore**) pour replacer la machine virtuelle dans l'état exact où elle se trouvait au moment de la capture du snapshot.

## Comment supprimer un Snapshot ?

Si vous n'avez plus besoin d'un snapshot, vous pouvez le supprimer pour libérer de l'espace disque.

1. **Ouvrir l'onglet Snapshots** :
   - Sélectionnez la machine virtuelle et allez dans l'onglet **Snapshots**.

2. **Supprimer le Snapshot** :
   - Sélectionnez le snapshot que vous voulez supprimer.
   - Cliquez sur **Supprimer** (ou **Delete Snapshot**).

## Considérations sur l'espace disque

- **Espace disque** : Les snapshots peuvent utiliser beaucoup d'espace disque, car chaque modification de la VM après la prise du snapshot est sauvegardée dans des fichiers séparés. Il est recommandé de supprimer les snapshots inutilisés pour éviter d'épuiser l'espace disque.
- **Performances** : De nombreux snapshots peuvent avoir un impact sur les performances de la machine virtuelle, car VirtualBox doit gérer plusieurs états simultanément.

## Notes supplémentaires

- **Limiter l'usage des snapshots** : Bien qu'ils soient très pratiques, ne considérez pas les snapshots comme une solution de sauvegarde à long terme. Ils sont plus adaptés pour des retours rapides à des états récents. Pour une sauvegarde à long terme, envisagez d'exporter la VM sous forme de fichier `.ova` ou `.ovf`.
- **Compatibilité** : Les snapshots sont spécifiques à VirtualBox et ne peuvent pas être utilisés directement avec d'autres outils de virtualisation.

## Références

- [Documentation officielle de VirtualBox](https://www.virtualbox.org/manual/ch01.html#snapshots)

