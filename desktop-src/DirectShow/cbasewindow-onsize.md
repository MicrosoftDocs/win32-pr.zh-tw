---
description: OnSize 方法會處理 WM \_ 大小的訊息。
ms.assetid: 21d867a4-4321-478a-9beb-5d3053569369
title: 'CBaseWindow. OnSize 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9020510030d3b3d4b30e066adfe67367618fb3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990538"
---
# <a name="cbasewindowonsize-method"></a><span data-ttu-id="5af69-103">CBaseWindow. OnSize 方法</span><span class="sxs-lookup"><span data-stu-id="5af69-103">CBaseWindow.OnSize method</span></span>

<span data-ttu-id="5af69-104">`OnSize`方法會處理 WM \_ 大小的訊息。</span><span class="sxs-lookup"><span data-stu-id="5af69-104">The `OnSize` method handles WM\_SIZE messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="5af69-105">語法</span><span class="sxs-lookup"><span data-stu-id="5af69-105">Syntax</span></span>


```C++
virtual BOOL OnSize(
   LONG Width,
   LONG Height
);
```



## <a name="parameters"></a><span data-ttu-id="5af69-106">參數</span><span class="sxs-lookup"><span data-stu-id="5af69-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5af69-107">*寬度*</span><span class="sxs-lookup"><span data-stu-id="5af69-107">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="5af69-108">工作區的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="5af69-108">Width of the client area, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="5af69-109">*高度*</span><span class="sxs-lookup"><span data-stu-id="5af69-109">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="5af69-110">用戶端區域的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="5af69-110">Height of the client area, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5af69-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="5af69-111">Return value</span></span>

<span data-ttu-id="5af69-112">傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="5af69-112">Returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5af69-113">備註</span><span class="sxs-lookup"><span data-stu-id="5af69-113">Remarks</span></span>

<span data-ttu-id="5af69-114">這個方法會儲存新的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="5af69-114">This method stores the new width and height.</span></span> <span data-ttu-id="5af69-115">若要取出這些值，請呼叫 [**CBaseWindow：： GetWindowHeight**](cbasewindow-getwindowheight.md) 和 [**CBaseWindow：： GetWindowWidth**](cbasewindow-getwindowwidth.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="5af69-115">To retrieve these values, call the [**CBaseWindow::GetWindowHeight**](cbasewindow-getwindowheight.md) and [**CBaseWindow::GetWindowWidth**](cbasewindow-getwindowwidth.md) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="5af69-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="5af69-116">Requirements</span></span>



| <span data-ttu-id="5af69-117">需求</span><span class="sxs-lookup"><span data-stu-id="5af69-117">Requirement</span></span> | <span data-ttu-id="5af69-118">值</span><span class="sxs-lookup"><span data-stu-id="5af69-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5af69-119">標頭</span><span class="sxs-lookup"><span data-stu-id="5af69-119">Header</span></span><br/>  | <dl> <span data-ttu-id="5af69-120"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="5af69-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5af69-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="5af69-121">Library</span></span><br/> | <dl> <span data-ttu-id="5af69-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="5af69-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5af69-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5af69-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5af69-124">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="5af69-124">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




