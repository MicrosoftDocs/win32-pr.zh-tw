---
title: Player. MouseDown 事件
description: 當使用者按下滑鼠按鍵時，就會發生 MouseDown 事件。 |Player. MouseDown 事件
ms.assetid: cc2fd2ca-c974-4683-98ca-2202c4d5b240
keywords:
- MouseDown 事件 Windows Media Player
- MouseDown 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，MouseDown 事件
topic_type:
- apiref
api_name:
- Player.MouseDown
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29eb0c8aa5f6731f94d0e4c3b4ff967cb7819f42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000403"
---
# <a name="playermousedown-event"></a><span data-ttu-id="06e9b-107">Player. MouseDown 事件</span><span class="sxs-lookup"><span data-stu-id="06e9b-107">Player.MouseDown event</span></span>

<span data-ttu-id="06e9b-108">當使用者按下滑鼠按鍵時，就會發生 **MouseDown** 事件。</span><span class="sxs-lookup"><span data-stu-id="06e9b-108">The **MouseDown** event occurs when the user presses a mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="06e9b-109">語法</span><span class="sxs-lookup"><span data-stu-id="06e9b-109">Syntax</span></span>


```JScript
Player.MouseDown(
  nButton,
  nShiftState,
  fX,
  fY
)
```



## <a name="parameters"></a><span data-ttu-id="06e9b-110">參數</span><span class="sxs-lookup"><span data-stu-id="06e9b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06e9b-111">*nButton*</span><span class="sxs-lookup"><span data-stu-id="06e9b-111">*nButton*</span></span> 
</dt> <dd>

<span data-ttu-id="06e9b-112">**Number** (**int**) 指定位的位位，其位對應于左按鈕 (位 0) ，右按鈕 (位 1) ，中間按鈕 (位 2) 。</span><span class="sxs-lookup"><span data-stu-id="06e9b-112">**Number** (**int**) specifying a bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="06e9b-113">這些位會分別對應至值1、2和4。</span><span class="sxs-lookup"><span data-stu-id="06e9b-113">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="06e9b-114">只會設定其中一個位，表示造成事件的按鈕。</span><span class="sxs-lookup"><span data-stu-id="06e9b-114">Only one of the bits is set, indicating the button that caused the event.</span></span>

</dd> <dt>

<span data-ttu-id="06e9b-115">*nShiftState*</span><span class="sxs-lookup"><span data-stu-id="06e9b-115">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="06e9b-116">**Number** (**int**) 指定具有最少有效位數的位位（對應至 SHIFT 鍵 (BIT 0) 、CTRL 鍵 (位 1) ，以及 ALT 鍵 (位 2) ）。</span><span class="sxs-lookup"><span data-stu-id="06e9b-116">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="06e9b-117">這些位會分別對應至值1、2和4。</span><span class="sxs-lookup"><span data-stu-id="06e9b-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="06e9b-118">Shift 引數表示這些索引鍵的狀態。</span><span class="sxs-lookup"><span data-stu-id="06e9b-118">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="06e9b-119">您可以設定部分、全部或全部的位，表示未按下部分、全部或未按下任何鍵。</span><span class="sxs-lookup"><span data-stu-id="06e9b-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> <dt>

<span data-ttu-id="06e9b-120">*外匯*</span><span class="sxs-lookup"><span data-stu-id="06e9b-120">*fX*</span></span> 
</dt> <dd>

<span data-ttu-id="06e9b-121">**數值** (**long**) 指定滑鼠指標相對於控制項左上角的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="06e9b-121">**Number** (**long**) specifying the x coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> <dt>

<span data-ttu-id="06e9b-122">*財年*</span><span class="sxs-lookup"><span data-stu-id="06e9b-122">*fY*</span></span> 
</dt> <dd>

<span data-ttu-id="06e9b-123">**數值** (**long**) 指定滑鼠指標相對於控制項左上角的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="06e9b-123">**Number** (**long**) specifying the y coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06e9b-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="06e9b-124">Return value</span></span>

<span data-ttu-id="06e9b-125">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="06e9b-125">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="06e9b-126">備註</span><span class="sxs-lookup"><span data-stu-id="06e9b-126">Remarks</span></span>

<span data-ttu-id="06e9b-127">事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。</span><span class="sxs-lookup"><span data-stu-id="06e9b-127">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="06e9b-128">此參數名稱的類型必須完全如所示，包括大小寫。</span><span class="sxs-lookup"><span data-stu-id="06e9b-128">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="06e9b-129">**Windows Media Player 10** 行動裝置版：不支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="06e9b-129">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="06e9b-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="06e9b-130">Requirements</span></span>



| <span data-ttu-id="06e9b-131">需求</span><span class="sxs-lookup"><span data-stu-id="06e9b-131">Requirement</span></span> | <span data-ttu-id="06e9b-132">值</span><span class="sxs-lookup"><span data-stu-id="06e9b-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="06e9b-133">版本</span><span class="sxs-lookup"><span data-stu-id="06e9b-133">Version</span></span><br/> | <span data-ttu-id="06e9b-134">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="06e9b-134">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="06e9b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="06e9b-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="06e9b-136"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06e9b-136"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06e9b-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06e9b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06e9b-138">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="06e9b-138">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





