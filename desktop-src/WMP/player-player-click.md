---
title: Player. 按一下事件
description: 當使用者按一下滑鼠按鍵時，就會發生 Click 事件。
ms.assetid: c2d5fab9-9b53-4d0c-a001-8cbf4430e713
keywords:
- 按一下事件 Windows Media Player
- Click event Windows Media Player，Player 類別
- Player 類別 Windows Media Player、Click 事件
topic_type:
- apiref
api_name:
- Player.Click
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8389460d59018b221749719d32edbaa89943808
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994096"
---
# <a name="playerclick-event"></a><span data-ttu-id="cfbd5-106">Player. 按一下事件</span><span class="sxs-lookup"><span data-stu-id="cfbd5-106">Player.Click event</span></span>

<span data-ttu-id="cfbd5-107">當使用者按一下滑鼠按鍵時，就會發生 **Click** 事件。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-107">The **Click** event occurs when the user clicks a mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfbd5-108">語法</span><span class="sxs-lookup"><span data-stu-id="cfbd5-108">Syntax</span></span>


```JScript
Player.Click(
  nButton,
  nShiftState,
  fX,
  fY
)
```



## <a name="parameters"></a><span data-ttu-id="cfbd5-109">參數</span><span class="sxs-lookup"><span data-stu-id="cfbd5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfbd5-110">*nButton*</span><span class="sxs-lookup"><span data-stu-id="cfbd5-110">*nButton*</span></span> 
</dt> <dd>

<span data-ttu-id="cfbd5-111">**Number** (**int**) 指定位的位位，其位對應于左按鈕 (位 0) ，右按鈕 (位 1) ，中間按鈕 (位 2) 。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-111">**Number** (**int**) specifying a bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="cfbd5-112">這些位會分別對應至值1、2和4。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-112">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="cfbd5-113">只會設定其中一個位，表示造成事件的按鈕。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-113">Only one of the bits is set, indicating the button that caused the event.</span></span>

</dd> <dt>

<span data-ttu-id="cfbd5-114">*nShiftState*</span><span class="sxs-lookup"><span data-stu-id="cfbd5-114">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="cfbd5-115">**Number** (**int**) 指定具有最少有效位數的位位（對應至 SHIFT 鍵 (BIT 0) 、CTRL 鍵 (位 1) ，以及 ALT 鍵 (位 2) ）。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-115">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="cfbd5-116">這些位會分別對應至值1、2和4。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="cfbd5-117">Shift 引數表示這些索引鍵的狀態。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-117">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="cfbd5-118">您可以設定部分、全部或全部的位，表示未按下部分、全部或未按下任何鍵。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> <dt>

<span data-ttu-id="cfbd5-119">*外匯*</span><span class="sxs-lookup"><span data-stu-id="cfbd5-119">*fX*</span></span> 
</dt> <dd>

<span data-ttu-id="cfbd5-120">**數值** (**long**) 指定滑鼠指標相對於控制項左上角的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-120">**Number** (**long**) specifying the x coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> <dt>

<span data-ttu-id="cfbd5-121">*財年*</span><span class="sxs-lookup"><span data-stu-id="cfbd5-121">*fY*</span></span> 
</dt> <dd>

<span data-ttu-id="cfbd5-122">**數值** (**long**) 指定滑鼠指標相對於控制項左上角的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-122">**Number** (**long**) specifying the y coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfbd5-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="cfbd5-123">Return value</span></span>

<span data-ttu-id="cfbd5-124">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-124">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfbd5-125">備註</span><span class="sxs-lookup"><span data-stu-id="cfbd5-125">Remarks</span></span>

<span data-ttu-id="cfbd5-126">事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-126">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="cfbd5-127">此參數名稱的類型必須完全如所示，包括大小寫。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-127">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="cfbd5-128">**Windows Media Player 10** 行動裝置版：不支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-128">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfbd5-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="cfbd5-129">Requirements</span></span>



| <span data-ttu-id="cfbd5-130">需求</span><span class="sxs-lookup"><span data-stu-id="cfbd5-130">Requirement</span></span> | <span data-ttu-id="cfbd5-131">值</span><span class="sxs-lookup"><span data-stu-id="cfbd5-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cfbd5-132">版本</span><span class="sxs-lookup"><span data-stu-id="cfbd5-132">Version</span></span><br/> | <span data-ttu-id="cfbd5-133">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-133">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="cfbd5-134">DLL</span><span class="sxs-lookup"><span data-stu-id="cfbd5-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="cfbd5-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfbd5-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfbd5-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cfbd5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfbd5-137">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="cfbd5-137">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





