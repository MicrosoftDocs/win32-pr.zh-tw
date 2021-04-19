---
title: SetMode 方法
description: SetMode 方法會將各種模式設定為作用中或非作用中。
ms.assetid: 9ab88aeb-53f6-4798-9299-14961e373ca6
keywords:
- setMode 方法 Windows Media Player
- setMode 方法 Windows Media Player，Settings 類別
- Settings 類別 Windows Media Player，setMode 方法
topic_type:
- apiref
api_name:
- Settings.setMode
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf5740bf5638ce34e161414ac96eaa0fc80fcdb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994261"
---
# <a name="settingssetmode-method"></a><span data-ttu-id="39e69-106">SetMode 方法</span><span class="sxs-lookup"><span data-stu-id="39e69-106">Settings.setMode method</span></span>

<span data-ttu-id="39e69-107">**SetMode** 方法會將各種模式設定為作用中或非作用中。</span><span class="sxs-lookup"><span data-stu-id="39e69-107">The **setMode** method sets various modes to active or inactive.</span></span>

## <a name="syntax"></a><span data-ttu-id="39e69-108">語法</span><span class="sxs-lookup"><span data-stu-id="39e69-108">Syntax</span></span>


```JScript
Settings.setMode(
  modeName,
  state
)
```



## <a name="parameters"></a><span data-ttu-id="39e69-109">參數</span><span class="sxs-lookup"><span data-stu-id="39e69-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39e69-110">*modeName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="39e69-110">*modeName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39e69-111">**字串** ，指定要變更的模式名稱，其中包含下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="39e69-111">**String** specifying the name of the mode being changed, containing one of the following values.</span></span>



| <span data-ttu-id="39e69-112">String</span><span class="sxs-lookup"><span data-stu-id="39e69-112">String</span></span>     | <span data-ttu-id="39e69-113">Description</span><span class="sxs-lookup"><span data-stu-id="39e69-113">Description</span></span>                                                                                                                                                       |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39e69-114">autoRewind</span><span class="sxs-lookup"><span data-stu-id="39e69-114">autoRewind</span></span> | <span data-ttu-id="39e69-115">模式，指出播放到結尾之後，是否要將曲目倒轉到開頭。</span><span class="sxs-lookup"><span data-stu-id="39e69-115">Mode indicating whether the tracks are rewound to the beginning after playing to the end.</span></span> <span data-ttu-id="39e69-116">預設狀態為 true。</span><span class="sxs-lookup"><span data-stu-id="39e69-116">Default state is true.</span></span>                                                  |
| <span data-ttu-id="39e69-117">loop</span><span class="sxs-lookup"><span data-stu-id="39e69-117">loop</span></span>       | <span data-ttu-id="39e69-118">指出曲目順序是否會自行重複的模式。</span><span class="sxs-lookup"><span data-stu-id="39e69-118">Mode indicating whether the sequence of tracks repeats itself.</span></span> <span data-ttu-id="39e69-119">預設狀態為 false。</span><span class="sxs-lookup"><span data-stu-id="39e69-119">Default state is false.</span></span>                                                                            |
| <span data-ttu-id="39e69-120">showFrame</span><span class="sxs-lookup"><span data-stu-id="39e69-120">showFrame</span></span>  | <span data-ttu-id="39e69-121">指出最近的影片主要畫面格是否在未播放時顯示于目前位置的模式。</span><span class="sxs-lookup"><span data-stu-id="39e69-121">Mode indicating whether the nearest video key frame is displayed at the current position when not playing.</span></span> <span data-ttu-id="39e69-122">預設狀態為 false。</span><span class="sxs-lookup"><span data-stu-id="39e69-122">Default state is false.</span></span> <span data-ttu-id="39e69-123">對音軌沒有任何影響。</span><span class="sxs-lookup"><span data-stu-id="39e69-123">Has no effect on audio tracks.</span></span> |
| <span data-ttu-id="39e69-124">隨機播放</span><span class="sxs-lookup"><span data-stu-id="39e69-124">shuffle</span></span>    | <span data-ttu-id="39e69-125">指出是否以隨機順序播放曲目的模式。</span><span class="sxs-lookup"><span data-stu-id="39e69-125">Mode indicating whether the tracks are played in random order.</span></span> <span data-ttu-id="39e69-126">預設狀態為 false。</span><span class="sxs-lookup"><span data-stu-id="39e69-126">Default state is false.</span></span>                                                                            |



 

</dd> <dt>

<span data-ttu-id="39e69-127">*狀態* \[在\]</span><span class="sxs-lookup"><span data-stu-id="39e69-127">*state* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39e69-128">**布林值** ，指定新指定的模式是否為使用中。</span><span class="sxs-lookup"><span data-stu-id="39e69-128">**Boolean** specifying whether the new specified mode is active or not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39e69-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="39e69-129">Return value</span></span>

<span data-ttu-id="39e69-130">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="39e69-130">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="39e69-131">備註</span><span class="sxs-lookup"><span data-stu-id="39e69-131">Remarks</span></span>

<span data-ttu-id="39e69-132">當 showFrame 模式為使用中時，播放程式必須存取曲目內容才能取出影片畫面。</span><span class="sxs-lookup"><span data-stu-id="39e69-132">When the showFrame mode is active, the Player must access the track content to retrieve the video frame.</span></span> <span data-ttu-id="39e69-133">基於頻寬考慮，播放非區域內容時請小心使用這個模式。</span><span class="sxs-lookup"><span data-stu-id="39e69-133">Due to bandwidth considerations, use this mode cautiously when playing non-local content.</span></span>

## <a name="requirements"></a><span data-ttu-id="39e69-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="39e69-134">Requirements</span></span>



| <span data-ttu-id="39e69-135">需求</span><span class="sxs-lookup"><span data-stu-id="39e69-135">Requirement</span></span> | <span data-ttu-id="39e69-136">值</span><span class="sxs-lookup"><span data-stu-id="39e69-136">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39e69-137">版本</span><span class="sxs-lookup"><span data-stu-id="39e69-137">Version</span></span><br/> | <span data-ttu-id="39e69-138">針對迴圈和隨機模式，Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="39e69-138">For loop and shuffle modes, Windows Media Player version 7.0 or later.</span></span> <span data-ttu-id="39e69-139">適用于 autoRewind 和 showFrame 模式，Windows Media Player 9 系列或更新版本。</span><span class="sxs-lookup"><span data-stu-id="39e69-139">For autoRewind and showFrame modes, Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="39e69-140">DLL</span><span class="sxs-lookup"><span data-stu-id="39e69-140">DLL</span></span><br/>     | <dl> <span data-ttu-id="39e69-141"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39e69-141"><dt>Wmp.dll</dt></span></span> </dl>                                                                            |



## <a name="see-also"></a><span data-ttu-id="39e69-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39e69-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39e69-143">**Settings 物件**</span><span class="sxs-lookup"><span data-stu-id="39e69-143">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="39e69-144">**設定. getMode**</span><span class="sxs-lookup"><span data-stu-id="39e69-144">**Settings.getMode**</span></span>](settings-getmode.md)
</dt> </dl>

 

 





