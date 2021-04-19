---
title: GetMode 方法
description: GetMode 方法會判斷迴圈模式或隨機播放模式是否為使用中狀態。
ms.assetid: 41c3725f-ae8f-4b45-856a-b7245c9ad2b3
keywords:
- getMode 方法 Windows Media Player
- getMode 方法 Windows Media Player，Settings 類別
- Settings 類別 Windows Media Player，getMode 方法
topic_type:
- apiref
api_name:
- Settings.getMode
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5fc3e82091200d05bb173c71f2c0e5a7d213b80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976045"
---
# <a name="settingsgetmode-method"></a><span data-ttu-id="8ff5f-106">GetMode 方法</span><span class="sxs-lookup"><span data-stu-id="8ff5f-106">Settings.getMode method</span></span>

<span data-ttu-id="8ff5f-107">**GetMode** 方法會判斷迴圈模式或隨機播放模式是否為使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="8ff5f-107">The **getMode** method determines whether the loop mode or shuffle mode is active.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ff5f-108">語法</span><span class="sxs-lookup"><span data-stu-id="8ff5f-108">Syntax</span></span>


```JScript
bRetVal = Settings.getMode(
  modeName
)
```



## <a name="parameters"></a><span data-ttu-id="8ff5f-109">參數</span><span class="sxs-lookup"><span data-stu-id="8ff5f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ff5f-110">*modeName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ff5f-110">*modeName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ff5f-111">**字串** ，指定有問題的模式名稱，其中包含下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="8ff5f-111">**String** specifying the name of the mode in question, containing one of the following values.</span></span>



| <span data-ttu-id="8ff5f-112">String</span><span class="sxs-lookup"><span data-stu-id="8ff5f-112">String</span></span>     | <span data-ttu-id="8ff5f-113">Description</span><span class="sxs-lookup"><span data-stu-id="8ff5f-113">Description</span></span>                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ff5f-114">autoRewind</span><span class="sxs-lookup"><span data-stu-id="8ff5f-114">autoRewind</span></span> | <span data-ttu-id="8ff5f-115">播放至結尾之後，會在一開始重新開機追蹤。</span><span class="sxs-lookup"><span data-stu-id="8ff5f-115">Tracks are restarted at the beginning after playing to the end.</span></span>                                                          |
| <span data-ttu-id="8ff5f-116">loop</span><span class="sxs-lookup"><span data-stu-id="8ff5f-116">loop</span></span>       | <span data-ttu-id="8ff5f-117">追蹤順序會自行重複。</span><span class="sxs-lookup"><span data-stu-id="8ff5f-117">The sequence of tracks repeats itself.</span></span>                                                                                   |
| <span data-ttu-id="8ff5f-118">showFrame</span><span class="sxs-lookup"><span data-stu-id="8ff5f-118">showFrame</span></span>  | <span data-ttu-id="8ff5f-119">未播放時，最接近的主要畫面格會顯示在目前的位置。</span><span class="sxs-lookup"><span data-stu-id="8ff5f-119">The nearest key frame is displayed at the current position when not playing.</span></span> <span data-ttu-id="8ff5f-120">此模式與音訊播放軌無關。</span><span class="sxs-lookup"><span data-stu-id="8ff5f-120">This mode is not relevant for audio tracks.</span></span> |
| <span data-ttu-id="8ff5f-121">隨機播放</span><span class="sxs-lookup"><span data-stu-id="8ff5f-121">shuffle</span></span>    | <span data-ttu-id="8ff5f-122">曲目會以隨機順序播放。</span><span class="sxs-lookup"><span data-stu-id="8ff5f-122">Tracks are played in random order.</span></span>                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ff5f-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="8ff5f-123">Return value</span></span>

<span data-ttu-id="8ff5f-124">這個方法會傳回 **布林** 值，指出指定的模式是否為使用中。</span><span class="sxs-lookup"><span data-stu-id="8ff5f-124">This method returns a **Boolean** value indicating whether the specified mode is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ff5f-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ff5f-125">Requirements</span></span>



| <span data-ttu-id="8ff5f-126">需求</span><span class="sxs-lookup"><span data-stu-id="8ff5f-126">Requirement</span></span> | <span data-ttu-id="8ff5f-127">值</span><span class="sxs-lookup"><span data-stu-id="8ff5f-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ff5f-128">版本</span><span class="sxs-lookup"><span data-stu-id="8ff5f-128">Version</span></span><br/> | <span data-ttu-id="8ff5f-129">針對迴圈和隨機模式，Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="8ff5f-129">For loop and shuffle modes, Windows Media Player version 7.0 or later.</span></span> <span data-ttu-id="8ff5f-130">適用于 autoRewind 和 showFrame 模式，Windows Media Player 9 系列或更新版本。</span><span class="sxs-lookup"><span data-stu-id="8ff5f-130">For autoRewind and showFrame modes, Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="8ff5f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="8ff5f-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="8ff5f-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ff5f-132"><dt>Wmp.dll</dt></span></span> </dl>                                                                            |



## <a name="see-also"></a><span data-ttu-id="8ff5f-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ff5f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ff5f-134">**Settings 物件**</span><span class="sxs-lookup"><span data-stu-id="8ff5f-134">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="8ff5f-135">**設定. setMode**</span><span class="sxs-lookup"><span data-stu-id="8ff5f-135">**Settings.setMode**</span></span>](settings-setmode.md)
</dt> </dl>

 

 





