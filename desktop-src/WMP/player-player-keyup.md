---
title: Player. KeyUp 事件
description: 當釋放索引鍵時，就會發生 KeyUp 事件。 |Player. KeyUp 事件
ms.assetid: 8b624374-403f-4d41-8481-5e94cee70861
keywords:
- KeyUp 事件 Windows Media Player
- KeyUp 事件 Windows Media Player、Player 類別
- Player 類別 Windows Media Player、KeyUp 事件
topic_type:
- apiref
api_name:
- Player.KeyUp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f06e9b77871e9f62d46bdfa223bfa40b87feaf06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994633"
---
# <a name="playerkeyup-event"></a><span data-ttu-id="6db5c-107">Player. KeyUp 事件</span><span class="sxs-lookup"><span data-stu-id="6db5c-107">Player.KeyUp event</span></span>

<span data-ttu-id="6db5c-108">當釋放索引鍵時，就會發生 **KeyUp** 事件。</span><span class="sxs-lookup"><span data-stu-id="6db5c-108">The **KeyUp** event occurs when a key is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="6db5c-109">語法</span><span class="sxs-lookup"><span data-stu-id="6db5c-109">Syntax</span></span>


```JScript
Player.KeyUp(
  nKeyCode,
  nShiftState
)
```



## <a name="parameters"></a><span data-ttu-id="6db5c-110">參數</span><span class="sxs-lookup"><span data-stu-id="6db5c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6db5c-111">*nKeyCode*</span><span class="sxs-lookup"><span data-stu-id="6db5c-111">*nKeyCode*</span></span> 
</dt> <dd>

<span data-ttu-id="6db5c-112"> (**int**) 指定按下哪個實體索引鍵的 **數目**。</span><span class="sxs-lookup"><span data-stu-id="6db5c-112">**Number** (**int**) specifying which physical key is pressed.</span></span> <span data-ttu-id="6db5c-113">如需可能的值，請參閱 [Player. KeyDown 事件](player-player-keydown.md)。</span><span class="sxs-lookup"><span data-stu-id="6db5c-113">For possible values, see [Player.KeyDown Event](player-player-keydown.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db5c-114">*nShiftState*</span><span class="sxs-lookup"><span data-stu-id="6db5c-114">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="6db5c-115">**Number** (**int**) 指定具有最少有效位數的位位（對應至 SHIFT 鍵 (BIT 0) 、CTRL 鍵 (位 1) ，以及 ALT 鍵 (位 2) ）。</span><span class="sxs-lookup"><span data-stu-id="6db5c-115">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="6db5c-116">這些位會分別對應至值1、2和4。</span><span class="sxs-lookup"><span data-stu-id="6db5c-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="6db5c-117">Shift 引數表示這些索引鍵的狀態。</span><span class="sxs-lookup"><span data-stu-id="6db5c-117">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="6db5c-118">您可以設定部分、全部或全部的位，表示未按下部分、全部或未按下任何鍵。</span><span class="sxs-lookup"><span data-stu-id="6db5c-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6db5c-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="6db5c-119">Return value</span></span>

<span data-ttu-id="6db5c-120">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6db5c-120">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6db5c-121">備註</span><span class="sxs-lookup"><span data-stu-id="6db5c-121">Remarks</span></span>

<span data-ttu-id="6db5c-122">事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。</span><span class="sxs-lookup"><span data-stu-id="6db5c-122">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="6db5c-123">此參數名稱的類型必須完全如所示，包括大小寫。</span><span class="sxs-lookup"><span data-stu-id="6db5c-123">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="6db5c-124">**Windows Media Player 10** 行動裝置版：不支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="6db5c-124">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="6db5c-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="6db5c-125">Requirements</span></span>



| <span data-ttu-id="6db5c-126">需求</span><span class="sxs-lookup"><span data-stu-id="6db5c-126">Requirement</span></span> | <span data-ttu-id="6db5c-127">值</span><span class="sxs-lookup"><span data-stu-id="6db5c-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6db5c-128">版本</span><span class="sxs-lookup"><span data-stu-id="6db5c-128">Version</span></span><br/> | <span data-ttu-id="6db5c-129">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="6db5c-129">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="6db5c-130">DLL</span><span class="sxs-lookup"><span data-stu-id="6db5c-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="6db5c-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6db5c-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6db5c-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6db5c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6db5c-133">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="6db5c-133">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





