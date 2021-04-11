---
description: 在 Windows Installer 安裝期間，安裝程式可以搜尋登錄專案，並建立保存登錄值的屬性。
ms.assetid: 3a663fc7-cdcf-4ac3-8251-836ba0d3cc11
title: 搜尋登錄專案，並建立保存登錄值的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82bd7572c0176f4870eed199800715190d9bbbf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847751"
---
# <a name="searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry"></a><span data-ttu-id="2cd2a-103">搜尋登錄專案，並建立保存登錄值的屬性</span><span class="sxs-lookup"><span data-stu-id="2cd2a-103">Searching for a Registry Entry and Creating a Property Holding the Value of the Registry</span></span>

<span data-ttu-id="2cd2a-104">**搜尋登錄專案並建立保存該檔案值的屬性**</span><span class="sxs-lookup"><span data-stu-id="2cd2a-104">**To search for a registry entry and create a property holding the value of that file**</span></span>

1.  <span data-ttu-id="2cd2a-105">請勿將簽章加入至簽章 [資料表](signature-table.md) 或 [CompLocator 資料表](complocator-table.md)。</span><span class="sxs-lookup"><span data-stu-id="2cd2a-105">Do not add the signature to the [Signature Table](signature-table.md) or the [CompLocator Table](complocator-table.md).</span></span> <span data-ttu-id="2cd2a-106">如果檔案簽章列在 [AppSearch 資料表](appsearch-table.md) 中，而且未列于 Signature 或 CompLocator 資料表中，安裝程式會在 [RegLocator 資料表](reglocator-table.md)中尋找。</span><span class="sxs-lookup"><span data-stu-id="2cd2a-106">If a file signature is listed in the [AppSearch Table](appsearch-table.md) and is not listed in the Signature or CompLocator tables, the Installer looks in the [RegLocator Table](reglocator-table.md).</span></span>

2.  <span data-ttu-id="2cd2a-107">指定要在 [RegLocator 資料表](reglocator-table.md)中搜尋的登錄專案。</span><span class="sxs-lookup"><span data-stu-id="2cd2a-107">Specify the registry entry to be searched for in the [RegLocator Table](reglocator-table.md).</span></span> <span data-ttu-id="2cd2a-108">如果簽章 [資料表](signature-table.md) 中沒有簽章，而且類型資料行的值是 **msidbLocatorTypeRawValue**，則會假設搜尋是針對 RegLocator 資料表所指向的特定登錄機碼名稱。</span><span class="sxs-lookup"><span data-stu-id="2cd2a-108">If the signature is absent from the [Signature Table](signature-table.md) and the value of the Type column is **msidbLocatorTypeRawValue**, then the search is assumed to be for the specific registry key name pointed to by the RegLocator Table.</span></span>

    <span data-ttu-id="2cd2a-109">[RegLocator 資料表](reglocator-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="2cd2a-109">[RegLocator Table](reglocator-table.md) (partial)</span></span>

    

    | <span data-ttu-id="2cd2a-110">簽名\_</span><span class="sxs-lookup"><span data-stu-id="2cd2a-110">Signature\_</span></span>         | <span data-ttu-id="2cd2a-111">Root</span><span class="sxs-lookup"><span data-stu-id="2cd2a-111">Root</span></span>         | <span data-ttu-id="2cd2a-112">按鍵</span><span class="sxs-lookup"><span data-stu-id="2cd2a-112">Key</span></span>                                                           | <span data-ttu-id="2cd2a-113">名稱</span><span class="sxs-lookup"><span data-stu-id="2cd2a-113">Name</span></span>                  | <span data-ttu-id="2cd2a-114">類型</span><span class="sxs-lookup"><span data-stu-id="2cd2a-114">Type</span></span>                                    |
    |---------------------|--------------|---------------------------------------------------------------|-----------------------|-----------------------------------------|
    | <span data-ttu-id="2cd2a-115">AppValue</span><span class="sxs-lookup"><span data-stu-id="2cd2a-115">AppValue</span></span><br/> | <span data-ttu-id="2cd2a-116">2</span><span class="sxs-lookup"><span data-stu-id="2cd2a-116">2</span></span><br/> | <span data-ttu-id="2cd2a-117">**軟體** \\**Microsoft** \\**MyApp**</span><span class="sxs-lookup"><span data-stu-id="2cd2a-117">**SOFTWARE**\\**Microsoft**\\**MyApp**</span></span><br/> <br/> | <span data-ttu-id="2cd2a-118">**Myname**</span><span class="sxs-lookup"><span data-stu-id="2cd2a-118">**Myname**</span></span><br/> | <span data-ttu-id="2cd2a-119">**msidbLocatorTypeRawValue**</span><span class="sxs-lookup"><span data-stu-id="2cd2a-119">**msidbLocatorTypeRawValue**</span></span><br/> |

    

     

3.  <span data-ttu-id="2cd2a-120">最後，填入 [AppSearch 資料表](appsearch-table.md) ，讓 [AppSearch 動作](appsearch-action.md) 傳回 AppValue 的值。</span><span class="sxs-lookup"><span data-stu-id="2cd2a-120">Finally, populate the [AppSearch Table](appsearch-table.md) so that the [AppSearch Action](appsearch-action.md) returns the value of AppValue.</span></span> <span data-ttu-id="2cd2a-121">在安裝程式執行 AppSearch 動作之後，MYREGVAL 的值就是 AppValue 的值。</span><span class="sxs-lookup"><span data-stu-id="2cd2a-121">After the Installer executes the AppSearch Action, the value of MYREGVAL is the value of AppValue.</span></span>

    <span data-ttu-id="2cd2a-122">[AppSearch 資料表](appsearch-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="2cd2a-122">[AppSearch Table](appsearch-table.md) (partial)</span></span>

    

    | <span data-ttu-id="2cd2a-123">屬性</span><span class="sxs-lookup"><span data-stu-id="2cd2a-123">Property</span></span>            | <span data-ttu-id="2cd2a-124">簽名</span><span class="sxs-lookup"><span data-stu-id="2cd2a-124">Signature</span></span>           |
    |---------------------|---------------------|
    | <span data-ttu-id="2cd2a-125">MYREGVAL</span><span class="sxs-lookup"><span data-stu-id="2cd2a-125">MYREGVAL</span></span><br/> | <span data-ttu-id="2cd2a-126">AppValue</span><span class="sxs-lookup"><span data-stu-id="2cd2a-126">AppValue</span></span><br/> |

    

     

 

 




