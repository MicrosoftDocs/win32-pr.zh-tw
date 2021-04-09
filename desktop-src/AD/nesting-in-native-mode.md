---
title: 以原生模式進行的嵌套
description: 下列清單描述存在於原生模式網域中的群組可以包含的內容。
ms.assetid: 7992ef2d-9dcf-4087-b09a-35235b23e499
ms.tgt_platform: multiple
keywords:
- 原生模式 AD 中的嵌套
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69dba115bb705fe706a049e85136475c6d5b3a16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839283"
---
# <a name="nesting-in-native-mode"></a>以原生模式進行的嵌套

下列清單描述存在於原生模式網域中的群組可以包含的內容。 同樣的清單也適用于混合模式網域中的通訊群組。 群組的範圍會決定這些內含專案規則。

-   萬用群組可以包含來自此萬用群組所在樹系內任何網域的其他萬用群組、通用群組和帳戶。
-   全域群組可包含來自該群組所屬網域的其他全域群組和帳戶。 全域群組不能包含任何萬用群組，或是來自另一個網域的任何全域群組或帳戶。
-   網域本機群組可以包含來自任何網域或樹系的萬用群組、通用群組和帳戶。 網域本機群組也可以包含來自該群組所屬網域的其他網域本機群組。 網域本機群組不能包含其他任何網域或樹系中的其他網域本機群組。

 

 




