---
title: 從 Visual Basic 轉換成 c + +
description: Visual Basic 會隱含地處理指標。 在 c + + 中，您的應用程式會負責執行任何必要的指標算術。
ms.assetid: bbbcaba1-cf5a-4768-ad1d-22a040bfe384
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53de112f19b51be92657fb3293bb35e1d41ff9b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183463"
---
# <a name="translating-to-c-from-visual-basic"></a>從 Visual Basic 轉換成 c + +

Visual Basic 會隱含地處理指標。 在 c + + 中，您的應用程式會負責執行任何必要的指標算術。

依預設，Visual Basic 會以傳址方式傳遞參數 (作為) 指標。 只以傳值方式傳遞的參數是由關鍵字 **ByVal** 指定。 例如，Visual Basic 中的 **ByVal**- **整數** 參數相當於 c + + 中的 **short** 參數，而 Visual Basic 中的 **ByRef**- **整數** 參數相當於 **short \*** 參數。

在 Visual Basic 中宣告 **為字串** 的參數會宣告為 c + + 中的 **BSTR** 指標。 在 c + + 中將字串指標設定為 **Null** ，相當於將字串設定為 Visual Basic 中的 **vbNullString** 常數。 將零長度的字串 ( "" ) 傳遞給設計用來接收 **Null** 的函式無法運作，因為這會將指標傳遞至長度為零的字串，而不是零指標。

C + + 和 Visual Basic 在其代表屬性的方式上稍有不同。 在 c + + 中，屬性是以一組存取子函式來表示，其中一個設定屬性值，另一個則會抓取屬性值。 在 Visual Basic 中，屬性會以單一專案的形式表示，可用於抓取或設定屬性值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉換成 c + +](translating-to-c--.md)
</dt> </dl>

 

 




