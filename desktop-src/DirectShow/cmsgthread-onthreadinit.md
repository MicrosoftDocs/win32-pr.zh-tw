---
description: 提供執行緒的初始化。
ms.assetid: a9c330bb-0a2b-45bf-9b24-d03dd61d7dbf
title: 'CMsgThread. OnThreadInit 方法 (Msgthrd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.OnThreadInit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 80e15d6430da77c0f22f5566375394b8fe6994ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995224"
---
# <a name="cmsgthreadonthreadinit-method"></a><span data-ttu-id="497f4-103">CMsgThread. OnThreadInit 方法</span><span class="sxs-lookup"><span data-stu-id="497f4-103">CMsgThread.OnThreadInit method</span></span>

<span data-ttu-id="497f4-104">提供執行緒的初始化。</span><span class="sxs-lookup"><span data-stu-id="497f4-104">Provides initialization on a thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="497f4-105">語法</span><span class="sxs-lookup"><span data-stu-id="497f4-105">Syntax</span></span>


```C++
virtual void OnThreadInit();
```



## <a name="parameters"></a><span data-ttu-id="497f4-106">參數</span><span class="sxs-lookup"><span data-stu-id="497f4-106">Parameters</span></span>

<span data-ttu-id="497f4-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="497f4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="497f4-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="497f4-108">Return value</span></span>

<span data-ttu-id="497f4-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="497f4-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="497f4-110">備註</span><span class="sxs-lookup"><span data-stu-id="497f4-110">Remarks</span></span>

<span data-ttu-id="497f4-111">如果您想要線上程啟動時進行自己的特定初始化，請覆寫此函數。</span><span class="sxs-lookup"><span data-stu-id="497f4-111">Override this function if you want to do your own specific initialization on thread startup.</span></span>

## <a name="requirements"></a><span data-ttu-id="497f4-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="497f4-112">Requirements</span></span>



| <span data-ttu-id="497f4-113">需求</span><span class="sxs-lookup"><span data-stu-id="497f4-113">Requirement</span></span> | <span data-ttu-id="497f4-114">值</span><span class="sxs-lookup"><span data-stu-id="497f4-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="497f4-115">標頭</span><span class="sxs-lookup"><span data-stu-id="497f4-115">Header</span></span><br/>  | <dl> <span data-ttu-id="497f4-116"><dt>Msgthrd (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="497f4-116"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="497f4-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="497f4-117">Library</span></span><br/> | <dl> <span data-ttu-id="497f4-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="497f4-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="497f4-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="497f4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="497f4-120">**CMsgThread 類別**</span><span class="sxs-lookup"><span data-stu-id="497f4-120">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




