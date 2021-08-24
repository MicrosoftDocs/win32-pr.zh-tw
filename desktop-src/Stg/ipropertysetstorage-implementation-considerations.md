---
title: IPropertySetStorage 實行考慮
description: 考慮如何提供 IPropertySetStorage 介面的執行，以讀取和寫入 COM 屬性集格式時，會發生數個問題。 下列各節會描述這些考量事項。
ms.assetid: 055da516-ed42-49ec-b20c-a5e98718bea8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c74800eb0721d881825d48781ac0f3dd2517e0beeb86077312e3ad8c8cbe9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961338"
---
# <a name="ipropertysetstorage-implementation-considerations"></a>IPropertySetStorage 實行考慮

考慮如何提供 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 介面的執行，以讀取和寫入 COM 屬性集格式時，會發生數個問題。 下列各節會描述這些考量事項。

-   [IStorage 中的名稱](names-in-istorage.md)
-   [屬性集的儲存體和資料流程物件](storage-vs--stream-for-a-property-set.md)
-   [設定屬性集類別識別碼](setting-the-property-set-class-identifier.md)
-   [同步處理點](synchronization-points.md)
-   [字碼頁和 Unicode 字串](code-pages-and-unicode-strings.md)
-   [Dictionary](dictionary.md)
-   [擴充功能](extensions.md)
-   [屬性集序列化](version-0-vs--version-1-property-set-serialization.md)

如需詳細資訊，請參閱介面下參考區段中的 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 。

 

 




