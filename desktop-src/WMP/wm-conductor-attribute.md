---
title: WM/導體屬性
description: WM/導體屬性是音樂的導線名稱。
ms.assetid: 31c7d310-da6a-4c30-86b0-15defaee1743
keywords:
- WM/導體屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/Conductor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d1ae08dfee807d130f04dd258c6af81a8d68057
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998779"
---
# <a name="wmconductor-attribute"></a><span data-ttu-id="eb57a-104">WM/導體屬性</span><span class="sxs-lookup"><span data-stu-id="eb57a-104">WM/Conductor Attribute</span></span>

<span data-ttu-id="eb57a-105">**WM/導體** 屬性是音樂的導線名稱。</span><span class="sxs-lookup"><span data-stu-id="eb57a-105">The **WM/Conductor** attribute is the name of the conductor of the music.</span></span>

## <a name="applies-to"></a><span data-ttu-id="eb57a-106">套用至</span><span class="sxs-lookup"><span data-stu-id="eb57a-106">Applies To</span></span>

-   [<span data-ttu-id="eb57a-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="eb57a-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="eb57a-108">CD 曲目</span><span class="sxs-lookup"><span data-stu-id="eb57a-108">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="eb57a-109">常用的 Windows Media 檔案屬性</span><span class="sxs-lookup"><span data-stu-id="eb57a-109">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="eb57a-110">備註</span><span class="sxs-lookup"><span data-stu-id="eb57a-110">Remarks</span></span>

<span data-ttu-id="eb57a-111">這個屬性會儲存在程式庫 (或快取) 和數位媒體檔案中。</span><span class="sxs-lookup"><span data-stu-id="eb57a-111">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="eb57a-112">這個屬性可以有多個值。</span><span class="sxs-lookup"><span data-stu-id="eb57a-112">This attribute may have multiple values.</span></span> <span data-ttu-id="eb57a-113">若要取得多重值屬性的所有值，您必須使用 **getItemInfoByType** 方法，而不是 **getItemInfo** 方法。</span><span class="sxs-lookup"><span data-stu-id="eb57a-113">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="eb57a-114">**導體** 是這個屬性的別名。</span><span class="sxs-lookup"><span data-stu-id="eb57a-114">**Conductor** is an alias for this attribute.</span></span>

<span data-ttu-id="eb57a-115">這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMConductor。</span><span class="sxs-lookup"><span data-stu-id="eb57a-115">The Windows Media Format SDK constant for this attribute is g\_wszWMConductor.</span></span>

<span data-ttu-id="eb57a-116">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="eb57a-116">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb57a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb57a-117">Requirements</span></span>



| <span data-ttu-id="eb57a-118">需求</span><span class="sxs-lookup"><span data-stu-id="eb57a-118">Requirement</span></span> | <span data-ttu-id="eb57a-119">值</span><span class="sxs-lookup"><span data-stu-id="eb57a-119">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="eb57a-120">版本</span><span class="sxs-lookup"><span data-stu-id="eb57a-120">Version</span></span><br/> | <span data-ttu-id="eb57a-121">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="eb57a-121">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eb57a-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb57a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb57a-123">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="eb57a-123">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="eb57a-124">**GetItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="eb57a-124">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 





