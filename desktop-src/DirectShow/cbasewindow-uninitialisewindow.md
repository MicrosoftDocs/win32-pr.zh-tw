---
description: UninitialiseWindow 方法會釋放視窗的資源。
ms.assetid: 8c5bb0c1-1d92-4025-bbbd-1e57ddde4456
title: 'CBaseWindow. UninitialiseWindow 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.UninitialiseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ceeadd0ec7a61422f0127c957125caa9a01dcefb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993666"
---
# <a name="cbasewindowuninitialisewindow-method"></a><span data-ttu-id="f59f3-103">CBaseWindow. UninitialiseWindow 方法</span><span class="sxs-lookup"><span data-stu-id="f59f3-103">CBaseWindow.UninitialiseWindow method</span></span>

<span data-ttu-id="f59f3-104">`UninitialiseWindow`方法會釋放視窗的資源。</span><span class="sxs-lookup"><span data-stu-id="f59f3-104">The `UninitialiseWindow` method releases the window's resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="f59f3-105">語法</span><span class="sxs-lookup"><span data-stu-id="f59f3-105">Syntax</span></span>


```C++
virtual HRESULT UninitialiseWindow();
```



## <a name="parameters"></a><span data-ttu-id="f59f3-106">參數</span><span class="sxs-lookup"><span data-stu-id="f59f3-106">Parameters</span></span>

<span data-ttu-id="f59f3-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f59f3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f59f3-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="f59f3-108">Return value</span></span>

<span data-ttu-id="f59f3-109">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="f59f3-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f59f3-110">備註</span><span class="sxs-lookup"><span data-stu-id="f59f3-110">Remarks</span></span>

<span data-ttu-id="f59f3-111">這個方法會釋放 [**CBaseWindow：： InitialiseWindow**](cbasewindow-initialisewindow.md) 方法所取得的資源。</span><span class="sxs-lookup"><span data-stu-id="f59f3-111">This method frees resources that were acquired by the [**CBaseWindow::InitialiseWindow**](cbasewindow-initialisewindow.md) method.</span></span> <span data-ttu-id="f59f3-112">[**CBaseWindow：:D onewithwindow**](cbasewindow-donewithwindow.md)方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="f59f3-112">The [**CBaseWindow::DoneWithWindow**](cbasewindow-donewithwindow.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f59f3-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="f59f3-113">Requirements</span></span>



| <span data-ttu-id="f59f3-114">需求</span><span class="sxs-lookup"><span data-stu-id="f59f3-114">Requirement</span></span> | <span data-ttu-id="f59f3-115">值</span><span class="sxs-lookup"><span data-stu-id="f59f3-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f59f3-116">標頭</span><span class="sxs-lookup"><span data-stu-id="f59f3-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f59f3-117"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f59f3-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f59f3-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="f59f3-118">Library</span></span><br/> | <dl> <span data-ttu-id="f59f3-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f59f3-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f59f3-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f59f3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f59f3-121">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="f59f3-121">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




