---
title: WM/編輯器屬性
description: WM/編輯器屬性是音樂編輯器的名稱。
ms.assetid: 48459027-ed80-46a2-ad5c-ace602144150
keywords:
- WM/編輯器屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/Composer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2f206b1a23126612f3f7c875b9a9b4badca8339
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992575"
---
# <a name="wmcomposer-attribute"></a><span data-ttu-id="04089-104">WM/編輯器屬性</span><span class="sxs-lookup"><span data-stu-id="04089-104">WM/Composer Attribute</span></span>

<span data-ttu-id="04089-105">**WM/編輯器** 屬性是音樂編輯器的名稱。</span><span class="sxs-lookup"><span data-stu-id="04089-105">The **WM/Composer** attribute is the name of the composer of the music.</span></span>

## <a name="applies-to"></a><span data-ttu-id="04089-106">套用至</span><span class="sxs-lookup"><span data-stu-id="04089-106">Applies To</span></span>

-   [<span data-ttu-id="04089-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="04089-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="04089-108">CD 播放清單</span><span class="sxs-lookup"><span data-stu-id="04089-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="04089-109">CD 曲目</span><span class="sxs-lookup"><span data-stu-id="04089-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="04089-110">常用的 Windows Media 檔案屬性</span><span class="sxs-lookup"><span data-stu-id="04089-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="04089-111">備註</span><span class="sxs-lookup"><span data-stu-id="04089-111">Remarks</span></span>

<span data-ttu-id="04089-112">這個屬性會儲存在程式庫 (或快取) 和數位媒體檔案中。</span><span class="sxs-lookup"><span data-stu-id="04089-112">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="04089-113">這個屬性可以有多個值。</span><span class="sxs-lookup"><span data-stu-id="04089-113">This attribute may have multiple values.</span></span> <span data-ttu-id="04089-114">若要取得多重值屬性的所有值，您必須使用 **getItemInfoByType** 方法，而不是 **getItemInfo** 方法。</span><span class="sxs-lookup"><span data-stu-id="04089-114">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="04089-115">**編輯器** 是這個屬性的別名。</span><span class="sxs-lookup"><span data-stu-id="04089-115">**Composer** is an alias for this attribute.</span></span>

<span data-ttu-id="04089-116">這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMComposer。</span><span class="sxs-lookup"><span data-stu-id="04089-116">The Windows Media Format SDK constant for this attribute is g\_wszWMComposer.</span></span>

<span data-ttu-id="04089-117">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="04089-117">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="04089-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="04089-118">Requirements</span></span>



| <span data-ttu-id="04089-119">需求</span><span class="sxs-lookup"><span data-stu-id="04089-119">Requirement</span></span> | <span data-ttu-id="04089-120">值</span><span class="sxs-lookup"><span data-stu-id="04089-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="04089-121">版本</span><span class="sxs-lookup"><span data-stu-id="04089-121">Version</span></span><br/> | <span data-ttu-id="04089-122">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="04089-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="04089-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04089-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04089-124">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="04089-124">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="04089-125">**GetItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="04089-125">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 





