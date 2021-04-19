---
title: BackgroundImage
description: BackgroundImage 屬性會指定或抓取 VIEW 或子視圖的背景影像。
ms.assetid: 60ffb257-2f43-4ae3-869d-3eb981ef4ae7
keywords:
- BackgroundImage Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e96f4a93882e02589d7f15b74ba5cb225f506d69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985553"
---
# <a name="viewbackgroundimage"></a><span data-ttu-id="0e90b-104">BackgroundImage</span><span class="sxs-lookup"><span data-stu-id="0e90b-104">VIEW.backgroundImage</span></span>

<span data-ttu-id="0e90b-105">**BackgroundImage** 屬性會指定或抓取 **VIEW** 或子視圖的背景影像 **。**</span><span class="sxs-lookup"><span data-stu-id="0e90b-105">The **backgroundImage** attribute specifies or retrieves the background image of the **VIEW** or **SUBVIEW**.</span></span>

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a><span data-ttu-id="0e90b-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="0e90b-106">Possible Values</span></span>

<span data-ttu-id="0e90b-107">此屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="0e90b-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e90b-108">備註</span><span class="sxs-lookup"><span data-stu-id="0e90b-108">Remarks</span></span>

<span data-ttu-id="0e90b-109">支援的格式為 BMP、JPG、GIF 和 PNG。</span><span class="sxs-lookup"><span data-stu-id="0e90b-109">The supported formats are BMP, JPG, GIF, and PNG.</span></span> <span data-ttu-id="0e90b-110">如果影像是8位的 BMP 檔案，則可以使用 **backgroundImageHueShift** 和 **backgroundImageSaturation** 屬性動態變更其色調和飽和度值。</span><span class="sxs-lookup"><span data-stu-id="0e90b-110">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **backgroundImageHueShift** and **backgroundImageSaturation** attributes.</span></span>

<span data-ttu-id="0e90b-111">在 Windows Media 下載封裝中，如果您為 **VIEW** 元素指定 **backgroundImage** 屬性，則還必須指定該元素的 **backgroundColor** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0e90b-111">In a Windows Media Download package, if you specify the **backgroundImage** attribute for a **VIEW** element, then you must also specify the **backgroundColor** attribute for that element.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e90b-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e90b-112">Requirements</span></span>



| <span data-ttu-id="0e90b-113">需求</span><span class="sxs-lookup"><span data-stu-id="0e90b-113">Requirement</span></span> | <span data-ttu-id="0e90b-114">值</span><span class="sxs-lookup"><span data-stu-id="0e90b-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="0e90b-115">版本</span><span class="sxs-lookup"><span data-stu-id="0e90b-115">Version</span></span><br/> | <span data-ttu-id="0e90b-116">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="0e90b-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0e90b-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e90b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e90b-118">**VIEW 元素**</span><span class="sxs-lookup"><span data-stu-id="0e90b-118">**VIEW Element**</span></span>](view-element.md)
</dt> <dt>

[<span data-ttu-id="0e90b-119">**BackgroundImageHueShift**</span><span class="sxs-lookup"><span data-stu-id="0e90b-119">**VIEW.backgroundImageHueShift**</span></span>](view-backgroundimagehueshift.md)
</dt> <dt>

[<span data-ttu-id="0e90b-120">**BackgroundImageSaturation**</span><span class="sxs-lookup"><span data-stu-id="0e90b-120">**VIEW.backgroundImageSaturation**</span></span>](view-backgroundimagesaturation.md)
</dt> </dl>

 

 





