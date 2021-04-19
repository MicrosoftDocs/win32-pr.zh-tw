---
title: OpenStateChange 事件
description: 當 openState 屬性變更值時，就會發生 OpenStateChange 事件。 |OpenStateChange 事件
ms.assetid: b6b840ab-72c7-4150-a259-1e7d8afcec81
keywords:
- OpenStateChange 事件 Windows Media Player
- OpenStateChange 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，OpenStateChange 事件
topic_type:
- apiref
api_name:
- Player.OpenStateChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 020a25a811623b9f7d7dd8f316c470cada6a142b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992863"
---
# <a name="playeropenstatechange-event"></a><span data-ttu-id="fb41f-107">OpenStateChange 事件</span><span class="sxs-lookup"><span data-stu-id="fb41f-107">Player.OpenStateChange event</span></span>

<span data-ttu-id="fb41f-108">當 **openState** 屬性變更值時，就會發生 **OpenStateChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="fb41f-108">The **OpenStateChange** event occurs when the **openState** property changes value.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb41f-109">語法</span><span class="sxs-lookup"><span data-stu-id="fb41f-109">Syntax</span></span>


```JScript
Player.OpenStateChange(
  NewState
)
```



## <a name="parameters"></a><span data-ttu-id="fb41f-110">參數</span><span class="sxs-lookup"><span data-stu-id="fb41f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb41f-111">*NewState*</span><span class="sxs-lookup"><span data-stu-id="fb41f-111">*NewState*</span></span> 
</dt> <dd>

<span data-ttu-id="fb41f-112">指定新的開啟狀態 (**長**) **數目**。</span><span class="sxs-lookup"><span data-stu-id="fb41f-112">**Number** (**long**) specifying the new open state.</span></span> <span data-ttu-id="fb41f-113">如需值的表格，請參閱 [openState](player-openstate.md) 。</span><span class="sxs-lookup"><span data-stu-id="fb41f-113">See [openState](player-openstate.md) for a table of values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb41f-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="fb41f-114">Return value</span></span>

<span data-ttu-id="fb41f-115">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="fb41f-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb41f-116">備註</span><span class="sxs-lookup"><span data-stu-id="fb41f-116">Remarks</span></span>

<span data-ttu-id="fb41f-117">Windows Media Player 可以在嘗試開啟網路檔案（例如找出伺服器、連線到伺服器，最後開啟檔案）時，經歷數個開啟的狀態。</span><span class="sxs-lookup"><span data-stu-id="fb41f-117">Windows Media Player can go through several open states while it attempts to open a network file, such as locating the server, connecting to the server, and finally opening the file.</span></span> <span data-ttu-id="fb41f-118">每次開啟狀態變更時，就會引發此事件。</span><span class="sxs-lookup"><span data-stu-id="fb41f-118">This event will be fired each time the open state changes.</span></span>

<span data-ttu-id="fb41f-119">事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。</span><span class="sxs-lookup"><span data-stu-id="fb41f-119">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="fb41f-120">此參數名稱的類型必須完全如所示，包括大小寫。</span><span class="sxs-lookup"><span data-stu-id="fb41f-120">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="fb41f-121">Windows Media Player 狀態不保證會以任何特定順序發生。</span><span class="sxs-lookup"><span data-stu-id="fb41f-121">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="fb41f-122">此外，並非每個狀態都一定會在一連串的事件期間發生。</span><span class="sxs-lookup"><span data-stu-id="fb41f-122">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="fb41f-123">您不應該撰寫依賴狀態順序的程式碼。</span><span class="sxs-lookup"><span data-stu-id="fb41f-123">You should not write code that relies upon state order.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb41f-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb41f-124">Requirements</span></span>



| <span data-ttu-id="fb41f-125">需求</span><span class="sxs-lookup"><span data-stu-id="fb41f-125">Requirement</span></span> | <span data-ttu-id="fb41f-126">值</span><span class="sxs-lookup"><span data-stu-id="fb41f-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fb41f-127">版本</span><span class="sxs-lookup"><span data-stu-id="fb41f-127">Version</span></span><br/> | <span data-ttu-id="fb41f-128">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="fb41f-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="fb41f-129">DLL</span><span class="sxs-lookup"><span data-stu-id="fb41f-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="fb41f-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb41f-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb41f-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb41f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb41f-132">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="fb41f-132">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="fb41f-133">**OpenState**</span><span class="sxs-lookup"><span data-stu-id="fb41f-133">**Player.openState**</span></span>](player-openstate.md)
</dt> </dl>

 

 





