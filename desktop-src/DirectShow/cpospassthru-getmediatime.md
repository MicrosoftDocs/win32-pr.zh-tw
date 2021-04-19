---
description: GetMediaTime 方法會抓取目前樣本上的時間戳記。
ms.assetid: 36f3b6d3-b884-4168-94f3-f334a5056c7d
title: 'CPosPassThru. GetMediaTime 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b2748d986f121a38041155dcd43f13a647916486
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989718"
---
# <a name="cpospassthrugetmediatime-method"></a><span data-ttu-id="32e46-103">CPosPassThru. GetMediaTime 方法</span><span class="sxs-lookup"><span data-stu-id="32e46-103">CPosPassThru.GetMediaTime method</span></span>

<span data-ttu-id="32e46-104">方法會抓取 `GetMediaTime` 目前樣本上的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="32e46-104">The `GetMediaTime` method retrieves the time stamps on the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="32e46-105">語法</span><span class="sxs-lookup"><span data-stu-id="32e46-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="32e46-106">參數</span><span class="sxs-lookup"><span data-stu-id="32e46-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32e46-107">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="32e46-107">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="32e46-108">接收開始時間之變數的指標，以目前時間格式的單位為單位。</span><span class="sxs-lookup"><span data-stu-id="32e46-108">Pointer to a variable that receives the start time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="32e46-109">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="32e46-109">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="32e46-110">接收結束時間之變數的指標，以目前時間格式的單位為單位。</span><span class="sxs-lookup"><span data-stu-id="32e46-110">Pointer to a variable that receives the end time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32e46-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="32e46-111">Return value</span></span>

<span data-ttu-id="32e46-112">傳回 E \_ 失敗。</span><span class="sxs-lookup"><span data-stu-id="32e46-112">Returns E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="32e46-113">備註</span><span class="sxs-lookup"><span data-stu-id="32e46-113">Remarks</span></span>

<span data-ttu-id="32e46-114">如果您的篩選準則會快取它所接收之範例的時間戳記，請覆寫這個方法。</span><span class="sxs-lookup"><span data-stu-id="32e46-114">Override this method if your filter caches the time stamps on the samples it receives.</span></span>

## <a name="requirements"></a><span data-ttu-id="32e46-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="32e46-115">Requirements</span></span>



| <span data-ttu-id="32e46-116">需求</span><span class="sxs-lookup"><span data-stu-id="32e46-116">Requirement</span></span> | <span data-ttu-id="32e46-117">值</span><span class="sxs-lookup"><span data-stu-id="32e46-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32e46-118">標頭</span><span class="sxs-lookup"><span data-stu-id="32e46-118">Header</span></span><br/>  | <dl> <span data-ttu-id="32e46-119"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="32e46-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="32e46-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="32e46-120">Library</span></span><br/> | <dl> <span data-ttu-id="32e46-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="32e46-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32e46-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32e46-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32e46-123">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="32e46-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




