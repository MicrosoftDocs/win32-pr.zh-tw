---
title: BackgroundColor
description: BackgroundColor 屬性會指定或抓取影片控制項的背景色彩。
ms.assetid: 7acf7dc8-80c3-4620-ad89-4c8de20d17ee
keywords:
- BackgroundColor Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 992ffd881498c3670eaaf5c075db9c6432cc1496
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990662"
---
# <a name="videobackgroundcolor"></a><span data-ttu-id="9a7be-104">BackgroundColor</span><span class="sxs-lookup"><span data-stu-id="9a7be-104">VIDEO.backgroundColor</span></span>

<span data-ttu-id="9a7be-105">**BackgroundColor** 屬性會指定或抓取影片控制項的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="9a7be-105">The **backgroundColor** attribute specifies or retrieves the background color of the Video control.</span></span>

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a><span data-ttu-id="9a7be-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="9a7be-106">Possible Values</span></span>

<span data-ttu-id="9a7be-107">這個屬性是包含任何 Microsoft Internet Explorer 色彩值或值為 "none" 的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="9a7be-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value or the value "none".</span></span> <span data-ttu-id="9a7be-108">預設值為 "none"，這表示如果沒有影片與影片控制項相關聯的影片，則影片控制項是透明的，而背景會顯示。</span><span class="sxs-lookup"><span data-stu-id="9a7be-108">It has a default value of "none", which means that if there is no video associated with the video control, the Video control is transparent and the background shows through.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a7be-109">備註</span><span class="sxs-lookup"><span data-stu-id="9a7be-109">Remarks</span></span>

<span data-ttu-id="9a7be-110">當影片小於視窗而 **stretchToFit** 為 false 時，背景色彩會顯示在影片周圍。</span><span class="sxs-lookup"><span data-stu-id="9a7be-110">When the video is smaller than the window and **stretchToFit** is false, the background color appears around the video.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a7be-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a7be-111">Requirements</span></span>



| <span data-ttu-id="9a7be-112">需求</span><span class="sxs-lookup"><span data-stu-id="9a7be-112">Requirement</span></span> | <span data-ttu-id="9a7be-113">值</span><span class="sxs-lookup"><span data-stu-id="9a7be-113">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="9a7be-114">版本</span><span class="sxs-lookup"><span data-stu-id="9a7be-114">Version</span></span><br/> | <span data-ttu-id="9a7be-115">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="9a7be-115">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9a7be-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a7be-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a7be-117">**色彩參考**</span><span class="sxs-lookup"><span data-stu-id="9a7be-117">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="9a7be-118">**影片元素**</span><span class="sxs-lookup"><span data-stu-id="9a7be-118">**VIDEO Element**</span></span>](video-element.md)
</dt> <dt>

[<span data-ttu-id="9a7be-119">**StretchToFit**</span><span class="sxs-lookup"><span data-stu-id="9a7be-119">**VIDEO.stretchToFit**</span></span>](video-stretchtofit.md)
</dt> </dl>

 

 





