---
description: 當 InkCollector 類別偵測到已關閉的資料指標按鈕時發生。
ms.assetid: 993b84a3-a5ac-4b00-bfb4-26ca1c9727c6
title: 'CursorButtonDown 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 393949be4d7b0f172805aa0b81ce86eac3cf3b3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980667"
---
# <a name="inkoverlaycursorbuttondown-event"></a><span data-ttu-id="d5cdf-103">CursorButtonDown 事件</span><span class="sxs-lookup"><span data-stu-id="d5cdf-103">InkOverlay.CursorButtonDown event</span></span>

<span data-ttu-id="d5cdf-104">當 [**InkCollector 類別**](inkcollector-class.md) 偵測到已關閉的資料指標按鈕時發生。</span><span class="sxs-lookup"><span data-stu-id="d5cdf-104">Occurs when the [**InkCollector Class**](inkcollector-class.md) detects a cursor button that is down.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5cdf-105">語法</span><span class="sxs-lookup"><span data-stu-id="d5cdf-105">Syntax</span></span>


```C++
void CursorButtonDown(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="d5cdf-106">參數</span><span class="sxs-lookup"><span data-stu-id="d5cdf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5cdf-107">資料 *指標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d5cdf-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5cdf-108">產生 [**CursorButtonDown**](inkcollector-cursorbuttondown.md)事件的 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件。</span><span class="sxs-lookup"><span data-stu-id="d5cdf-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorButtonDown**](inkcollector-cursorbuttondown.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="d5cdf-109">*按鈕* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d5cdf-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5cdf-110">已按下的按鈕。</span><span class="sxs-lookup"><span data-stu-id="d5cdf-110">The button that was pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5cdf-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d5cdf-111">Return value</span></span>

<span data-ttu-id="d5cdf-112">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d5cdf-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5cdf-113">備註</span><span class="sxs-lookup"><span data-stu-id="d5cdf-113">Remarks</span></span>

<span data-ttu-id="d5cdf-114">當使用者將畫筆降至數位板並開始追蹤筆劃時，畫筆提示上的按鈕會關閉。</span><span class="sxs-lookup"><span data-stu-id="d5cdf-114">A button on a pen tip is down when the user lowers the pen to the digitizer and starts tracing a stroke.</span></span> <span data-ttu-id="d5cdf-115">當按下按鈕時，會關閉圓柱上的按鈕。</span><span class="sxs-lookup"><span data-stu-id="d5cdf-115">A button on a barrel is down when the button is pressed.</span></span>

<span data-ttu-id="d5cdf-116">當您按下滑鼠右鍵時，您實際上會收到兩個 [**CursorButtonDown**](inkcollector-cursorbuttondown.md) 事件-一個是按下滑鼠右鍵，另一個用於按下滑鼠左鍵。</span><span class="sxs-lookup"><span data-stu-id="d5cdf-116">When you press the right mouse button, you actually receive two [**CursorButtonDown**](inkcollector-cursorbuttondown.md) events - one for right button pressed and one for left button pressed.</span></span>

<span data-ttu-id="d5cdf-117">此事件方法是在 \_ IInkCollectorEvents、 \_ IInkOverlayEvents 和 \_ IInkPictureEvents 分派專用介面中定義， (具有 DISPID ICECursorButtonDown 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5cdf-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorButtonDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5cdf-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5cdf-118">Requirements</span></span>



| <span data-ttu-id="d5cdf-119">需求</span><span class="sxs-lookup"><span data-stu-id="d5cdf-119">Requirement</span></span> | <span data-ttu-id="d5cdf-120">值</span><span class="sxs-lookup"><span data-stu-id="d5cdf-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5cdf-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d5cdf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d5cdf-122">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5cdf-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d5cdf-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d5cdf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d5cdf-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="d5cdf-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d5cdf-125">標頭</span><span class="sxs-lookup"><span data-stu-id="d5cdf-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5cdf-126"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="d5cdf-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d5cdf-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="d5cdf-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="d5cdf-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5cdf-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d5cdf-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5cdf-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5cdf-130">**InkOverlay 類別**</span><span class="sxs-lookup"><span data-stu-id="d5cdf-130">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="d5cdf-131">**CursorDown 事件**</span><span class="sxs-lookup"><span data-stu-id="d5cdf-131">**CursorDown Event**</span></span>](inkcollector-cursordown.md)
</dt> <dt>

[<span data-ttu-id="d5cdf-132">**CursorButtonUp 事件**</span><span class="sxs-lookup"><span data-stu-id="d5cdf-132">**CursorButtonUp Event**</span></span>](inkcollector-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="d5cdf-133">**IInkCursor 介面**</span><span class="sxs-lookup"><span data-stu-id="d5cdf-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="d5cdf-134">**IInkCursorButton 介面**</span><span class="sxs-lookup"><span data-stu-id="d5cdf-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




