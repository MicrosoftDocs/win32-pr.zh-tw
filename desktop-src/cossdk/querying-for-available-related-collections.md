---
description: 查詢可用的相關集合
ms.assetid: 9c7d2a01-5dc3-4d35-b938-f1d0525a8286
title: 查詢可用的相關集合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0203df5bb7b5bf89396d5687dc28b19e9b183d56
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317904"
---
# <a name="querying-for-available-related-collections"></a>查詢可用的相關集合

如果您撰寫的是一般用途的管理工具，您可能需要撰寫用來導覽整個集合階層的常式。 為了支援此功能，COM + 的功能可讓您以動態方式查詢任何指定集合中可用的相關集合。

[**RelatedCollectionInfo**](relatedcollectioninfo.md)集合可從任何您持有的集合中取得，而且每個可用的相關集合都包含一個專案。 您可以列舉這些專案，以判斷指定的集合是否可用。

您可以使用 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件上的 [**>getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection)方法，從您持有的任何集合取得 [**RelatedCollectionInfo**](relatedcollectioninfo.md)集合，將第二個參數保留空白，您通常會在此指定父專案的索引鍵屬性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[流覽 COM + 集合階層](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[填入 COM + 集合](populating-com--collections.md)
</dt> <dt>

[在 COM + 類別目錄上取出集合](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



