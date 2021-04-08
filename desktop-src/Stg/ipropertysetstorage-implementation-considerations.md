---
title: IPropertySetStorage 實行考慮
description: 考慮如何提供 IPropertySetStorage 介面的執行，以讀取和寫入 COM 屬性集格式時，會發生數個問題。 下列各節會描述這些考量事項。
ms.assetid: 055da516-ed42-49ec-b20c-a5e98718bea8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f7532211668fa1ecf290484a707b19e1c263b9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674692"
---
# <a name="ipropertysetstorage-implementation-considerations"></a>IPropertySetStorage 實行考慮

考慮如何提供 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 介面的執行，以讀取和寫入 COM 屬性集格式時，會發生數個問題。 下列各節會描述這些考量事項。

-   [IStorage 中的名稱](names-in-istorage.md)
-   [屬性集的儲存和資料流程物件](storage-vs--stream-for-a-property-set.md)
-   [設定屬性集類別識別碼](setting-the-property-set-class-identifier.md)
-   [同步處理點](synchronization-points.md)
-   [字碼頁和 Unicode 字串](code-pages-and-unicode-strings.md)
-   [Dictionary](dictionary.md)
-   [擴充功能](extensions.md)
-   [屬性集序列化](version-0-vs--version-1-property-set-serialization.md)

如需詳細資訊，請參閱介面下參考區段中的 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 。

 

 




