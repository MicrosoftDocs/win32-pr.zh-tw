---
title: MediaCollectionAttributeStringChanged 事件
description: 當程式庫中的屬性值變更時，就會發生 MediaCollectionAttributeStringChanged 事件。 |MediaCollectionAttributeStringChanged 事件
ms.assetid: 9bc81cf2-50a9-41cf-8eff-25c9395dfdac
keywords:
- MediaCollectionAttributeStringChanged 事件 Windows Media Player
- MediaCollectionAttributeStringChanged 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，MediaCollectionAttributeStringChanged 事件
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringChanged
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f92eba7f0f585b9bbff7a8eb52ab13ec0d74aaa5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990144"
---
# <a name="playermediacollectionattributestringchanged-event"></a><span data-ttu-id="0d73e-107">MediaCollectionAttributeStringChanged 事件</span><span class="sxs-lookup"><span data-stu-id="0d73e-107">Player.MediaCollectionAttributeStringChanged event</span></span>

<span data-ttu-id="0d73e-108">當程式庫中的屬性值變更時，就會發生 **MediaCollectionAttributeStringChanged** 事件。</span><span class="sxs-lookup"><span data-stu-id="0d73e-108">The **MediaCollectionAttributeStringChanged** event occurs when an attribute value in the library is changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d73e-109">語法</span><span class="sxs-lookup"><span data-stu-id="0d73e-109">Syntax</span></span>


```JScript
Player.MediaCollectionAttributeStringChanged(
  bstrAttribName,
  bstrOldAttribVal,
  bstrNewAttribVal
)
```



## <a name="parameters"></a><span data-ttu-id="0d73e-110">參數</span><span class="sxs-lookup"><span data-stu-id="0d73e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d73e-111">*bstrAttribName*</span><span class="sxs-lookup"><span data-stu-id="0d73e-111">*bstrAttribName*</span></span> 
</dt> <dd>

<span data-ttu-id="0d73e-112">指定屬性名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="0d73e-112">**String** specifying the name of the attribute.</span></span> <span data-ttu-id="0d73e-113">如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player [屬性參考](attribute-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="0d73e-113">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d73e-114">*bstrOldAttribVal*</span><span class="sxs-lookup"><span data-stu-id="0d73e-114">*bstrOldAttribVal*</span></span> 
</dt> <dd>

<span data-ttu-id="0d73e-115">**字串** ，指定屬性的舊值。</span><span class="sxs-lookup"><span data-stu-id="0d73e-115">**String** specifying the old value of the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="0d73e-116">*bstrNewAttribVal*</span><span class="sxs-lookup"><span data-stu-id="0d73e-116">*bstrNewAttribVal*</span></span> 
</dt> <dd>

<span data-ttu-id="0d73e-117">**字串** ，指定屬性的新值。</span><span class="sxs-lookup"><span data-stu-id="0d73e-117">**String** specifying the new value of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d73e-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="0d73e-118">Return value</span></span>

<span data-ttu-id="0d73e-119">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0d73e-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d73e-120">備註</span><span class="sxs-lookup"><span data-stu-id="0d73e-120">Remarks</span></span>

<span data-ttu-id="0d73e-121">當使用者修改程式庫中繼資料時，會更新 **MediaCollection** 物件，並針對每個屬性變更引發此事件。</span><span class="sxs-lookup"><span data-stu-id="0d73e-121">When a user modifies library metadata, the **MediaCollection** object is updated and this event fires for each attribute changed.</span></span>

<span data-ttu-id="0d73e-122">事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。</span><span class="sxs-lookup"><span data-stu-id="0d73e-122">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="0d73e-123">此參數名稱的類型必須完全如所示，包括大小寫。</span><span class="sxs-lookup"><span data-stu-id="0d73e-123">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="0d73e-124">**Windows Media Player 10** 行動裝置版：不支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="0d73e-124">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d73e-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d73e-125">Requirements</span></span>



| <span data-ttu-id="0d73e-126">需求</span><span class="sxs-lookup"><span data-stu-id="0d73e-126">Requirement</span></span> | <span data-ttu-id="0d73e-127">值</span><span class="sxs-lookup"><span data-stu-id="0d73e-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0d73e-128">版本</span><span class="sxs-lookup"><span data-stu-id="0d73e-128">Version</span></span><br/> | <span data-ttu-id="0d73e-129">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="0d73e-129">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="0d73e-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0d73e-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="0d73e-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d73e-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d73e-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d73e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d73e-133">**MediaCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="0d73e-133">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="0d73e-134">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="0d73e-134">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="0d73e-135">**MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="0d73e-135">**Player.mediaCollection**</span></span>](player-mediacollection.md)
</dt> </dl>

 

 





