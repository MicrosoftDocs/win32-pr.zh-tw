---
title: AmbientAttributes.clippingColor
description: ClippingColor 屬性會指定或抓取從 clippingImage 點陣圖裁剪的色彩。
ms.assetid: d6ea43d3-c118-43d3-bfdc-29ddd6ea4978
keywords:
- AmbientAttributes. clippingColor Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ad526eb0f705d1fce95f3813a666420b29db9de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995958"
---
# <a name="ambientattributesclippingcolor"></a><span data-ttu-id="2e185-104">AmbientAttributes.clippingColor</span><span class="sxs-lookup"><span data-stu-id="2e185-104">AmbientAttributes.clippingColor</span></span>

<span data-ttu-id="2e185-105">**ClippingColor** 屬性會指定或抓取從 **clippingImage** 點陣圖裁剪的色彩。</span><span class="sxs-lookup"><span data-stu-id="2e185-105">The **clippingColor** attribute specifies or retrieves the color to clip out from the **clippingImage** bitmap.</span></span>

``` syntax
        elementID.clippingColor
```

## <a name="possible-values"></a><span data-ttu-id="2e185-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="2e185-106">Possible Values</span></span>

<span data-ttu-id="2e185-107">此屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="2e185-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="2e185-108">值</span><span class="sxs-lookup"><span data-stu-id="2e185-108">Value</span></span>                                       | <span data-ttu-id="2e185-109">描述</span><span class="sxs-lookup"><span data-stu-id="2e185-109">Description</span></span>                                       |
|---------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="2e185-110">自動</span><span class="sxs-lookup"><span data-stu-id="2e185-110">Auto</span></span>                                        | <span data-ttu-id="2e185-111">預設值。</span><span class="sxs-lookup"><span data-stu-id="2e185-111">Default.</span></span> <span data-ttu-id="2e185-112">使用圖元位置0、0的色彩。</span><span class="sxs-lookup"><span data-stu-id="2e185-112">The color at pixel location 0,0 is used.</span></span> |
| <span data-ttu-id="2e185-113">任何 Microsoft Internet Explorer 色彩值</span><span class="sxs-lookup"><span data-stu-id="2e185-113">any Microsoft Internet Explorer color value</span></span> | <span data-ttu-id="2e185-114">使用指定的 Internet Explorer 色彩。</span><span class="sxs-lookup"><span data-stu-id="2e185-114">The specified Internet Explorer color is used.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="2e185-115">備註</span><span class="sxs-lookup"><span data-stu-id="2e185-115">Remarks</span></span>

<span data-ttu-id="2e185-116">裁剪色彩表示 **clippingImage** 的區域 (**或)** **backgroundImage** ，可對應 **至控制項的** 透明、不可按的部分。</span><span class="sxs-lookup"><span data-stu-id="2e185-116">The clipping color indicates the regions of the **clippingImage** (or **backgroundImage** for **VIEW** or **SUBVIEW**) that correspond to transparent, non-clickable portions of the control.</span></span> <span data-ttu-id="2e185-117">裁剪色彩可以表示要裁剪多個區域。如果 **clippingImage** 是一個 JPG 來警告 jpg 中的色彩遺失，就會發出警告。</span><span class="sxs-lookup"><span data-stu-id="2e185-117">The clipping color can indicate multiple regions to be clipped out. A warning is issued if the **clippingImage** is a JPG to warn of loss of color in JPGs.</span></span>

<span data-ttu-id="2e185-118">**播放清單** 元素不支援 **clippingColor** 屬性。</span><span class="sxs-lookup"><span data-stu-id="2e185-118">The **clippingColor** attribute is not supported by the **PLAYLIST** element.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e185-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e185-119">Requirements</span></span>



| <span data-ttu-id="2e185-120">需求</span><span class="sxs-lookup"><span data-stu-id="2e185-120">Requirement</span></span> | <span data-ttu-id="2e185-121">值</span><span class="sxs-lookup"><span data-stu-id="2e185-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="2e185-122">版本</span><span class="sxs-lookup"><span data-stu-id="2e185-122">Version</span></span><br/> | <span data-ttu-id="2e185-123">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="2e185-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2e185-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e185-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e185-125">**環境屬性**</span><span class="sxs-lookup"><span data-stu-id="2e185-125">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="2e185-126">**AmbientAttributes.clippingImage**</span><span class="sxs-lookup"><span data-stu-id="2e185-126">**AmbientAttributes.clippingImage**</span></span>](ambientattributes-clippingimage.md)
</dt> <dt>

[<span data-ttu-id="2e185-127">**色彩參考**</span><span class="sxs-lookup"><span data-stu-id="2e185-127">**Color Reference**</span></span>](color-reference.md)
</dt> </dl>

 

 





