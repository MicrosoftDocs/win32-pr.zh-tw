---
description: OnClose 方法會處理 WM \_ 關閉訊息。
ms.assetid: e562add4-752e-4665-a75e-a5526fb7f045
title: CBaseWindow) 的方法 (Winutil
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnClose
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 189b08c116f66ff864ffe308befb990973c6ce43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977637"
---
# <a name="cbasewindowonclose-method"></a><span data-ttu-id="a7261-103">CBaseWindow： OnClose 方法</span><span class="sxs-lookup"><span data-stu-id="a7261-103">CBaseWindow.OnClose method</span></span>

<span data-ttu-id="a7261-104">`OnClose`方法會處理 WM \_ 關閉訊息。</span><span class="sxs-lookup"><span data-stu-id="a7261-104">The `OnClose` method handles WM\_CLOSE messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7261-105">語法</span><span class="sxs-lookup"><span data-stu-id="a7261-105">Syntax</span></span>


```C++
virtual BOOL OnClose();
```



## <a name="parameters"></a><span data-ttu-id="a7261-106">參數</span><span class="sxs-lookup"><span data-stu-id="a7261-106">Parameters</span></span>

<span data-ttu-id="a7261-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="a7261-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a7261-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="a7261-108">Return value</span></span>

<span data-ttu-id="a7261-109">傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="a7261-109">Returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7261-110">備註</span><span class="sxs-lookup"><span data-stu-id="a7261-110">Remarks</span></span>

<span data-ttu-id="a7261-111">在基類中，此方法只會隱藏視窗。</span><span class="sxs-lookup"><span data-stu-id="a7261-111">In the base class, this method simply hides the window.</span></span> <span data-ttu-id="a7261-112">一般而言，衍生類別會覆寫這個方法，讓它也會傳送 [**EC \_ USERABORT**](ec-userabort.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="a7261-112">Typically, a derived class will override this method so that it sends an [**EC\_USERABORT**](ec-userabort.md) event as well.</span></span> <span data-ttu-id="a7261-113">請勿覆寫方法以損毀視窗。</span><span class="sxs-lookup"><span data-stu-id="a7261-113">Do not override the method to destroy the window.</span></span> <span data-ttu-id="a7261-114">相反地，當擁有篩選準則終結時，請呼叫 [**CBaseWindow：:D onewithwindow**](cbasewindow-donewithwindow.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="a7261-114">Instead, call the [**CBaseWindow::DoneWithWindow**](cbasewindow-donewithwindow.md) method when the owning filter is destroyed.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7261-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7261-115">Requirements</span></span>



| <span data-ttu-id="a7261-116">需求</span><span class="sxs-lookup"><span data-stu-id="a7261-116">Requirement</span></span> | <span data-ttu-id="a7261-117">值</span><span class="sxs-lookup"><span data-stu-id="a7261-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7261-118">標頭</span><span class="sxs-lookup"><span data-stu-id="a7261-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a7261-119"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a7261-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a7261-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="a7261-120">Library</span></span><br/> | <dl> <span data-ttu-id="a7261-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a7261-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7261-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7261-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7261-123">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="a7261-123">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




