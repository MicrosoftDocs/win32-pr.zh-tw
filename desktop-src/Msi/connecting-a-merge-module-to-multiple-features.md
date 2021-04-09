---
description: Merge 物件的 Connect 方法可以用來將模組連接至已合併至資料庫或將合併到資料庫的其他功能。 在呼叫這個方法之前，此功能必須存在。
ms.assetid: 8b59de42-bc3f-468b-a410-8f935ff73345
title: 將合併模組連接至多個功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d57b49f1ee27b4c8d3aa5d0b3ac1b0d7b8b8e11c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850928"
---
# <a name="connecting-a-merge-module-to-multiple-features"></a>將合併模組連接至多個功能

[Merge 物件](merge-object.md)的 [**connect**](merge-connect.md)方法可以用來將模組連接至已合併至資料庫或將合併到資料庫的其他功能。 在呼叫這個方法之前，此功能必須存在。

合併模組永遠不應該將包含系統檔案的元件傳遞至應用程式的主要功能，因為這可能會在每次使用系統檔案時，導致安裝程式驗證和修復應用程式。 要從合併模組接受元件的 .msi 檔應該要撰寫，如此一來，包含系統檔案的任何元件都只屬於與應用程式主要功能不同的功能。

如果您的套件使用的合併模組包含將所有元件從合併模組連結到應用程式主要功能的系統檔案，則嘗試使用系統檔案可能會觸發安裝程式，以嘗試修復應用程式的主要功能。 如果無法修復主要功能，安裝可能會失敗。

 

 



