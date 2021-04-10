---
description: Windows Installer 可以使用安裝封裝或使用者所定義的變數值來設定軟體安裝。
ms.assetid: b7b715e7-e92c-4b84-b60d-a0ff8412749b
title: 關於屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dc5d8154533cfebf4163983a149a547372ef4a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192478"
---
# <a name="about-properties"></a>關於屬性

Windows Installer 可以使用安裝封裝或使用者所定義的變數值來設定軟體安裝。

在安裝期間，Windows Installer 會使用三種類別的全域變數：

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

 

 



