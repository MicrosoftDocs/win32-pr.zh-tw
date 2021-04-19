---
title: MediaContentTypes 屬性
description: MediaContentTypes 屬性會指定專案中的內容類型。
ms.assetid: b91bab65-d6d2-4e05-9338-c24f28b7c71e
keywords:
- MediaContentTypes 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- MediaContentTypes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8979864151e029abf2731f6f0b4663e078a2c061
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987084"
---
# <a name="mediacontenttypes-attribute"></a><span data-ttu-id="e8e9c-104">MediaContentTypes 屬性</span><span class="sxs-lookup"><span data-stu-id="e8e9c-104">MediaContentTypes Attribute</span></span>

<span data-ttu-id="e8e9c-105">**MediaContentTypes** 屬性會指定專案中的內容類型。</span><span class="sxs-lookup"><span data-stu-id="e8e9c-105">The **MediaContentTypes** attribute specifies the type of content in the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="e8e9c-106">套用至</span><span class="sxs-lookup"><span data-stu-id="e8e9c-106">Applies To</span></span>

-   [<span data-ttu-id="e8e9c-107">播放清單</span><span class="sxs-lookup"><span data-stu-id="e8e9c-107">Playlists</span></span>](playlist-attributes-ref.md)

## <a name="remarks"></a><span data-ttu-id="e8e9c-108">備註</span><span class="sxs-lookup"><span data-stu-id="e8e9c-108">Remarks</span></span>

<span data-ttu-id="e8e9c-109">這個屬性可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="e8e9c-109">This attribute can be one of the following values:</span></span>



| <span data-ttu-id="e8e9c-110">值</span><span class="sxs-lookup"><span data-stu-id="e8e9c-110">Value</span></span> | <span data-ttu-id="e8e9c-111">意義</span><span class="sxs-lookup"><span data-stu-id="e8e9c-111">Meaning</span></span>                                |
|-------|----------------------------------------|
| <span data-ttu-id="e8e9c-112">1</span><span class="sxs-lookup"><span data-stu-id="e8e9c-112">1</span></span>     | <span data-ttu-id="e8e9c-113">播放清單包含音訊內容。</span><span class="sxs-lookup"><span data-stu-id="e8e9c-113">The playlist contains audio content.</span></span>   |
| <span data-ttu-id="e8e9c-114">2</span><span class="sxs-lookup"><span data-stu-id="e8e9c-114">2</span></span>     | <span data-ttu-id="e8e9c-115">提供。</span><span class="sxs-lookup"><span data-stu-id="e8e9c-115">To be supplied.</span></span>                        |
| <span data-ttu-id="e8e9c-116">3</span><span class="sxs-lookup"><span data-stu-id="e8e9c-116">3</span></span>     | <span data-ttu-id="e8e9c-117">播放清單包含音訊內容。</span><span class="sxs-lookup"><span data-stu-id="e8e9c-117">The playlist contains audio content.</span></span>   |
| <span data-ttu-id="e8e9c-118">4</span><span class="sxs-lookup"><span data-stu-id="e8e9c-118">4</span></span>     | <span data-ttu-id="e8e9c-119">播放清單包含影片內容。</span><span class="sxs-lookup"><span data-stu-id="e8e9c-119">The playlist contains video content.</span></span>   |
| <span data-ttu-id="e8e9c-120">5</span><span class="sxs-lookup"><span data-stu-id="e8e9c-120">5</span></span>     | <span data-ttu-id="e8e9c-121">播放清單包含圖片內容。</span><span class="sxs-lookup"><span data-stu-id="e8e9c-121">The playlist contains picture content.</span></span> |
| <span data-ttu-id="e8e9c-122">6</span><span class="sxs-lookup"><span data-stu-id="e8e9c-122">6</span></span>     | <span data-ttu-id="e8e9c-123">播放清單包含電視內容。</span><span class="sxs-lookup"><span data-stu-id="e8e9c-123">The playlist contains TV content.</span></span>      |



 

<span data-ttu-id="e8e9c-124">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="e8e9c-124">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8e9c-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8e9c-125">Requirements</span></span>



| <span data-ttu-id="e8e9c-126">需求</span><span class="sxs-lookup"><span data-stu-id="e8e9c-126">Requirement</span></span> | <span data-ttu-id="e8e9c-127">值</span><span class="sxs-lookup"><span data-stu-id="e8e9c-127">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="e8e9c-128">版本</span><span class="sxs-lookup"><span data-stu-id="e8e9c-128">Version</span></span><br/> | <span data-ttu-id="e8e9c-129">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="e8e9c-129">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e8e9c-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8e9c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8e9c-131">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="e8e9c-131">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





