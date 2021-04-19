---
title: AmbientAttributes 高度
description: Height 屬性會指定或抓取控制項的高度。
ms.assetid: a5c85d86-15d4-451d-b8bc-ed3b6e0dfd7d
keywords:
- AmbientAttributes 高度 Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.height
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 662268bfeaf00b3185d531ff10d8dd17c9127a66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999661"
---
# <a name="ambientattributesheight"></a><span data-ttu-id="8c4e9-104">AmbientAttributes 高度</span><span class="sxs-lookup"><span data-stu-id="8c4e9-104">AmbientAttributes.height</span></span>

<span data-ttu-id="8c4e9-105">**Height** 屬性會指定或抓取控制項的高度。</span><span class="sxs-lookup"><span data-stu-id="8c4e9-105">The **height** attribute specifies or retrieves the height of the control.</span></span>

``` syntax
        elementID.height
```

## <a name="possible-values"></a><span data-ttu-id="8c4e9-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="8c4e9-106">Possible Values</span></span>

<span data-ttu-id="8c4e9-107">此屬性是讀取/寫入 **號碼** (**long**) 代表控制項的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="8c4e9-107">This attribute is a read/write **Number** (**long**) representing the height of the control in pixels.</span></span> <span data-ttu-id="8c4e9-108">預設值為零或控制項 **影像** 屬性中所指定影像的高度。</span><span class="sxs-lookup"><span data-stu-id="8c4e9-108">The default value is zero or the height of the image specified in the control's **image** attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c4e9-109">備註</span><span class="sxs-lookup"><span data-stu-id="8c4e9-109">Remarks</span></span>

<span data-ttu-id="8c4e9-110">如果指定的高度小於所提供影像的高度，則會裁剪影像。</span><span class="sxs-lookup"><span data-stu-id="8c4e9-110">If the height specified is smaller than the height of the image provided, then the image will be clipped.</span></span> <span data-ttu-id="8c4e9-111">如果高度大於影像的高度，則按一下區域會超出影像界限。</span><span class="sxs-lookup"><span data-stu-id="8c4e9-111">If the height is larger than the height of the image, then the click region will go beyond the image boundary.</span></span> <span data-ttu-id="8c4e9-112">無論這個屬性的值為何，影像都不能成長到其父視圖 **或子\*\*\*\*視圖** 之外。</span><span class="sxs-lookup"><span data-stu-id="8c4e9-112">No matter what value is given to this attribute, the image cannot grow beyond its parent **VIEW** or **SUBVIEW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c4e9-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c4e9-113">Requirements</span></span>



| <span data-ttu-id="8c4e9-114">需求</span><span class="sxs-lookup"><span data-stu-id="8c4e9-114">Requirement</span></span> | <span data-ttu-id="8c4e9-115">值</span><span class="sxs-lookup"><span data-stu-id="8c4e9-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="8c4e9-116">版本</span><span class="sxs-lookup"><span data-stu-id="8c4e9-116">Version</span></span><br/> | <span data-ttu-id="8c4e9-117">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="8c4e9-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8c4e9-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c4e9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c4e9-119">**環境屬性**</span><span class="sxs-lookup"><span data-stu-id="8c4e9-119">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





