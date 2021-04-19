---
title: MediaCollection. getPlaylistByQuery 方法
description: GetPlaylistByQuery 方法會抓取包含符合查詢準則之媒體物件的播放清單物件。
ms.assetid: 3487d442-a5bb-4519-ac45-d0138516305e
keywords:
- getPlaylistByQuery 方法 Windows Media Player
- getPlaylistByQuery 方法 Windows Media Player，MediaCollection 類別
- MediaCollection 類別 Windows Media Player，getPlaylistByQuery 方法
topic_type:
- apiref
api_name:
- MediaCollection.getPlaylistByQuery
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50b57d4303ba8784f912db9570faacb26d01677d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001559"
---
# <a name="mediacollectiongetplaylistbyquery-method"></a><span data-ttu-id="a87ad-106">MediaCollection. getPlaylistByQuery 方法</span><span class="sxs-lookup"><span data-stu-id="a87ad-106">MediaCollection.getPlaylistByQuery method</span></span>

<span data-ttu-id="a87ad-107">**GetPlaylistByQuery** 方法會抓取包含符合查詢準則之 **媒體** 物件的 **播放清單** 物件。</span><span class="sxs-lookup"><span data-stu-id="a87ad-107">The **getPlaylistByQuery** method retrieves a **Playlist** object containing **Media** objects that match the query conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="a87ad-108">語法</span><span class="sxs-lookup"><span data-stu-id="a87ad-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getPlaylistByQuery(
  query,
  mediaType,
  sortAttribute,
  sortAscending
)
```



## <a name="parameters"></a><span data-ttu-id="a87ad-109">參數</span><span class="sxs-lookup"><span data-stu-id="a87ad-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a87ad-110">*查詢* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a87ad-110">*query* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a87ad-111">**查詢** 物件，定義用來建立播放清單的條件。</span><span class="sxs-lookup"><span data-stu-id="a87ad-111">**Query** object that defines the conditions used to create the playlist.</span></span>

</dd> <dt>

<span data-ttu-id="a87ad-112">*媒體媒體* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a87ad-112">*mediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a87ad-113">包含媒體類型的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="a87ad-113">**String** containing the media type.</span></span> <span data-ttu-id="a87ad-114">必須包含下列其中一個值：「音訊」、「影片」、「相片」、「播放清單」或「其他」。</span><span class="sxs-lookup"><span data-stu-id="a87ad-114">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> <dt>

<span data-ttu-id="a87ad-115">*sortAttribute* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a87ad-115">*sortAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a87ad-116">包含用於排序之屬性名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="a87ad-116">**String** containing the attribute name used for sorting.</span></span> <span data-ttu-id="a87ad-117">空字串 ( "" ) 表示不套用排序。</span><span class="sxs-lookup"><span data-stu-id="a87ad-117">An empty string ("") means no sorting is applied.</span></span>

</dd> <dt>

<span data-ttu-id="a87ad-118">*sortAscending* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a87ad-118">*sortAscending* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a87ad-119">**布林** 值，表示播放清單必須以遞增順序排序。</span><span class="sxs-lookup"><span data-stu-id="a87ad-119">**Boolean**, true indicating that the playlist must be sorted in ascending order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a87ad-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="a87ad-120">Return value</span></span>

<span data-ttu-id="a87ad-121">這個方法會傳回 **播放清單** 物件。</span><span class="sxs-lookup"><span data-stu-id="a87ad-121">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a87ad-122">備註</span><span class="sxs-lookup"><span data-stu-id="a87ad-122">Remarks</span></span>

<span data-ttu-id="a87ad-123">使用 **查詢** 的複合查詢不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a87ad-123">Compound queries using **Query** are not case sensitive.</span></span>

<span data-ttu-id="a87ad-124">當 *查詢* 參數所指定的複合查詢包含以「 **媒體** 類型」（attribute）為基礎的條件時，就會忽略該條件。</span><span class="sxs-lookup"><span data-stu-id="a87ad-124">When the compound query specified by the *query* parameter contains a condition built on the **MediaType** attribute, that condition is ignored.</span></span> <span data-ttu-id="a87ad-125">[ *媒體* ] 參數的值一律會使用。</span><span class="sxs-lookup"><span data-stu-id="a87ad-125">The value for the *mediaType* parameter is always used.</span></span> <span data-ttu-id="a87ad-126">例如，如果複合查詢包含「媒體的等於音訊」條件，而「 *媒體媒體* 」參數的值為「影片」，則產生的播放清單只會包含影片專案。</span><span class="sxs-lookup"><span data-stu-id="a87ad-126">For example, if the compound query contains the condition "MediaType Equals audio" and the value for the *mediaType* parameter is "video", the resulting playlist will contain only video items.</span></span>

## <a name="requirements"></a><span data-ttu-id="a87ad-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="a87ad-127">Requirements</span></span>



| <span data-ttu-id="a87ad-128">需求</span><span class="sxs-lookup"><span data-stu-id="a87ad-128">Requirement</span></span> | <span data-ttu-id="a87ad-129">值</span><span class="sxs-lookup"><span data-stu-id="a87ad-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a87ad-130">版本</span><span class="sxs-lookup"><span data-stu-id="a87ad-130">Version</span></span><br/> | <span data-ttu-id="a87ad-131">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="a87ad-131">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="a87ad-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a87ad-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="a87ad-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a87ad-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a87ad-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a87ad-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a87ad-135">**MediaCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="a87ad-135">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="a87ad-136">**媒體屬性**</span><span class="sxs-lookup"><span data-stu-id="a87ad-136">**MediaType Attribute**</span></span>](mediatype-attribute.md)
</dt> <dt>

[<span data-ttu-id="a87ad-137">**Query 物件**</span><span class="sxs-lookup"><span data-stu-id="a87ad-137">**Query Object**</span></span>](query-object.md)
</dt> </dl>

 

 





