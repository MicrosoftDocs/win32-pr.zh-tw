---
title: 播放清單。 itemMedia
description: ItemMedia 屬性會抓取與播放清單元素中的指定索引對應的媒體物件。
ms.assetid: 38085798-7986-432f-8c88-de886bfc2ac5
keywords:
- 播放清單. itemMedia Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.itemMedia
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 269e9011ade69ee61d99c29c1fa5bd1b9fa3deeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994062"
---
# <a name="playlistitemmedia"></a><span data-ttu-id="fed09-104">播放清單。 itemMedia</span><span class="sxs-lookup"><span data-stu-id="fed09-104">PLAYLIST.itemMedia</span></span>

<span data-ttu-id="fed09-105">**ItemMedia** 屬性會抓取與 **播放清單** 元素中的指定索引對應的 **媒體** 物件。</span><span class="sxs-lookup"><span data-stu-id="fed09-105">The **itemMedia** attribute retrieves the **Media** object corresponding to the given index in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.itemMedia(index)
```

## <a name="possible-values"></a><span data-ttu-id="fed09-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="fed09-106">Possible Values</span></span>

<span data-ttu-id="fed09-107">這個屬性是唯讀 **媒體** 物件。</span><span class="sxs-lookup"><span data-stu-id="fed09-107">This attribute is a read-only **Media** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="fed09-108">參數</span><span class="sxs-lookup"><span data-stu-id="fed09-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fed09-109"><span id="index"></span><span id="INDEX"></span>*指數*</span><span class="sxs-lookup"><span data-stu-id="fed09-109"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="fed09-110">包含播放清單專案索引的 (**長**) **數目**。</span><span class="sxs-lookup"><span data-stu-id="fed09-110">**Number**(**long**) containing the index of a playlist item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fed09-111">備註</span><span class="sxs-lookup"><span data-stu-id="fed09-111">Remarks</span></span>

<span data-ttu-id="fed09-112">**ItemMedia** 屬性會傳回在 **播放清單** 元素中展開的媒體物件。</span><span class="sxs-lookup"><span data-stu-id="fed09-112">The **itemMedia** property will return media objects that are expanded in the **PLAYLIST** element.</span></span> <span data-ttu-id="fed09-113">例如，如果播放清單中包含的三個媒體剪輯都未在 **播放清單** 元素中展開， **itemMedia** (0) 將會傳回播放清單作為媒體物件。</span><span class="sxs-lookup"><span data-stu-id="fed09-113">For example, if there is a playlist that contains three media clips that is not expanded in the **PLAYLIST** element, **itemMedia**(0) will return the playlist as the media object.</span></span> <span data-ttu-id="fed09-114">如果已展開播放清單， **itemMedia** (0) 將會傳回播放清單中的第一個媒體剪輯。</span><span class="sxs-lookup"><span data-stu-id="fed09-114">If the playlist is expanded, **itemMedia**(0) will return the first media clip in the playlist.</span></span>

## <a name="requirements"></a><span data-ttu-id="fed09-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="fed09-115">Requirements</span></span>



| <span data-ttu-id="fed09-116">需求</span><span class="sxs-lookup"><span data-stu-id="fed09-116">Requirement</span></span> | <span data-ttu-id="fed09-117">值</span><span class="sxs-lookup"><span data-stu-id="fed09-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="fed09-118">版本</span><span class="sxs-lookup"><span data-stu-id="fed09-118">Version</span></span><br/> | <span data-ttu-id="fed09-119">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="fed09-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fed09-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fed09-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fed09-121">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="fed09-121">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="fed09-122">**播放清單元素**</span><span class="sxs-lookup"><span data-stu-id="fed09-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





