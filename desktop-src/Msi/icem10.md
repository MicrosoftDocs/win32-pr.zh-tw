---
description: ICEM10 會確認合併模組只包含屬性資料表中允許的屬性。
ms.assetid: 9ac7a724-ea0e-4caa-bb4f-846bfb802037
title: ICEM10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80263e5033ec14bd669c5d046c7f3842d58e332f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998133"
---
# <a name="icem10"></a><span data-ttu-id="f47d5-103">ICEM10</span><span class="sxs-lookup"><span data-stu-id="f47d5-103">ICEM10</span></span>

<span data-ttu-id="f47d5-104">ICEM10 會確認合併模組只包含 [屬性資料表](property-table.md)中允許的屬性。</span><span class="sxs-lookup"><span data-stu-id="f47d5-104">ICEM10 verifies that a merge module contains only properties that are allowed in the [Property Table](property-table.md).</span></span> <span data-ttu-id="f47d5-105">屬性工作表中不允許下列產品特定屬性：</span><span class="sxs-lookup"><span data-stu-id="f47d5-105">The following product specific properties are not allowed in the Property Table:</span></span>

-   [<span data-ttu-id="f47d5-106">**ProductLanguage 屬性**</span><span class="sxs-lookup"><span data-stu-id="f47d5-106">**ProductLanguage Property**</span></span>](productlanguage.md)
-   [<span data-ttu-id="f47d5-107">**ProductCode 屬性**</span><span class="sxs-lookup"><span data-stu-id="f47d5-107">**ProductCode Property**</span></span>](productcode.md)
-   [<span data-ttu-id="f47d5-108">**ProductVersion 屬性**</span><span class="sxs-lookup"><span data-stu-id="f47d5-108">**ProductVersion Property**</span></span>](productversion.md)
-   [<span data-ttu-id="f47d5-109">**ProductName 屬性**</span><span class="sxs-lookup"><span data-stu-id="f47d5-109">**ProductName Property**</span></span>](productname.md)
-   [<span data-ttu-id="f47d5-110">**Manufacturer 屬性**</span><span class="sxs-lookup"><span data-stu-id="f47d5-110">**Manufacturer Property**</span></span>](manufacturer.md)

## <a name="result"></a><span data-ttu-id="f47d5-111">結果</span><span class="sxs-lookup"><span data-stu-id="f47d5-111">Result</span></span>

<span data-ttu-id="f47d5-112">當合併模組包含 [屬性資料表](property-table.md)中不允許的屬性時，ICEM10 會張貼錯誤。</span><span class="sxs-lookup"><span data-stu-id="f47d5-112">ICEM10 posts an error when a merge module contains a property that is not allowed in the [Property Table](property-table.md).</span></span>

## <a name="example"></a><span data-ttu-id="f47d5-113">範例</span><span class="sxs-lookup"><span data-stu-id="f47d5-113">Example</span></span>

<span data-ttu-id="f47d5-114">ICEM10 會針對包含所顯示資料庫專案的模組，張貼下列錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="f47d5-114">ICEM10 posts the following error messages for a module that contains the database entries shown.</span></span>

``` syntax
The property 'ProductLanguage' is not allowed in a merge module.

The property 'Manufacturer' is not allowed in a merge module.
```

<span data-ttu-id="f47d5-115">下表顯示部分 [屬性資料表](property-table.md)。</span><span class="sxs-lookup"><span data-stu-id="f47d5-115">The following table shows you a partial [Property Table](property-table.md).</span></span>



| <span data-ttu-id="f47d5-116">屬性</span><span class="sxs-lookup"><span data-stu-id="f47d5-116">Property</span></span>                                   | <span data-ttu-id="f47d5-117">值</span><span class="sxs-lookup"><span data-stu-id="f47d5-117">Values</span></span>    |
|--------------------------------------------|-----------|
| <span data-ttu-id="f47d5-118">Color</span><span class="sxs-lookup"><span data-stu-id="f47d5-118">Color</span></span>                                      | <span data-ttu-id="f47d5-119">紅色</span><span class="sxs-lookup"><span data-stu-id="f47d5-119">Red</span></span>       |
| [<span data-ttu-id="f47d5-120">**製造商**</span><span class="sxs-lookup"><span data-stu-id="f47d5-120">**Manufacturer**</span></span>](manufacturer.md)       | <span data-ttu-id="f47d5-121">Microsoft</span><span class="sxs-lookup"><span data-stu-id="f47d5-121">Microsoft</span></span> |
| [<span data-ttu-id="f47d5-122">**ProductLanguage**</span><span class="sxs-lookup"><span data-stu-id="f47d5-122">**ProductLanguage**</span></span>](productlanguage.md) | <span data-ttu-id="f47d5-123">1033</span><span class="sxs-lookup"><span data-stu-id="f47d5-123">1033</span></span>      |



 

<span data-ttu-id="f47d5-124">下列程式說明如何修正錯誤。</span><span class="sxs-lookup"><span data-stu-id="f47d5-124">The following procedure shows you how to fix errors.</span></span>

<span data-ttu-id="f47d5-125">**若要修正錯誤**</span><span class="sxs-lookup"><span data-stu-id="f47d5-125">**To fix the errors**</span></span>

1.  <span data-ttu-id="f47d5-126">從 [屬性工作表](property-table.md)中移除「[**製造商**](manufacturer.md)」屬性。</span><span class="sxs-lookup"><span data-stu-id="f47d5-126">Remove the '[**Manufacturer**](manufacturer.md)' property from the [Property Table](property-table.md).</span></span>
2.  <span data-ttu-id="f47d5-127">從 [屬性資料表](property-table.md)中移除 '[**ProductLanguage**](productlanguage.md)' 屬性。</span><span class="sxs-lookup"><span data-stu-id="f47d5-127">Remove the '[**ProductLanguage**](productlanguage.md)' property from the [Property Table](property-table.md).</span></span>

## <a name="table-used-during-execution"></a><span data-ttu-id="f47d5-128">執行期間所使用的資料表</span><span class="sxs-lookup"><span data-stu-id="f47d5-128">Table Used During Execution</span></span>

<span data-ttu-id="f47d5-129">在執行期間，會使用 [屬性資料表](property-table.md) 。</span><span class="sxs-lookup"><span data-stu-id="f47d5-129">The [Property Table](property-table.md) is used during execution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f47d5-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="f47d5-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f47d5-131">Merge Module ICE 參考</span><span class="sxs-lookup"><span data-stu-id="f47d5-131">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



