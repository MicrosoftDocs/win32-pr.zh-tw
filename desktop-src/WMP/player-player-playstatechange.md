---
title: PlayStateChange 事件
description: 當 playState 屬性中有變更時，就會發生 PlayStateChange 事件。
ms.assetid: d4c4b114-04b6-4079-b6a2-52b336fc6dc1
keywords:
- PlayStateChange 事件 Windows Media Player
- PlayStateChange 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，PlayStateChange 事件
topic_type:
- apiref
api_name:
- Player.PlayStateChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e621d8698a5379b0d39a55db141fc0012f6ef969
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993268"
---
# <a name="playerplaystatechange-event"></a><span data-ttu-id="d94e8-106">PlayStateChange 事件</span><span class="sxs-lookup"><span data-stu-id="d94e8-106">Player.PlayStateChange event</span></span>

<span data-ttu-id="d94e8-107">當 **playState** 屬性中有變更時，就會發生 **PlayStateChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="d94e8-107">The **PlayStateChange** event occurs when there is a change in the **playState** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="d94e8-108">語法</span><span class="sxs-lookup"><span data-stu-id="d94e8-108">Syntax</span></span>


```JScript
Player.PlayStateChange(
  NewState
)
```



## <a name="parameters"></a><span data-ttu-id="d94e8-109">參數</span><span class="sxs-lookup"><span data-stu-id="d94e8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d94e8-110">*NewState*</span><span class="sxs-lookup"><span data-stu-id="d94e8-110">*NewState*</span></span> 
</dt> <dd>

<span data-ttu-id="d94e8-111">指定新 **playState** 的數位 (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="d94e8-111">Number (**long**) which specifies the new **playState**.</span></span> <span data-ttu-id="d94e8-112">如需可能值的表格，請參閱 [playState](player-playstate.md) 。</span><span class="sxs-lookup"><span data-stu-id="d94e8-112">See [playState](player-playstate.md) for a table of possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d94e8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d94e8-113">Return value</span></span>

<span data-ttu-id="d94e8-114">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d94e8-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d94e8-115">備註</span><span class="sxs-lookup"><span data-stu-id="d94e8-115">Remarks</span></span>

<span data-ttu-id="d94e8-116">事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。</span><span class="sxs-lookup"><span data-stu-id="d94e8-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="d94e8-117">此參數名稱的類型必須完全如所示，包括大小寫。</span><span class="sxs-lookup"><span data-stu-id="d94e8-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="d94e8-118">Windows Media Player 狀態不保證會以任何特定順序發生。</span><span class="sxs-lookup"><span data-stu-id="d94e8-118">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="d94e8-119">此外，並非每個狀態都一定會在一連串的事件期間發生。</span><span class="sxs-lookup"><span data-stu-id="d94e8-119">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="d94e8-120">您不應該撰寫依賴狀態順序的程式碼。</span><span class="sxs-lookup"><span data-stu-id="d94e8-120">You should not write code that relies upon state order.</span></span>

## <a name="examples"></a><span data-ttu-id="d94e8-121">範例</span><span class="sxs-lookup"><span data-stu-id="d94e8-121">Examples</span></span>

<span data-ttu-id="d94e8-122">下列範例示範 *播放* 程式的事件處理常式。**playStateChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="d94e8-122">The following example demonstrates an event handler for the *Player*.**playStateChange** event.</span></span> <span data-ttu-id="d94e8-123">名為 "myText" 的 HTML 文字元素會顯示新的播放狀態。</span><span class="sxs-lookup"><span data-stu-id="d94e8-123">An HTML text element, named "myText", displays the new play state.</span></span> <span data-ttu-id="d94e8-124">使用 ID = "Player" 建立 player 物件。</span><span class="sxs-lookup"><span data-stu-id="d94e8-124">The player object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player EVENT = playStateChange(NewState)>

// Test for the player current state, display a message for each.
switch (NewState){
    case 1:
        myText.value = "Stopped";
        break;

    case 2:
        myText.value = "Paused";
        break;

    case 3:
        myText.value = "Playing";
        break;

    // Other cases go here.

    default:
        myText.value = "";
}
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="d94e8-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="d94e8-125">Requirements</span></span>



| <span data-ttu-id="d94e8-126">需求</span><span class="sxs-lookup"><span data-stu-id="d94e8-126">Requirement</span></span> | <span data-ttu-id="d94e8-127">值</span><span class="sxs-lookup"><span data-stu-id="d94e8-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d94e8-128">版本</span><span class="sxs-lookup"><span data-stu-id="d94e8-128">Version</span></span><br/> | <span data-ttu-id="d94e8-129">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="d94e8-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d94e8-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d94e8-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="d94e8-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d94e8-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d94e8-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d94e8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d94e8-133">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="d94e8-133">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="d94e8-134">**PlayState**</span><span class="sxs-lookup"><span data-stu-id="d94e8-134">**Player.playState**</span></span>](player-playstate.md)
</dt> </dl>

 

 





