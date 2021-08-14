---
title: '索引屬性 (AD DS) '
description: 可以編制屬性的索引。 編制屬性的索引可改善該屬性的查詢效能。
ms.assetid: 20e10fc9-d767-4d82-9ed6-b9f384e77b12
ms.tgt_platform: multiple
keywords:
- 已編制索引的屬性廣告
- 屬性 AD、索引
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cabd205fea66b198096a9a9427822eb4ba0ccb609fb3e6fef0854fa91848371c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187582"
---
# <a name="indexed-attributes-ad-ds"></a>索引屬性 (AD DS) 

可以編制屬性的索引。 編制屬性的索引可改善該屬性的查詢效能。

當屬性架構定義中的 [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) 屬性將最小的位設定為1時，就會編制屬性的索引。 將 **searchFlags** 屬性架構定義的最小有效位設定為1，將會動態建立索引。 將 **searchFlags** 屬性架構定義的最小有效位設定為0，將會移除屬性的索引。 索引將由網域控制站上的背景執行緒自動建立。

在理想的情況下，索引屬性應該是具有高度唯一值的單一值，而這些值會平均分散到一組實例。 屬性的唯一值越少，索引的效率就愈低。

您也可以編制多值屬性的索引，但為多重值屬性建立索引的成本會比儲存體、更新和搜尋時間更大。 多重值屬性的唯一性需求與單一值屬性的唯一性需求相同，唯一的值愈多，就越能有效地使用索引。

類別所擁有的索引屬性愈多，建立類別的新實例需要更多時間。

索引適用于屬性，不適用於類別。 也就是說，當屬性標示為已編制索引時，會將屬性的所有實例加入至索引，而不只是特定類別的成員實例。

若要確認伺服器是否使用索引來處理查詢，請將網域控制站上的下列登錄值設定為4。 然後在該網域控制站上執行查詢，並在目錄事件記錄檔中查看用來處理查詢的索引相關資料（如果有的話）。

```
HKEY_LOCAL_MACHINE
   SYSTEM
      Current Control Set
         Services
            NTDS
               Diagnostics
                  9 Internal Processing
```

如需 [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) 屬性中其他位的詳細資訊，請參閱 [屬性的特性](characteristics-of-attributes.md)。

 

 