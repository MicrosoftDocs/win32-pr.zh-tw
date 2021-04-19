---
description: 在辨識系統手勢時發生。
ms.assetid: 36e2ac5a-dc91-47c2-a8e5-e555437c0a5d
title: 'InkPicture.SystemGesture 事件 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 918198e4d18a854bb4238ce9d878dc70ab1f2f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980053"
---
# <a name="inkpicturesystemgesture-event"></a><span data-ttu-id="fa43e-103">InkPicture.SystemGesture 事件</span><span class="sxs-lookup"><span data-stu-id="fa43e-103">InkPicture.SystemGesture event</span></span>

<span data-ttu-id="fa43e-104">在辨識系統手勢時發生。</span><span class="sxs-lookup"><span data-stu-id="fa43e-104">Occurs when a system gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa43e-105">語法</span><span class="sxs-lookup"><span data-stu-id="fa43e-105">Syntax</span></span>


```C++
void SystemGesture(
  [in] IInkCursor       *Cursor,
  [in] InkSystemGesture Id,
  [in] long             X,
  [in] long             Y,
  [in] long             Modifier,
  [in] BSTR             Character,
  [in] long             CursorMode
);
```



## <a name="parameters"></a><span data-ttu-id="fa43e-106">參數</span><span class="sxs-lookup"><span data-stu-id="fa43e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa43e-107">資料 *指標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fa43e-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa43e-108">產生 **SystemGesture** 事件的 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件。</span><span class="sxs-lookup"><span data-stu-id="fa43e-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **SystemGesture** event.</span></span>

</dd> <dt>

<span data-ttu-id="fa43e-109"> \[ 中的識別碼\]</span><span class="sxs-lookup"><span data-stu-id="fa43e-109">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa43e-110">系統手勢的值。</span><span class="sxs-lookup"><span data-stu-id="fa43e-110">The value of the system gesture.</span></span>

</dd> <dt>

<span data-ttu-id="fa43e-111">*X* \[ 于\]</span><span class="sxs-lookup"><span data-stu-id="fa43e-111">*X* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa43e-112">手勢位置的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="fa43e-112">The x-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="fa43e-113">*Y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa43e-113">*Y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa43e-114">手勢位置的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="fa43e-114">The y-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="fa43e-115">*修飾* \[ 詞在\]</span><span class="sxs-lookup"><span data-stu-id="fa43e-115">*Modifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa43e-116">保留的。</span><span class="sxs-lookup"><span data-stu-id="fa43e-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="fa43e-117">*字元* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fa43e-117">*Character* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa43e-118">保留的。</span><span class="sxs-lookup"><span data-stu-id="fa43e-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="fa43e-119">*CursorMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fa43e-119">*CursorMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa43e-120">值，指出 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) 物件為正常模式或橡皮擦模式。</span><span class="sxs-lookup"><span data-stu-id="fa43e-120">A value that indicates whether the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object is in normal mode or eraser mode.</span></span> <span data-ttu-id="fa43e-121">1適用于標準模式，2適用于橡皮擦模式。</span><span class="sxs-lookup"><span data-stu-id="fa43e-121">1 is for normal mode and 2 are for eraser mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa43e-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="fa43e-122">Return value</span></span>

<span data-ttu-id="fa43e-123">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="fa43e-123">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa43e-124">備註</span><span class="sxs-lookup"><span data-stu-id="fa43e-124">Remarks</span></span>

<span data-ttu-id="fa43e-125">系統手勢提供用來建立手勢之 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) 物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fa43e-125">System gestures give information about the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that is being used to create the gesture.</span></span> <span data-ttu-id="fa43e-126">它們也提供滑鼠事件組合的快捷方式，也是偵測滑鼠事件的方式，對效能的影響較小。</span><span class="sxs-lookup"><span data-stu-id="fa43e-126">They also provide shortcuts to combinations of mouse events and are ways to detect mouse events with less impact on performance.</span></span>

<span data-ttu-id="fa43e-127">例如，您可以尋找點一下或 RightTap 系統手勢，而不是尋找 [**MouseUp 事件 \[ InkPicture 控制項 \]**](inkpicture-mouseup.md) / 的 [**MouseDown 事件 \[ InkPicture 控制 \]**](inkpicture-mousedown.md)事件配對。</span><span class="sxs-lookup"><span data-stu-id="fa43e-127">For example, instead of looking for a [**MouseUp Event \[InkPicture Control\]**](inkpicture-mouseup.md)/[**MouseDown Event \[InkPicture Control\]**](inkpicture-mousedown.md) pair of events with no other mouse events occurring in between, you can look for the Tap or RightTap system gestures.</span></span>

<span data-ttu-id="fa43e-128">另一個範例是，而不是接聽 [**\[ InkPicture 控制項 \]**](inkpicture-mousedown.md)mousemove 事件 / [**\[ InkPicture 控制項 \]**](inkpicture-mousemove.md)事件，以及取得許多 **MouseMove 事件 \[ InkPicture 控制 \]** 訊息，只要您對滑鼠的每個位置的 (x，y) 座標都不感興趣，您就可以觀賞拖曳或 RightDrag 系統手勢。</span><span class="sxs-lookup"><span data-stu-id="fa43e-128">As another example, instead of listening for [**MouseDown Event \[InkPicture Control\]**](inkpicture-mousedown.md)/[**MouseMove Event \[InkPicture Control\]**](inkpicture-mousemove.md) events and getting numerous **MouseMove Event \[InkPicture Control\]** messages, you can watch for the Drag or RightDrag system gestures as long as you're not interested in the (x, y) coordinates of every position of the mouse.</span></span> <span data-ttu-id="fa43e-129">這可讓您只接收一個訊息，而不是多個 **MouseMove 事件 \[ InkPicture 控制 \]** 訊息。</span><span class="sxs-lookup"><span data-stu-id="fa43e-129">This allows you to receive only one message instead of numerous **MouseMove Event \[InkPicture Control\]** messages.</span></span>

<span data-ttu-id="fa43e-130">如需特定系統手勢的清單，請參閱 [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) 列舉型別。</span><span class="sxs-lookup"><span data-stu-id="fa43e-130">For a list of specific system gestures, see the [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) enumeration type.</span></span> <span data-ttu-id="fa43e-131">如需系統手勢的詳細資訊，請參閱在[TABLET PC 上](/previous-versions//dd314533(v=vs.85))[使用筆勢](using-gestures.md)和命令輸入。</span><span class="sxs-lookup"><span data-stu-id="fa43e-131">For more information about system gestures, see [Using Gestures](using-gestures.md) and [Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85)).</span></span>

<span data-ttu-id="fa43e-132">此事件方法是在 **\_ IInkCollectorEvents**、 **\_ IInkOverlayEvents** 和 **\_ IInkPictureEvents** 分派專用介面中定義， (具有 DISPID ICESystemGesture 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="fa43e-132">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICESystemGesture.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa43e-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa43e-133">Requirements</span></span>



| <span data-ttu-id="fa43e-134">需求</span><span class="sxs-lookup"><span data-stu-id="fa43e-134">Requirement</span></span> | <span data-ttu-id="fa43e-135">值</span><span class="sxs-lookup"><span data-stu-id="fa43e-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa43e-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa43e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="fa43e-137">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa43e-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="fa43e-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa43e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="fa43e-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="fa43e-139">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="fa43e-140">標頭</span><span class="sxs-lookup"><span data-stu-id="fa43e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa43e-141"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="fa43e-141"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fa43e-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="fa43e-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="fa43e-143"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa43e-143"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="fa43e-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa43e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa43e-145">InkPicture</span><span class="sxs-lookup"><span data-stu-id="fa43e-145">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="fa43e-146">**InkSystemGesture 列舉**</span><span class="sxs-lookup"><span data-stu-id="fa43e-146">**InkSystemGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[<span data-ttu-id="fa43e-147">使用手勢</span><span class="sxs-lookup"><span data-stu-id="fa43e-147">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

