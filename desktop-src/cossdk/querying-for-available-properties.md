---
description: 查詢可用的屬性
ms.assetid: 9acf10cd-19a8-4542-8078-3e4ee275d4d5
title: 查詢可用的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22238e04404d2b88efa81ce98d0b0fb0e09d245f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111285"
---
# <a name="querying-for-available-properties"></a>查詢可用的屬性

如果您撰寫的是一般用途的系統管理工具，您很可能需要撰寫常式來設定完整的屬性（property）。 為了支援此功能，有一項工具可讓您以動態方式查詢任何指定集合中的專案可用的屬性。

您可能保留的任何集合都可以使用 [**PropertyInfo**](propertyinfo.md) 集合。 **PropertyInfo** 集合包含每個可用屬性的專案。 您可以列舉這些專案，以判斷指定的屬性是否可用。

您可以使用 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件上的 [**>getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection)方法，從您持有的任何集合取得 [**PropertyInfo**](propertyinfo.md)集合，將第二個參數保留空白，您通常會在此指定父專案的索引鍵屬性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[取得和設定屬性](getting-and-setting-properties.md)
</dt> <dt>

[屬性之間的相互相關性](interdependencies-between-properties.md)
</dt> <dt>

[儲存或捨棄變更](saving-or-discarding-changes.md)
</dt> </dl>

 

 



