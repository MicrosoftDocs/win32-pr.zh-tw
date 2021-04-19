---
title: AlbumIDAlbumArtist 屬性
description: AlbumIDAlbumArtist 屬性是專輯的唯一識別碼。
ms.assetid: beaa8d01-1722-4545-8705-6b3d130113b1
keywords:
- AlbumIDAlbumArtist 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- AlbumIDAlbumArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1925f40a50b15efcd339ad949d5d54ddb915cbe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001845"
---
# <a name="albumidalbumartist-attribute"></a><span data-ttu-id="69d60-104">AlbumIDAlbumArtist 屬性</span><span class="sxs-lookup"><span data-stu-id="69d60-104">AlbumIDAlbumArtist Attribute</span></span>

<span data-ttu-id="69d60-105">**AlbumIDAlbumArtist** 屬性是專輯的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="69d60-105">The **AlbumIDAlbumArtist** attribute is a unique identifier for the album.</span></span>

## <a name="applies-to"></a><span data-ttu-id="69d60-106">套用至</span><span class="sxs-lookup"><span data-stu-id="69d60-106">Applies To</span></span>

-   [<span data-ttu-id="69d60-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="69d60-107">Audio Items</span></span>](audio-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="69d60-108">備註</span><span class="sxs-lookup"><span data-stu-id="69d60-108">Remarks</span></span>

<span data-ttu-id="69d60-109">這個屬性只會儲存在程式庫中。</span><span class="sxs-lookup"><span data-stu-id="69d60-109">This attribute is stored only in the library.</span></span>

<span data-ttu-id="69d60-110">唯一識別碼是專輯標題和專輯演出者名稱的組合。</span><span class="sxs-lookup"><span data-stu-id="69d60-110">The unique identifier is a combination of the album title and the album artist name.</span></span> <span data-ttu-id="69d60-111">在此屬性中，專輯演出者名稱優先。</span><span class="sxs-lookup"><span data-stu-id="69d60-111">In this attribute, the album artist name comes first.</span></span> <span data-ttu-id="69d60-112">當您使用 [MediaCollection. getAttributeStringCollection](mediacollection-getattributestringcollection.md) 方法取得使用此屬性的 **StringCollection** 物件時，這些值會依專輯演出者名稱排序。</span><span class="sxs-lookup"><span data-stu-id="69d60-112">When you use the [MediaCollection.getAttributeStringCollection](mediacollection-getattributestringcollection.md) method to get a **StringCollection** object using this attribute, the values are sorted by album artist name.</span></span>

<span data-ttu-id="69d60-113">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="69d60-113">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="69d60-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="69d60-114">Requirements</span></span>



| <span data-ttu-id="69d60-115">需求</span><span class="sxs-lookup"><span data-stu-id="69d60-115">Requirement</span></span> | <span data-ttu-id="69d60-116">值</span><span class="sxs-lookup"><span data-stu-id="69d60-116">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="69d60-117">版本</span><span class="sxs-lookup"><span data-stu-id="69d60-117">Version</span></span><br/> | <span data-ttu-id="69d60-118">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="69d60-118">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="69d60-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69d60-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69d60-120">**AlbumID 屬性**</span><span class="sxs-lookup"><span data-stu-id="69d60-120">**AlbumID Attribute**</span></span>](albumid-attribute.md)
</dt> <dt>

[<span data-ttu-id="69d60-121">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="69d60-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





