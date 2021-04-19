---
title: 按鈕. downImage
description: DownImage 屬性會指定或抓取代表按鈕關閉狀態的影像。
ms.assetid: 18149668-5be6-4b64-8adf-8904585ff0be
keywords:
- DownImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7a405a5df20a04ae9d093f2b28ee4c68cab67d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982075"
---
# <a name="buttondownimage"></a><span data-ttu-id="5827f-104">按鈕. downImage</span><span class="sxs-lookup"><span data-stu-id="5827f-104">BUTTON.downImage</span></span>

<span data-ttu-id="5827f-105">**DownImage** 屬性會指定或抓取代表 **按鈕** 關閉狀態的影像。</span><span class="sxs-lookup"><span data-stu-id="5827f-105">The **downImage** attribute specifies or retrieves the image representing the down state of the **BUTTON**.</span></span>

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a><span data-ttu-id="5827f-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="5827f-106">Possible Values</span></span>

<span data-ttu-id="5827f-107">這個屬性是包含影像檔案名稱的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="5827f-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="5827f-108">備註</span><span class="sxs-lookup"><span data-stu-id="5827f-108">Remarks</span></span>

<span data-ttu-id="5827f-109">支援的影像格式為 BMP、JPG、PNG 和 GIF。</span><span class="sxs-lookup"><span data-stu-id="5827f-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span>

<span data-ttu-id="5827f-110">預設影像是 **image** 屬性中指定的影像或其預設值。</span><span class="sxs-lookup"><span data-stu-id="5827f-110">The default image is the one specified in the **image** attribute, or its default.</span></span>

<span data-ttu-id="5827f-111">如果下圖大於環境屬性中定義的區域，則會裁剪下圖。</span><span class="sxs-lookup"><span data-stu-id="5827f-111">If the down image is larger than the defined region in the ambient attribute, the down image will be cropped.</span></span>

<span data-ttu-id="5827f-112">如果無法抓取影像，則會顯示 (紅 x 影像) 的預設影像。</span><span class="sxs-lookup"><span data-stu-id="5827f-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="5827f-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="5827f-113">Requirements</span></span>



| <span data-ttu-id="5827f-114">需求</span><span class="sxs-lookup"><span data-stu-id="5827f-114">Requirement</span></span> | <span data-ttu-id="5827f-115">值</span><span class="sxs-lookup"><span data-stu-id="5827f-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="5827f-116">版本</span><span class="sxs-lookup"><span data-stu-id="5827f-116">Version</span></span><br/> | <span data-ttu-id="5827f-117">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="5827f-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5827f-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5827f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5827f-119">**BUTTON 元素**</span><span class="sxs-lookup"><span data-stu-id="5827f-119">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="5827f-120">**按鈕。向下鍵**</span><span class="sxs-lookup"><span data-stu-id="5827f-120">**BUTTON.down**</span></span>](button-down.md)
</dt> <dt>

[<span data-ttu-id="5827f-121">**按鈕。影像**</span><span class="sxs-lookup"><span data-stu-id="5827f-121">**BUTTON.image**</span></span>](button-image.md)
</dt> </dl>

 

 





