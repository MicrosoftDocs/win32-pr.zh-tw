---
description: 函式方法。
ms.assetid: 996adc69-8727-431e-a7f5-8fbcc0e305ae
title: 'CDynamicOutputPin. CDynamicOutputPin (Amfilter. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.CDynamicOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7f45a2fee25796f39c7d8b358b1ac83e4a5b1daa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984467"
---
# <a name="cdynamicoutputpincdynamicoutputpin-constructor"></a><span data-ttu-id="946a2-103">CDynamicOutputPin. CDynamicOutputPin 函數</span><span class="sxs-lookup"><span data-stu-id="946a2-103">CDynamicOutputPin.CDynamicOutputPin constructor</span></span>

<span data-ttu-id="946a2-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="946a2-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="946a2-105">語法</span><span class="sxs-lookup"><span data-stu-id="946a2-105">Syntax</span></span>


```C++
CDynamicOutputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="946a2-106">參數</span><span class="sxs-lookup"><span data-stu-id="946a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="946a2-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="946a2-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="946a2-108">包含物件名稱之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="946a2-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="946a2-109">如需詳細資訊，請參閱 [**CBaseObject**](cbaseobject.md)。</span><span class="sxs-lookup"><span data-stu-id="946a2-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="946a2-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="946a2-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="946a2-111">建立此釘選之篩選準則的指標。</span><span class="sxs-lookup"><span data-stu-id="946a2-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="946a2-112">*pLock*</span><span class="sxs-lookup"><span data-stu-id="946a2-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="946a2-113">[**CCritSec**](ccritsec.md)鎖定的指標，用來序列化狀態變更。</span><span class="sxs-lookup"><span data-stu-id="946a2-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="946a2-114">使用與篩選鎖定相同的重要區段 [ **CBaseFilter：： m \_ pLock**](cbasefilter-m-plock.md)</span><span class="sxs-lookup"><span data-stu-id="946a2-114">Use the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md)</span></span>

</dd> <dt>

<span data-ttu-id="946a2-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="946a2-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="946a2-116">變數的指標，此變數會接收 **HRESULT** 值，指出方法的成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="946a2-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="946a2-117">在建立物件之前，將值初始化為「 \_ 確定」。</span><span class="sxs-lookup"><span data-stu-id="946a2-117">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="946a2-118">只有在發生錯誤時，才會變更此值。</span><span class="sxs-lookup"><span data-stu-id="946a2-118">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="946a2-119">*pName*</span><span class="sxs-lookup"><span data-stu-id="946a2-119">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="946a2-120">包含 pin 識別碼之寬字元字串的指標。</span><span class="sxs-lookup"><span data-stu-id="946a2-120">Pointer to a wide-character string containing the pin identifier.</span></span> <span data-ttu-id="946a2-121">如需詳細資訊，請參閱 [**IPin：： QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)。</span><span class="sxs-lookup"><span data-stu-id="946a2-121">For more information, see [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="946a2-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="946a2-122">Requirements</span></span>



| <span data-ttu-id="946a2-123">需求</span><span class="sxs-lookup"><span data-stu-id="946a2-123">Requirement</span></span> | <span data-ttu-id="946a2-124">值</span><span class="sxs-lookup"><span data-stu-id="946a2-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="946a2-125">標頭</span><span class="sxs-lookup"><span data-stu-id="946a2-125">Header</span></span><br/>  | <dl> <span data-ttu-id="946a2-126"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="946a2-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="946a2-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="946a2-127">Library</span></span><br/> | <dl> <span data-ttu-id="946a2-128"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="946a2-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="946a2-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="946a2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="946a2-130">**CDynamicOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="946a2-130">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




