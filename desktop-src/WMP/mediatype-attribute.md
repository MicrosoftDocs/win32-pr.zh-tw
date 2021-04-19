---
title: 媒體屬性
description: '[媒體類型] 屬性是專案中的內容類型。'
ms.assetid: 0d8a6937-32d8-4a4a-87e5-0002f077fefe
keywords:
- 媒體屬性 Windows Media Player
topic_type:
- apiref
api_name:
- MediaType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5779552f62007aa3dd3da0e2f4253fcf5499a6be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977678"
---
# <a name="mediatype-attribute"></a><span data-ttu-id="d7c81-104">媒體屬性</span><span class="sxs-lookup"><span data-stu-id="d7c81-104">MediaType Attribute</span></span>

<span data-ttu-id="d7c81-105">[ **媒體** 類型] 屬性是專案中的內容類型。</span><span class="sxs-lookup"><span data-stu-id="d7c81-105">The **MediaType** attribute is the type of content in the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="d7c81-106">套用至</span><span class="sxs-lookup"><span data-stu-id="d7c81-106">Applies To</span></span>

-   [<span data-ttu-id="d7c81-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="d7c81-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="d7c81-108">其他專案</span><span class="sxs-lookup"><span data-stu-id="d7c81-108">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="d7c81-109">相片專案</span><span class="sxs-lookup"><span data-stu-id="d7c81-109">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="d7c81-110">播放清單</span><span class="sxs-lookup"><span data-stu-id="d7c81-110">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="d7c81-111">單選項目</span><span class="sxs-lookup"><span data-stu-id="d7c81-111">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="d7c81-112">影片專案</span><span class="sxs-lookup"><span data-stu-id="d7c81-112">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="d7c81-113">備註</span><span class="sxs-lookup"><span data-stu-id="d7c81-113">Remarks</span></span>

<span data-ttu-id="d7c81-114">這個屬性只會儲存在程式庫中。</span><span class="sxs-lookup"><span data-stu-id="d7c81-114">This attribute is stored only in the library.</span></span>

<span data-ttu-id="d7c81-115">此屬性具有下列其中一個值：「音訊」、「其他」、「相片」、「播放清單」、「單選」或「影片」。</span><span class="sxs-lookup"><span data-stu-id="d7c81-115">This attribute has one of the following values: "audio", "other", "photo", "playlist", "radio", or "video".</span></span> <span data-ttu-id="d7c81-116">將此屬性與 *MediaCollection* 搭配使用。**getByAttribute** 方法，以取得包含特定類型之所有專案的播放清單。</span><span class="sxs-lookup"><span data-stu-id="d7c81-116">Use this attribute with the *MediaCollection*.**getByAttribute** method to retrieve a playlist containing all of the items of a particular type.</span></span>

<span data-ttu-id="d7c81-117">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="d7c81-117">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7c81-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7c81-118">Requirements</span></span>



| <span data-ttu-id="d7c81-119">需求</span><span class="sxs-lookup"><span data-stu-id="d7c81-119">Requirement</span></span> | <span data-ttu-id="d7c81-120">值</span><span class="sxs-lookup"><span data-stu-id="d7c81-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="d7c81-121">版本</span><span class="sxs-lookup"><span data-stu-id="d7c81-121">Version</span></span><br/> | <span data-ttu-id="d7c81-122">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="d7c81-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d7c81-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7c81-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7c81-124">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="d7c81-124">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="d7c81-125">**MediaCollection.getByAttribute**</span><span class="sxs-lookup"><span data-stu-id="d7c81-125">**MediaCollection.getByAttribute**</span></span>](mediacollection-getbyattribute.md)
</dt> </dl>

 

 





