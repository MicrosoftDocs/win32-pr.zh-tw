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
# <a name="search-attributes-only"></a><span data-ttu-id="f3df8-104">僅搜尋屬性</span><span class="sxs-lookup"><span data-stu-id="f3df8-104">Search Attributes Only</span></span>

<span data-ttu-id="f3df8-105">有時您會執行搜尋，以判斷物件可使用的資料類型。</span><span class="sxs-lookup"><span data-stu-id="f3df8-105">Sometimes you perform a search to determine what type of data is available for an object.</span></span> <span data-ttu-id="f3df8-106">在此情況下，您只會對物件的屬性（而非值）感興趣。</span><span class="sxs-lookup"><span data-stu-id="f3df8-106">In this case, you are interested only in the attributes, and not the values, of the object.</span></span> <span data-ttu-id="f3df8-107">若要完成此動作，請設定 [僅搜尋屬性] 選項。</span><span class="sxs-lookup"><span data-stu-id="f3df8-107">To accomplish this, you set the "search attributes only" option.</span></span> <span data-ttu-id="f3df8-108">指定此選項會傳回沒有值的屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="f3df8-108">Specifying this option returns the attribute names without their values.</span></span> <span data-ttu-id="f3df8-109">不過，結果集會包含已指派值的屬性。</span><span class="sxs-lookup"><span data-stu-id="f3df8-109">However, the result set includes only those attributes that have values assigned.</span></span> <span data-ttu-id="f3df8-110">例如，請考慮具有下列屬性的物件：</span><span class="sxs-lookup"><span data-stu-id="f3df8-110">For example, consider an object with the following attributes:</span></span>

``` syntax
First Name = Jeff
Last Name = Smith
Department = <Empty>
Phone Number = (425) 432-3442
```

<span data-ttu-id="f3df8-111">當設定 [僅搜尋屬性] 選項時，結果集會包含：</span><span class="sxs-lookup"><span data-stu-id="f3df8-111">When the search attributes only option is set, the result set includes:</span></span>

``` syntax
First Name
Last Name
Phone Number
```

<span data-ttu-id="f3df8-112">如需有關使用僅搜尋屬性選項搭配特定搜尋介面的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="f3df8-112">For more information about using the search attributes only option with a specific search interface, see:</span></span>

-   [<span data-ttu-id="f3df8-113">使用 >idirectorysearch 只傳回屬性名稱</span><span class="sxs-lookup"><span data-stu-id="f3df8-113">Returning Only Attribute Names with IDirectorySearch</span></span>](returning-only-attribute-names-with-idirectorysearch.md)
-   [<span data-ttu-id="f3df8-114">使用 ActiveX Data Objects 搜尋</span><span class="sxs-lookup"><span data-stu-id="f3df8-114">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="f3df8-115">使用 OLE DB 搜尋</span><span class="sxs-lookup"><span data-stu-id="f3df8-115">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




