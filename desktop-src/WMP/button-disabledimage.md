---
title: 按鈕. disabledImage
description: DisabledImage 屬性會指定或抓取在停用按鈕時所顯示的影像。
ms.assetid: b5654323-589a-45da-9534-6fa67c3a4c4b
keywords:
- DisabledImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eac407f6e7fbdd155f4bcabe98cecc0546f7d97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985960"
---
# <a name="buttondisabledimage"></a><span data-ttu-id="8f8df-104">按鈕. disabledImage</span><span class="sxs-lookup"><span data-stu-id="8f8df-104">BUTTON.disabledImage</span></span>

<span data-ttu-id="8f8df-105">**DisabledImage** 屬性會指定或抓取在停用 **按鈕** 時所顯示的影像。</span><span class="sxs-lookup"><span data-stu-id="8f8df-105">The **disabledImage** attribute specifies or retrieves the image that displays when the **BUTTON** is disabled.</span></span>

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a><span data-ttu-id="8f8df-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="8f8df-106">Possible Values</span></span>

<span data-ttu-id="8f8df-107">這個屬性是包含影像檔案名稱的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="8f8df-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f8df-108">備註</span><span class="sxs-lookup"><span data-stu-id="8f8df-108">Remarks</span></span>

<span data-ttu-id="8f8df-109">支援的影像格式為 BMP、JPG、PNG 和 GIF。</span><span class="sxs-lookup"><span data-stu-id="8f8df-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span>

<span data-ttu-id="8f8df-110">只要控制項的 [ **已停用** ] 屬性設定為 [true]，就會顯示此影像。</span><span class="sxs-lookup"><span data-stu-id="8f8df-110">This image will be displayed whenever the **disabled** attribute of the control is set to true.</span></span> <span data-ttu-id="8f8df-111">如果停用的映射大於定義的區域，則會裁剪停用的映射。</span><span class="sxs-lookup"><span data-stu-id="8f8df-111">If the disabled image is larger than the defined region, the disabled image will be cropped.</span></span>

<span data-ttu-id="8f8df-112">如果無法抓取影像，則會顯示 (紅 x 影像) 的預設影像。</span><span class="sxs-lookup"><span data-stu-id="8f8df-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f8df-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f8df-113">Requirements</span></span>



| <span data-ttu-id="8f8df-114">需求</span><span class="sxs-lookup"><span data-stu-id="8f8df-114">Requirement</span></span> | <span data-ttu-id="8f8df-115">值</span><span class="sxs-lookup"><span data-stu-id="8f8df-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="8f8df-116">版本</span><span class="sxs-lookup"><span data-stu-id="8f8df-116">Version</span></span><br/> | <span data-ttu-id="8f8df-117">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="8f8df-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8f8df-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f8df-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f8df-119">**BUTTON 元素**</span><span class="sxs-lookup"><span data-stu-id="8f8df-119">**BUTTON Element**</span></span>](button-element.md)
</dt> </dl>

 

 





