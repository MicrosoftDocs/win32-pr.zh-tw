---
description: CAMMsgEvent。 CAMMsgEvent 函式-函數方法。
ms.assetid: 7871a624-70c0-4f21-b62a-2c4c2eaa762b
title: 'CAMMsgEvent. CAMMsgEvent (Wxutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent.CAMMsgEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dac72ecb97a1ea1fd2594af9c11b8a03078cf2cb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096530"
---
# <a name="cammsgeventcammsgevent-constructor"></a><span data-ttu-id="c264c-103">CAMMsgEvent. CAMMsgEvent 函數</span><span class="sxs-lookup"><span data-stu-id="c264c-103">CAMMsgEvent.CAMMsgEvent constructor</span></span>

<span data-ttu-id="c264c-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="c264c-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c264c-105">語法</span><span class="sxs-lookup"><span data-stu-id="c264c-105">Syntax</span></span>


```C++
CAMMsgEvent(
   HRESULT *phr
);
```



## <a name="parameters"></a><span data-ttu-id="c264c-106">參數</span><span class="sxs-lookup"><span data-stu-id="c264c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c264c-107">*phr*</span><span class="sxs-lookup"><span data-stu-id="c264c-107">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="c264c-108">**HRESULT** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="c264c-108">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="c264c-109">如果函式失敗，此參數會收到錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c264c-109">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="c264c-110">如果發生這種情況，則物件不是處於有效的狀態。</span><span class="sxs-lookup"><span data-stu-id="c264c-110">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="c264c-111">為了與舊版 strmbase 回溯相容，此參數預設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c264c-111">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="c264c-112">不過，最好是傳遞非 **Null** 值，讓呼叫端可以檢查物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="c264c-112">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c264c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="c264c-113">Requirements</span></span>



| <span data-ttu-id="c264c-114">需求</span><span class="sxs-lookup"><span data-stu-id="c264c-114">Requirement</span></span> | <span data-ttu-id="c264c-115">值</span><span class="sxs-lookup"><span data-stu-id="c264c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c264c-116">標頭</span><span class="sxs-lookup"><span data-stu-id="c264c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c264c-117"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c264c-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c264c-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="c264c-118">Library</span></span><br/> | <dl> <span data-ttu-id="c264c-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c264c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c264c-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c264c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c264c-121">**CAMMsgEvent 類別**</span><span class="sxs-lookup"><span data-stu-id="c264c-121">**CAMMsgEvent Class**</span></span>](cammsgevent.md)
</dt> </dl>

 

 




