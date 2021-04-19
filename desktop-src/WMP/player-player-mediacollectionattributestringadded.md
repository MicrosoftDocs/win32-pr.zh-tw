---
title: MediaCollectionAttributeStringAdded 事件
description: 將屬性值新增至程式庫時，就會發生 MediaCollectionAttributeStringAdded 事件。 |MediaCollectionAttributeStringAdded 事件
ms.assetid: 0a7fd61f-0429-4c1c-8790-d2f0e7f41d44
keywords:
- MediaCollectionAttributeStringAdded 事件 Windows Media Player
- MediaCollectionAttributeStringAdded 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，MediaCollectionAttributeStringAdded 事件
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61ec30cf22b36fe97902d6eb6d6949daeb751f8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993616"
---
# <a name="playermediacollectionattributestringadded-event"></a><span data-ttu-id="14cb9-107">MediaCollectionAttributeStringAdded 事件</span><span class="sxs-lookup"><span data-stu-id="14cb9-107">Player.MediaCollectionAttributeStringAdded event</span></span>

<span data-ttu-id="14cb9-108">將屬性值新增至程式庫時，就會發生 **MediaCollectionAttributeStringAdded** 事件。</span><span class="sxs-lookup"><span data-stu-id="14cb9-108">The **MediaCollectionAttributeStringAdded** event occurs when an attribute value is added to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="14cb9-109">語法</span><span class="sxs-lookup"><span data-stu-id="14cb9-109">Syntax</span></span>


```JScript
Player.MediaCollectionAttributeStringAdded(
  bstrAttribName,
  bstrAttribVal
)
```



## <a name="parameters"></a><span data-ttu-id="14cb9-110">參數</span><span class="sxs-lookup"><span data-stu-id="14cb9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14cb9-111">*bstrAttribName*</span><span class="sxs-lookup"><span data-stu-id="14cb9-111">*bstrAttribName*</span></span> 
</dt> <dd>

<span data-ttu-id="14cb9-112">指定屬性名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="14cb9-112">**String** specifying the name of the attribute.</span></span> <span data-ttu-id="14cb9-113">如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player [屬性參考](attribute-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="14cb9-113">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="14cb9-114">*bstrAttribVal*</span><span class="sxs-lookup"><span data-stu-id="14cb9-114">*bstrAttribVal*</span></span> 
</dt> <dd>

<span data-ttu-id="14cb9-115">**字串** ，指定屬性的值。</span><span class="sxs-lookup"><span data-stu-id="14cb9-115">**String** specifying the value of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14cb9-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="14cb9-116">Return value</span></span>

<span data-ttu-id="14cb9-117">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="14cb9-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="14cb9-118">備註</span><span class="sxs-lookup"><span data-stu-id="14cb9-118">Remarks</span></span>

<span data-ttu-id="14cb9-119">當媒體專案加入至程式庫時，它的中繼資料會加入至 **MediaCollection** 物件，而且會針對每個加入的屬性引發此事件。</span><span class="sxs-lookup"><span data-stu-id="14cb9-119">When a media item is added to the library its metadata is added to the **MediaCollection** object and this event is fired for each attribute added.</span></span>

<span data-ttu-id="14cb9-120">事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。</span><span class="sxs-lookup"><span data-stu-id="14cb9-120">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="14cb9-121">此參數名稱的類型必須完全如所示，包括大小寫。</span><span class="sxs-lookup"><span data-stu-id="14cb9-121">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="14cb9-122">**Windows Media Player 10** 行動裝置版：不支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="14cb9-122">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="14cb9-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="14cb9-123">Requirements</span></span>



| <span data-ttu-id="14cb9-124">需求</span><span class="sxs-lookup"><span data-stu-id="14cb9-124">Requirement</span></span> | <span data-ttu-id="14cb9-125">值</span><span class="sxs-lookup"><span data-stu-id="14cb9-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="14cb9-126">版本</span><span class="sxs-lookup"><span data-stu-id="14cb9-126">Version</span></span><br/> | <span data-ttu-id="14cb9-127">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="14cb9-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="14cb9-128">DLL</span><span class="sxs-lookup"><span data-stu-id="14cb9-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="14cb9-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14cb9-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14cb9-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14cb9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14cb9-131">**MediaCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="14cb9-131">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="14cb9-132">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="14cb9-132">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="14cb9-133">**MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="14cb9-133">**Player.mediaCollection**</span></span>](player-mediacollection.md)
</dt> </dl>

 

 





