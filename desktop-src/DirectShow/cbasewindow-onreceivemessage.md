---
description: OnReceiveMessage 方法會處理視窗訊息。
ms.assetid: 0f074f9b-00e5-42ff-a491-020d441acad1
title: 'CBaseWindow. OnReceiveMessage 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnReceiveMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: defef9a7ca24d6875eda508989615f308a2385b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982549"
---
# <a name="cbasewindowonreceivemessage-method"></a><span data-ttu-id="cc442-103">CBaseWindow. OnReceiveMessage 方法</span><span class="sxs-lookup"><span data-stu-id="cc442-103">CBaseWindow.OnReceiveMessage method</span></span>

<span data-ttu-id="cc442-104">`OnReceiveMessage`方法會處理視窗訊息。</span><span class="sxs-lookup"><span data-stu-id="cc442-104">The `OnReceiveMessage` method handles window messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc442-105">語法</span><span class="sxs-lookup"><span data-stu-id="cc442-105">Syntax</span></span>


```C++
virtual LRESULT OnReceiveMessage(
   HWND   hwnd,
   INT    uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="cc442-106">參數</span><span class="sxs-lookup"><span data-stu-id="cc442-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc442-107">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="cc442-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="cc442-108">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="cc442-108">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="cc442-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="cc442-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="cc442-110">訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="cc442-110">Message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="cc442-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cc442-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc442-112">第一個訊息參數。</span><span class="sxs-lookup"><span data-stu-id="cc442-112">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="cc442-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cc442-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc442-114">第二個訊息參數。</span><span class="sxs-lookup"><span data-stu-id="cc442-114">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc442-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="cc442-115">Return value</span></span>

<span data-ttu-id="cc442-116">如果已處理訊息，則傳回 0; 如果未處理訊息，則傳回1。</span><span class="sxs-lookup"><span data-stu-id="cc442-116">Returns 0 if the message was processed, or 1 if the message was not processed.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc442-117">備註</span><span class="sxs-lookup"><span data-stu-id="cc442-117">Remarks</span></span>

<span data-ttu-id="cc442-118">基底類別會處理下列訊息：</span><span class="sxs-lookup"><span data-stu-id="cc442-118">The base class handles the following messages:</span></span>

-   <span data-ttu-id="cc442-119">WM \_ 關閉</span><span class="sxs-lookup"><span data-stu-id="cc442-119">WM\_CLOSE</span></span>
-   <span data-ttu-id="cc442-120">WM \_ 移動</span><span class="sxs-lookup"><span data-stu-id="cc442-120">WM\_MOVE</span></span>
-   <span data-ttu-id="cc442-121">WM \_ PALETTECHANGED</span><span class="sxs-lookup"><span data-stu-id="cc442-121">WM\_PALETTECHANGED</span></span>
-   <span data-ttu-id="cc442-122">WM \_ QUERYNEWPALETTE</span><span class="sxs-lookup"><span data-stu-id="cc442-122">WM\_QUERYNEWPALETTE</span></span>
-   <span data-ttu-id="cc442-123">WM \_ 大小</span><span class="sxs-lookup"><span data-stu-id="cc442-123">WM\_SIZE</span></span>
-   <span data-ttu-id="cc442-124">WM \_ SYSCOLORCHANGE</span><span class="sxs-lookup"><span data-stu-id="cc442-124">WM\_SYSCOLORCHANGE</span></span>

<span data-ttu-id="cc442-125">衍生類別可以覆寫這個方法來處理其他訊息。</span><span class="sxs-lookup"><span data-stu-id="cc442-125">A derived class can override this method to handle other messages.</span></span> <span data-ttu-id="cc442-126">衍生類別應該呼叫基類方法，以處理衍生類別忽略的任何訊息。</span><span class="sxs-lookup"><span data-stu-id="cc442-126">The derived class should call the base class method to handle any messages that the derived class ignores.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc442-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="cc442-127">Requirements</span></span>



| <span data-ttu-id="cc442-128">需求</span><span class="sxs-lookup"><span data-stu-id="cc442-128">Requirement</span></span> | <span data-ttu-id="cc442-129">值</span><span class="sxs-lookup"><span data-stu-id="cc442-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc442-130">標頭</span><span class="sxs-lookup"><span data-stu-id="cc442-130">Header</span></span><br/>  | <dl> <span data-ttu-id="cc442-131"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="cc442-131"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cc442-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="cc442-132">Library</span></span><br/> | <dl> <span data-ttu-id="cc442-133"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="cc442-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc442-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cc442-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc442-135">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="cc442-135">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




