---
description: CancelNotification 方法會取消排程轉譯的計時器事件。
ms.assetid: 56ddf692-a2e3-40f2-848f-2d592601ec00
title: 'CBaseRenderer. CancelNotification 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CancelNotification
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3330f369c5fcc45fe051a1964a504d5d40fcd091
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994347"
---
# <a name="cbaserenderercancelnotification-method"></a><span data-ttu-id="55b74-103">CBaseRenderer. CancelNotification 方法</span><span class="sxs-lookup"><span data-stu-id="55b74-103">CBaseRenderer.CancelNotification method</span></span>

<span data-ttu-id="55b74-104">`CancelNotification`方法會取消排程轉譯的計時器事件。</span><span class="sxs-lookup"><span data-stu-id="55b74-104">The `CancelNotification` method cancels the timer event that schedules rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="55b74-105">語法</span><span class="sxs-lookup"><span data-stu-id="55b74-105">Syntax</span></span>


```C++
virtual HRESULT CancelNotification();
```



## <a name="parameters"></a><span data-ttu-id="55b74-106">參數</span><span class="sxs-lookup"><span data-stu-id="55b74-106">Parameters</span></span>

<span data-ttu-id="55b74-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="55b74-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="55b74-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="55b74-108">Return value</span></span>

<span data-ttu-id="55b74-109">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="55b74-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="55b74-110">傳回碼</span><span class="sxs-lookup"><span data-stu-id="55b74-110">Return code</span></span>                                                                             | <span data-ttu-id="55b74-111">Description</span><span class="sxs-lookup"><span data-stu-id="55b74-111">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="55b74-112"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="55b74-112"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="55b74-113">沒有暫止的計時器事件。</span><span class="sxs-lookup"><span data-stu-id="55b74-113">There was no pending timer event.</span></span><br/> |
| <dl> <span data-ttu-id="55b74-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="55b74-114"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="55b74-115">成功。</span><span class="sxs-lookup"><span data-stu-id="55b74-115">Success.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="55b74-116">備註</span><span class="sxs-lookup"><span data-stu-id="55b74-116">Remarks</span></span>

<span data-ttu-id="55b74-117">當串流停止時，篩選會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="55b74-117">The filter calls this method when streaming stops.</span></span> <span data-ttu-id="55b74-118">方法會取消任何已排程的呈現。</span><span class="sxs-lookup"><span data-stu-id="55b74-118">The method cancels any scheduled rendering.</span></span>

## <a name="requirements"></a><span data-ttu-id="55b74-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="55b74-119">Requirements</span></span>



| <span data-ttu-id="55b74-120">需求</span><span class="sxs-lookup"><span data-stu-id="55b74-120">Requirement</span></span> | <span data-ttu-id="55b74-121">值</span><span class="sxs-lookup"><span data-stu-id="55b74-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55b74-122">標頭</span><span class="sxs-lookup"><span data-stu-id="55b74-122">Header</span></span><br/>  | <dl> <span data-ttu-id="55b74-123"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="55b74-123"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="55b74-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="55b74-124">Library</span></span><br/> | <dl> <span data-ttu-id="55b74-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="55b74-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55b74-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55b74-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55b74-127">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="55b74-127">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




