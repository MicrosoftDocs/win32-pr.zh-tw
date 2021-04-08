---
title: 變更群組的範圍或類型
description: 本主題說明如何變更原生模式網域中的群組範圍或類型。
ms.assetid: bdae7bc9-072a-4063-9562-8e0fcb1b7937
ms.tgt_platform: multiple
keywords:
- 群組 AD、變更群組的範圍或類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65c64b4a2dafe4bf6c0e65463ef16e0270c0be3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671004"
---
# <a name="changing-a-groups-scope-or-type"></a>變更群組的範圍或類型

混合模式網域中不允許變更群組領域或類型。 不過，原生模式網域中允許下列轉換：

全域群組至萬用群組：只有在全域群組不是另一個全域群組的成員時，才允許這種情況。

網域本機群組到萬用群組：要轉換的網網域本機群組不能包含另一個網域本機群組。

萬用群組對全域或網域本機群組：若要轉換為全域群組，正在轉換的萬用群組不能包含來自另一個網域的使用者或全域群組。 若要轉換為網域本機群組，正在轉換的萬用群組不能是任何萬用群組的成員，也不能是來自另一個網域的網域本機群組成員。

在原生模式中，群組類型可以在安全性群組和通訊群組之間自由轉換。

請注意，如果群組是用來設定存取控制，則變更範圍或類型可能會影響包含該群組 (Ace) 的存取控制專案。 安全性系統會忽略包含不是安全性群組之群組的 Ace。

 

 




