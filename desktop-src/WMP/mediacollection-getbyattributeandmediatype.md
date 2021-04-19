---
title: MediaCollection. getByAttributeAndMediaType 方法
description: GetByAttributeAndMediaType 方法會抓取播放清單物件，其中包含具有指定之屬性和媒體類型的媒體物件。
ms.assetid: 75241b38-ae0e-4216-b405-af9a9c71f5ec
keywords:
- getByAttributeAndMediaType 方法 Windows Media Player
- getByAttributeAndMediaType 方法 Windows Media Player，MediaCollection 類別
- MediaCollection 類別 Windows Media Player，getByAttributeAndMediaType 方法
topic_type:
- apiref
api_name:
- MediaCollection.getByAttributeAndMediaType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e26abbf2f19d50ec6a10ebbafe12afae8576f34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982694"
---
# <a name="mediacollectiongetbyattributeandmediatype-method"></a><span data-ttu-id="f5eb7-106">MediaCollection. getByAttributeAndMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="f5eb7-106">MediaCollection.getByAttributeAndMediaType method</span></span>

<span data-ttu-id="f5eb7-107">**GetByAttributeAndMediaType** 方法會抓取 **播放清單** 物件，其中包含具有指定之屬性和媒體類型的 **媒體** 物件。</span><span class="sxs-lookup"><span data-stu-id="f5eb7-107">The **getByAttributeAndMediaType** method retrieves a **Playlist** object containing **Media** objects having the specified attribute and media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5eb7-108">語法</span><span class="sxs-lookup"><span data-stu-id="f5eb7-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByAttributeAndMediaType(
  attribute,
  value,
  mediaType
)
```



## <a name="parameters"></a><span data-ttu-id="f5eb7-109">參數</span><span class="sxs-lookup"><span data-stu-id="f5eb7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5eb7-110">*屬性* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f5eb7-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5eb7-111">包含屬性的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="f5eb7-111">**String** containing the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="f5eb7-112">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f5eb7-112">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5eb7-113">包含值的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="f5eb7-113">**String** containing the value.</span></span>

</dd> <dt>

<span data-ttu-id="f5eb7-114">*媒體媒體* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f5eb7-114">*mediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5eb7-115">包含媒體類型的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="f5eb7-115">**String** containing the media type.</span></span> <span data-ttu-id="f5eb7-116">必須包含下列其中一個值：「音訊」、「影片」、「相片」、「播放清單」或「其他」。</span><span class="sxs-lookup"><span data-stu-id="f5eb7-116">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5eb7-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="f5eb7-117">Return value</span></span>

<span data-ttu-id="f5eb7-118">這個方法會傳回 **播放清單** 物件</span><span class="sxs-lookup"><span data-stu-id="f5eb7-118">This method returns a **Playlist** object</span></span>

## <a name="requirements"></a><span data-ttu-id="f5eb7-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5eb7-119">Requirements</span></span>



| <span data-ttu-id="f5eb7-120">需求</span><span class="sxs-lookup"><span data-stu-id="f5eb7-120">Requirement</span></span> | <span data-ttu-id="f5eb7-121">值</span><span class="sxs-lookup"><span data-stu-id="f5eb7-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f5eb7-122">版本</span><span class="sxs-lookup"><span data-stu-id="f5eb7-122">Version</span></span><br/> | <span data-ttu-id="f5eb7-123">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="f5eb7-123">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="f5eb7-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f5eb7-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="f5eb7-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5eb7-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5eb7-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f5eb7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5eb7-127">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="f5eb7-127">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="f5eb7-128">**MediaCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="f5eb7-128">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="f5eb7-129">**播放清單物件**</span><span class="sxs-lookup"><span data-stu-id="f5eb7-129">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 





