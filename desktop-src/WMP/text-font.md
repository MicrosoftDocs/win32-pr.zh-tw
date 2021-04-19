---
title: 文字字型
description: 文字字型
ms.assetid: 4f9e305b-bba0-4f39-974b-4ac511656bc3
keywords:
- Windows Media Player 行動外觀、文字
- 外觀，文字
- 外觀的參考、文字
- 外觀、字型中的文字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 968a6b8105141f8efae7b35f6aa57c73f5614e45
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967418"
---
# <a name="text-font"></a><span data-ttu-id="cdb73-107">文字字型</span><span class="sxs-lookup"><span data-stu-id="cdb73-107">Text Font</span></span>

<span data-ttu-id="cdb73-108">您必須定義您想要使用的文字顯示框所使用的字型。</span><span class="sxs-lookup"><span data-stu-id="cdb73-108">You must define the font used by the text display box you want to use.</span></span> <span data-ttu-id="cdb73-109">字型是由三個以逗號分隔的值所定義，表示字型的臉部、大小和權數。</span><span class="sxs-lookup"><span data-stu-id="cdb73-109">The font is defined by three values, separated by commas, representing the face, size, and weight of the font.</span></span>

<span data-ttu-id="cdb73-110">**字樣值**</span><span class="sxs-lookup"><span data-stu-id="cdb73-110">**Typeface Values**</span></span>

<span data-ttu-id="cdb73-111">如果您有可能在使用者的電腦上安裝任何字體名稱，則可以使用該名稱。</span><span class="sxs-lookup"><span data-stu-id="cdb73-111">Any typeface name can be used if it is likely to be installed on the user's machine.</span></span> <span data-ttu-id="cdb73-112">如果在電腦上找不到字樣，則作業系統會選取替代選項。</span><span class="sxs-lookup"><span data-stu-id="cdb73-112">If a typeface is not found on the machine, an alternate will be selected by the operating system.</span></span> <span data-ttu-id="cdb73-113">下表顯示通常會在 Windows Mobile 2003 裝置上找到的字樣。</span><span class="sxs-lookup"><span data-stu-id="cdb73-113">The following table shows typefaces that are usually found on Windows Mobile 2003-based devices.</span></span>



| <span data-ttu-id="cdb73-114">字樣</span><span class="sxs-lookup"><span data-stu-id="cdb73-114">Typeface</span></span>       | <span data-ttu-id="cdb73-115">Description</span><span class="sxs-lookup"><span data-stu-id="cdb73-115">Description</span></span>              |
|----------------|--------------------------|
| <span data-ttu-id="cdb73-116">Tahoma</span><span class="sxs-lookup"><span data-stu-id="cdb73-116">Tahoma</span></span>         | <span data-ttu-id="cdb73-117">Sans-serif 字型。</span><span class="sxs-lookup"><span data-stu-id="cdb73-117">A sans-serif typeface.</span></span>   |
| <span data-ttu-id="cdb73-118">華文中的主控台</span><span class="sxs-lookup"><span data-stu-id="cdb73-118">Lucida Console</span></span> | <span data-ttu-id="cdb73-119">雙 serif 字型。</span><span class="sxs-lookup"><span data-stu-id="cdb73-119">A square-serif typeface.</span></span> |



 

<span data-ttu-id="cdb73-120">**大小值**</span><span class="sxs-lookup"><span data-stu-id="cdb73-120">**Size Values**</span></span>

<span data-ttu-id="cdb73-121">這是以點為單位的字樣大小。</span><span class="sxs-lookup"><span data-stu-id="cdb73-121">This is the size of the typeface in points.</span></span> <span data-ttu-id="cdb73-122">任何正整數值都是有效的，但建議使用介於10到18之間的數位。</span><span class="sxs-lookup"><span data-stu-id="cdb73-122">Any positive integer value is valid, though numbers between 10 and 18 are recommended.</span></span> <span data-ttu-id="cdb73-123">小於10的大小可能很難讀取，而且18以上的大小可能不會留下足夠的空間來顯示一次以上的字母。</span><span class="sxs-lookup"><span data-stu-id="cdb73-123">Sizes smaller than 10 may be difficult to read, and sizes above 18 may not leave enough space to display more than a few letters at a time.</span></span>

<span data-ttu-id="cdb73-124">**權數值**</span><span class="sxs-lookup"><span data-stu-id="cdb73-124">**Weight Values**</span></span>

<span data-ttu-id="cdb73-125">下表顯示唯一允許的值。</span><span class="sxs-lookup"><span data-stu-id="cdb73-125">The only values allowed are shown in the following table.</span></span>



| <span data-ttu-id="cdb73-126">值</span><span class="sxs-lookup"><span data-stu-id="cdb73-126">Value</span></span> | <span data-ttu-id="cdb73-127">描述</span><span class="sxs-lookup"><span data-stu-id="cdb73-127">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="cdb73-128">B</span><span class="sxs-lookup"><span data-stu-id="cdb73-128">B</span></span>     | <span data-ttu-id="cdb73-129">粗體</span><span class="sxs-lookup"><span data-stu-id="cdb73-129">Bold</span></span>        |
| <span data-ttu-id="cdb73-130">N</span><span class="sxs-lookup"><span data-stu-id="cdb73-130">N</span></span>     | <span data-ttu-id="cdb73-131">正常</span><span class="sxs-lookup"><span data-stu-id="cdb73-131">Normal</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="cdb73-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="cdb73-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdb73-133">**Text**</span><span class="sxs-lookup"><span data-stu-id="cdb73-133">**Text**</span></span>](text.md)
</dt> </dl>

 

 




