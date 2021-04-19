---
title: 文字。滾動
description: 滾動屬性會指定或抓取值，指出文字是否會滾動。
ms.assetid: 1cd5cb4e-673f-4273-91ff-50165c2b08fa
keywords:
- 文字。滾動 Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.scrolling
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fdbb80b2033d542da4894172d58451ed5da224f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984082"
---
# <a name="textscrolling"></a><span data-ttu-id="635ff-104">文字。滾動</span><span class="sxs-lookup"><span data-stu-id="635ff-104">TEXT.scrolling</span></span>

<span data-ttu-id="635ff-105">**滾動** 屬性會指定或抓取值，指出文字是否會滾動。</span><span class="sxs-lookup"><span data-stu-id="635ff-105">The **scrolling** attribute specifies or retrieves a value indicating whether the text scrolls.</span></span>

``` syntax
        elementID.scrolling
```

## <a name="possible-values"></a><span data-ttu-id="635ff-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="635ff-106">Possible Values</span></span>

<span data-ttu-id="635ff-107">此屬性是讀取/寫入 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="635ff-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="635ff-108">值</span><span class="sxs-lookup"><span data-stu-id="635ff-108">Value</span></span> | <span data-ttu-id="635ff-109">描述</span><span class="sxs-lookup"><span data-stu-id="635ff-109">Description</span></span>                     |
|-------|---------------------------------|
| <span data-ttu-id="635ff-110">true</span><span class="sxs-lookup"><span data-stu-id="635ff-110">true</span></span>  | <span data-ttu-id="635ff-111">已啟用滾動。</span><span class="sxs-lookup"><span data-stu-id="635ff-111">Scrolling is enabled.</span></span>           |
| <span data-ttu-id="635ff-112">false</span><span class="sxs-lookup"><span data-stu-id="635ff-112">false</span></span> | <span data-ttu-id="635ff-113">預設值。</span><span class="sxs-lookup"><span data-stu-id="635ff-113">Default.</span></span> <span data-ttu-id="635ff-114">滾動已停用。</span><span class="sxs-lookup"><span data-stu-id="635ff-114">Scrolling is disabled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="635ff-115">備註</span><span class="sxs-lookup"><span data-stu-id="635ff-115">Remarks</span></span>

<span data-ttu-id="635ff-116">滾動功能會在文字結尾和重複行的開頭之間提供兩個空間的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="635ff-116">The scrolling feature provides a two-space buffer between the end of the text and the beginning of the repeated line.</span></span>

<span data-ttu-id="635ff-117">[ **對齊** ] 屬性會指定文字首次出現的位置，然後才開始滾動。</span><span class="sxs-lookup"><span data-stu-id="635ff-117">The **justification** attribute specifies where the text first appears before the scrolling begins.</span></span>

<span data-ttu-id="635ff-118">如需說明如何使用 **TEXT** 元素屬性的範例，請參閱 [value](text-value.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="635ff-118">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="635ff-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="635ff-119">Requirements</span></span>



| <span data-ttu-id="635ff-120">需求</span><span class="sxs-lookup"><span data-stu-id="635ff-120">Requirement</span></span> | <span data-ttu-id="635ff-121">值</span><span class="sxs-lookup"><span data-stu-id="635ff-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="635ff-122">版本</span><span class="sxs-lookup"><span data-stu-id="635ff-122">Version</span></span><br/> | <span data-ttu-id="635ff-123">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="635ff-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="635ff-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="635ff-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="635ff-125">**TEXT 元素**</span><span class="sxs-lookup"><span data-stu-id="635ff-125">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="635ff-126">**文字。對齊方式**</span><span class="sxs-lookup"><span data-stu-id="635ff-126">**TEXT.justification**</span></span>](text-justification.md)
</dt> <dt>

[<span data-ttu-id="635ff-127">**ScrollingAmount**</span><span class="sxs-lookup"><span data-stu-id="635ff-127">**TEXT.scrollingAmount**</span></span>](text-scrollingamount.md)
</dt> <dt>

[<span data-ttu-id="635ff-128">**ScrollingDelay**</span><span class="sxs-lookup"><span data-stu-id="635ff-128">**TEXT.scrollingDelay**</span></span>](text-scrollingdelay.md)
</dt> <dt>

[<span data-ttu-id="635ff-129">**ScrollingDirection**</span><span class="sxs-lookup"><span data-stu-id="635ff-129">**TEXT.scrollingDirection**</span></span>](text-scrollingdirection.md)
</dt> </dl>

 

 





