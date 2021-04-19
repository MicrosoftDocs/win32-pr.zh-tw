---
title: 按鈕. hoverImage
description: HoverImage 屬性會指定或抓取按鈕處於啟動狀態時所顯示的影像，並使用滑鼠指標將滑鼠停留在其上方。
ms.assetid: 6704e63d-1def-4e8e-808f-131c3cc1c0de
keywords:
- HoverImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80b17a461ffde4b9f6777f3ce360c6b3f1747235
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995208"
---
# <a name="buttonhoverimage"></a><span data-ttu-id="fc1cf-104">按鈕. hoverImage</span><span class="sxs-lookup"><span data-stu-id="fc1cf-104">BUTTON.hoverImage</span></span>

<span data-ttu-id="fc1cf-105">**HoverImage** 屬性會指定或抓取 **按鈕** 處於啟動狀態時所顯示的影像，並使用滑鼠指標將滑鼠停留在其上方。</span><span class="sxs-lookup"><span data-stu-id="fc1cf-105">The **hoverImage** attribute specifies or retrieves the image displayed when the **BUTTON** is in the up state and the user hovers over it with the mouse pointer.</span></span>

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a><span data-ttu-id="fc1cf-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="fc1cf-106">Possible Values</span></span>

<span data-ttu-id="fc1cf-107">這個屬性是包含影像檔案名稱的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="fc1cf-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc1cf-108">備註</span><span class="sxs-lookup"><span data-stu-id="fc1cf-108">Remarks</span></span>

<span data-ttu-id="fc1cf-109">支援的影像格式為 BMP、JPG、PNG 和 GIF。</span><span class="sxs-lookup"><span data-stu-id="fc1cf-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span>

<span data-ttu-id="fc1cf-110">預設影像是 **image** 屬性中指定的影像或其預設值。</span><span class="sxs-lookup"><span data-stu-id="fc1cf-110">The default image is the one specified in the **image** attribute, or its default.</span></span>

<span data-ttu-id="fc1cf-111">如果暫留影像大於環境屬性中定義的區域，則會裁剪停留影像。</span><span class="sxs-lookup"><span data-stu-id="fc1cf-111">If the hover image is larger than the defined region in the ambient attribute, the hover image will be cropped.</span></span>

<span data-ttu-id="fc1cf-112">如果無法抓取影像，則會顯示 (紅 x 影像) 的預設影像。</span><span class="sxs-lookup"><span data-stu-id="fc1cf-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc1cf-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc1cf-113">Requirements</span></span>



| <span data-ttu-id="fc1cf-114">需求</span><span class="sxs-lookup"><span data-stu-id="fc1cf-114">Requirement</span></span> | <span data-ttu-id="fc1cf-115">值</span><span class="sxs-lookup"><span data-stu-id="fc1cf-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="fc1cf-116">版本</span><span class="sxs-lookup"><span data-stu-id="fc1cf-116">Version</span></span><br/> | <span data-ttu-id="fc1cf-117">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="fc1cf-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fc1cf-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc1cf-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc1cf-119">**BUTTON 元素**</span><span class="sxs-lookup"><span data-stu-id="fc1cf-119">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="fc1cf-120">**按鈕。影像**</span><span class="sxs-lookup"><span data-stu-id="fc1cf-120">**BUTTON.image**</span></span>](button-image.md)
</dt> </dl>

 

 





