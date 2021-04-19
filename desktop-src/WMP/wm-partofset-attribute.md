---
title: WM/PartOfSet 屬性
description: WM/PartOfSet 屬性是專案所屬之集合的部分編號和總數。
ms.assetid: c6827c31-c625-4283-a50d-f08eccf87271
keywords:
- WM/PartOfSet 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/PartOfSet
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c27d6297931c503c95c8ef0462bf7b119a0ffb75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999654"
---
# <a name="wmpartofset-attribute"></a><span data-ttu-id="98fef-104">WM/PartOfSet 屬性</span><span class="sxs-lookup"><span data-stu-id="98fef-104">WM/PartOfSet Attribute</span></span>

<span data-ttu-id="98fef-105">**WM/PartOfSet** 屬性是專案所屬之集合的部分編號和總數。</span><span class="sxs-lookup"><span data-stu-id="98fef-105">The **WM/PartOfSet** attribute is the part number and the total number of parts of the set to which the item belongs.</span></span>

## <a name="applies-to"></a><span data-ttu-id="98fef-106">套用至</span><span class="sxs-lookup"><span data-stu-id="98fef-106">Applies To</span></span>

-   [<span data-ttu-id="98fef-107">音樂檔案</span><span class="sxs-lookup"><span data-stu-id="98fef-107">Music Files</span></span>](music-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="98fef-108">備註</span><span class="sxs-lookup"><span data-stu-id="98fef-108">Remarks</span></span>

<span data-ttu-id="98fef-109">這個屬性只會儲存在不在文件庫中的音樂檔案中。</span><span class="sxs-lookup"><span data-stu-id="98fef-109">This attribute is stored only in a music file that is not in the library.</span></span>

<span data-ttu-id="98fef-110">這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMPartOfSet。</span><span class="sxs-lookup"><span data-stu-id="98fef-110">The Windows Media Format SDK constant for this attribute is g\_wszWMPartOfSet.</span></span>

<span data-ttu-id="98fef-111">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="98fef-111">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="98fef-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="98fef-112">Requirements</span></span>



| <span data-ttu-id="98fef-113">需求</span><span class="sxs-lookup"><span data-stu-id="98fef-113">Requirement</span></span> | <span data-ttu-id="98fef-114">值</span><span class="sxs-lookup"><span data-stu-id="98fef-114">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="98fef-115">版本</span><span class="sxs-lookup"><span data-stu-id="98fef-115">Version</span></span><br/> | <span data-ttu-id="98fef-116">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="98fef-116">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="98fef-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="98fef-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98fef-118">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="98fef-118">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





