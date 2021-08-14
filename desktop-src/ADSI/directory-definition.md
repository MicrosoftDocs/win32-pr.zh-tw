---
title: 目錄定義
description: 範例提供者元件使用相當簡單的目錄設計來說明元件之間的關聯性，以及顯示成為 ADSI 提供者所需的最低需求。
ms.assetid: d8dcd255-4a17-4c80-a749-61c1af605dba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8a46ee47bfa280fb9cffce32480fdad3164a648eee59a0c0b2740834b1f21cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118691944"
---
# <a name="directory-definition"></a>目錄定義

範例提供者元件使用相當簡單的目錄設計來說明元件之間的關聯性，以及顯示成為 ADSI 提供者所需的最低需求。

範例提供者元件的「目錄」包含兩個根節點：「西雅圖」和「多倫多」。 西雅圖還包含兩個子級別：「Bellevue」和「Redmond」。 其中每個專案都包含數個使用者帳戶。 「多倫多」專案沒有進一步的子層級，但直接包含數個使用者帳戶。 下圖顯示兩個連接到網路的根節點。

![目錄定義](images/dssmdo.png)

在階層式詞彙中，命名空間節點包含「西雅圖」和「多倫多」。 「西雅圖」包含「Bellevue」和「Redmond」。 "Bellevue" 和 "Redmond" 各包含一組使用者帳戶。 「多倫多」直接包含沒有中繼組織節點的使用者帳戶。

範例提供者元件只會以兩個 Active Directory 物件類型來表示此結構：容器物件和分葉物件。 「西雅圖」、「多倫多」、「Bellevue」和「Redmond」是容器物件，而每個使用者帳戶都是分葉物件。

範例提供者元件會建立名為「組織單位」的架構類別做為容器物件類型，並為使用者帳戶建立名為 "User" 的架構類別。

每個架構類別的屬性、其方法以及管理這些物件之內含專案關聯性的規則全都定義在 [架構管理](schema-management.md)中。

 

 




