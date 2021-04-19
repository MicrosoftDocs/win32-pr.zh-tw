---
description: NotifyOwnerMessage 方法會將特定訊息傳遞至影片視窗。
ms.assetid: 8b27281a-5b8a-46c3-aa66-390d4496f30e
title: 'CBaseControlWindow. NotifyOwnerMessage 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.NotifyOwnerMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9073d37987404849ba8aa3acbda9919df840b410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001221"
---
# <a name="cbasecontrolwindownotifyownermessage-method"></a><span data-ttu-id="54a1b-103">CBaseControlWindow. NotifyOwnerMessage 方法</span><span class="sxs-lookup"><span data-stu-id="54a1b-103">CBaseControlWindow.NotifyOwnerMessage method</span></span>

<span data-ttu-id="54a1b-104">方法會將 `NotifyOwnerMessage` 特定訊息傳遞至影片視窗。</span><span class="sxs-lookup"><span data-stu-id="54a1b-104">The `NotifyOwnerMessage` method passes along specific messages to the video window.</span></span>

## <a name="syntax"></a><span data-ttu-id="54a1b-105">語法</span><span class="sxs-lookup"><span data-stu-id="54a1b-105">Syntax</span></span>


```C++
HRESULT NotifyOwnerMessage(
   long     hwnd,
   long     uMsg,
   LONG_PTR wParam,
   LONG_PTR lParam
);
```



## <a name="parameters"></a><span data-ttu-id="54a1b-106">參數</span><span class="sxs-lookup"><span data-stu-id="54a1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54a1b-107">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="54a1b-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="54a1b-108">影片視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="54a1b-108">Handle to the video window.</span></span>

</dd> <dt>

<span data-ttu-id="54a1b-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="54a1b-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="54a1b-110">訊息詳細資料。</span><span class="sxs-lookup"><span data-stu-id="54a1b-110">Message details.</span></span>

</dd> <dt>

<span data-ttu-id="54a1b-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="54a1b-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54a1b-112">第一個訊息參數。</span><span class="sxs-lookup"><span data-stu-id="54a1b-112">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="54a1b-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54a1b-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54a1b-114">第二個訊息參數。</span><span class="sxs-lookup"><span data-stu-id="54a1b-114">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54a1b-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="54a1b-115">Return value</span></span>

<span data-ttu-id="54a1b-116">不傳回任何 \_ 錯誤。</span><span class="sxs-lookup"><span data-stu-id="54a1b-116">Returns NO\_ERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="54a1b-117">備註</span><span class="sxs-lookup"><span data-stu-id="54a1b-117">Remarks</span></span>

<span data-ttu-id="54a1b-118">當影片視窗是另一個視窗的子系時，不會收到特定的最上層視窗訊息。</span><span class="sxs-lookup"><span data-stu-id="54a1b-118">When the video window is a child of another window, it does not receive certain top-level window messages.</span></span> <span data-ttu-id="54a1b-119">這些訊息可能對轉譯器很有價值，因為它們可能會影響其行為。</span><span class="sxs-lookup"><span data-stu-id="54a1b-119">These messages can be valuable to a renderer, because they could affect its behavior.</span></span> <span data-ttu-id="54a1b-120">`NotifyOwnerMessage` 將下列任何訊息傳遞至影片視窗。</span><span class="sxs-lookup"><span data-stu-id="54a1b-120">`NotifyOwnerMessage` passes any of the following messages to the video window.</span></span>

-   <span data-ttu-id="54a1b-121">WM \_ ACTI加值稅EAPP</span><span class="sxs-lookup"><span data-stu-id="54a1b-121">WM\_ACTIVATEAPP</span></span>
-   <span data-ttu-id="54a1b-122">WM \_ DEVMODECHANGE</span><span class="sxs-lookup"><span data-stu-id="54a1b-122">WM\_DEVMODECHANGE</span></span>
-   <span data-ttu-id="54a1b-123">WM \_ DISPLAYCHANGE</span><span class="sxs-lookup"><span data-stu-id="54a1b-123">WM\_DISPLAYCHANGE</span></span>
-   <span data-ttu-id="54a1b-124">WM \_ PALETTECHANGED</span><span class="sxs-lookup"><span data-stu-id="54a1b-124">WM\_PALETTECHANGED</span></span>
-   <span data-ttu-id="54a1b-125">WM \_ PALETTEISCHANGING</span><span class="sxs-lookup"><span data-stu-id="54a1b-125">WM\_PALETTEISCHANGING</span></span>
-   <span data-ttu-id="54a1b-126">WM \_ QUERYNEWPALETTE</span><span class="sxs-lookup"><span data-stu-id="54a1b-126">WM\_QUERYNEWPALETTE</span></span>
-   <span data-ttu-id="54a1b-127">WM \_ SYSCOLORCHANGE</span><span class="sxs-lookup"><span data-stu-id="54a1b-127">WM\_SYSCOLORCHANGE</span></span>

<span data-ttu-id="54a1b-128">您可以要求 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) 外掛程式散發者 (PID) 讓視窗變成另一個視窗的子系。</span><span class="sxs-lookup"><span data-stu-id="54a1b-128">You can request that the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) plug-in distributor (PID) make a window become a child of another window.</span></span> <span data-ttu-id="54a1b-129">發生這種情況時，PID 會尋找可能傳送至主控視窗的特定訊息。</span><span class="sxs-lookup"><span data-stu-id="54a1b-129">When this occurs, the PID will look for certain messages that might be sent to the owning window.</span></span> <span data-ttu-id="54a1b-130">然後，PID 會將這些訊息轉送到擁有的視窗。</span><span class="sxs-lookup"><span data-stu-id="54a1b-130">The PID will then forward those messages to the owned window.</span></span> <span data-ttu-id="54a1b-131">訊息的預設處理方式是藉由呼叫 Win32 **SendMessage** 函式，以同步方式將訊息傳送到擁有的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="54a1b-131">The default processing for the messages is to send them to the owned window procedure synchronously by calling the Win32 **SendMessage** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="54a1b-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="54a1b-132">Requirements</span></span>



| <span data-ttu-id="54a1b-133">需求</span><span class="sxs-lookup"><span data-stu-id="54a1b-133">Requirement</span></span> | <span data-ttu-id="54a1b-134">值</span><span class="sxs-lookup"><span data-stu-id="54a1b-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54a1b-135">標頭</span><span class="sxs-lookup"><span data-stu-id="54a1b-135">Header</span></span><br/>  | <dl> <span data-ttu-id="54a1b-136"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="54a1b-136"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="54a1b-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="54a1b-137">Library</span></span><br/> | <dl> <span data-ttu-id="54a1b-138"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="54a1b-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54a1b-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54a1b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54a1b-140">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="54a1b-140">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




