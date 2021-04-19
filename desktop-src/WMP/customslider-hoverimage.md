---
title: CUSTOMSLIDER.hoverImage
description: 當滑鼠停留在自訂滑杆上時，hoverImage 屬性會指定或抓取顯示的影像。
ms.assetid: b5d10289-280c-4578-83e8-6259249ff448
keywords:
- CUSTOMSLIDER. hoverImage Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 361f7d903b6231e92f331ab38a3a9f51bc3ec679
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978457"
---
# <a name="customsliderhoverimage"></a><span data-ttu-id="6cbb2-104">CUSTOMSLIDER.hoverImage</span><span class="sxs-lookup"><span data-stu-id="6cbb2-104">CUSTOMSLIDER.hoverImage</span></span>

<span data-ttu-id="6cbb2-105">當滑鼠停留在自訂滑杆上時， **hoverImage** 屬性會指定或抓取顯示的影像。</span><span class="sxs-lookup"><span data-stu-id="6cbb2-105">The **hoverImage** attribute specifies or retrieves the image that appears when the mouse is over the custom slider.</span></span>

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a><span data-ttu-id="6cbb2-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="6cbb2-106">Possible Values</span></span>

<span data-ttu-id="6cbb2-107">這個屬性是包含影像檔案名稱的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="6cbb2-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cbb2-108">備註</span><span class="sxs-lookup"><span data-stu-id="6cbb2-108">Remarks</span></span>

<span data-ttu-id="6cbb2-109">此屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="6cbb2-109">This attribute is optional.</span></span> <span data-ttu-id="6cbb2-110">如果未指定，將會使用 **image** 屬性中指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="6cbb2-110">If it not specified, the file specified in the **image** attribute will be used.</span></span>

<span data-ttu-id="6cbb2-111">**HoverImage** 代表 CUSTOMSLIDER 控制項的停留狀態;也就是滑鼠游標停留在其上方時所顯示的狀態。</span><span class="sxs-lookup"><span data-stu-id="6cbb2-111">The **hoverImage** represents the hover state of the CUSTOMSLIDER control; that is, the state that is shown when the mouse cursor hovers over it.</span></span> <span data-ttu-id="6cbb2-112">它可以是單一影像或一系列的影像，代表滑杆的各種狀態。</span><span class="sxs-lookup"><span data-stu-id="6cbb2-112">It can be a single image or a series of images representing the various states of the slider.</span></span> <span data-ttu-id="6cbb2-113">如果使用多個映射，則會以與 **圖像** 檔相同的方式來排列它們</span><span class="sxs-lookup"><span data-stu-id="6cbb2-113">If multiple images are used, they are arranged in the same way as the **image** file</span></span>

<span data-ttu-id="6cbb2-114">支援的影像檔案類型為 BMP、JPG、PNG 和 GIF (不包括動畫 Gif) 。</span><span class="sxs-lookup"><span data-stu-id="6cbb2-114">The supported image file types are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="requirements"></a><span data-ttu-id="6cbb2-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="6cbb2-115">Requirements</span></span>



| <span data-ttu-id="6cbb2-116">需求</span><span class="sxs-lookup"><span data-stu-id="6cbb2-116">Requirement</span></span> | <span data-ttu-id="6cbb2-117">值</span><span class="sxs-lookup"><span data-stu-id="6cbb2-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="6cbb2-118">版本</span><span class="sxs-lookup"><span data-stu-id="6cbb2-118">Version</span></span><br/> | <span data-ttu-id="6cbb2-119">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="6cbb2-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6cbb2-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6cbb2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cbb2-121">**CUSTOMSLIDER 元素**</span><span class="sxs-lookup"><span data-stu-id="6cbb2-121">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> <dt>

[<span data-ttu-id="6cbb2-122">**CUSTOMSLIDER 影像**</span><span class="sxs-lookup"><span data-stu-id="6cbb2-122">**CUSTOMSLIDER.image**</span></span>](customslider-image.md)
</dt> </dl>

 

 





