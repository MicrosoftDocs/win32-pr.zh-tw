---
description: GetMediaTime 方法會抓取目前樣本上的時間戳記。
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
ms.openlocfilehash: 628c0f0c65dad4e00dd259edbeee97fd8f6f13ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982688"
---
# <a name="crendererpospassthrugetmediatime-method"></a><span data-ttu-id="45ec7-103">CRendererPosPassThru. GetMediaTime 方法</span><span class="sxs-lookup"><span data-stu-id="45ec7-103">CRendererPosPassThru.GetMediaTime method</span></span>

<span data-ttu-id="45ec7-104">方法會抓取 `GetMediaTime` 目前樣本上的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="45ec7-104">The `GetMediaTime` method retrieves the time stamps on the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="45ec7-105">語法</span><span class="sxs-lookup"><span data-stu-id="45ec7-105">Syntax</span></span>


```C++
HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="45ec7-106">參數</span><span class="sxs-lookup"><span data-stu-id="45ec7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45ec7-107">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="45ec7-107">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="45ec7-108">接收開始時間之變數的指標，以目前時間格式的單位為單位。</span><span class="sxs-lookup"><span data-stu-id="45ec7-108">Pointer to a variable that receives the start time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="45ec7-109">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="45ec7-109">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="45ec7-110">接收結束時間之變數的指標，以目前時間格式的單位為單位。</span><span class="sxs-lookup"><span data-stu-id="45ec7-110">Pointer to a variable that receives the end time, in units of the current time format.</span></span> <span data-ttu-id="45ec7-111">可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="45ec7-111">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45ec7-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="45ec7-112">Return value</span></span>

<span data-ttu-id="45ec7-113">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="45ec7-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="45ec7-114">可能的值包括下表所列的值。</span><span class="sxs-lookup"><span data-stu-id="45ec7-114">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="45ec7-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="45ec7-115">Return code</span></span>                                                                                  | <span data-ttu-id="45ec7-116">Description</span><span class="sxs-lookup"><span data-stu-id="45ec7-116">Description</span></span>                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="45ec7-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="45ec7-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="45ec7-118">成功。</span><span class="sxs-lookup"><span data-stu-id="45ec7-118">Success.</span></span><br/>                                    |
| <dl> <span data-ttu-id="45ec7-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="45ec7-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="45ec7-120">不支援轉換成此格式。</span><span class="sxs-lookup"><span data-stu-id="45ec7-120">Conversion to this format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="45ec7-121"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="45ec7-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="45ec7-122">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="45ec7-122">**NULL** pointer argument.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="45ec7-123">備註</span><span class="sxs-lookup"><span data-stu-id="45ec7-123">Remarks</span></span>

<span data-ttu-id="45ec7-124">這個方法會覆寫 [**CPosPassThru：： GetMediaTime**](cpospassthru-getmediatime.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="45ec7-124">This method overrides the [**CPosPassThru::GetMediaTime**](cpospassthru-getmediatime.md) method.</span></span> <span data-ttu-id="45ec7-125">時間戳記值會藉由呼叫 [**CPosPassThru：： ConvertTimeFormat**](cpospassthru-converttimeformat.md) 方法轉換為目前的時間格式。</span><span class="sxs-lookup"><span data-stu-id="45ec7-125">The time-stamp values are converted to the current time format by calling the [**CPosPassThru::ConvertTimeFormat**](cpospassthru-converttimeformat.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="45ec7-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="45ec7-126">Requirements</span></span>



| <span data-ttu-id="45ec7-127">需求</span><span class="sxs-lookup"><span data-stu-id="45ec7-127">Requirement</span></span> | <span data-ttu-id="45ec7-128">值</span><span class="sxs-lookup"><span data-stu-id="45ec7-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45ec7-129">標頭</span><span class="sxs-lookup"><span data-stu-id="45ec7-129">Header</span></span><br/>  | <dl> <span data-ttu-id="45ec7-130"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="45ec7-130"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="45ec7-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="45ec7-131">Library</span></span><br/> | <dl> <span data-ttu-id="45ec7-132"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="45ec7-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




