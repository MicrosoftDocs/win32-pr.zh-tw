---
title: AmbientAttributes.nineGridMargins
description: NineGridMargins 屬性會指定面板元素之非統一縮放的邊界寬度。
ms.assetid: b8a7efd0-6c12-4436-9d53-0dcfa1600aa5
keywords:
- AmbientAttributes. nineGridMargins Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.nineGridMargins
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cf77c1fcfdb64fb9e4b0dde8753572255c17eda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999327"
---
# <a name="ambientattributesninegridmargins"></a><span data-ttu-id="0ff11-104">AmbientAttributes.nineGridMargins</span><span class="sxs-lookup"><span data-stu-id="0ff11-104">AmbientAttributes.nineGridMargins</span></span>

<span data-ttu-id="0ff11-105">**NineGridMargins** 屬性會指定面板元素之非統一縮放的邊界寬度。</span><span class="sxs-lookup"><span data-stu-id="0ff11-105">The **nineGridMargins** attribute specifies margin widths for non-uniform scaling of the skin element.</span></span>

``` syntax
        elementID.nineGridMargins
```

## <a name="possible-values"></a><span data-ttu-id="0ff11-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="0ff11-106">Possible Values</span></span>

<span data-ttu-id="0ff11-107">這個屬性是包含邊界寬度的讀取/寫入 **字串** ，格式為 "*widthLeft*，*widthTop*，*widthRight*，*widthBottom*"。</span><span class="sxs-lookup"><span data-stu-id="0ff11-107">This attribute is a read/write **String** that contains the widths of the margins in the form "*widthLeft*,*widthTop*,*widthRight*,*widthBottom*".</span></span> <span data-ttu-id="0ff11-108">每個寬度值都是一個數位，代表九個方格的邊界寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="0ff11-108">Each width value is a number representing the width, in pixels, of a margin for the nine grid.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ff11-109">備註</span><span class="sxs-lookup"><span data-stu-id="0ff11-109">Remarks</span></span>

<span data-ttu-id="0ff11-110">*九個方格* 是一種技術，用來將使用者介面元素分割成以 3 x 3 矩陣排列的九個矩形區域。</span><span class="sxs-lookup"><span data-stu-id="0ff11-110">A *nine grid* is a technique used to divide user interface elements into nine rectangular regions arranged in a 3 by 3 matrix.</span></span> <span data-ttu-id="0ff11-111">當專案調整大小時，九個方格區域可以依不同的因數進行調整。</span><span class="sxs-lookup"><span data-stu-id="0ff11-111">When an element is resized, the nine grid regions can each scale by a different factor.</span></span>

<span data-ttu-id="0ff11-112">您指定的四個寬度值都代表三個相鄰區域中資料列或資料行的寬度。</span><span class="sxs-lookup"><span data-stu-id="0ff11-112">Each of the four width values you specify represents the width of a row or column of three adjacent regions.</span></span> <span data-ttu-id="0ff11-113">每個資料列或資料行會形成九個方格的左邊、右上角或底部。</span><span class="sxs-lookup"><span data-stu-id="0ff11-113">Each row or column forms the left side, top, right side, or bottom of the nine grid.</span></span>

<span data-ttu-id="0ff11-114">[AmbientAttributes](ambientattributes-resizeimages.md) 必須設定為 true，此屬性才能運作。</span><span class="sxs-lookup"><span data-stu-id="0ff11-114">[AmbientAttributes.resizeImages](ambientattributes-resizeimages.md) must be set to true for this attribute to work.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ff11-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ff11-115">Requirements</span></span>



| <span data-ttu-id="0ff11-116">需求</span><span class="sxs-lookup"><span data-stu-id="0ff11-116">Requirement</span></span> | <span data-ttu-id="0ff11-117">值</span><span class="sxs-lookup"><span data-stu-id="0ff11-117">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="0ff11-118">版本</span><span class="sxs-lookup"><span data-stu-id="0ff11-118">Version</span></span><br/> | <span data-ttu-id="0ff11-119">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="0ff11-119">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0ff11-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ff11-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ff11-121">**環境屬性**</span><span class="sxs-lookup"><span data-stu-id="0ff11-121">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





