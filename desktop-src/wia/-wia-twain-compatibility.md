---
description: WIA 提供一個 twain 相容性層，可讓認知感知的應用程式與 Windows 的影像取得 (WIA) 裝置進行通訊。
ms.assetid: 8e5673b9-c234-4722-b244-41aae015ac0c
title: TWAIN 相容性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3633dfc97a5356f2d63dd2d377e798312a9a2fb10fd03144222e5ed3b4fd0dc2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056978"
---
# <a name="twain-compatibility"></a>TWAIN 相容性

WIA 提供一個 twain 相容性層，可讓認知感知的應用程式與 Windows 的影像取得 (WIA) 裝置進行通訊。 TWAIN 感知的應用程式不具有 WIA 功能的完整存取權。 例如，應用程式無法使用 TWAIN 相容性層來隱藏使用者介面。

WIA 裝置會在應用程式中出現兩次，以辨識 WIA 和 TWAIN：一次是透過一般的 WIA 通訊，一次是透過 TWAIN 相容性層。 若要避免列出 WIA 裝置兩次，可感知 WIA 和 TWAIN 的應用程式，都必須篩選出來自 TWAIN 相容性層的 WIA 裝置。 所有通過 TWAIN 相容性層的 WIA 裝置都有 "WIA" 作為前置詞，因此很容易就能進行篩選。

 

 



