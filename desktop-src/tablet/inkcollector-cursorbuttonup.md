---
description: InkCollector. CursorButtonUp 事件-當 InkCollector 偵測到已啟動的資料指標按鈕時，就會發生此事件。
ms.assetid: f07daad7-e0d1-45cf-a708-5486a5dfda8b
title: 'InkCollector. CursorButtonUp 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 936b050c64d07a6957039278f0455bc71d77dbdf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110306"
---
# <a name="inkcollectorcursorbuttonup-event"></a><span data-ttu-id="085e9-103">InkCollector. CursorButtonUp 事件</span><span class="sxs-lookup"><span data-stu-id="085e9-103">InkCollector.CursorButtonUp event</span></span>

<span data-ttu-id="085e9-104">當 [**InkCollector**](inkcollector-class.md) 偵測到已啟動的資料指標按鈕時發生。</span><span class="sxs-lookup"><span data-stu-id="085e9-104">Occurs when the [**InkCollector**](inkcollector-class.md) detects a cursor button that is up.</span></span>

## <a name="syntax"></a><span data-ttu-id="085e9-105">語法</span><span class="sxs-lookup"><span data-stu-id="085e9-105">Syntax</span></span>


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="085e9-106">參數</span><span class="sxs-lookup"><span data-stu-id="085e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="085e9-107">資料 *指標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="085e9-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="085e9-108">產生 **CursorButtonUp** 事件的 [**IInkCursor 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件。</span><span class="sxs-lookup"><span data-stu-id="085e9-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorButtonUp** event.</span></span>

</dd> <dt>

<span data-ttu-id="085e9-109">*按鈕* \[在\]</span><span class="sxs-lookup"><span data-stu-id="085e9-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="085e9-110">已發行的按鈕。</span><span class="sxs-lookup"><span data-stu-id="085e9-110">The button that was released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="085e9-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="085e9-111">Return value</span></span>

<span data-ttu-id="085e9-112">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="085e9-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="085e9-113">備註</span><span class="sxs-lookup"><span data-stu-id="085e9-113">Remarks</span></span>

<span data-ttu-id="085e9-114">當使用者完成筆觸並將畫筆從數位板中提起時，畫筆提示上的按鈕就會啟動。</span><span class="sxs-lookup"><span data-stu-id="085e9-114">A button on a pen tip is up when the user completes a stroke and lifts the pen from the digitizer.</span></span> <span data-ttu-id="085e9-115">當未按下按鈕時，會開啟張圓柱上的按鈕。</span><span class="sxs-lookup"><span data-stu-id="085e9-115">A button on a barrel is up when the button is not pressed.</span></span>

<span data-ttu-id="085e9-116">當您放開滑鼠右鍵時，您實際上會收到兩個 **CursorButtonUp** 事件：一個用於右按鈕，另一個用於左按鈕。</span><span class="sxs-lookup"><span data-stu-id="085e9-116">When you release the right mouse button, you actually receive two **CursorButtonUp** events - one for right button up and one for left button up.</span></span>

<span data-ttu-id="085e9-117">此事件方法是在 \_ IInkCollectorEvents、 \_ IInkOverlayEvents 和 \_ IInkPictureEvents 分派專用介面中定義， (具有 DISPID ICECursorButtonUp 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="085e9-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorButtonUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="085e9-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="085e9-118">Requirements</span></span>



| <span data-ttu-id="085e9-119">需求</span><span class="sxs-lookup"><span data-stu-id="085e9-119">Requirement</span></span> | <span data-ttu-id="085e9-120">值</span><span class="sxs-lookup"><span data-stu-id="085e9-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="085e9-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="085e9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="085e9-122">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="085e9-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="085e9-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="085e9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="085e9-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="085e9-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="085e9-125">標頭</span><span class="sxs-lookup"><span data-stu-id="085e9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="085e9-126"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="085e9-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="085e9-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="085e9-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="085e9-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="085e9-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="085e9-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="085e9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="085e9-130">**InkCollector 類別**</span><span class="sxs-lookup"><span data-stu-id="085e9-130">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="085e9-131">**CursorButtonDown 事件**</span><span class="sxs-lookup"><span data-stu-id="085e9-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="085e9-132">**CursorDown 事件**</span><span class="sxs-lookup"><span data-stu-id="085e9-132">**CursorDown Event**</span></span>](inkcollector-cursordown.md)
</dt> <dt>

[<span data-ttu-id="085e9-133">**IInkCursor 介面**</span><span class="sxs-lookup"><span data-stu-id="085e9-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="085e9-134">**IInkCursorButton 介面**</span><span class="sxs-lookup"><span data-stu-id="085e9-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




