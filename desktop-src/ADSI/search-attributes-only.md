---
title: 僅搜尋屬性
description: 有時您會執行搜尋，以判斷物件可使用的資料類型。
ms.assetid: 97eccea6-6a2b-4785-afd8-4af3dc7bd657
ms.tgt_platform: multiple
keywords:
- 僅搜尋屬性 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c2a97873dfb52f56b123919c3eedd277a63a74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931829"
---
# <a name="search-attributes-only"></a>僅搜尋屬性

有時您會執行搜尋，以判斷物件可使用的資料類型。 在此情況下，您只會對物件的屬性（而非值）感興趣。 若要完成此動作，請設定 [僅搜尋屬性] 選項。 指定此選項會傳回沒有值的屬性名稱。 不過，結果集會包含已指派值的屬性。 例如，請考慮具有下列屬性的物件：

``` syntax
First Name = Jeff
Last Name = Smith
Department = <Empty>
Phone Number = (425) 432-3442
```

當設定 [僅搜尋屬性] 選項時，結果集會包含：

``` syntax
First Name
Last Name
Phone Number
```

如需有關使用僅搜尋屬性選項搭配特定搜尋介面的詳細資訊，請參閱：

-   [使用 >idirectorysearch 只傳回屬性名稱](returning-only-attribute-names-with-idirectorysearch.md)
-   [使用 ActiveX Data Objects 搜尋](searching-with-activex-data-objects-ado.md)
-   [使用 OLE DB 搜尋](searching-with-ole-db.md)

 

 




