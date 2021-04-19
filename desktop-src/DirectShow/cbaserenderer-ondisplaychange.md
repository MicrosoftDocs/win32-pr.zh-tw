---
description: OnDisplayChange 方法會將 EC \_ 顯示 \_ 變更事件張貼至篩選圖形管理員。
ms.assetid: e4cdcdf2-7fc2-4893-9897-97bcf2c12610
title: 'CBaseRenderer. OnDisplayChange 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnDisplayChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1e99a8626d523e8b14b013acc9d2ead462f48df3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976266"
---
# <a name="cbaserendererondisplaychange-method"></a><span data-ttu-id="e0e51-103">CBaseRenderer. OnDisplayChange 方法</span><span class="sxs-lookup"><span data-stu-id="e0e51-103">CBaseRenderer.OnDisplayChange method</span></span>

<span data-ttu-id="e0e51-104">方法會將 `OnDisplayChange` [**EC \_ 顯示 \_ 變更**](ec-display-changed.md) 事件張貼至篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="e0e51-104">The `OnDisplayChange` method posts an [**EC\_DISPLAY\_CHANGED**](ec-display-changed.md) event to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0e51-105">語法</span><span class="sxs-lookup"><span data-stu-id="e0e51-105">Syntax</span></span>


```C++
BOOL OnDisplayChange();
```



## <a name="parameters"></a><span data-ttu-id="e0e51-106">參數</span><span class="sxs-lookup"><span data-stu-id="e0e51-106">Parameters</span></span>

<span data-ttu-id="e0e51-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e0e51-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e0e51-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="e0e51-108">Return value</span></span>

<span data-ttu-id="e0e51-109">如果已張貼事件，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="e0e51-109">Returns **TRUE** if the event was posted, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0e51-110">備註</span><span class="sxs-lookup"><span data-stu-id="e0e51-110">Remarks</span></span>

<span data-ttu-id="e0e51-111">影片轉譯器應該呼叫這個方法以回應 WM \_ DISPLAYCHANGE 訊息。</span><span class="sxs-lookup"><span data-stu-id="e0e51-111">Video renderers should call this method in response to WM\_DISPLAYCHANGE messages.</span></span> <span data-ttu-id="e0e51-112">如果輸入連接已連接，方法會將 EC \_ 顯示 \_ 已變更的事件傳送至篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="e0e51-112">If the input pin is connected, the method sends an EC\_DISPLAY\_CHANGED event to the filter graph manager.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0e51-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="e0e51-113">Requirements</span></span>



| <span data-ttu-id="e0e51-114">需求</span><span class="sxs-lookup"><span data-stu-id="e0e51-114">Requirement</span></span> | <span data-ttu-id="e0e51-115">值</span><span class="sxs-lookup"><span data-stu-id="e0e51-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0e51-116">標頭</span><span class="sxs-lookup"><span data-stu-id="e0e51-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e0e51-117"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e0e51-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e0e51-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="e0e51-118">Library</span></span><br/> | <dl> <span data-ttu-id="e0e51-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e0e51-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0e51-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e0e51-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0e51-121">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="e0e51-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




