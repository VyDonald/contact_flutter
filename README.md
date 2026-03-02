# 📇 Contact Manager - Flutter App

Application mobile cross-platform de gestion de contacts développée avec Flutter, connectée à une API Laravel.

## ✨ Fonctionnalités

- 🔐 **Authentification** (inscription, connexion, déconnexion)
- 👥 **Gestion des contacts** (ajout, modification, suppression, recherche)
- 📂 **Organisation par groupes**
- 🔗 **Association contacts-groupes**
- 📱 **Interface moderne et intuitive**
- 🌐 **Synchronisation en temps réel** avec l'API
- 🎨 **Design Material** adaptatif

## 📋 Prérequis

- Flutter SDK >= 3.0.0
- Dart >= 3.0.0
- Android Studio / Xcode (pour émulateurs)
- Un appareil Android/iOS ou un émulateur

## 🔧 Installation

1. **Cloner le repository**
```bash
git clone https://github.com/VyDonald/contact_flutter.git
cd contact_flutter
```

2. **Installer les dépendances**
```bash
flutter pub get
```

3. **Configurer l'API**

Créez un fichier `lib/config/api_config.dart` :
```dart
class ApiConfig {
  static const String baseUrl = 'http://your-api-url.com/api';
  // Pour émulateur Android: http://10.0.2.2:8000/api
  // Pour appareil physique: http://votre-ip:8000/api
}
```

4. **Lancer l'application**
```bash
flutter run
```

## 📦 Dépendances Principales
```yaml
dependencies:
  flutter:
    sdk: flutter
  http: ^1.1.0           # Requêtes HTTP
  provider: ^6.1.1        # Gestion d'état
  shared_preferences: ^2.2.2  # Stockage local
  flutter_secure_storage: ^9.0.0  # Stockage sécurisé du token
```

## 🏗️ Structure du Projet
```
lib/
├── config/
│   └── api_config.dart
├── models/
│   ├── user.dart
│   ├── contact.dart
│   └── group.dart
├── services/
│   ├── auth_service.dart
│   ├── contact_service.dart
│   └── group_service.dart
├── providers/
│   ├── auth_provider.dart
│   ├── contact_provider.dart
│   └── group_provider.dart
├── screens/
│   ├── auth/
│   │   ├── login_screen.dart
│   │   └── register_screen.dart
│   ├── contacts/
│   │   ├── contact_list_screen.dart
│   │   ├── contact_detail_screen.dart
│   │   └── contact_form_screen.dart
│   └── groups/
│       ├── group_list_screen.dart
│       └── group_form_screen.dart
├── widgets/
│   ├── contact_card.dart
│   └── group_card.dart
└── main.dart
```

## 🎯 Captures d'écran

[Ajoutez vos captures d'écran ici]

## 🔌 Connexion à l'API

L'application communique avec l'API Laravel via HTTP. Exemple de configuration :

**Pour développement local :**
- Émulateur Android : `http://10.0.2.2:8000/api`
- Émulateur iOS : `http://localhost:8000/api`
- Appareil physique : `http://VOTRE_IP:8000/api`

**Pour production :**
- `https://votre-domaine.com/api`

## 📱 Build de Production

### Android
```bash
flutter build apk --release
# ou pour un App Bundle
flutter build appbundle --release
```

### iOS
```bash
flutter build ios --release
```

## 🧪 Tests
```bash
# Tests unitaires
flutter test

# Tests d'intégration
flutter test integration_test
```

## 🔐 Sécurité

- Token JWT stocké de manière sécurisée avec `flutter_secure_storage`
- Validation des entrées utilisateur
- Gestion des erreurs réseau
- Timeout des requêtes HTTP

## 🌐 Backend

L'API backend Laravel est disponible ici : [Contact Management API](lien-vers-votre-repo-backend)

## 🐛 Problèmes Connus

- Assurez-vous que l'API est accessible depuis votre appareil/émulateur
- Pour Android, vérifiez les permissions internet dans `AndroidManifest.xml`
- Pour iOS, configurez App Transport Security si nécessaire

## 🚀 Fonctionnalités à Venir

- [ ] Mode hors ligne avec synchronisation
- [ ] Import/Export de contacts
- [ ] Recherche avancée et filtres
- [ ] Thème sombre
- [ ] Notifications push
- [ ] Partage de contacts

## 🤝 Contribution

Les contributions sont les bienvenues ! Pour contribuer :

1. Forkez le projet
2. Créez une branche (`git checkout -b feature/AmazingFeature`)
3. Committez vos changements (`git commit -m 'Add AmazingFeature'`)
4. Poussez vers la branche (`git push origin feature/AmazingFeature`)
5. Ouvrez une Pull Request

## 📄 Licence

Ce projet est sous licence MIT.

## 👨‍💻 Auteur

**VyDonald**

- GitHub: [@VyDonald](https://github.com/VyDonald)

## 🙏 Remerciements

- Flutter Team pour cet excellent framework
- La communauté Flutter pour les packages
- Tous les contributeurs

---

Développé avec ❤️ et Flutter
