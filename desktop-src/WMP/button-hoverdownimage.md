---
title: 按鈕. hoverDownImage
description: HoverDownImage 屬性會指定或抓取按鈕處於關閉狀態時所顯示的影像，並使用滑鼠指標將滑鼠停留在其上方。
ms.assetid: 06645307-50f1-400d-aa73-c48d0fba3ee1
keywords:
- HoverDownImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bc8221875656c38a35eb6539dce25f58133984f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992822"
---
# <a name="buttonhoverdownimage"></a><span data-ttu-id="8aa12-104">按鈕. hoverDownImage</span><span class="sxs-lookup"><span data-stu-id="8aa12-104">BUTTON.hoverDownImage</span></span>

<span data-ttu-id="8aa12-105">**HoverDownImage** 屬性會指定或抓取 **按鈕** 處於關閉狀態時所顯示的影像，並使用滑鼠指標將滑鼠停留在其上方。</span><span class="sxs-lookup"><span data-stu-id="8aa12-105">The **hoverDownImage** attribute specifies or retrieves the image displayed when the **BUTTON** is in the down state and the user hovers over it with the mouse pointer.</span></span>

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a><span data-ttu-id="8aa12-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="8aa12-106">Possible Values</span></span>

<span data-ttu-id="8aa12-107">這個屬性是包含影像檔案名稱的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="8aa12-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="8aa12-108">備註</span><span class="sxs-lookup"><span data-stu-id="8aa12-108">Remarks</span></span>

<span data-ttu-id="8aa12-109">支援的影像格式為 BMP、JPG、PNG 和 GIF。</span><span class="sxs-lookup"><span data-stu-id="8aa12-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span>

<span data-ttu-id="8aa12-110">預設影像是 **downImage** 屬性中指定的影像，或其預設值。</span><span class="sxs-lookup"><span data-stu-id="8aa12-110">The default image is the one specified in the **downImage** attribute, or its default.</span></span>

<span data-ttu-id="8aa12-111">如果暫止的影像大於環境屬性中定義的區域，則會裁剪暫止的影像。</span><span class="sxs-lookup"><span data-stu-id="8aa12-111">If the hover-down image is larger than the defined region in the ambient attribute, the hover-down image will be cropped.</span></span>

<span data-ttu-id="8aa12-112">如果無法抓取影像，則會顯示 (紅 x 影像) 的預設影像。</span><span class="sxs-lookup"><span data-stu-id="8aa12-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="8aa12-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="8aa12-113">Requirements</span></span>



| <span data-ttu-id="8aa12-114">需求</span><span class="sxs-lookup"><span data-stu-id="8aa12-114">Requirement</span></span> | <span data-ttu-id="8aa12-115">值</span><span class="sxs-lookup"><span data-stu-id="8aa12-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="8aa12-116">版本</span><span class="sxs-lookup"><span data-stu-id="8aa12-116">Version</span></span><br/> | <span data-ttu-id="8aa12-117">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="8aa12-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8aa12-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8aa12-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8aa12-119">**BUTTON 元素**</span><span class="sxs-lookup"><span data-stu-id="8aa12-119">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="8aa12-120">**按鈕. downImage**</span><span class="sxs-lookup"><span data-stu-id="8aa12-120">**BUTTON.downImage**</span></span>](button-downimage.md)
</dt> </dl>

 

 





