# HelloToast – Application Android (Java)

Cette application simple permet d’afficher un message Toast et d’incrémenter un compteur à chaque clic sur un bouton.

## Objectif
- Apprendre à créer une interface utilisateur Android avec XML
- Gérer des événements de clics sur des boutons
- Mettre à jour dynamiquement un élément TextView

---

## Technologies utilisées
- Android Studio
- Java
- XML (Layout Android)
- API Minimum : 24 (Android 7.0)

---

## Structure de l’interface (activity_main.xml)

```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:background="#FFFFFF"
    android:padding="16dp"
    tools:context=".MainActivity">

    <!-- Bouton TOAST -->
    <Button
        android:id="@+id/button_toast"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="TOAST"
        android:textAllCaps="true"
        android:textStyle="bold"
        android:textColor="#FFFFFF"
        android:background="#3F51B5"
        android:layout_marginBottom="8dp" />

    <!-- Zone jaune avec le chiffre -->
    <TextView
        android:id="@+id/text_count"
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:gravity="center"
        android:text="0"
        android:textSize="120sp"
        android:textStyle="bold"
        android:textColor="#3F51B5"
        android:background="#FFFF00" />

    <!-- Bouton marron Hello Toast -->
    <Button
        android:id="@+id/button_hello"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Hello Toast!"
        android:textColor="#FFFFFF"
        android:background="#5D4037"
        android:layout_gravity="center"
        android:layout_margin="8dp" />

    <!-- Bouton COUNT -->
    <Button
        android:id="@+id/button_count"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="COUNT"
        android:textAllCaps="true"
        android:textStyle="bold"
        android:textColor="#FFFFFF"
        android:background="#3F51B5"
        android:layout_marginTop="8dp" />

</LinearLayout>
```

---

## Fonctionnement (MainActivity.java)

button_toast → affiche un message Toast : "Bonjour !"

button_count → incrémente la valeur affichée dans le TextView

private int count = 0;

buttonToast.setOnClickListener(v -> {
    Toast.makeText(this, "Bonjour !", Toast.LENGTH_SHORT).show();
});

buttonCount.setOnClickListener(v -> {
    count++;
    textCount.setText(String.valueOf(count));
});

---

## Résultat

Un clic sur « Afficher un message » → affiche un Toast

Un clic sur « Incrémenter le compteur » → augmente le compteur à l’écran

---

## Capture

<img width="484" height="776" alt="image" src="https://github.com/user-attachments/assets/59422e6a-a22b-4fb3-bf8f-7b2e383e356f" />

https://github.com/user-attachments/assets/1a98e3e8-851f-4313-8a47-b8830f036c55



---

## Installation

Cloner le projet

git clone [https://github.com/ton-compte/HelloToast.git](https://github.com/sihamjardi/Android-Java-HelloToast)

Ouvrir dans Android Studio

Lancer l’application sur un émulateur ou un téléphone Android



