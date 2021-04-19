---
title: BUTTONGROUP. hoverDownImage
description: HoverDownImage 屬性會指定或抓取影像的名稱，代表 BUTTONGROUP 中按鈕的暫止狀態。 當按鈕處於關閉狀態，且使用者將滑鼠停留在該按鈕上方時，就會出現暫止狀態。
ms.assetid: dc048303-21d1-40ba-99bb-8d1c2f46628b
keywords:
- BUTTONGROUP. hoverDownImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a40788fafffd6eb4626bc834a941f7330c988fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989242"
---
# <a name="buttongrouphoverdownimage"></a><span data-ttu-id="358ce-105">BUTTONGROUP. hoverDownImage</span><span class="sxs-lookup"><span data-stu-id="358ce-105">BUTTONGROUP.hoverDownImage</span></span>

<span data-ttu-id="358ce-106">**HoverDownImage** 屬性會指定或抓取影像的名稱，代表 **BUTTONGROUP** 中按鈕的暫止狀態。</span><span class="sxs-lookup"><span data-stu-id="358ce-106">The **hoverDownImage** attribute specifies or retrieves the name of the image representing the hover-down state of a button in the **BUTTONGROUP**.</span></span> <span data-ttu-id="358ce-107">當按鈕處於關閉狀態，且使用者將滑鼠停留在該按鈕上方時，就會出現暫止狀態。</span><span class="sxs-lookup"><span data-stu-id="358ce-107">The hover-down state occurs when the button is in the down state and the user hovers over it with the mouse.</span></span>

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a><span data-ttu-id="358ce-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="358ce-108">Possible Values</span></span>

<span data-ttu-id="358ce-109">此屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="358ce-109">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="358ce-110">備註</span><span class="sxs-lookup"><span data-stu-id="358ce-110">Remarks</span></span>

<span data-ttu-id="358ce-111">支援的影像格式為 BMP、JPG、PNG 和 GIF。</span><span class="sxs-lookup"><span data-stu-id="358ce-111">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="358ce-112">如果影像是8位的 BMP 檔案，則可以使用 **hueShift** 和 **飽和度** 屬性動態變更其色調和飽和度值。</span><span class="sxs-lookup"><span data-stu-id="358ce-112">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="358ce-113">預設影像是 **downImage** 屬性中指定的影像，或其預設值。</span><span class="sxs-lookup"><span data-stu-id="358ce-113">The default image is the one specified in the **downImage** attribute, or its default.</span></span>

<span data-ttu-id="358ce-114">如果暫留的影像大於所定義的區域，則會裁剪停留影像。</span><span class="sxs-lookup"><span data-stu-id="358ce-114">If the hover-down image is larger than the defined region, the hover-down image will be cropped.</span></span>

<span data-ttu-id="358ce-115">如果無法抓取影像，則會顯示 (紅 x 影像) 的預設影像。</span><span class="sxs-lookup"><span data-stu-id="358ce-115">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="358ce-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="358ce-116">Requirements</span></span>



| <span data-ttu-id="358ce-117">需求</span><span class="sxs-lookup"><span data-stu-id="358ce-117">Requirement</span></span> | <span data-ttu-id="358ce-118">值</span><span class="sxs-lookup"><span data-stu-id="358ce-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="358ce-119">版本</span><span class="sxs-lookup"><span data-stu-id="358ce-119">Version</span></span><br/> | <span data-ttu-id="358ce-120">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="358ce-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="358ce-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="358ce-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="358ce-122">**BUTTONGROUP 元素**</span><span class="sxs-lookup"><span data-stu-id="358ce-122">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="358ce-123">**BUTTONGROUP. downImage**</span><span class="sxs-lookup"><span data-stu-id="358ce-123">**BUTTONGROUP.downImage**</span></span>](buttongroup-downimage.md)
</dt> <dt>

[<span data-ttu-id="358ce-124">**BUTTONGROUP. hueShift**</span><span class="sxs-lookup"><span data-stu-id="358ce-124">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="358ce-125">**BUTTONGROUP 飽和度**</span><span class="sxs-lookup"><span data-stu-id="358ce-125">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





