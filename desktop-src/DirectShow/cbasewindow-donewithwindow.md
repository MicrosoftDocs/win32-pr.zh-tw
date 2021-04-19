---
description: DoneWithWindow 方法會終結視窗。
ms.assetid: 03c97884-7d91-4b59-b867-dda231d2a184
title: 'CBaseWindow. DoneWithWindow 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoneWithWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc31e893a4015aa8b4356d265ca4065ee336c3ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995627"
---
# <a name="cbasewindowdonewithwindow-method"></a><span data-ttu-id="7c17e-103">CBaseWindow. DoneWithWindow 方法</span><span class="sxs-lookup"><span data-stu-id="7c17e-103">CBaseWindow.DoneWithWindow method</span></span>

<span data-ttu-id="7c17e-104">方法會終結 `DoneWithWindow` 視窗。</span><span class="sxs-lookup"><span data-stu-id="7c17e-104">The `DoneWithWindow` method destroys the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c17e-105">語法</span><span class="sxs-lookup"><span data-stu-id="7c17e-105">Syntax</span></span>


```C++
virtual HRESULT DoneWithWindow();
```



## <a name="parameters"></a><span data-ttu-id="7c17e-106">參數</span><span class="sxs-lookup"><span data-stu-id="7c17e-106">Parameters</span></span>

<span data-ttu-id="7c17e-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="7c17e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7c17e-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="7c17e-108">Return value</span></span>

<span data-ttu-id="7c17e-109">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="7c17e-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c17e-110">備註</span><span class="sxs-lookup"><span data-stu-id="7c17e-110">Remarks</span></span>

<span data-ttu-id="7c17e-111">從衍生物件的「析構函式」方法呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="7c17e-111">Call this method from the derived object's destructor method.</span></span>

<span data-ttu-id="7c17e-112">如果從建立視窗的相同執行緒呼叫這個方法，則此方法會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="7c17e-112">If this method is called from the same thread that created the window, the method performs the following actions:</span></span>

-   <span data-ttu-id="7c17e-113">呼叫 [**CBaseWindow：： InactivateWindow**](cbasewindow-inactivatewindow.md) 方法，該方法會停用視窗。</span><span class="sxs-lookup"><span data-stu-id="7c17e-113">Calls the [**CBaseWindow::InactivateWindow**](cbasewindow-inactivatewindow.md) method, which deactivates the window.</span></span>
-   <span data-ttu-id="7c17e-114">呼叫 [**CBaseWindow：： UninitialiseWindow**](cbasewindow-uninitialisewindow.md) 方法，該方法會釋放視窗所使用的資源。</span><span class="sxs-lookup"><span data-stu-id="7c17e-114">Calls the [**CBaseWindow::UninitialiseWindow**](cbasewindow-uninitialisewindow.md) method, which releases resources used by the window.</span></span>
-   <span data-ttu-id="7c17e-115">終結視窗。</span><span class="sxs-lookup"><span data-stu-id="7c17e-115">Destroys the window.</span></span>

<span data-ttu-id="7c17e-116">如果呼叫的執行緒 `DoneWithWindow` 不是建立視窗的執行緒，則方法會將「終結」私用訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="7c17e-116">If the thread calling `DoneWithWindow` is not the thread that created the window, the method sends a private "destroy" message to the window.</span></span> <span data-ttu-id="7c17e-117">當視窗收到這個訊息時，它會 `DoneWithWindow` 自行呼叫。</span><span class="sxs-lookup"><span data-stu-id="7c17e-117">When the window receives this message, it calls `DoneWithWindow` on itself.</span></span> <span data-ttu-id="7c17e-118"> (如果 [**CBaseWindow：： m \_ BDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) 為 **TRUE**，則視窗會張貼訊息。 ) </span><span class="sxs-lookup"><span data-stu-id="7c17e-118">(If [**CBaseWindow::m\_bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) is **TRUE**, the window posts the message.)</span></span>

## <a name="requirements"></a><span data-ttu-id="7c17e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c17e-119">Requirements</span></span>



| <span data-ttu-id="7c17e-120">需求</span><span class="sxs-lookup"><span data-stu-id="7c17e-120">Requirement</span></span> | <span data-ttu-id="7c17e-121">值</span><span class="sxs-lookup"><span data-stu-id="7c17e-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c17e-122">標頭</span><span class="sxs-lookup"><span data-stu-id="7c17e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="7c17e-123"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7c17e-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7c17e-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="7c17e-124">Library</span></span><br/> | <dl> <span data-ttu-id="7c17e-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7c17e-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c17e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c17e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c17e-127">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="7c17e-127">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




