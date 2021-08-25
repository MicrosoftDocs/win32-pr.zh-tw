---
description: 合併模組很少需要使用者介面。
ms.assetid: 53bd2064-09dd-406f-a8ff-7b04f3525b9f
title: 在合併模組中撰寫使用者介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 931e539d8880c490853b20a6e53b3000f390c0b29f81bf8bb9d3e3703e3f7905
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829188"
---
# <a name="authoring-user-interfaces-in-merge-modules"></a>在合併模組中撰寫使用者介面

合併模組很少需要使用者介面。 釋放包含可安裝元件和使用者介面的合併模組，最終會限制模組使用者的彈性。 將元件和 UI 結合成一個模組，可防止開發人員使用自己的 UI 或提供無訊息安裝。 更好的替代方式是釋放兩個合併模組，一個是以無訊息方式安裝元件，另一個則是包含 UI 的選擇性模組。 具有 UI 的模組應該會列出其 [ModuleDependency 資料表](moduledependency-table.md)中的元件模組。 此方法可讓模組作者提供 UI，而不需要在開發人員上強制執行。

當在合併模組中使用 UI 資料表時，可以使用與任何其他資料表相同的方式進行合併。

 

 



