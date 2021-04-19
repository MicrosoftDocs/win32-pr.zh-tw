---
title: CUSTOMSLIDER 影像
description: Image 屬性會指定或抓取檔案的名稱，其中包含對應至自訂滑杆之各種狀態的影像。
ms.assetid: 7db4f924-76af-4451-831c-1ed8ab1315ee
keywords:
- CUSTOMSLIDER Windows Media Player 映射
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f425ce138b2a11d2be834f39603ecc295c52c706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983940"
---
# <a name="customsliderimage"></a><span data-ttu-id="82fd6-104">CUSTOMSLIDER 影像</span><span class="sxs-lookup"><span data-stu-id="82fd6-104">CUSTOMSLIDER.image</span></span>

<span data-ttu-id="82fd6-105">**Image** 屬性會指定或抓取檔案的名稱，其中包含對應至自訂滑杆之各種狀態的影像。</span><span class="sxs-lookup"><span data-stu-id="82fd6-105">The **image** attribute specifies or retrieves the name of the file containing the images corresponding to the various states of the custom slider.</span></span>

``` syntax
        elementID.image
```

## <a name="possible-values"></a><span data-ttu-id="82fd6-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="82fd6-106">Possible Values</span></span>

<span data-ttu-id="82fd6-107">這個屬性是包含影像檔案名稱的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="82fd6-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="82fd6-108">備註</span><span class="sxs-lookup"><span data-stu-id="82fd6-108">Remarks</span></span>

<span data-ttu-id="82fd6-109">需要 **image** 屬性。</span><span class="sxs-lookup"><span data-stu-id="82fd6-109">The **image** attribute is required.</span></span> <span data-ttu-id="82fd6-110">它會指定包含一或多個子影像（以水準或垂直方式排列）的影像檔案，表示自訂滑杆的各種狀態。</span><span class="sxs-lookup"><span data-stu-id="82fd6-110">It specifies an image file that consists of one or more sub-images, arranged either horizontally or vertically, representing the various states of the custom slider.</span></span> <span data-ttu-id="82fd6-111">每個子影像都必須有與 **positionImage** 相同的維度，否則自訂滑杆將無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="82fd6-111">Each sub-image must have the same dimensions as the **positionImage** or the custom slider will not work correctly.</span></span> <span data-ttu-id="82fd6-112">因此，整體影像的高度或寬度必須是 **positionImage** 高度或寬度的偶數倍數。</span><span class="sxs-lookup"><span data-stu-id="82fd6-112">The height or width of the overall image must therefore be an even multiple of the height or width of the **positionImage**.</span></span>

<span data-ttu-id="82fd6-113">支援的影像檔案類型為 BMP、JPG、PNG 和 GIF (不包括動畫 Gif) 。</span><span class="sxs-lookup"><span data-stu-id="82fd6-113">The supported image file types are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="examples"></a><span data-ttu-id="82fd6-114">範例</span><span class="sxs-lookup"><span data-stu-id="82fd6-114">Examples</span></span>

<span data-ttu-id="82fd6-115">以下是自訂滑杆影像的範例。</span><span class="sxs-lookup"><span data-stu-id="82fd6-115">The following is an example of a custom slider image.</span></span> <span data-ttu-id="82fd6-116">對應的 **positionImage** 會顯示在 [ **positionImage** ] 屬性的 [範例] 區段中。</span><span class="sxs-lookup"><span data-stu-id="82fd6-116">The corresponding **positionImage** is shown in the example section of the **positionImage** property.</span></span>

![範例 customslider 影像](images/dial.png)

<span data-ttu-id="82fd6-118">**PositionImage** 屬性也包含程式碼範例，說明如何使用 **CUSTOMSLIDER** 元素的屬性。</span><span class="sxs-lookup"><span data-stu-id="82fd6-118">The **positionImage** attribute also contains a code sample illustrating how the attributes of the **CUSTOMSLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="82fd6-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="82fd6-119">Requirements</span></span>



| <span data-ttu-id="82fd6-120">需求</span><span class="sxs-lookup"><span data-stu-id="82fd6-120">Requirement</span></span> | <span data-ttu-id="82fd6-121">值</span><span class="sxs-lookup"><span data-stu-id="82fd6-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="82fd6-122">版本</span><span class="sxs-lookup"><span data-stu-id="82fd6-122">Version</span></span><br/> | <span data-ttu-id="82fd6-123">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="82fd6-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="82fd6-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82fd6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82fd6-125">**CUSTOMSLIDER 元素**</span><span class="sxs-lookup"><span data-stu-id="82fd6-125">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> <dt>

[<span data-ttu-id="82fd6-126">**CUSTOMSLIDER.positionImage**</span><span class="sxs-lookup"><span data-stu-id="82fd6-126">**CUSTOMSLIDER.positionImage**</span></span>](customslider-positionimage.md)
</dt> </dl>

 

 





