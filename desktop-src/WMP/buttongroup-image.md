---
title: BUTTONGROUP 影像
description: Image 屬性會指定或抓取代表 BUTTONGROUP 按鈕的影像名稱。
ms.assetid: dad50a1e-d147-4e0f-b5d6-8cbfeef32438
keywords:
- BUTTONGROUP Windows Media Player 映射
topic_type:
- apiref
api_name:
- BUTTONGROUP.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fa395edc149671ad05a38a5ff7c77053b6e3d82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999485"
---
# <a name="buttongroupimage"></a><span data-ttu-id="4ad20-104">BUTTONGROUP 影像</span><span class="sxs-lookup"><span data-stu-id="4ad20-104">BUTTONGROUP.image</span></span>

<span data-ttu-id="4ad20-105">**Image** 屬性會指定或抓取代表 **BUTTONGROUP** 按鈕的影像名稱。</span><span class="sxs-lookup"><span data-stu-id="4ad20-105">The **image** attribute specifies or retrieves the name of the image representing the buttons of a **BUTTONGROUP**.</span></span>

``` syntax
        elementID.image
```

## <a name="possible-values"></a><span data-ttu-id="4ad20-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="4ad20-106">Possible Values</span></span>

<span data-ttu-id="4ad20-107">此屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="4ad20-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ad20-108">備註</span><span class="sxs-lookup"><span data-stu-id="4ad20-108">Remarks</span></span>

<span data-ttu-id="4ad20-109">支援的影像格式為 BMP、JPG、PNG 和 GIF。</span><span class="sxs-lookup"><span data-stu-id="4ad20-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="4ad20-110">如果影像是8位的 BMP 檔案，則可以使用 **hueShift** 和 **飽和度** 屬性動態變更其色調和飽和度值。</span><span class="sxs-lookup"><span data-stu-id="4ad20-110">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="4ad20-111">如果控制項的影像大於定義的區域，則會裁剪影像。</span><span class="sxs-lookup"><span data-stu-id="4ad20-111">If the image of the control is larger than the defined region, the image will be cropped.</span></span>

<span data-ttu-id="4ad20-112">如果無法抓取影像，則會顯示 (紅 x 影像) 的預設影像。</span><span class="sxs-lookup"><span data-stu-id="4ad20-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ad20-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ad20-113">Requirements</span></span>



| <span data-ttu-id="4ad20-114">需求</span><span class="sxs-lookup"><span data-stu-id="4ad20-114">Requirement</span></span> | <span data-ttu-id="4ad20-115">值</span><span class="sxs-lookup"><span data-stu-id="4ad20-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="4ad20-116">版本</span><span class="sxs-lookup"><span data-stu-id="4ad20-116">Version</span></span><br/> | <span data-ttu-id="4ad20-117">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="4ad20-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4ad20-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ad20-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ad20-119">**BUTTONGROUP 元素**</span><span class="sxs-lookup"><span data-stu-id="4ad20-119">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="4ad20-120">**BUTTONGROUP. hueShift**</span><span class="sxs-lookup"><span data-stu-id="4ad20-120">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="4ad20-121">**BUTTONGROUP 飽和度**</span><span class="sxs-lookup"><span data-stu-id="4ad20-121">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





