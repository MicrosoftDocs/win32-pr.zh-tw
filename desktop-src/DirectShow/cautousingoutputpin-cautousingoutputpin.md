---
description: 函式方法。 此函式會取得指定之 pin 的存取權。
ms.assetid: 518d41aa-8361-4769-aa9b-14676b676d6f
title: 'CAutoUsingOutputPin. CAutoUsingOutputPin (Amfilter. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin.CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94bafcdcb6e44a07afdccea382d783c20a9ad2ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001155"
---
# <a name="cautousingoutputpincautousingoutputpin-constructor"></a><span data-ttu-id="71973-104">CAutoUsingOutputPin. CAutoUsingOutputPin 函數</span><span class="sxs-lookup"><span data-stu-id="71973-104">CAutoUsingOutputPin.CAutoUsingOutputPin constructor</span></span>

<span data-ttu-id="71973-105">函式方法。</span><span class="sxs-lookup"><span data-stu-id="71973-105">Constructor method.</span></span> <span data-ttu-id="71973-106">此函式會取得指定之 pin 的存取權。</span><span class="sxs-lookup"><span data-stu-id="71973-106">The constructor obtains access to the specified pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="71973-107">語法</span><span class="sxs-lookup"><span data-stu-id="71973-107">Syntax</span></span>


```C++
CAutoUsingOutputPin(
   CDynamicOutputPin *pOutputPin,
   HRESULT           *phr
);
```



## <a name="parameters"></a><span data-ttu-id="71973-108">參數</span><span class="sxs-lookup"><span data-stu-id="71973-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71973-109">*pOutputPin*</span><span class="sxs-lookup"><span data-stu-id="71973-109">*pOutputPin*</span></span> 
</dt> <dd>

<span data-ttu-id="71973-110">[**CDynamicOutputPin**](cdynamicoutputpin.md)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="71973-110">Pointer to a [**CDynamicOutputPin**](cdynamicoutputpin.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="71973-111">*phr*</span><span class="sxs-lookup"><span data-stu-id="71973-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="71973-112">包含 **HRESULT** 值之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="71973-112">Pointer to a variable that contains an **HRESULT** value.</span></span> <span data-ttu-id="71973-113">值必須為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="71973-113">The value must be S\_OK.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="71973-114">備註</span><span class="sxs-lookup"><span data-stu-id="71973-114">Remarks</span></span>

<span data-ttu-id="71973-115">當方法傳回時， *\* phr* 的值會指出方法的成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="71973-115">When the method returns, the value of *\*phr* indicates the success or failure of the method.</span></span>

## <a name="requirements"></a><span data-ttu-id="71973-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="71973-116">Requirements</span></span>



| <span data-ttu-id="71973-117">需求</span><span class="sxs-lookup"><span data-stu-id="71973-117">Requirement</span></span> | <span data-ttu-id="71973-118">值</span><span class="sxs-lookup"><span data-stu-id="71973-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71973-119">標頭</span><span class="sxs-lookup"><span data-stu-id="71973-119">Header</span></span><br/>  | <dl> <span data-ttu-id="71973-120"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="71973-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="71973-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="71973-121">Library</span></span><br/> | <dl> <span data-ttu-id="71973-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="71973-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71973-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71973-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71973-124">**CAutoUsingOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="71973-124">**CAutoUsingOutputPin Class**</span></span>](cautousingoutputpin-cautousingoutputpin.md)
</dt> </dl>

 

 




