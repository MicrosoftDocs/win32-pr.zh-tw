---
title: 滑杆. disabledImage
description: DisabledImage 屬性會指定或抓取滑杆控制項停用時使用的滑杆影像。
ms.assetid: b6c4237d-8eb0-44ce-a23f-9bdc5c21aca8
keywords:
- DisabledImage Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1b90dcbd551ca0f8bb332f858eac0b69c46733
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987048"
---
# <a name="sliderdisabledimage"></a><span data-ttu-id="a4dcf-104">滑杆. disabledImage</span><span class="sxs-lookup"><span data-stu-id="a4dcf-104">SLIDER.disabledImage</span></span>

<span data-ttu-id="a4dcf-105">**DisabledImage** 屬性會指定或抓取滑杆控制項停用時使用的滑杆影像。</span><span class="sxs-lookup"><span data-stu-id="a4dcf-105">The **disabledImage** attribute specifies or retrieves the image of the slider that is used when the slider control is disabled.</span></span>

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a><span data-ttu-id="a4dcf-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="a4dcf-106">Possible Values</span></span>

<span data-ttu-id="a4dcf-107">這個屬性是包含影像檔案名稱的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="a4dcf-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4dcf-108">備註</span><span class="sxs-lookup"><span data-stu-id="a4dcf-108">Remarks</span></span>

<span data-ttu-id="a4dcf-109">**DisabledImage** 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="a4dcf-109">The **disabledImage** is optional.</span></span> <span data-ttu-id="a4dcf-110">如果未提供，則會將 **backgroundImage** 用於所有停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="a4dcf-110">If it is not provided, the **backgroundImage** is used for all disabled states.</span></span> <span data-ttu-id="a4dcf-111">當滑杆控制項停用時，就不會顯示任何前景影像。</span><span class="sxs-lookup"><span data-stu-id="a4dcf-111">When a slider control is disabled, no foreground image is visible.</span></span>

<span data-ttu-id="a4dcf-112">支援的格式為 BMP、JPG、PNG 和 GIF (不包括動畫 Gif) 。</span><span class="sxs-lookup"><span data-stu-id="a4dcf-112">The supported formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4dcf-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4dcf-113">Requirements</span></span>



| <span data-ttu-id="a4dcf-114">需求</span><span class="sxs-lookup"><span data-stu-id="a4dcf-114">Requirement</span></span> | <span data-ttu-id="a4dcf-115">值</span><span class="sxs-lookup"><span data-stu-id="a4dcf-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="a4dcf-116">版本</span><span class="sxs-lookup"><span data-stu-id="a4dcf-116">Version</span></span><br/> | <span data-ttu-id="a4dcf-117">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="a4dcf-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a4dcf-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4dcf-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4dcf-119">**滑杆元素**</span><span class="sxs-lookup"><span data-stu-id="a4dcf-119">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="a4dcf-120">**滑杆. backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="a4dcf-120">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> </dl>

 

 





