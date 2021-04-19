---
title: MediaCollection. getStringCollectionByQuery 方法
description: GetStringCollectionByQuery 方法會捕獲 StringCollection 物件，其中包含符合查詢準則的所有字串。
ms.assetid: 17442151-7eb1-4256-ac5f-142b11645216
keywords:
- getStringCollectionByQuery 方法 Windows Media Player
- getStringCollectionByQuery 方法 Windows Media Player，MediaCollection 類別
- MediaCollection 類別 Windows Media Player，getStringCollectionByQuery 方法
topic_type:
- apiref
api_name:
- MediaCollection.getStringCollectionByQuery
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf304d22cb207d8a2bfb046522e8704e900d508
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000772"
---
# <a name="mediacollectiongetstringcollectionbyquery-method"></a><span data-ttu-id="0c57d-106">MediaCollection. getStringCollectionByQuery 方法</span><span class="sxs-lookup"><span data-stu-id="0c57d-106">MediaCollection.getStringCollectionByQuery method</span></span>

<span data-ttu-id="0c57d-107">**GetStringCollectionByQuery** 方法會捕獲 **StringCollection** 物件，其中包含符合查詢準則的所有字串。</span><span class="sxs-lookup"><span data-stu-id="0c57d-107">The **getStringCollectionByQuery** method retrieves a **StringCollection** object containing all strings that match the query conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c57d-108">語法</span><span class="sxs-lookup"><span data-stu-id="0c57d-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getStringCollectionByQuery(
  attribute,
  query,
  mediaType,
  sortAttribute,
  sortAscending
)
```



## <a name="parameters"></a><span data-ttu-id="0c57d-109">參數</span><span class="sxs-lookup"><span data-stu-id="0c57d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c57d-110">*屬性* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0c57d-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c57d-111">包含屬性名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="0c57d-111">**String** containing the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="0c57d-112">*查詢* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0c57d-112">*query* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c57d-113">**Query** 物件。</span><span class="sxs-lookup"><span data-stu-id="0c57d-113">**Query** object.</span></span>

</dd> <dt>

<span data-ttu-id="0c57d-114">*媒體媒體* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0c57d-114">*mediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c57d-115">包含媒體類型的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="0c57d-115">**String** containing the media type.</span></span> <span data-ttu-id="0c57d-116">必須包含下列其中一個值：「音訊」、「影片」、「相片」、「播放清單」或「其他」。</span><span class="sxs-lookup"><span data-stu-id="0c57d-116">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> <dt>

<span data-ttu-id="0c57d-117">*sortAttribute* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0c57d-117">*sortAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c57d-118">包含用於排序之屬性名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="0c57d-118">**String** containing the attribute name used for sorting.</span></span> <span data-ttu-id="0c57d-119">空字串 ( "" ) 表示不套用排序。</span><span class="sxs-lookup"><span data-stu-id="0c57d-119">An empty string ("") means no sorting is applied.</span></span>

</dd> <dt>

<span data-ttu-id="0c57d-120">*sortAscending* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0c57d-120">*sortAscending* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c57d-121">**布林** 值，表示 **StringCollection** 必須以遞增順序排序。</span><span class="sxs-lookup"><span data-stu-id="0c57d-121">**Boolean**, true indicating that the **StringCollection** must be sorted in ascending order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c57d-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="0c57d-122">Return value</span></span>

<span data-ttu-id="0c57d-123">這個方法會傳回 **StringCollection** 物件。</span><span class="sxs-lookup"><span data-stu-id="0c57d-123">This method returns a **StringCollection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c57d-124">備註</span><span class="sxs-lookup"><span data-stu-id="0c57d-124">Remarks</span></span>

<span data-ttu-id="0c57d-125">使用 **查詢** 的複合查詢不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="0c57d-125">Compound queries using **Query** are not case sensitive.</span></span>

<span data-ttu-id="0c57d-126">當 *查詢* 參數所指定的複合查詢包含以「 **媒體** 類型」（attribute）為基礎的條件時，就會忽略該條件。</span><span class="sxs-lookup"><span data-stu-id="0c57d-126">When the compound query specified by the *query* parameter contains a condition built on the **MediaType** attribute, that condition is ignored.</span></span> <span data-ttu-id="0c57d-127">[ *媒體* ] 參數的值一律會使用。</span><span class="sxs-lookup"><span data-stu-id="0c57d-127">The value for the *mediaType* parameter is always used.</span></span> <span data-ttu-id="0c57d-128">例如，如果複合查詢包含「媒體的等於音訊」條件，而「 *媒體媒體* 」參數的值為「影片」，則產生的播放清單只會包含影片專案。</span><span class="sxs-lookup"><span data-stu-id="0c57d-128">For example, if the compound query contains the condition "MediaType Equals audio" and the value for the *mediaType* parameter is "video", the resulting playlist will contain only video items.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c57d-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c57d-129">Requirements</span></span>



| <span data-ttu-id="0c57d-130">需求</span><span class="sxs-lookup"><span data-stu-id="0c57d-130">Requirement</span></span> | <span data-ttu-id="0c57d-131">值</span><span class="sxs-lookup"><span data-stu-id="0c57d-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0c57d-132">版本</span><span class="sxs-lookup"><span data-stu-id="0c57d-132">Version</span></span><br/> | <span data-ttu-id="0c57d-133">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="0c57d-133">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="0c57d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0c57d-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="0c57d-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c57d-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c57d-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c57d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c57d-137">**MediaCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="0c57d-137">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="0c57d-138">**媒體屬性**</span><span class="sxs-lookup"><span data-stu-id="0c57d-138">**MediaType Attribute**</span></span>](mediatype-attribute.md)
</dt> <dt>

[<span data-ttu-id="0c57d-139">**Query 物件**</span><span class="sxs-lookup"><span data-stu-id="0c57d-139">**Query Object**</span></span>](query-object.md)
</dt> </dl>

 

 





