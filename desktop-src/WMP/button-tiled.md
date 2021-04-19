---
title: 按鈕。磚
description: 並排顯示的屬性會指定或抓取值，指出是否將按鈕影像並排顯示。
ms.assetid: 5526477d-a235-4960-adef-5cf0ef9c46be
keywords:
- 按鈕。磚 Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c6c1316f10ce9ae3135f4ac35ab214ecdd1096d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993669"
---
# <a name="buttontiled"></a><span data-ttu-id="08738-104">按鈕。磚</span><span class="sxs-lookup"><span data-stu-id="08738-104">BUTTON.tiled</span></span>

<span data-ttu-id="08738-105">並排顯示 **的屬性會** 指定或抓取值，指出是否將 **按鈕** 影像並排顯示。</span><span class="sxs-lookup"><span data-stu-id="08738-105">The **tiled** attribute specifies or retrieves a value indicating whether the **BUTTON** image will be tiled.</span></span>

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a><span data-ttu-id="08738-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="08738-106">Possible Values</span></span>

<span data-ttu-id="08738-107">此屬性是讀取/寫入 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="08738-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="08738-108">值</span><span class="sxs-lookup"><span data-stu-id="08738-108">Value</span></span> | <span data-ttu-id="08738-109">描述</span><span class="sxs-lookup"><span data-stu-id="08738-109">Description</span></span>                       |
|-------|-----------------------------------|
| <span data-ttu-id="08738-110">true</span><span class="sxs-lookup"><span data-stu-id="08738-110">true</span></span>  | <span data-ttu-id="08738-111">影像將會並排顯示。</span><span class="sxs-lookup"><span data-stu-id="08738-111">Image will be tiled.</span></span>              |
| <span data-ttu-id="08738-112">false</span><span class="sxs-lookup"><span data-stu-id="08738-112">false</span></span> | <span data-ttu-id="08738-113">預設值。</span><span class="sxs-lookup"><span data-stu-id="08738-113">Default.</span></span> <span data-ttu-id="08738-114">影像將不會並排顯示。</span><span class="sxs-lookup"><span data-stu-id="08738-114">Image will not be tiled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="08738-115">備註</span><span class="sxs-lookup"><span data-stu-id="08738-115">Remarks</span></span>

<span data-ttu-id="08738-116">如果影像小於控制項的實際區域，則平鋪影像將會重複，直到填滿整個區域為止。</span><span class="sxs-lookup"><span data-stu-id="08738-116">If the image is smaller than the actual region of the control, then tiling the image will repeat it until it fills the entire region.</span></span> <span data-ttu-id="08738-117">如果未指定或無法抓取影像，則會將 **磚** 設定為 false。</span><span class="sxs-lookup"><span data-stu-id="08738-117">If an image is not specified or cannot be retrieved, **tiled** will be set to false.</span></span>

## <a name="requirements"></a><span data-ttu-id="08738-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="08738-118">Requirements</span></span>



| <span data-ttu-id="08738-119">需求</span><span class="sxs-lookup"><span data-stu-id="08738-119">Requirement</span></span> | <span data-ttu-id="08738-120">值</span><span class="sxs-lookup"><span data-stu-id="08738-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="08738-121">版本</span><span class="sxs-lookup"><span data-stu-id="08738-121">Version</span></span><br/> | <span data-ttu-id="08738-122">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="08738-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="08738-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08738-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08738-124">**BUTTON 元素**</span><span class="sxs-lookup"><span data-stu-id="08738-124">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="08738-125">**按鈕。影像**</span><span class="sxs-lookup"><span data-stu-id="08738-125">**BUTTON.image**</span></span>](button-image.md)
</dt> </dl>

 

 





