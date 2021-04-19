---
title: AmbientAttributes 寬度
description: Width 屬性會指定或抓取控制項的寬度。
ms.assetid: f246958a-563c-40c0-8a74-4511103b95b2
keywords:
- AmbientAttributes width Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.width
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c3f91ee47277dc511d54747197edfa44e80e251
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992827"
---
# <a name="ambientattributeswidth"></a><span data-ttu-id="92c29-104">AmbientAttributes 寬度</span><span class="sxs-lookup"><span data-stu-id="92c29-104">AmbientAttributes.width</span></span>

<span data-ttu-id="92c29-105">**Width** 屬性會指定或抓取控制項的寬度。</span><span class="sxs-lookup"><span data-stu-id="92c29-105">The **width** attribute specifies or retrieves the width of the control.</span></span>

``` syntax
        elementID.width
```

## <a name="possible-values"></a><span data-ttu-id="92c29-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="92c29-106">Possible Values</span></span>

<span data-ttu-id="92c29-107">此屬性是讀取/寫入的16位 **整數** (0 到 32767) 代表控制項的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="92c29-107">This attribute is a read/write 16-bit **Integer** (0 to 32,767) representing the width of the control in pixels.</span></span> <span data-ttu-id="92c29-108">預設值為零或控制項 **影像** 屬性中所指定影像的寬度。</span><span class="sxs-lookup"><span data-stu-id="92c29-108">The default value is zero or the width of the image specified in the control's **image** attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="92c29-109">備註</span><span class="sxs-lookup"><span data-stu-id="92c29-109">Remarks</span></span>

<span data-ttu-id="92c29-110">如果指定的寬度比提供的影像寬度窄，則會裁剪影像。</span><span class="sxs-lookup"><span data-stu-id="92c29-110">If the width specified is narrower than the width of the image provided, then the image will be clipped.</span></span> <span data-ttu-id="92c29-111">如果寬度超過影像的寬度，則按一下區域將會超出影像界限。</span><span class="sxs-lookup"><span data-stu-id="92c29-111">If the width is wider than the width of the image, then the click region will go beyond the image boundary.</span></span> <span data-ttu-id="92c29-112">無論這個屬性的值為何，影像都不能成長到其父視圖 **或子\*\*\*\*視圖** 之外。</span><span class="sxs-lookup"><span data-stu-id="92c29-112">No matter what value is given to this attribute, the image cannot grow beyond its parent **VIEW** or **SUBVIEW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="92c29-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="92c29-113">Requirements</span></span>



| <span data-ttu-id="92c29-114">需求</span><span class="sxs-lookup"><span data-stu-id="92c29-114">Requirement</span></span> | <span data-ttu-id="92c29-115">值</span><span class="sxs-lookup"><span data-stu-id="92c29-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="92c29-116">版本</span><span class="sxs-lookup"><span data-stu-id="92c29-116">Version</span></span><br/> | <span data-ttu-id="92c29-117">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="92c29-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="92c29-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="92c29-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92c29-119">**環境屬性**</span><span class="sxs-lookup"><span data-stu-id="92c29-119">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





