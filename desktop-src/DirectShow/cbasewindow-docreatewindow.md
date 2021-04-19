---
description: DoCreateWindow 方法會建立視窗。
ms.assetid: bbe38a71-bbf7-4380-96a3-074b992a1d1e
title: " (Winutil 的 CBaseWindow.DoCreateWindow 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoCreateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 76bea1523f48a6e22a3c2d9370fa32bcea022621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994193"
---
# <a name="cbasewindowdocreatewindow-method"></a><span data-ttu-id="1fa21-103">CBaseWindow.DoCreateWindow 方法</span><span class="sxs-lookup"><span data-stu-id="1fa21-103">CBaseWindow.DoCreateWindow method</span></span>

<span data-ttu-id="1fa21-104">`DoCreateWindow`方法會建立視窗。</span><span class="sxs-lookup"><span data-stu-id="1fa21-104">The `DoCreateWindow` method creates the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fa21-105">語法</span><span class="sxs-lookup"><span data-stu-id="1fa21-105">Syntax</span></span>


```C++
HRESULT DoCreateWindow();
```



## <a name="parameters"></a><span data-ttu-id="1fa21-106">參數</span><span class="sxs-lookup"><span data-stu-id="1fa21-106">Parameters</span></span>

<span data-ttu-id="1fa21-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="1fa21-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1fa21-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="1fa21-108">Return value</span></span>

<span data-ttu-id="1fa21-109">\_如果成功，則傳回，否則會傳回指出失敗原因的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="1fa21-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fa21-110">備註</span><span class="sxs-lookup"><span data-stu-id="1fa21-110">Remarks</span></span>

<span data-ttu-id="1fa21-111">[**CBaseWindow：:P reparewindow**](cbasewindow-preparewindow.md)方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="1fa21-111">The [**CBaseWindow::PrepareWindow**](cbasewindow-preparewindow.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fa21-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="1fa21-112">Requirements</span></span>



| <span data-ttu-id="1fa21-113">需求</span><span class="sxs-lookup"><span data-stu-id="1fa21-113">Requirement</span></span> | <span data-ttu-id="1fa21-114">值</span><span class="sxs-lookup"><span data-stu-id="1fa21-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fa21-115">標頭</span><span class="sxs-lookup"><span data-stu-id="1fa21-115">Header</span></span><br/>  | <dl> <span data-ttu-id="1fa21-116"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1fa21-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1fa21-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="1fa21-117">Library</span></span><br/> | <dl> <span data-ttu-id="1fa21-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="1fa21-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fa21-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1fa21-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fa21-120">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="1fa21-120">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




