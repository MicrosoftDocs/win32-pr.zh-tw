---
description: PrepareWindow 方法會建立視窗。
ms.assetid: c4c0d177-6351-4ecc-b1eb-399b4a94c463
title: 'CBaseWindow. PrepareWindow 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PrepareWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91331ede15feb756f3ddd08d0d368621b35eda00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991216"
---
# <a name="cbasewindowpreparewindow-method"></a><span data-ttu-id="b53d8-103">CBaseWindow. PrepareWindow 方法</span><span class="sxs-lookup"><span data-stu-id="b53d8-103">CBaseWindow.PrepareWindow method</span></span>

<span data-ttu-id="b53d8-104">`PrepareWindow`方法會建立視窗。</span><span class="sxs-lookup"><span data-stu-id="b53d8-104">The `PrepareWindow` method creates the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="b53d8-105">語法</span><span class="sxs-lookup"><span data-stu-id="b53d8-105">Syntax</span></span>


```C++
virtual HRESULT PrepareWindow();
```



## <a name="parameters"></a><span data-ttu-id="b53d8-106">參數</span><span class="sxs-lookup"><span data-stu-id="b53d8-106">Parameters</span></span>

<span data-ttu-id="b53d8-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="b53d8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b53d8-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="b53d8-108">Return value</span></span>

<span data-ttu-id="b53d8-109">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="b53d8-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b53d8-110">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="b53d8-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="b53d8-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b53d8-111">Return code</span></span>                                                                            | <span data-ttu-id="b53d8-112">Description</span><span class="sxs-lookup"><span data-stu-id="b53d8-112">Description</span></span>         |
|----------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="b53d8-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="b53d8-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="b53d8-114">成功。</span><span class="sxs-lookup"><span data-stu-id="b53d8-114">Success.</span></span><br/> |
| <dl> <span data-ttu-id="b53d8-115"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="b53d8-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="b53d8-116">失敗。</span><span class="sxs-lookup"><span data-stu-id="b53d8-116">Failure.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b53d8-117">備註</span><span class="sxs-lookup"><span data-stu-id="b53d8-117">Remarks</span></span>

<span data-ttu-id="b53d8-118">建立物件之後，請呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="b53d8-118">Call this method after creating the object.</span></span> <span data-ttu-id="b53d8-119">這個方法會執行一些初始的簿記，然後呼叫 [**CBaseWindow：:D ocreatewindow**](cbasewindow-docreatewindow.md) 方法來建立視窗。</span><span class="sxs-lookup"><span data-stu-id="b53d8-119">This method performs some initial bookkeeping and then calls the [**CBaseWindow::DoCreateWindow**](cbasewindow-docreatewindow.md) method to create the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="b53d8-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="b53d8-120">Requirements</span></span>



| <span data-ttu-id="b53d8-121">需求</span><span class="sxs-lookup"><span data-stu-id="b53d8-121">Requirement</span></span> | <span data-ttu-id="b53d8-122">值</span><span class="sxs-lookup"><span data-stu-id="b53d8-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b53d8-123">標頭</span><span class="sxs-lookup"><span data-stu-id="b53d8-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b53d8-124"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b53d8-124"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b53d8-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="b53d8-125">Library</span></span><br/> | <dl> <span data-ttu-id="b53d8-126"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b53d8-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b53d8-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b53d8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b53d8-128">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="b53d8-128">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




