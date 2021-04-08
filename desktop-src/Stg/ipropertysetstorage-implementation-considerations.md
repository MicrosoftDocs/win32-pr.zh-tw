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
# <a name="ipropertysetstorage-implementation-considerations"></a><span data-ttu-id="56ead-104">IPropertySetStorage 實行考慮</span><span class="sxs-lookup"><span data-stu-id="56ead-104">IPropertySetStorage Implementation Considerations</span></span>

<span data-ttu-id="56ead-105">考慮如何提供 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 介面的執行，以讀取和寫入 COM 屬性集格式時，會發生數個問題。</span><span class="sxs-lookup"><span data-stu-id="56ead-105">Several issues arise when considering how to provide an implementation of the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interface that reads and writes the COM property set format.</span></span> <span data-ttu-id="56ead-106">下列各節會描述這些考量事項。</span><span class="sxs-lookup"><span data-stu-id="56ead-106">The following sections describe these considerations.</span></span>

-   [<span data-ttu-id="56ead-107">IStorage 中的名稱</span><span class="sxs-lookup"><span data-stu-id="56ead-107">Names in IStorage</span></span>](names-in-istorage.md)
-   [<span data-ttu-id="56ead-108">屬性集的儲存和資料流程物件</span><span class="sxs-lookup"><span data-stu-id="56ead-108">Storage and Stream Objects for a Property Set</span></span>](storage-vs--stream-for-a-property-set.md)
-   [<span data-ttu-id="56ead-109">設定屬性集類別識別碼</span><span class="sxs-lookup"><span data-stu-id="56ead-109">Setting the Property Set Class Identifier</span></span>](setting-the-property-set-class-identifier.md)
-   [<span data-ttu-id="56ead-110">同步處理點</span><span class="sxs-lookup"><span data-stu-id="56ead-110">Synchronization Points</span></span>](synchronization-points.md)
-   [<span data-ttu-id="56ead-111">字碼頁和 Unicode 字串</span><span class="sxs-lookup"><span data-stu-id="56ead-111">Code Pages and Unicode Strings</span></span>](code-pages-and-unicode-strings.md)
-   [<span data-ttu-id="56ead-112">Dictionary</span><span class="sxs-lookup"><span data-stu-id="56ead-112">Dictionary</span></span>](dictionary.md)
-   [<span data-ttu-id="56ead-113">擴充功能</span><span class="sxs-lookup"><span data-stu-id="56ead-113">Extensions</span></span>](extensions.md)
-   [<span data-ttu-id="56ead-114">屬性集序列化</span><span class="sxs-lookup"><span data-stu-id="56ead-114">Property Set Serialization</span></span>](version-0-vs--version-1-property-set-serialization.md)

<span data-ttu-id="56ead-115">如需詳細資訊，請參閱介面下參考區段中的 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 。</span><span class="sxs-lookup"><span data-stu-id="56ead-115">For more information, see [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) in the Reference section under Interfaces.</span></span>

 

 




