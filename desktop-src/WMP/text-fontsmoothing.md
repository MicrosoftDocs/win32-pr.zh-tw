---
title: FontSmoothing
description: FontSmoothing 屬性會指定或抓取值，指出是否已啟用字型平滑處理。
ms.assetid: bd6f0468-285e-44b3-a5e8-361744c5ce4a
keywords:
- FontSmoothing Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.fontSmoothing
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcdf285572b4edda0f514cb3519b6953f9e94677
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977616"
---
# <a name="textfontsmoothing"></a><span data-ttu-id="18a21-104">FontSmoothing</span><span class="sxs-lookup"><span data-stu-id="18a21-104">TEXT.fontSmoothing</span></span>

<span data-ttu-id="18a21-105">**FontSmoothing** 屬性會指定或抓取值，指出是否已啟用字型平滑處理。</span><span class="sxs-lookup"><span data-stu-id="18a21-105">The **fontSmoothing** attribute specifies or retrieves a value indicating whether font smoothing is enabled.</span></span>

``` syntax
        elementID.fontSmoothing
```

## <a name="possible-values"></a><span data-ttu-id="18a21-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="18a21-106">Possible Values</span></span>

<span data-ttu-id="18a21-107">此屬性是讀取/寫入 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="18a21-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="18a21-108">值</span><span class="sxs-lookup"><span data-stu-id="18a21-108">Value</span></span> | <span data-ttu-id="18a21-109">描述</span><span class="sxs-lookup"><span data-stu-id="18a21-109">Description</span></span>                          |
|-------|--------------------------------------|
| <span data-ttu-id="18a21-110">true</span><span class="sxs-lookup"><span data-stu-id="18a21-110">true</span></span>  | <span data-ttu-id="18a21-111">啟用字型凹凸貼圖。</span><span class="sxs-lookup"><span data-stu-id="18a21-111">Font smoothing is enabled.</span></span>           |
| <span data-ttu-id="18a21-112">false</span><span class="sxs-lookup"><span data-stu-id="18a21-112">false</span></span> | <span data-ttu-id="18a21-113">預設值。</span><span class="sxs-lookup"><span data-stu-id="18a21-113">Default.</span></span> <span data-ttu-id="18a21-114">字型平滑處理已停用。</span><span class="sxs-lookup"><span data-stu-id="18a21-114">Font smoothing is disabled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="18a21-115">備註</span><span class="sxs-lookup"><span data-stu-id="18a21-115">Remarks</span></span>

<span data-ttu-id="18a21-116">字型平滑處理會使用作業系統的消除鋸齒功能。</span><span class="sxs-lookup"><span data-stu-id="18a21-116">Font smoothing uses the anti-aliasing feature of the operating system.</span></span> <span data-ttu-id="18a21-117">如果已啟用字型凹凸貼圖，而且作業系統支援消除鋸齒，Windows Media Player 會嘗試將文字平滑。</span><span class="sxs-lookup"><span data-stu-id="18a21-117">If font smoothing is enabled and the operating system supports anti-aliasing, Windows Media Player attempts to smooth the text.</span></span> <span data-ttu-id="18a21-118">並非所有字型都支援消除鋸齒。</span><span class="sxs-lookup"><span data-stu-id="18a21-118">Not all fonts support anti-aliasing.</span></span> <span data-ttu-id="18a21-119">Windows Media Player 10 使用 Windows XP ClearType 消除鋸齒方法。</span><span class="sxs-lookup"><span data-stu-id="18a21-119">Windows Media Player 10 uses the Windows XP ClearType anti-aliasing method.</span></span>

-   <span data-ttu-id="18a21-120">**警告** 透明色彩的字型平滑化可能會導致透明色彩混合成字元。</span><span class="sxs-lookup"><span data-stu-id="18a21-120">**Warning** Font smoothing over a transparent color may cause the transparent color to blend into the characters.</span></span> <span data-ttu-id="18a21-121">如果文字會顯示在透明上，則不建議使用 **fontSmoothing** 。</span><span class="sxs-lookup"><span data-stu-id="18a21-121">It is not recommended that you use **fontSmoothing** if the text will display over a transparency.</span></span>

<span data-ttu-id="18a21-122">如需說明如何使用 **TEXT** 元素屬性的範例，請參閱 [value](text-value.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="18a21-122">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="18a21-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="18a21-123">Requirements</span></span>



| <span data-ttu-id="18a21-124">需求</span><span class="sxs-lookup"><span data-stu-id="18a21-124">Requirement</span></span> | <span data-ttu-id="18a21-125">值</span><span class="sxs-lookup"><span data-stu-id="18a21-125">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="18a21-126">版本</span><span class="sxs-lookup"><span data-stu-id="18a21-126">Version</span></span><br/> | <span data-ttu-id="18a21-127">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="18a21-127">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="18a21-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18a21-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18a21-129">**TEXT 元素**</span><span class="sxs-lookup"><span data-stu-id="18a21-129">**TEXT Element**</span></span>](text-element.md)
</dt> </dl>

 

 





