---
title: 按鈕。影像
description: Image 屬性會指定或抓取按鈕的預設影像。
ms.assetid: d0d97f14-2c4d-4769-b45c-c6cde7282bea
keywords:
- 按鈕。影像 Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d27363383d72110ebe7b3e94187013ab701a6a3c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980176"
---
# <a name="buttonimage"></a><span data-ttu-id="bd715-104">按鈕。影像</span><span class="sxs-lookup"><span data-stu-id="bd715-104">BUTTON.image</span></span>

<span data-ttu-id="bd715-105">**Image** 屬性會指定或抓取 **按鈕** 的預設影像。</span><span class="sxs-lookup"><span data-stu-id="bd715-105">The **image** attribute specifies or retrieves the default image of the **BUTTON**.</span></span>

``` syntax
        elementID.image
```

## <a name="possible-values"></a><span data-ttu-id="bd715-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="bd715-106">Possible Values</span></span>

<span data-ttu-id="bd715-107">這個屬性是包含影像檔案名稱的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="bd715-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd715-108">備註</span><span class="sxs-lookup"><span data-stu-id="bd715-108">Remarks</span></span>

<span data-ttu-id="bd715-109">支援的影像格式為 BMP、JPG、PNG 和 GIF (包括動畫 Gif) 。</span><span class="sxs-lookup"><span data-stu-id="bd715-109">The supported image formats are BMP, JPG, PNG, and GIF (including animated GIFs).</span></span>

<span data-ttu-id="bd715-110">如果 **按鈕** 影像大於 [ **寬度** ] 和 [ **高度** ] 屬性所定義的區域，則會裁剪影像。</span><span class="sxs-lookup"><span data-stu-id="bd715-110">If the **BUTTON** image is larger than the region defined by the **width** and **height** attributes, the image will be cropped.</span></span>

<span data-ttu-id="bd715-111">如果未指定影像，但 **高度** 和 **寬度** 為，則會顯示直接在此控制項後方的影像。</span><span class="sxs-lookup"><span data-stu-id="bd715-111">If the image is not specified but the **height** and **width** are, then the image directly behind this control is displayed.</span></span> <span data-ttu-id="bd715-112">這有助於在 **視圖** 本身繪製影像，減少所需的個別影像檔案數目。</span><span class="sxs-lookup"><span data-stu-id="bd715-112">This can facilitate drawing the image on the **VIEW** itself, reducing the number of separate image files needed.</span></span>

<span data-ttu-id="bd715-113">如果無法抓取影像，則會顯示 (紅 x 影像) 的預設影像。</span><span class="sxs-lookup"><span data-stu-id="bd715-113">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd715-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd715-114">Requirements</span></span>



| <span data-ttu-id="bd715-115">需求</span><span class="sxs-lookup"><span data-stu-id="bd715-115">Requirement</span></span> | <span data-ttu-id="bd715-116">值</span><span class="sxs-lookup"><span data-stu-id="bd715-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="bd715-117">版本</span><span class="sxs-lookup"><span data-stu-id="bd715-117">Version</span></span><br/> | <span data-ttu-id="bd715-118">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="bd715-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bd715-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd715-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd715-120">**BUTTON 元素**</span><span class="sxs-lookup"><span data-stu-id="bd715-120">**BUTTON Element**</span></span>](button-element.md)
</dt> </dl>

 

 





