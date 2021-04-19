---
title: BUTTONGROUP. disabledImage
description: DisabledImage 屬性會指定或抓取影像的名稱，此影像代表 BUTTONGROUP 中按鈕的停用狀態。
ms.assetid: 34d4e6a9-de73-4dfa-9c23-4f17b55298f6
keywords:
- BUTTONGROUP. disabledImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9659c4d726313c0fb202a840e12891f00ad3fcf0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975964"
---
# <a name="buttongroupdisabledimage"></a><span data-ttu-id="ca79e-104">BUTTONGROUP. disabledImage</span><span class="sxs-lookup"><span data-stu-id="ca79e-104">BUTTONGROUP.disabledImage</span></span>

<span data-ttu-id="ca79e-105">**DisabledImage** 屬性會指定或抓取影像的名稱，此影像代表 **BUTTONGROUP** 中按鈕的停用狀態。</span><span class="sxs-lookup"><span data-stu-id="ca79e-105">The **disabledImage** attribute specifies or retrieves the name of the image representing the disabled state of the buttons in the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a><span data-ttu-id="ca79e-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="ca79e-106">Possible Values</span></span>

<span data-ttu-id="ca79e-107">此屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="ca79e-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca79e-108">備註</span><span class="sxs-lookup"><span data-stu-id="ca79e-108">Remarks</span></span>

<span data-ttu-id="ca79e-109">支援的影像格式為 BMP、JPG、PNG 和 GIF。</span><span class="sxs-lookup"><span data-stu-id="ca79e-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="ca79e-110">如果影像是8位的 BMP 檔案，則可以使用 **hueShift** 和 **飽和度** 屬性動態變更其色調和飽和度值。</span><span class="sxs-lookup"><span data-stu-id="ca79e-110">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="ca79e-111">當 **BUTTONELEMENT** 專案的 **disabled** 屬性設定為 true 時，會顯示 **BUTTONGROUP** 之 **disabledImage** 的對應區域。</span><span class="sxs-lookup"><span data-stu-id="ca79e-111">When the **disabled** attribute of a **BUTTONELEMENT** element is set to true, the corresponding region of the **disabledImage** for the **BUTTONGROUP** is displayed.</span></span> <span data-ttu-id="ca79e-112">如果停用的映射大於定義的區域，則會裁剪停用的映射。</span><span class="sxs-lookup"><span data-stu-id="ca79e-112">If the disabled image is larger than the defined region, the disabled image will be cropped.</span></span>

<span data-ttu-id="ca79e-113">如果無法抓取影像，則會顯示 (紅 x 影像) 的預設影像。</span><span class="sxs-lookup"><span data-stu-id="ca79e-113">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca79e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ca79e-114">Requirements</span></span>



| <span data-ttu-id="ca79e-115">需求</span><span class="sxs-lookup"><span data-stu-id="ca79e-115">Requirement</span></span> | <span data-ttu-id="ca79e-116">值</span><span class="sxs-lookup"><span data-stu-id="ca79e-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="ca79e-117">版本</span><span class="sxs-lookup"><span data-stu-id="ca79e-117">Version</span></span><br/> | <span data-ttu-id="ca79e-118">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="ca79e-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ca79e-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ca79e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca79e-120">**BUTTONGROUP 元素**</span><span class="sxs-lookup"><span data-stu-id="ca79e-120">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="ca79e-121">**BUTTONGROUP. hueShift**</span><span class="sxs-lookup"><span data-stu-id="ca79e-121">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="ca79e-122">**BUTTONGROUP 飽和度**</span><span class="sxs-lookup"><span data-stu-id="ca79e-122">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





