---
title: BackgroundColor
description: BackgroundColor 屬性會指定或抓取視圖或子視圖的背景色彩。
ms.assetid: 02804e03-3518-4825-8ad0-bf91f74b5f74
keywords:
- BackgroundColor Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73bbee10c6f442c9c03f46baa26251a7f6f85c22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989733"
---
# <a name="viewbackgroundcolor"></a><span data-ttu-id="010fb-104">BackgroundColor</span><span class="sxs-lookup"><span data-stu-id="010fb-104">VIEW.backgroundColor</span></span>

<span data-ttu-id="010fb-105">**BackgroundColor** 屬性會指定或抓取 **視圖** 或子視圖的背景色彩 **。**</span><span class="sxs-lookup"><span data-stu-id="010fb-105">The **backgroundColor** attribute specifies or retrieves the background color of the **VIEW** or **SUBVIEW**.</span></span>

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a><span data-ttu-id="010fb-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="010fb-106">Possible Values</span></span>

<span data-ttu-id="010fb-107">這個屬性是包含任何 Microsoft Internet Explorer 色彩值或值為 "none" 的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="010fb-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value or the value "none".</span></span> <span data-ttu-id="010fb-108">針對 **VIEW** 專案，其預設值為 "白色"，子視圖專案的預設 **值為 "** none"。</span><span class="sxs-lookup"><span data-stu-id="010fb-108">It has a default value of "white" for **VIEW** elements or "none" for **SUBVIEW** elements.</span></span>

<span data-ttu-id="010fb-109">在 Windows Media 下載封裝中，如果您為 **VIEW** 元素指定 backgroundImage 屬性，則還必須指定該元素的 **backgroundColor** 屬性。</span><span class="sxs-lookup"><span data-stu-id="010fb-109">In a Windows Media Download package, if you specify the backgroundImage attribute for a **VIEW** element, then you must also specify the **backgroundColor** attribute for that element.</span></span>

## <a name="requirements"></a><span data-ttu-id="010fb-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="010fb-110">Requirements</span></span>



| <span data-ttu-id="010fb-111">需求</span><span class="sxs-lookup"><span data-stu-id="010fb-111">Requirement</span></span> | <span data-ttu-id="010fb-112">值</span><span class="sxs-lookup"><span data-stu-id="010fb-112">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="010fb-113">版本</span><span class="sxs-lookup"><span data-stu-id="010fb-113">Version</span></span><br/> | <span data-ttu-id="010fb-114">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="010fb-114">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="010fb-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="010fb-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="010fb-116">**色彩參考**</span><span class="sxs-lookup"><span data-stu-id="010fb-116">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="010fb-117">**VIEW 元素**</span><span class="sxs-lookup"><span data-stu-id="010fb-117">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 





