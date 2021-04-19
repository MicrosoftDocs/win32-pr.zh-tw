---
title: WM/UniqueFileIdentifier 屬性
description: WM/UniqueFileIdentifier 屬性是可唯一識別專案的字串。
ms.assetid: 8196fc38-05dc-4c9e-98cb-1e160ce28a9a
keywords:
- WM/UniqueFileIdentifier 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/UniqueFileIdentifier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0a4297f299f6e7df64088066b3137d844a0c78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977784"
---
# <a name="wmuniquefileidentifier-attribute"></a><span data-ttu-id="2d04f-104">WM/UniqueFileIdentifier 屬性</span><span class="sxs-lookup"><span data-stu-id="2d04f-104">WM/UniqueFileIdentifier Attribute</span></span>

<span data-ttu-id="2d04f-105">**WM/UniqueFileIdentifier** 屬性是可唯一識別專案的字串。</span><span class="sxs-lookup"><span data-stu-id="2d04f-105">The **WM/UniqueFileIdentifier** attribute is a string that uniquely identifies the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="2d04f-106">套用至</span><span class="sxs-lookup"><span data-stu-id="2d04f-106">Applies To</span></span>

-   [<span data-ttu-id="2d04f-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="2d04f-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="2d04f-108">CD 播放清單</span><span class="sxs-lookup"><span data-stu-id="2d04f-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="2d04f-109">CD 曲目</span><span class="sxs-lookup"><span data-stu-id="2d04f-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="2d04f-110">常用的 Windows Media 檔案屬性</span><span class="sxs-lookup"><span data-stu-id="2d04f-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="2d04f-111">備註</span><span class="sxs-lookup"><span data-stu-id="2d04f-111">Remarks</span></span>

<span data-ttu-id="2d04f-112">這個屬性會儲存在程式庫 (或快取) 和數位媒體檔案中。</span><span class="sxs-lookup"><span data-stu-id="2d04f-112">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="2d04f-113">**UniqueFileIdentifier** 是此屬性的別名。</span><span class="sxs-lookup"><span data-stu-id="2d04f-113">**UniqueFileIdentifier** is an alias for this attribute.</span></span>

<span data-ttu-id="2d04f-114">這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMUniqueFileIdentifier。</span><span class="sxs-lookup"><span data-stu-id="2d04f-114">The Windows Media Format SDK constant for this attribute is g\_wszWMUniqueFileIdentifier.</span></span>

<span data-ttu-id="2d04f-115">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="2d04f-115">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d04f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d04f-116">Requirements</span></span>



| <span data-ttu-id="2d04f-117">需求</span><span class="sxs-lookup"><span data-stu-id="2d04f-117">Requirement</span></span> | <span data-ttu-id="2d04f-118">值</span><span class="sxs-lookup"><span data-stu-id="2d04f-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="2d04f-119">版本</span><span class="sxs-lookup"><span data-stu-id="2d04f-119">Version</span></span><br/> | <span data-ttu-id="2d04f-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="2d04f-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2d04f-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d04f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d04f-122">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="2d04f-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





