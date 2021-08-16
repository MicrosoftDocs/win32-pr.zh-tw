---
description: Windows安裝程式可以使用安裝封裝或使用者所定義的變數值來設定軟體安裝。
ms.assetid: b7b715e7-e92c-4b84-b60d-a0ff8412749b
title: 關於屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4a7bdd5a70721520c4d2afb975aabaca312975dc3bf4b7d94215112f69a0a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382075"
---
# <a name="about-properties"></a>關於屬性

Windows安裝程式可以使用安裝封裝或使用者所定義的變數值來設定軟體安裝。

Windows安裝程式在安裝期間會使用三種全域變數類別：

-   私用屬性：安裝程式會在內部使用私用屬性，且其值必須撰寫至安裝資料庫，或設定為作業環境所決定的值。
-   公用屬性：公用屬性可以撰寫至資料庫中，並且由使用者或系統管理員在命令列上進行變更，方法是套用轉換，或與撰寫的使用者介面互動。
-   受限制的公用屬性：基於安全性目的，安裝套件的作者可以限制使用者可變更的公用屬性。

並非所有屬性都必須在每個封裝中定義，因此必須在每個封裝中定義一組小型的必要屬性。 安裝程式會以特定的優先順序順序設定屬性的值。

[私用屬性](private-properties.md)

[公用屬性](public-properties.md)

[受限制的公用屬性](restricted-public-properties.md)

[必要屬性](required-properties.md)

[屬性優先順序的順序](order-of-property-precedence.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用屬性](using-properties.md)
</dt> <dt>

[屬性參考](property-reference.md)
</dt> </dl>

 

 



