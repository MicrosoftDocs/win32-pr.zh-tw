---
title: BUTTONGROUP. downImage
description: DownImage 屬性會指定或抓取代表 BUTTONGROUP 關閉狀態之影像的名稱。
ms.assetid: 022e77e7-d3c0-41b5-984a-84d016a5a25a
keywords:
- BUTTONGROUP. downImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82b8a1d5bc2f4c68894a3bba1ad8ce9f2b3aa28a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001885"
---
# <a name="buttongroupdownimage"></a><span data-ttu-id="0c945-104">BUTTONGROUP. downImage</span><span class="sxs-lookup"><span data-stu-id="0c945-104">BUTTONGROUP.downImage</span></span>

<span data-ttu-id="0c945-105">**DownImage** 屬性會指定或抓取代表 **BUTTONGROUP** 關閉狀態之影像的名稱。</span><span class="sxs-lookup"><span data-stu-id="0c945-105">The **downImage** attribute specifies or retrieves the name of the image representing the down state of the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a><span data-ttu-id="0c945-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="0c945-106">Possible Values</span></span>

<span data-ttu-id="0c945-107">此屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="0c945-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c945-108">備註</span><span class="sxs-lookup"><span data-stu-id="0c945-108">Remarks</span></span>

<span data-ttu-id="0c945-109">支援的影像格式為 BMP、JPG、PNG 和 GIF。</span><span class="sxs-lookup"><span data-stu-id="0c945-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="0c945-110">如果影像是8位的 BMP 檔案，則可以使用 **hueShift** 和 **飽和度** 屬性動態變更其色調和飽和度值。</span><span class="sxs-lookup"><span data-stu-id="0c945-110">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="0c945-111">預設影像是在 **image** 屬性中指定的影像。</span><span class="sxs-lookup"><span data-stu-id="0c945-111">The default image is the one specified in the **image** attribute.</span></span>

<span data-ttu-id="0c945-112">如果向下影像大於定義的區域，則會裁剪下圖。</span><span class="sxs-lookup"><span data-stu-id="0c945-112">If the down image is larger than the defined region, the down image will be cropped.</span></span>

<span data-ttu-id="0c945-113">如果無法抓取影像，則會顯示 (紅 x 影像) 的預設影像。</span><span class="sxs-lookup"><span data-stu-id="0c945-113">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c945-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c945-114">Requirements</span></span>



| <span data-ttu-id="0c945-115">需求</span><span class="sxs-lookup"><span data-stu-id="0c945-115">Requirement</span></span> | <span data-ttu-id="0c945-116">值</span><span class="sxs-lookup"><span data-stu-id="0c945-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="0c945-117">版本</span><span class="sxs-lookup"><span data-stu-id="0c945-117">Version</span></span><br/> | <span data-ttu-id="0c945-118">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="0c945-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0c945-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c945-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c945-120">**BUTTONGROUP 元素**</span><span class="sxs-lookup"><span data-stu-id="0c945-120">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="0c945-121">**BUTTONGROUP. hueShift**</span><span class="sxs-lookup"><span data-stu-id="0c945-121">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="0c945-122">**BUTTONGROUP 影像**</span><span class="sxs-lookup"><span data-stu-id="0c945-122">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> <dt>

[<span data-ttu-id="0c945-123">**BUTTONGROUP 飽和度**</span><span class="sxs-lookup"><span data-stu-id="0c945-123">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





