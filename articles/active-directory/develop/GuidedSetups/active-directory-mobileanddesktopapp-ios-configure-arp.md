---
title: "Prise en main d’Azure AD v2 iOS - Configuration (ARP)| Microsoft Docs"
description: "Cet article explique comment les applications iOS (Swift) peuvent appeler une API qui nécessite des jetons d’accès à partir d’un point de terminaison Azure Active Directory v2."
services: active-directory
documentationcenter: dev-center-name
author: andretms
manager: mbaldwin
editor: 
ms.service: active-directory
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: identity
ms.date: 05/09/2017
ms.author: andret
ms.translationtype: HT
ms.sourcegitcommit: b309108b4edaf5d1b198393aa44f55fc6aca231e
ms.openlocfilehash: 5ce5d26943839d9fe53508d396825289d77cf2f8
ms.contentlocale: fr-fr
ms.lasthandoff: 08/15/2017

---
## <a name="add-the-applications-registration-information-to-your-app"></a>Ajouter les informations d’inscription de l’application à votre application

Dans cette étape, vous devez ajouter l’ID d’application à votre projet :

1.  Dans `ViewController.swift`, remplacez la ligne commençant par '`let kClientID`' par :
```swift
let kClientID = "[Enter the application Id here]"
```
<!-- Workaround for Docs conversion bug -->
<ol start="2">
<li>
Maintenez la touche Ctrl enfoncée et cliquez sur <code>Info.plist</code> pour faire apparaître le menu contextuel, puis cliquez sur : <code>Open As</code> > <code>Source Code</code>
</li>
<li>
Sous le nœud racine <code>dict</code>, ajoutez le code suivant :
</li>
</ol>

```xml
<key>CFBundleURLTypes</key>
<array>
    <dict>
        <key>CFBundleTypeRole</key>
        <string>Editor</string>
        <key>CFBundleURLName</key>
        <string>$(PRODUCT_BUNDLE_IDENTIFIER)</string>
        <key>CFBundleURLSchemes</key>
        <array>
            <string>msal[Enter the application Id here]</string>
            <string>auth</string>
        </array>
    </dict>
</array>
```

