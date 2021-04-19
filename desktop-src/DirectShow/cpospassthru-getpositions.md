---
description: GetPositions 方法會抓取目前的位置和停止位置，相對於資料流程的總持續時間。 這個方法會實 IMediaSeeking：： GetPositions 方法。
ms.assetid: 51e45bc3-ae30-4b05-b9d9-684c1b028f51
title: 'CPosPassThru. GetPositions 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0852199e8e143ce5b0348c3b79afd495a5a47627
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999281"
---
# <a name="cpospassthrugetpositions-method"></a><span data-ttu-id="29027-104">CPosPassThru. GetPositions 方法</span><span class="sxs-lookup"><span data-stu-id="29027-104">CPosPassThru.GetPositions method</span></span>

<span data-ttu-id="29027-105">方法會抓取 `GetPositions` 目前的位置和停止位置，相對於資料流程的總持續時間。</span><span class="sxs-lookup"><span data-stu-id="29027-105">The `GetPositions` method retrieves the current position and the stop position, relative to the total duration of the stream.</span></span> <span data-ttu-id="29027-106">這個方法會實 [**IMediaSeeking：： GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) 方法。</span><span class="sxs-lookup"><span data-stu-id="29027-106">This method implements the [**IMediaSeeking::GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="29027-107">語法</span><span class="sxs-lookup"><span data-stu-id="29027-107">Syntax</span></span>


```C++
HRESULT GetPositions(
   LONGLONG *pCurrent,
   LONGLONG *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="29027-108">參數</span><span class="sxs-lookup"><span data-stu-id="29027-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29027-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="29027-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="29027-110">變數的指標，此變數會接收目前的位置，以目前時間格式的單位為單位。</span><span class="sxs-lookup"><span data-stu-id="29027-110">Pointer to a variable that receives the current position, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="29027-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="29027-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="29027-112">接收停止位置之變數的指標，以目前時間格式的單位為單位。</span><span class="sxs-lookup"><span data-stu-id="29027-112">Pointer to a variable that receives the stop position, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29027-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="29027-113">Return value</span></span>

<span data-ttu-id="29027-114">從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="29027-114">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="29027-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="29027-115">Requirements</span></span>



| <span data-ttu-id="29027-116">需求</span><span class="sxs-lookup"><span data-stu-id="29027-116">Requirement</span></span> | <span data-ttu-id="29027-117">值</span><span class="sxs-lookup"><span data-stu-id="29027-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29027-118">標頭</span><span class="sxs-lookup"><span data-stu-id="29027-118">Header</span></span><br/>  | <dl> <span data-ttu-id="29027-119"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="29027-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="29027-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="29027-120">Library</span></span><br/> | <dl> <span data-ttu-id="29027-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="29027-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29027-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29027-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29027-123">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="29027-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




