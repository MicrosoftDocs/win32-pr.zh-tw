---
title: CUSTOMSLIDER.downImage
description: DownImage 屬性會指定或抓取自訂滑杆的向下狀態影像。
ms.assetid: e1efe703-df0a-4ef9-92a9-c9cfb991ee37
keywords:
- CUSTOMSLIDER. downImage Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8365043654bc3cca9fbf79162302cf804155956d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981390"
---
# <a name="customsliderdownimage"></a><span data-ttu-id="aa7e8-104">CUSTOMSLIDER.downImage</span><span class="sxs-lookup"><span data-stu-id="aa7e8-104">CUSTOMSLIDER.downImage</span></span>

<span data-ttu-id="aa7e8-105">**DownImage** 屬性會指定或抓取自訂滑杆的向下狀態影像。</span><span class="sxs-lookup"><span data-stu-id="aa7e8-105">The **downImage** attribute specifies or retrieves the down state image of the custom slider.</span></span>

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a><span data-ttu-id="aa7e8-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="aa7e8-106">Possible Values</span></span>

<span data-ttu-id="aa7e8-107">這個屬性是包含影像檔案名稱的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="aa7e8-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa7e8-108">備註</span><span class="sxs-lookup"><span data-stu-id="aa7e8-108">Remarks</span></span>

<span data-ttu-id="aa7e8-109">此屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="aa7e8-109">This attribute is optional.</span></span> <span data-ttu-id="aa7e8-110">如果未指定，將會使用 **image** 屬性中指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="aa7e8-110">If it not specified, the file specified in the **image** attribute will be used.</span></span>

<span data-ttu-id="aa7e8-111">**DownImage** 代表 **CUSTOMSLIDER** 控制項的關閉狀態。</span><span class="sxs-lookup"><span data-stu-id="aa7e8-111">The **downImage** represents the down state of the **CUSTOMSLIDER** control.</span></span> <span data-ttu-id="aa7e8-112">它可以是單一影像或一系列的影像，代表滑杆的各種狀態。</span><span class="sxs-lookup"><span data-stu-id="aa7e8-112">It can be a single image or a series of images representing the various states of the slider.</span></span> <span data-ttu-id="aa7e8-113">如果使用多個映射，則會以與 **圖像** 檔相同的方式來排列它們。</span><span class="sxs-lookup"><span data-stu-id="aa7e8-113">If multiple images are used, they are arranged in the same way as the **image** file.</span></span>

<span data-ttu-id="aa7e8-114">支援的影像檔案類型為 BMP、JPG、PNG 和 GIF (不包括動畫 Gif) 。</span><span class="sxs-lookup"><span data-stu-id="aa7e8-114">The supported image file types are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa7e8-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa7e8-115">Requirements</span></span>



| <span data-ttu-id="aa7e8-116">需求</span><span class="sxs-lookup"><span data-stu-id="aa7e8-116">Requirement</span></span> | <span data-ttu-id="aa7e8-117">值</span><span class="sxs-lookup"><span data-stu-id="aa7e8-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="aa7e8-118">版本</span><span class="sxs-lookup"><span data-stu-id="aa7e8-118">Version</span></span><br/> | <span data-ttu-id="aa7e8-119">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="aa7e8-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aa7e8-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa7e8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa7e8-121">**CUSTOMSLIDER 元素**</span><span class="sxs-lookup"><span data-stu-id="aa7e8-121">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> <dt>

[<span data-ttu-id="aa7e8-122">**CUSTOMSLIDER 影像**</span><span class="sxs-lookup"><span data-stu-id="aa7e8-122">**CUSTOMSLIDER.image**</span></span>](customslider-image.md)
</dt> </dl>

 

 





