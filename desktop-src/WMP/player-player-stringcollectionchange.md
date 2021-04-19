---
title: StringCollectionChange 事件
description: 當字串集合變更時，就會發生 StringCollectionChange 事件。 |StringCollectionChange 事件
ms.assetid: 465ec694-afd1-4baa-b559-3ab75874388f
keywords:
- StringCollectionChange 事件 Windows Media Player
- StringCollectionChange 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，StringCollectionChange 事件
topic_type:
- apiref
api_name:
- Player.StringCollectionChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29f72d7af0f73d74393d980b2506a3b7f05e578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983971"
---
# <a name="playerstringcollectionchange-event"></a><span data-ttu-id="5bbb7-107">StringCollectionChange 事件</span><span class="sxs-lookup"><span data-stu-id="5bbb7-107">Player.StringCollectionChange event</span></span>

<span data-ttu-id="5bbb7-108">當字串集合變更時，就會發生 StringCollectionChange 事件。</span><span class="sxs-lookup"><span data-stu-id="5bbb7-108">The StringCollectionChange event occurs when a string collection changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bbb7-109">語法</span><span class="sxs-lookup"><span data-stu-id="5bbb7-109">Syntax</span></span>


```JScript
Player.StringCollectionChange(
  pdispStringCollection,
  change,
  lCollectionIndex
)
```



## <a name="parameters"></a><span data-ttu-id="5bbb7-110">參數</span><span class="sxs-lookup"><span data-stu-id="5bbb7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bbb7-111">*pdispStringCollection*</span><span class="sxs-lookup"><span data-stu-id="5bbb7-111">*pdispStringCollection*</span></span> 
</dt> <dd>

<span data-ttu-id="5bbb7-112">**StringCollection** 已變更的物件。</span><span class="sxs-lookup"><span data-stu-id="5bbb7-112">**StringCollection** object that changed.</span></span>

</dd> <dt>

<span data-ttu-id="5bbb7-113">*change*</span><span class="sxs-lookup"><span data-stu-id="5bbb7-113">*change*</span></span> 
</dt> <dd>

<span data-ttu-id="5bbb7-114">Number (long) 表示字串集合發生的變更類型。</span><span class="sxs-lookup"><span data-stu-id="5bbb7-114">Number (long)indicating the type of change that occurred to the string collection.</span></span> <span data-ttu-id="5bbb7-115">包含下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5bbb7-115">Includes one of the following values.</span></span>



|        |                                    |
|--------|------------------------------------|
| <span data-ttu-id="5bbb7-116">Number</span><span class="sxs-lookup"><span data-stu-id="5bbb7-116">Number</span></span> | <span data-ttu-id="5bbb7-117">描述</span><span class="sxs-lookup"><span data-stu-id="5bbb7-117">Description</span></span>                        |
| <span data-ttu-id="5bbb7-118">0</span><span class="sxs-lookup"><span data-stu-id="5bbb7-118">0</span></span>      | <span data-ttu-id="5bbb7-119">不明。</span><span class="sxs-lookup"><span data-stu-id="5bbb7-119">Unknown.</span></span> <span data-ttu-id="5bbb7-120"> (不是有效的值) </span><span class="sxs-lookup"><span data-stu-id="5bbb7-120">(Not a valid value)</span></span>       |
| <span data-ttu-id="5bbb7-121">1</span><span class="sxs-lookup"><span data-stu-id="5bbb7-121">1</span></span>      | <span data-ttu-id="5bbb7-122">已插入專案。</span><span class="sxs-lookup"><span data-stu-id="5bbb7-122">An item was inserted.</span></span>              |
| <span data-ttu-id="5bbb7-123">2</span><span class="sxs-lookup"><span data-stu-id="5bbb7-123">2</span></span>      | <span data-ttu-id="5bbb7-124">字串集合已變更。</span><span class="sxs-lookup"><span data-stu-id="5bbb7-124">The string collection changed.</span></span>     |
| <span data-ttu-id="5bbb7-125">3</span><span class="sxs-lookup"><span data-stu-id="5bbb7-125">3</span></span>      | <span data-ttu-id="5bbb7-126">已刪除專案。</span><span class="sxs-lookup"><span data-stu-id="5bbb7-126">An item was deleted.</span></span>               |
| <span data-ttu-id="5bbb7-127">4</span><span class="sxs-lookup"><span data-stu-id="5bbb7-127">4</span></span>      | <span data-ttu-id="5bbb7-128">已清除字串集合。</span><span class="sxs-lookup"><span data-stu-id="5bbb7-128">The string collection was cleared.</span></span> |
| <span data-ttu-id="5bbb7-129">5</span><span class="sxs-lookup"><span data-stu-id="5bbb7-129">5</span></span>      | <span data-ttu-id="5bbb7-130">大量更新即將開始。</span><span class="sxs-lookup"><span data-stu-id="5bbb7-130">Bulk updates are beginning.</span></span>        |
| <span data-ttu-id="5bbb7-131">6</span><span class="sxs-lookup"><span data-stu-id="5bbb7-131">6</span></span>      | <span data-ttu-id="5bbb7-132">大量更新已結束。</span><span class="sxs-lookup"><span data-stu-id="5bbb7-132">Bulk updates have ended.</span></span>           |



 

</dd> <dt>

<span data-ttu-id="5bbb7-133">*lCollectionIndex*</span><span class="sxs-lookup"><span data-stu-id="5bbb7-133">*lCollectionIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="5bbb7-134">Number (long) ，其中包含已變更之字串收集項目的索引。</span><span class="sxs-lookup"><span data-stu-id="5bbb7-134">Number (long) containing the index of the string collection item that changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bbb7-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="5bbb7-135">Return value</span></span>

<span data-ttu-id="5bbb7-136">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5bbb7-136">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bbb7-137">備註</span><span class="sxs-lookup"><span data-stu-id="5bbb7-137">Remarks</span></span>

<span data-ttu-id="5bbb7-138">**Windows Media Player 10** 行動裝置版：不支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="5bbb7-138">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bbb7-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="5bbb7-139">Requirements</span></span>



| <span data-ttu-id="5bbb7-140">需求</span><span class="sxs-lookup"><span data-stu-id="5bbb7-140">Requirement</span></span> | <span data-ttu-id="5bbb7-141">值</span><span class="sxs-lookup"><span data-stu-id="5bbb7-141">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5bbb7-142">版本</span><span class="sxs-lookup"><span data-stu-id="5bbb7-142">Version</span></span><br/> | <span data-ttu-id="5bbb7-143">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="5bbb7-143">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="5bbb7-144">DLL</span><span class="sxs-lookup"><span data-stu-id="5bbb7-144">DLL</span></span><br/>     | <dl> <span data-ttu-id="5bbb7-145"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5bbb7-145"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bbb7-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5bbb7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bbb7-147">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="5bbb7-147">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="5bbb7-148">**StringCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="5bbb7-148">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





