---
description: PossiblyEatMessage 方法會將鍵盤和滑鼠訊息轉送至訊息清空視窗。
ms.assetid: 8e344c5d-2f94-454f-89b7-45c539b6e833
title: 'CBaseControlWindow. PossiblyEatMessage 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.PossiblyEatMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9bfadcfbbd6833d8f3e9b65bd39d0cdbef4a006e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990604"
---
# <a name="cbasecontrolwindowpossiblyeatmessage-method"></a><span data-ttu-id="e72f7-103">CBaseControlWindow. PossiblyEatMessage 方法</span><span class="sxs-lookup"><span data-stu-id="e72f7-103">CBaseControlWindow.PossiblyEatMessage method</span></span>

<span data-ttu-id="e72f7-104">方法會將 `PossiblyEatMessage` 鍵盤和滑鼠訊息轉送至訊息清空視窗。</span><span class="sxs-lookup"><span data-stu-id="e72f7-104">The `PossiblyEatMessage` method forwards keyboard and mouse messages to the message-drain window.</span></span>

## <a name="syntax"></a><span data-ttu-id="e72f7-105">語法</span><span class="sxs-lookup"><span data-stu-id="e72f7-105">Syntax</span></span>


```C++
BOOL PossiblyEatMessage(
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="e72f7-106">參數</span><span class="sxs-lookup"><span data-stu-id="e72f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e72f7-107">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="e72f7-107">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="e72f7-108">視窗訊息。</span><span class="sxs-lookup"><span data-stu-id="e72f7-108">Window message.</span></span>

</dd> <dt>

<span data-ttu-id="e72f7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e72f7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e72f7-110">第一個訊息參數。</span><span class="sxs-lookup"><span data-stu-id="e72f7-110">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e72f7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e72f7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e72f7-112">第二個訊息參數。</span><span class="sxs-lookup"><span data-stu-id="e72f7-112">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e72f7-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e72f7-113">Return value</span></span>

<span data-ttu-id="e72f7-114">如果訊息已轉送至視窗，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="e72f7-114">Returns **TRUE** if the message was forwarded to the window, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e72f7-115">備註</span><span class="sxs-lookup"><span data-stu-id="e72f7-115">Remarks</span></span>

<span data-ttu-id="e72f7-116">[訊息清空] 視窗是指定用來接收特定滑鼠和鍵盤訊息的視窗。</span><span class="sxs-lookup"><span data-stu-id="e72f7-116">The message-drain window is a window designated to receive certain mouse and keyboard messages.</span></span> <span data-ttu-id="e72f7-117">視窗一開始是 **Null**;您可以藉由呼叫 [**CBaseControlWindow：:p 的 \_ MessageDrain**](cbasecontrolwindow-put-messagedrain.md)來設定它。</span><span class="sxs-lookup"><span data-stu-id="e72f7-117">Initially the window is **NULL**; it can be set by calling [**CBaseControlWindow::put\_MessageDrain**](cbasecontrolwindow-put-messagedrain.md).</span></span>

<span data-ttu-id="e72f7-118">如果訊息清空視窗為非 **Null**，則會將 `PossiblyEatMessage` 下列訊息張貼至該視窗：</span><span class="sxs-lookup"><span data-stu-id="e72f7-118">If the message-drain window is non-**NULL**, `PossiblyEatMessage` posts the following messages to that window:</span></span>

-   <span data-ttu-id="e72f7-119">WM \_ 字元</span><span class="sxs-lookup"><span data-stu-id="e72f7-119">WM\_CHAR</span></span>
-   <span data-ttu-id="e72f7-120">WM \_ DEADCHAR</span><span class="sxs-lookup"><span data-stu-id="e72f7-120">WM\_DEADCHAR</span></span>
-   <span data-ttu-id="e72f7-121">WM \_ KEYDOWN</span><span class="sxs-lookup"><span data-stu-id="e72f7-121">WM\_KEYDOWN</span></span>
-   <span data-ttu-id="e72f7-122">WM \_ KEYUP</span><span class="sxs-lookup"><span data-stu-id="e72f7-122">WM\_KEYUP</span></span>
-   <span data-ttu-id="e72f7-123">WM \_ LBUTTONDBLCLK</span><span class="sxs-lookup"><span data-stu-id="e72f7-123">WM\_LBUTTONDBLCLK</span></span>
-   <span data-ttu-id="e72f7-124">WM \_ LBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="e72f7-124">WM\_LBUTTONDOWN</span></span>
-   <span data-ttu-id="e72f7-125">WM \_ LBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="e72f7-125">WM\_LBUTTONUP</span></span>
-   <span data-ttu-id="e72f7-126">WM \_ MBUTTONDBLCLK</span><span class="sxs-lookup"><span data-stu-id="e72f7-126">WM\_MBUTTONDBLCLK</span></span>
-   <span data-ttu-id="e72f7-127">WM \_ MBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="e72f7-127">WM\_MBUTTONDOWN</span></span>
-   <span data-ttu-id="e72f7-128">WM \_ MBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="e72f7-128">WM\_MBUTTONUP</span></span>
-   <span data-ttu-id="e72f7-129">WM \_ MOUSEACTI加值稅E</span><span class="sxs-lookup"><span data-stu-id="e72f7-129">WM\_MOUSEACTIVATE</span></span>
-   <span data-ttu-id="e72f7-130">WM \_ MOUSEMOVE</span><span class="sxs-lookup"><span data-stu-id="e72f7-130">WM\_MOUSEMOVE</span></span>
-   <span data-ttu-id="e72f7-131">WM \_ NCLBUTTONDBLCLK</span><span class="sxs-lookup"><span data-stu-id="e72f7-131">WM\_NCLBUTTONDBLCLK</span></span>
-   <span data-ttu-id="e72f7-132">WM \_ NCLBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="e72f7-132">WM\_NCLBUTTONDOWN</span></span>
-   <span data-ttu-id="e72f7-133">WM \_ NCLBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="e72f7-133">WM\_NCLBUTTONUP</span></span>
-   <span data-ttu-id="e72f7-134">WM \_ NCMBUTTONDBLCLK</span><span class="sxs-lookup"><span data-stu-id="e72f7-134">WM\_NCMBUTTONDBLCLK</span></span>
-   <span data-ttu-id="e72f7-135">WM \_ NCMBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="e72f7-135">WM\_NCMBUTTONDOWN</span></span>
-   <span data-ttu-id="e72f7-136">WM \_ NCMBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="e72f7-136">WM\_NCMBUTTONUP</span></span>
-   <span data-ttu-id="e72f7-137">WM \_ NCMOUSEMOVE</span><span class="sxs-lookup"><span data-stu-id="e72f7-137">WM\_NCMOUSEMOVE</span></span>
-   <span data-ttu-id="e72f7-138">WM \_ NCRBUTTONDBLCLK</span><span class="sxs-lookup"><span data-stu-id="e72f7-138">WM\_NCRBUTTONDBLCLK</span></span>
-   <span data-ttu-id="e72f7-139">WM \_ NCRBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="e72f7-139">WM\_NCRBUTTONDOWN</span></span>
-   <span data-ttu-id="e72f7-140">WM \_ NCRBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="e72f7-140">WM\_NCRBUTTONUP</span></span>
-   <span data-ttu-id="e72f7-141">WM \_ RBUTTONDBLCLK</span><span class="sxs-lookup"><span data-stu-id="e72f7-141">WM\_RBUTTONDBLCLK</span></span>
-   <span data-ttu-id="e72f7-142">WM \_ RBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="e72f7-142">WM\_RBUTTONDOWN</span></span>
-   <span data-ttu-id="e72f7-143">WM \_ RBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="e72f7-143">WM\_RBUTTONUP</span></span>
-   <span data-ttu-id="e72f7-144">WM \_ SYSCHAR</span><span class="sxs-lookup"><span data-stu-id="e72f7-144">WM\_SYSCHAR</span></span>
-   <span data-ttu-id="e72f7-145">WM \_ SYSDEADCHAR</span><span class="sxs-lookup"><span data-stu-id="e72f7-145">WM\_SYSDEADCHAR</span></span>
-   <span data-ttu-id="e72f7-146">WM \_ SYSKEYDOWN</span><span class="sxs-lookup"><span data-stu-id="e72f7-146">WM\_SYSKEYDOWN</span></span>
-   <span data-ttu-id="e72f7-147">WM \_ SYSKEYUP</span><span class="sxs-lookup"><span data-stu-id="e72f7-147">WM\_SYSKEYUP</span></span>

<span data-ttu-id="e72f7-148">它會忽略其他訊息。</span><span class="sxs-lookup"><span data-stu-id="e72f7-148">It ignores other messages.</span></span> <span data-ttu-id="e72f7-149">如果訊息清空視窗為 **Null**，則方法會忽略所有視窗訊息。</span><span class="sxs-lookup"><span data-stu-id="e72f7-149">If the message-drain window is **NULL**, the method ignores all window messages.</span></span> <span data-ttu-id="e72f7-150">如果它張貼訊息，方法會傳回 **TRUE** ，否則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="e72f7-150">The method returns **TRUE** if it posts the message, or **FALSE** otherwise.</span></span> <span data-ttu-id="e72f7-151">**CBaseWindow** 類別會在收到視窗訊息時呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="e72f7-151">The **CBaseWindow** class calls this method when it receives a window message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e72f7-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="e72f7-152">Requirements</span></span>



| <span data-ttu-id="e72f7-153">需求</span><span class="sxs-lookup"><span data-stu-id="e72f7-153">Requirement</span></span> | <span data-ttu-id="e72f7-154">值</span><span class="sxs-lookup"><span data-stu-id="e72f7-154">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e72f7-155">標頭</span><span class="sxs-lookup"><span data-stu-id="e72f7-155">Header</span></span><br/>  | <dl> <span data-ttu-id="e72f7-156"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e72f7-156"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e72f7-157">程式庫</span><span class="sxs-lookup"><span data-stu-id="e72f7-157">Library</span></span><br/> | <dl> <span data-ttu-id="e72f7-158"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e72f7-158"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e72f7-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e72f7-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e72f7-160">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="e72f7-160">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




