---
title: 狀態字型
description: 狀態字型
ms.assetid: eba697e8-8be5-4692-b7b2-a52c5642022a
keywords:
- Windows Media Player 行動外觀、狀態顯示
- 外觀，狀態顯示
- 外觀的參考、狀態顯示
- 外觀、字型中的狀態顯示
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a773f3baaeda0eaa90dfe0702957b5b7888271
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932489"
---
# <a name="status-font"></a><span data-ttu-id="4699d-107">狀態字型</span><span class="sxs-lookup"><span data-stu-id="4699d-107">Status Font</span></span>

<span data-ttu-id="4699d-108">您必須定義您想要使用的狀態顯示所使用的字型。</span><span class="sxs-lookup"><span data-stu-id="4699d-108">You must define the font used by the status display you wish to use.</span></span> <span data-ttu-id="4699d-109">字型是由三個以逗號分隔的值所定義，表示字型的臉部、大小和權數。</span><span class="sxs-lookup"><span data-stu-id="4699d-109">The font is defined by three values, separated by commas, representing the face, size, and weight of the font.</span></span>

<span data-ttu-id="4699d-110">**字樣值**</span><span class="sxs-lookup"><span data-stu-id="4699d-110">**Typeface Values**</span></span>

<span data-ttu-id="4699d-111">如果您有可能在使用者的電腦上安裝任何字體名稱，則可以使用該名稱。</span><span class="sxs-lookup"><span data-stu-id="4699d-111">Any typeface name can be used if it is likely to be installed on the user's machine.</span></span> <span data-ttu-id="4699d-112">如果在電腦上找不到字樣，則作業系統會選取替代選項。</span><span class="sxs-lookup"><span data-stu-id="4699d-112">If a typeface is not found on the machine, an alternate will be selected by the operating system.</span></span> <span data-ttu-id="4699d-113">下表顯示通常會在 Windows Mobile 2003 裝置上找到的字樣。</span><span class="sxs-lookup"><span data-stu-id="4699d-113">The following table shows the typefaces that are usually found on Windows Mobile 2003-based devices.</span></span>



| <span data-ttu-id="4699d-114">字樣</span><span class="sxs-lookup"><span data-stu-id="4699d-114">Typeface</span></span>       | <span data-ttu-id="4699d-115">Description</span><span class="sxs-lookup"><span data-stu-id="4699d-115">Description</span></span>              |
|----------------|--------------------------|
| <span data-ttu-id="4699d-116">Tahoma</span><span class="sxs-lookup"><span data-stu-id="4699d-116">Tahoma</span></span>         | <span data-ttu-id="4699d-117">Sans-serif 字型。</span><span class="sxs-lookup"><span data-stu-id="4699d-117">A sans-serif typeface.</span></span>   |
| <span data-ttu-id="4699d-118">華文中的主控台</span><span class="sxs-lookup"><span data-stu-id="4699d-118">Lucida Console</span></span> | <span data-ttu-id="4699d-119">雙 serif 字型。</span><span class="sxs-lookup"><span data-stu-id="4699d-119">A square-serif typeface.</span></span> |



 

<span data-ttu-id="4699d-120">**大小值**</span><span class="sxs-lookup"><span data-stu-id="4699d-120">**Size Values**</span></span>

<span data-ttu-id="4699d-121">這是以點為單位的字樣大小。</span><span class="sxs-lookup"><span data-stu-id="4699d-121">This is the size of the typeface in points.</span></span> <span data-ttu-id="4699d-122">任何正整數值都是有效的，但建議使用介於10到18之間的數位。</span><span class="sxs-lookup"><span data-stu-id="4699d-122">Any positive integer value is valid, though numbers between 10 and 18 are recommended.</span></span> <span data-ttu-id="4699d-123">小於10的大小可能很難讀取，而且18以上的大小可能不會留下足夠的空間來顯示一次以上的字母。</span><span class="sxs-lookup"><span data-stu-id="4699d-123">Sizes smaller than 10 may be difficult to read, and sizes above 18 may not leave enough space to display more than a few letters at a time.</span></span>

<span data-ttu-id="4699d-124">**權數值**</span><span class="sxs-lookup"><span data-stu-id="4699d-124">**Weight Values**</span></span>

<span data-ttu-id="4699d-125">下表顯示唯一允許的值。</span><span class="sxs-lookup"><span data-stu-id="4699d-125">The only values allowed are shown in the following table.</span></span>



| <span data-ttu-id="4699d-126">值</span><span class="sxs-lookup"><span data-stu-id="4699d-126">Value</span></span> | <span data-ttu-id="4699d-127">描述</span><span class="sxs-lookup"><span data-stu-id="4699d-127">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="4699d-128">B</span><span class="sxs-lookup"><span data-stu-id="4699d-128">B</span></span>     | <span data-ttu-id="4699d-129">粗體</span><span class="sxs-lookup"><span data-stu-id="4699d-129">Bold</span></span>        |
| <span data-ttu-id="4699d-130">N</span><span class="sxs-lookup"><span data-stu-id="4699d-130">N</span></span>     | <span data-ttu-id="4699d-131">正常</span><span class="sxs-lookup"><span data-stu-id="4699d-131">Normal</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="4699d-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="4699d-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4699d-133">**地位**</span><span class="sxs-lookup"><span data-stu-id="4699d-133">**Status**</span></span>](status.md)
</dt> </dl>

 

 




