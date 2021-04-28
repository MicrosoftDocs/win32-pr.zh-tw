---
description: CRendererPosPassThru. GetMediaTime 方法-GetMediaTime 方法會抓取目前樣本上的時間戳記。
ms.assetid: 13710373-04fd-4c1d-ba97-78be5cf27e7d
title: 'CRendererPosPassThru. GetMediaTime 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 588c92faec6b68cfa51392d4df00567c4e881460
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085366"
---
# <a name="crendererpospassthrugetmediatime-method"></a><span data-ttu-id="aa0bc-103">CRendererPosPassThru. GetMediaTime 方法</span><span class="sxs-lookup"><span data-stu-id="aa0bc-103">CRendererPosPassThru.GetMediaTime method</span></span>

<span data-ttu-id="aa0bc-104">方法會抓取 `GetMediaTime` 目前樣本上的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="aa0bc-104">The `GetMediaTime` method retrieves the time stamps on the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa0bc-105">語法</span><span class="sxs-lookup"><span data-stu-id="aa0bc-105">Syntax</span></span>


```C++
HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="aa0bc-106">參數</span><span class="sxs-lookup"><span data-stu-id="aa0bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa0bc-107">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="aa0bc-107">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="aa0bc-108">接收開始時間之變數的指標，以目前時間格式的單位為單位。</span><span class="sxs-lookup"><span data-stu-id="aa0bc-108">Pointer to a variable that receives the start time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="aa0bc-109">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="aa0bc-109">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="aa0bc-110">接收結束時間之變數的指標，以目前時間格式的單位為單位。</span><span class="sxs-lookup"><span data-stu-id="aa0bc-110">Pointer to a variable that receives the end time, in units of the current time format.</span></span> <span data-ttu-id="aa0bc-111">可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="aa0bc-111">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa0bc-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="aa0bc-112">Return value</span></span>

<span data-ttu-id="aa0bc-113">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="aa0bc-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="aa0bc-114">可能的值包括下表所列的值。</span><span class="sxs-lookup"><span data-stu-id="aa0bc-114">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="aa0bc-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="aa0bc-115">Return code</span></span>                                                                                  | <span data-ttu-id="aa0bc-116">Description</span><span class="sxs-lookup"><span data-stu-id="aa0bc-116">Description</span></span>                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="aa0bc-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="aa0bc-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="aa0bc-118">成功。</span><span class="sxs-lookup"><span data-stu-id="aa0bc-118">Success.</span></span><br/>                                    |
| <dl> <span data-ttu-id="aa0bc-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="aa0bc-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="aa0bc-120">不支援轉換成此格式。</span><span class="sxs-lookup"><span data-stu-id="aa0bc-120">Conversion to this format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="aa0bc-121"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="aa0bc-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="aa0bc-122">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="aa0bc-122">**NULL** pointer argument.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="aa0bc-123">備註</span><span class="sxs-lookup"><span data-stu-id="aa0bc-123">Remarks</span></span>

<span data-ttu-id="aa0bc-124">這個方法會覆寫 [**CPosPassThru：： GetMediaTime**](cpospassthru-getmediatime.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="aa0bc-124">This method overrides the [**CPosPassThru::GetMediaTime**](cpospassthru-getmediatime.md) method.</span></span> <span data-ttu-id="aa0bc-125">時間戳記值會藉由呼叫 [**CPosPassThru：： ConvertTimeFormat**](cpospassthru-converttimeformat.md) 方法轉換為目前的時間格式。</span><span class="sxs-lookup"><span data-stu-id="aa0bc-125">The time-stamp values are converted to the current time format by calling the [**CPosPassThru::ConvertTimeFormat**](cpospassthru-converttimeformat.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa0bc-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa0bc-126">Requirements</span></span>



| <span data-ttu-id="aa0bc-127">需求</span><span class="sxs-lookup"><span data-stu-id="aa0bc-127">Requirement</span></span> | <span data-ttu-id="aa0bc-128">值</span><span class="sxs-lookup"><span data-stu-id="aa0bc-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0bc-129">標頭</span><span class="sxs-lookup"><span data-stu-id="aa0bc-129">Header</span></span><br/>  | <dl> <span data-ttu-id="aa0bc-130"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="aa0bc-130"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="aa0bc-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="aa0bc-131">Library</span></span><br/> | <dl> <span data-ttu-id="aa0bc-132"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="aa0bc-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




