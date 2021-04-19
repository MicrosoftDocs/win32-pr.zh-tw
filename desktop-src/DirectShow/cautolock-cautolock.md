---
description: 函式方法。 此函數會鎖定指定的重要區段物件。
ms.assetid: 5a0d74f9-bb99-4922-9a92-2e7c1863421f
title: 'CAutoLock. CAutoLock (Wxutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoLock.CAutoLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fed29011d4fe581ed146f64800351a3f1053d957
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998614"
---
# <a name="cautolockcautolock-constructor"></a><span data-ttu-id="5cdec-104">CAutoLock. CAutoLock 函數</span><span class="sxs-lookup"><span data-stu-id="5cdec-104">CAutoLock.CAutoLock constructor</span></span>

<span data-ttu-id="5cdec-105">函式方法。</span><span class="sxs-lookup"><span data-stu-id="5cdec-105">Constructor method.</span></span> <span data-ttu-id="5cdec-106">此函數會鎖定指定的重要區段物件。</span><span class="sxs-lookup"><span data-stu-id="5cdec-106">The constructor locks the specified critical section object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cdec-107">語法</span><span class="sxs-lookup"><span data-stu-id="5cdec-107">Syntax</span></span>


```C++
CAutoLock(
   CCritSec *plock
);
```



## <a name="parameters"></a><span data-ttu-id="5cdec-108">參數</span><span class="sxs-lookup"><span data-stu-id="5cdec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cdec-109">*plock*</span><span class="sxs-lookup"><span data-stu-id="5cdec-109">*plock*</span></span> 
</dt> <dd>

<span data-ttu-id="5cdec-110">[**CCritSec**](ccritsec.md)物件的指標，其中包含重要區段物件。</span><span class="sxs-lookup"><span data-stu-id="5cdec-110">Pointer to a [**CCritSec**](ccritsec.md) object, which contains a critical section object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5cdec-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="5cdec-111">Requirements</span></span>



| <span data-ttu-id="5cdec-112">需求</span><span class="sxs-lookup"><span data-stu-id="5cdec-112">Requirement</span></span> | <span data-ttu-id="5cdec-113">值</span><span class="sxs-lookup"><span data-stu-id="5cdec-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cdec-114">標頭</span><span class="sxs-lookup"><span data-stu-id="5cdec-114">Header</span></span><br/>  | <dl> <span data-ttu-id="5cdec-115"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="5cdec-115"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="5cdec-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="5cdec-116">Library</span></span><br/> | <dl> <span data-ttu-id="5cdec-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="5cdec-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cdec-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5cdec-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cdec-119">**CAutoLock 類別**</span><span class="sxs-lookup"><span data-stu-id="5cdec-119">**CAutoLock Class**</span></span>](cautolock.md)
</dt> </dl>

 

 




