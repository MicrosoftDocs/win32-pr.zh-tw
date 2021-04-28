---
description: InkOverlay.SystemGesture 事件-在辨識系統手勢時發生。
ms.assetid: 6f82b234-2088-4207-a6b4-6c6919623d6a
title: 'InkOverlay.SystemGesture 事件 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3498d6b5fa779f6a15866ac93d53be8348f3d1a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086666"
---
# <a name="inkoverlaysystemgesture-event"></a><span data-ttu-id="c8caa-103">InkOverlay.SystemGesture 事件</span><span class="sxs-lookup"><span data-stu-id="c8caa-103">InkOverlay.SystemGesture event</span></span>

<span data-ttu-id="c8caa-104">在辨識系統手勢時發生。</span><span class="sxs-lookup"><span data-stu-id="c8caa-104">Occurs when a system gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8caa-105">語法</span><span class="sxs-lookup"><span data-stu-id="c8caa-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="c8caa-106">參數</span><span class="sxs-lookup"><span data-stu-id="c8caa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8caa-107">資料 *指標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8caa-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8caa-108">產生 [**SystemGesture**](inkcollector-systemgesture.md)事件的 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件。</span><span class="sxs-lookup"><span data-stu-id="c8caa-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**SystemGesture**](inkcollector-systemgesture.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="c8caa-109"> \[ 中的識別碼\]</span><span class="sxs-lookup"><span data-stu-id="c8caa-109">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8caa-110">系統手勢的值。</span><span class="sxs-lookup"><span data-stu-id="c8caa-110">The value of the system gesture.</span></span>

</dd> <dt>

<span data-ttu-id="c8caa-111">*X* \[ 于\]</span><span class="sxs-lookup"><span data-stu-id="c8caa-111">*X* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8caa-112">手勢位置的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="c8caa-112">The x-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="c8caa-113">*Y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8caa-113">*Y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8caa-114">手勢位置的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="c8caa-114">The y-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="c8caa-115">*修飾* \[ 詞在\]</span><span class="sxs-lookup"><span data-stu-id="c8caa-115">*Modifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8caa-116">保留的。</span><span class="sxs-lookup"><span data-stu-id="c8caa-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="c8caa-117">*字元* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8caa-117">*Character* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8caa-118">保留的。</span><span class="sxs-lookup"><span data-stu-id="c8caa-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="c8caa-119">*CursorMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8caa-119">*CursorMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8caa-120">值，指出 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) 物件為正常模式或橡皮擦模式。</span><span class="sxs-lookup"><span data-stu-id="c8caa-120">A value that indicates whether the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object is in normal mode or eraser mode.</span></span> <span data-ttu-id="c8caa-121">1適用于標準模式，2適用于橡皮擦模式。</span><span class="sxs-lookup"><span data-stu-id="c8caa-121">1 is for normal mode and 2 are for eraser mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8caa-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8caa-122">Return value</span></span>

<span data-ttu-id="c8caa-123">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c8caa-123">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8caa-124">備註</span><span class="sxs-lookup"><span data-stu-id="c8caa-124">Remarks</span></span>

<span data-ttu-id="c8caa-125">系統手勢很有用，因為它們會提供用來建立手勢之 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) 物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c8caa-125">System gestures are useful because they give information about the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that is being used to create the gesture.</span></span> <span data-ttu-id="c8caa-126">它們也提供滑鼠事件組合的快捷方式，並以「更便宜」的方式偵測滑鼠事件。</span><span class="sxs-lookup"><span data-stu-id="c8caa-126">They also provide shortcuts to combinations of mouse events and are "cheaper" ways to detect mouse events.</span></span>

<span data-ttu-id="c8caa-127">例如，您可以尋找 [點一下 [](inkcollector-mouseup.md)] 或 [RightTap 系統] 手勢，而不是尋找  /  不是在兩者之間發生其他滑鼠事件 [](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)的 MouseUp 事件 [**MouseDown 事件**](inkcollector-mousedown.md)。</span><span class="sxs-lookup"><span data-stu-id="c8caa-127">For example, instead of looking for a [**MouseUp Event**](inkcollector-mouseup.md) / [**MouseDown Event**](inkcollector-mousedown.md) pair of events with no other mouse events occurring in between, you can look for the [**Tap**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) or **RightTap** system gestures.</span></span>

<span data-ttu-id="c8caa-128">另一個範例是，您不需要接聽 [**MouseDown 事件**](inkcollector-mousedown.md)  /  [**MouseMove 事件**](inkcollector-mousemove.md)事件，也可以取得許多 **MouseMove 事件** 訊息，只要您對滑鼠的每個位置 (x，y) 座標都不感興趣，就可以觀賞 [**拖曳**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)或 **RightDrag** 系統手勢。</span><span class="sxs-lookup"><span data-stu-id="c8caa-128">As another example, instead of listening for [**MouseDown Event**](inkcollector-mousedown.md) / [**MouseMove Event**](inkcollector-mousemove.md) events and getting numerous **MouseMove Event** messages, you can watch for the [**Drag**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) or **RightDrag** system gestures as long as you're not interested in the (x, y) coordinates of every position of the mouse.</span></span> <span data-ttu-id="c8caa-129">這可讓您只接收一個訊息，而不是多個 **MouseMove 事件** 訊息。</span><span class="sxs-lookup"><span data-stu-id="c8caa-129">This allows you to receive only one message instead of numerous **MouseMove Event** messages.</span></span>

<span data-ttu-id="c8caa-130">如需特定系統手勢的清單，請參閱 [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) 列舉型別。</span><span class="sxs-lookup"><span data-stu-id="c8caa-130">For a list of specific system gestures, see the [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) enumeration type.</span></span> <span data-ttu-id="c8caa-131">如需系統手勢的詳細資訊，請參閱在[TABLET PC 上](/previous-versions//dd314533(v=vs.85))[使用筆勢](using-gestures.md)和命令輸入。</span><span class="sxs-lookup"><span data-stu-id="c8caa-131">For more information about system gestures, see [Using Gestures](using-gestures.md) and [Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85)).</span></span>

<span data-ttu-id="c8caa-132">此事件方法是在 \_ IInkCollectorEvents、 \_ IInkOverlayEvents 和 \_ IInkPictureEvents 分派專用介面中定義， (具有 DISPID ICESystemGesture 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="c8caa-132">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICESystemGesture.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8caa-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8caa-133">Requirements</span></span>



| <span data-ttu-id="c8caa-134">需求</span><span class="sxs-lookup"><span data-stu-id="c8caa-134">Requirement</span></span> | <span data-ttu-id="c8caa-135">值</span><span class="sxs-lookup"><span data-stu-id="c8caa-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8caa-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c8caa-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c8caa-137">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8caa-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c8caa-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c8caa-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c8caa-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="c8caa-139">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="c8caa-140">標頭</span><span class="sxs-lookup"><span data-stu-id="c8caa-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8caa-141"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="c8caa-141"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c8caa-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="c8caa-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="c8caa-143"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8caa-143"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="c8caa-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8caa-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8caa-145">**InkOverlay 類別**</span><span class="sxs-lookup"><span data-stu-id="c8caa-145">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="c8caa-146">**InkSystemGesture 列舉**</span><span class="sxs-lookup"><span data-stu-id="c8caa-146">**InkSystemGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[<span data-ttu-id="c8caa-147">**IInkCursor 介面**</span><span class="sxs-lookup"><span data-stu-id="c8caa-147">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="c8caa-148">使用手勢</span><span class="sxs-lookup"><span data-stu-id="c8caa-148">Using Gestures</span></span>](using-gestures.md)
</dt> <dt>

[<span data-ttu-id="c8caa-149">畫筆輸入、筆跡和辨識</span><span class="sxs-lookup"><span data-stu-id="c8caa-149">Pen Input, Ink, and Recognition</span></span>](pen-input--ink--and-recognition.md)
</dt> <dt>

<span data-ttu-id="c8caa-150">[Tablet PC 上的命令輸入](/previous-versions//dd314533(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c8caa-150">[Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85))</span></span>
</dt> </dl>

 

