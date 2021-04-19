---
title: ModeChange 事件
description: 當 Windows Media Player 的模式變更時，就會發生 ModeChange 事件。 |ModeChange 事件
ms.assetid: 45b57660-b186-4c0f-8735-61134058b8c9
keywords:
- ModeChange 事件 Windows Media Player
- ModeChange 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，ModeChange 事件
topic_type:
- apiref
api_name:
- Player.ModeChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb202672c7fce6705b8e86889c0ca44d7004a19e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998597"
---
# <a name="playermodechange-event"></a><span data-ttu-id="5742a-107">ModeChange 事件</span><span class="sxs-lookup"><span data-stu-id="5742a-107">Player.ModeChange event</span></span>

<span data-ttu-id="5742a-108">當 Windows Media Player 的模式變更時，就會發生 **ModeChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="5742a-108">The **ModeChange** event occurs when a mode of Windows Media Player is changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="5742a-109">語法</span><span class="sxs-lookup"><span data-stu-id="5742a-109">Syntax</span></span>


```JScript
Player.ModeChange(
  ModeName,
  NewValue
)
```



## <a name="parameters"></a><span data-ttu-id="5742a-110">參數</span><span class="sxs-lookup"><span data-stu-id="5742a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5742a-111">*ModeName*</span><span class="sxs-lookup"><span data-stu-id="5742a-111">*ModeName*</span></span> 
</dt> <dd>

<span data-ttu-id="5742a-112">表示已變更之模式的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="5742a-112">**String** indicating the mode that was changed.</span></span> <span data-ttu-id="5742a-113">包含下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5742a-113">Contains one of the following values.</span></span>



| <span data-ttu-id="5742a-114">值</span><span class="sxs-lookup"><span data-stu-id="5742a-114">Value</span></span>   | <span data-ttu-id="5742a-115">描述</span><span class="sxs-lookup"><span data-stu-id="5742a-115">Description</span></span>                                         |
|---------|-----------------------------------------------------|
| <span data-ttu-id="5742a-116">隨機播放</span><span class="sxs-lookup"><span data-stu-id="5742a-116">shuffle</span></span> | <span data-ttu-id="5742a-117">曲目會以隨機順序播放。</span><span class="sxs-lookup"><span data-stu-id="5742a-117">Tracks are played in random order.</span></span>                  |
| <span data-ttu-id="5742a-118">loop</span><span class="sxs-lookup"><span data-stu-id="5742a-118">loop</span></span>    | <span data-ttu-id="5742a-119">整個播放曲目順序都會重複播放。</span><span class="sxs-lookup"><span data-stu-id="5742a-119">The entire sequence of tracks is played repeatedly.</span></span> |



 

</dd> <dt>

<span data-ttu-id="5742a-120">*NewValue*</span><span class="sxs-lookup"><span data-stu-id="5742a-120">*NewValue*</span></span> 
</dt> <dd>

<span data-ttu-id="5742a-121">**布林值** ，表示指定之模式的新狀態。</span><span class="sxs-lookup"><span data-stu-id="5742a-121">**Boolean** indicating the new state of the specified mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5742a-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="5742a-122">Return value</span></span>

<span data-ttu-id="5742a-123">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5742a-123">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5742a-124">備註</span><span class="sxs-lookup"><span data-stu-id="5742a-124">Remarks</span></span>

<span data-ttu-id="5742a-125">事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。</span><span class="sxs-lookup"><span data-stu-id="5742a-125">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="5742a-126">此參數名稱的類型必須完全如所示，包括大小寫。</span><span class="sxs-lookup"><span data-stu-id="5742a-126">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="5742a-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="5742a-127">Requirements</span></span>



| <span data-ttu-id="5742a-128">需求</span><span class="sxs-lookup"><span data-stu-id="5742a-128">Requirement</span></span> | <span data-ttu-id="5742a-129">值</span><span class="sxs-lookup"><span data-stu-id="5742a-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5742a-130">版本</span><span class="sxs-lookup"><span data-stu-id="5742a-130">Version</span></span><br/> | <span data-ttu-id="5742a-131">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="5742a-131">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5742a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5742a-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="5742a-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5742a-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5742a-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5742a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5742a-135">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="5742a-135">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="5742a-136">**設定. getMode**</span><span class="sxs-lookup"><span data-stu-id="5742a-136">**Settings.getMode**</span></span>](settings-getmode.md)
</dt> <dt>

[<span data-ttu-id="5742a-137">**設定. setMode**</span><span class="sxs-lookup"><span data-stu-id="5742a-137">**Settings.setMode**</span></span>](settings-setmode.md)
</dt> </dl>

 

 





