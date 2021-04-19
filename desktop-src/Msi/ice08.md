---
description: ICE08 會驗證元件資料表不包含重複的 Guid。 每個元件都必須有唯一的 GUID。 如果元件資料表不存在，則不會進行驗證。
ms.assetid: c8ff53f3-6587-479d-afb8-b09d0df3b673
title: ICE08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 051f32aa983fdae39fc3717d3c9036b542f14369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978018"
---
# <a name="ice08"></a><span data-ttu-id="56462-105">ICE08</span><span class="sxs-lookup"><span data-stu-id="56462-105">ICE08</span></span>

<span data-ttu-id="56462-106">ICE08 會驗證 [元件資料表](component-table.md) 不包含重複的 [guid](guid.md)。</span><span class="sxs-lookup"><span data-stu-id="56462-106">ICE08 validates that the [Component table](component-table.md) contains no duplicate [GUIDs](guid.md).</span></span> <span data-ttu-id="56462-107">每個元件都必須有唯一的 GUID。</span><span class="sxs-lookup"><span data-stu-id="56462-107">Every component must have a unique GUID.</span></span> <span data-ttu-id="56462-108">如果元件資料表不存在，則不會進行驗證。</span><span class="sxs-lookup"><span data-stu-id="56462-108">No validation is done if the Component table does not exist.</span></span>

## <a name="result"></a><span data-ttu-id="56462-109">結果</span><span class="sxs-lookup"><span data-stu-id="56462-109">Result</span></span>

<span data-ttu-id="56462-110">如果元件資料表的 [元件] 資料行中有兩個或多個專案包含相同的 GUID，ICE08 會張貼錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="56462-110">ICE08 posts an error message if two or more entries in the ComponentId column of the Component table contain the same GUID.</span></span>

## <a name="example"></a><span data-ttu-id="56462-111">範例</span><span class="sxs-lookup"><span data-stu-id="56462-111">Example</span></span>

<span data-ttu-id="56462-112">在下列範例中，ICE08 會張貼訊息，指出紅色和綠色元件有重複的 Guid。</span><span class="sxs-lookup"><span data-stu-id="56462-112">For the following example, ICE08 would post a message stating that components Red and Green have duplicate GUIDs.</span></span>

<span data-ttu-id="56462-113">[元件資料表](component-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="56462-113">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="56462-114">元件</span><span class="sxs-lookup"><span data-stu-id="56462-114">Component</span></span> | <span data-ttu-id="56462-115">ComponentId</span><span class="sxs-lookup"><span data-stu-id="56462-115">ComponentId</span></span>                            |
|-----------|----------------------------------------|
| <span data-ttu-id="56462-116">紅色</span><span class="sxs-lookup"><span data-stu-id="56462-116">Red</span></span>       | <span data-ttu-id="56462-117">{0000000A-0003-0000-0000-624474736554}</span><span class="sxs-lookup"><span data-stu-id="56462-117">{0000000A-0003-0000-0000-624474736554}</span></span> |
| <span data-ttu-id="56462-118">藍色</span><span class="sxs-lookup"><span data-stu-id="56462-118">Blue</span></span>      | <span data-ttu-id="56462-119">{0000000A-0003-0000-0000-624474736354}</span><span class="sxs-lookup"><span data-stu-id="56462-119">{0000000A-0003-0000-0000-624474736354}</span></span> |
| <span data-ttu-id="56462-120">綠色</span><span class="sxs-lookup"><span data-stu-id="56462-120">Green</span></span>     | <span data-ttu-id="56462-121">{0000000A-0003-0000-0000-624474736554}</span><span class="sxs-lookup"><span data-stu-id="56462-121">{0000000A-0003-0000-0000-624474736554}</span></span> |



 

<span data-ttu-id="56462-122">若要修正這個錯誤，請變更其中一個重複的 Guid。</span><span class="sxs-lookup"><span data-stu-id="56462-122">To fix this error, change either of the duplicate GUIDs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="56462-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="56462-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56462-124">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="56462-124">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



