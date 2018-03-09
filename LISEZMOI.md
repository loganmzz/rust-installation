_🇬🇧 For english instructions, please read `README.md`_

## Installation de Rust

### Procédure standard

Actuellemet, la façon la plus simple est d'utiliser [rustup](https://www.rustup.rs/).

_Note: sous Windows, vous avez le choix entre deux options. `gnu`, vous n'aurez besoin de rien de particulier ; rustup installera automatiquement les outils de compilation GNU. `msvc`, vous aurez besoin d'installer `Visual C++ Build Tools 2015` ; [cliquez ici pour plus de détails](https://github.com/rust-lang-nursery/rustup.rs/#user-content-vs2015)._

### Docker

Si vous ne souhaitez pas installer Rust directement sur votre machine, vous pouvez utiliser Docker: 

```bash
alias cargo='docker run --rm --tty --user $(id -u) --volume $(pwd):$(pwd) --workdir $(pwd) -e "USER=$(id -un)" loganmzz/rust cargo test'

cargo new foobar
cargo run
```

_Note: Si vous souhaitez une version spécifique, veuillez consulter les [tags disponibles](https://hub.docker.com/r/loganmzz/rust/tags/). Souvenez-vous de mettre à jour avec la dernière version en utilisant `docker pull loganmzz/rust`._

### Vérification

Pour contrôler votre installation, exécutez `cargo run` depuis le répertoire racine de ce dépôt. Le message suivant devrait s'afficher :

```text
Congrulations !
You have compiled and run your first Rust program
```

## Installation d'un éditeur

### [IntelliJ IDEA](https://www.jetbrains.com/idea/)

_Note: vous pouvez utiliser n'importe quelle autre produit basé sur IntelliJ. Cependant IntelliJ IDEA est disponible en version Community._

[IntelliJ Rust](https://intellij-rust.github.io/) est l'extension officielle. Elle a d'abord démarré en tant que _side project_ d'employés JetBrains. Depuis l'été 2017, elle est officiellement supportée par JetBrains.

### [Visual Studio Code](https://code.visualstudio.com/)

[Rust (rls)](https://marketplace.visualstudio.com/items?itemName=rust-lang.rust) is actuellement l'extension recommandée. Elle est fournie par l'équipe de développement des outils Rust (ceux-ci fournissent également [Rust Language Server](https://github.com/rust-lang-nursery/rls)).


Il existe également l'extension [Rust](https://marketplace.visualstudio.com/items?itemName=kalitaalexey.vscode-rust) mais elle n'est plus maintenue. Dans son cas, il est fortement recommandé d'utiliser le mode RLS.


### Autres

Vous pouvez trouver d'avantes d'IDEs supportés à [Are we (I)DE yet?](https://areweideyet.com/).
