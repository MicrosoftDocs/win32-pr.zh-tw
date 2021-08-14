---
title: 以分葉節點形式來查看容器
description: Active Directory Domain Services 中的任何物件都可以是其他物件的容器。
ms.assetid: 38300ca5-745a-4640-9723-6052a9843f45
ms.tgt_platform: multiple
keywords:
- 以分葉節點形式來查看容器
- 容器廣告，作為分葉節點來查看
- 分葉廣告，以分葉節點形式來查看容器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33713f70e1b84ded536a928f8489f4fd41461bd4e37de46a84036bc6370327db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182252"
---
# <a name="viewing-containers-as-leaf-nodes"></a>以分葉節點形式來查看容器

Active Directory Domain Services 中的任何物件都可以是其他物件的容器。 這可能會讓使用者介面雜亂，因此可以宣告特定類別的物件只在使用者介面中顯示為分葉。 **TreatAsLeaf** 屬性是單一值的顯示規範屬性，可判斷該類別的物件是否應該只顯示為分葉物件。 這個屬性是布林值，如果 **為 TRUE**，表示類別的物件應該只顯示為分葉元素。 如果 **為 FALSE**，表示類別的物件可以顯示為容器或分葉。 如同所有顯示規範屬性， **treatAsLeaf** 屬性是根據每個地區設定來設定，因此此屬性可以視需要當地語系化。 例如，英文地區設定 (0409) 顯示規範的 **使用者顯示** 預設會將 **treatAsLeaf** 屬性設定為 **TRUE** 。 這會導致使用者介面將所有 **使用者** 物件顯示為分葉物件。

**若要設定 **treatAsLeaf** 屬性的值**

1.  系結至所需的地區設定中所需的顯示內容。 如需詳細資訊和程式碼範例，請參閱 [DisplaySpecifiers 容器](displayspecifiers-container.md)。
2.  使用 [**IADs：:P**](/windows/desktop/api/iads/nf-iads-iads-put) 的錯誤方法，將 **treatAsLeaf** 屬性設定為 **TRUE** 或 **FALSE**。
3.  若要認可目錄的變更，請呼叫 [**IADs：： SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) 方法。

 

 