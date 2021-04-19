---
title: WM/Year 屬性
description: WM/Year 屬性是發佈內容的年份。
ms.assetid: b64e37f1-6f12-43a6-8a66-7d61b470853c
keywords:
- WM/Year 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/Year
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10bf10d4e905e10c74cfaf9986445ce9a68dc9b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993407"
---
# <a name="wmyear-attribute"></a><span data-ttu-id="3d1e8-104">WM/Year 屬性</span><span class="sxs-lookup"><span data-stu-id="3d1e8-104">WM/Year Attribute</span></span>

<span data-ttu-id="3d1e8-105">**WM/Year** 屬性是發佈內容的年份。</span><span class="sxs-lookup"><span data-stu-id="3d1e8-105">The **WM/Year** attribute is the year the content was published.</span></span>

## <a name="applies-to"></a><span data-ttu-id="3d1e8-106">套用至</span><span class="sxs-lookup"><span data-stu-id="3d1e8-106">Applies To</span></span>

-   [<span data-ttu-id="3d1e8-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="3d1e8-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="3d1e8-108">常用的 Windows Media 檔案屬性</span><span class="sxs-lookup"><span data-stu-id="3d1e8-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="3d1e8-109">備註</span><span class="sxs-lookup"><span data-stu-id="3d1e8-109">Remarks</span></span>

<span data-ttu-id="3d1e8-110">這個屬性只會儲存在數位媒體檔案中。</span><span class="sxs-lookup"><span data-stu-id="3d1e8-110">This attribute is stored only in the digital media file.</span></span>

<span data-ttu-id="3d1e8-111">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="3d1e8-111">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

<span data-ttu-id="3d1e8-112">這個屬性不應該當做查詢準則的一部分使用。</span><span class="sxs-lookup"><span data-stu-id="3d1e8-112">This attribute should not be used as part of a query condition.</span></span> <span data-ttu-id="3d1e8-113">它是衍生自另一個屬性，而且無法在媒體集合中直接查詢。</span><span class="sxs-lookup"><span data-stu-id="3d1e8-113">It is derived from another attribute and cannot be directly queried against in a media collection.</span></span>

<span data-ttu-id="3d1e8-114">這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMYear。</span><span class="sxs-lookup"><span data-stu-id="3d1e8-114">The Windows Media Format SDK constant for this attribute is g\_wszWMYear.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d1e8-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d1e8-115">Requirements</span></span>



| <span data-ttu-id="3d1e8-116">需求</span><span class="sxs-lookup"><span data-stu-id="3d1e8-116">Requirement</span></span> | <span data-ttu-id="3d1e8-117">值</span><span class="sxs-lookup"><span data-stu-id="3d1e8-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d1e8-118">版本</span><span class="sxs-lookup"><span data-stu-id="3d1e8-118">Version</span></span><br/> | <span data-ttu-id="3d1e8-119">Windows Media Player 9 系列 Windows Media Player 10 或更新版本不支援此屬性</span><span class="sxs-lookup"><span data-stu-id="3d1e8-119">Windows Media Player 9 Series Windows Media Player 10 or later does not support this attribute</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3d1e8-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d1e8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d1e8-121">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="3d1e8-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





