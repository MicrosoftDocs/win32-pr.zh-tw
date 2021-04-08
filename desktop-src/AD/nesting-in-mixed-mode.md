---
title: 在混合模式中進行嵌套
description: 本主題列出混合模式網域中安全性群組的限制。
ms.assetid: e9f50485-db09-4d8c-8cf4-0ee7e78cb133
ms.tgt_platform: multiple
keywords:
- 混合模式 AD 中的嵌套
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54d63d475edf77398a69a519a08f3803f69d67d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839284"
---
# <a name="nesting-in-mixed-mode"></a>在混合模式中進行嵌套

本主題列出混合模式網域中安全性群組的限制。

混合模式網域中的安全性群組有下列限制：

-   無法在混合模式網域中建立萬用群組，因為只有在 Windows 2000 原生模式網域中才支援通用範圍。
-   全域群組可以包含群組所屬的相同網域中的帳戶。 全域群組不能包含任何萬用群組、任何全域群組或其他網域中的帳戶。
-   網域本機群組可以包含來自任何網域或樹系的全域群組和帳戶。 網域本機群組不能包含任何其他的網域本機群組。

請注意，您可以根據原生模式的嵌套規則來嵌套通訊群組。

 

 




