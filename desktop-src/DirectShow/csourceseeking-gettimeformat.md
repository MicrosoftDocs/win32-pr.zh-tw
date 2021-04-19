---
description: GetTimeFormat 方法會抓取目前的時間格式。 這個方法會實 IMediaSeeking：： GetTimeFormat 方法。
ms.assetid: c90804f7-9a0a-423c-8b26-87abf15eddc5
title: 'CSourceSeeking. GetTimeFormat 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce53f4a6cabcc5face6c332666701dc208c3f8bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995786"
---
# <a name="csourceseekinggettimeformat-method"></a><span data-ttu-id="d94ff-104">CSourceSeeking. GetTimeFormat 方法</span><span class="sxs-lookup"><span data-stu-id="d94ff-104">CSourceSeeking.GetTimeFormat method</span></span>

<span data-ttu-id="d94ff-105">方法會抓取 `GetTimeFormat` 目前的時間格式。</span><span class="sxs-lookup"><span data-stu-id="d94ff-105">The `GetTimeFormat` method retrieves the current time format.</span></span> <span data-ttu-id="d94ff-106">這個方法會實 [**IMediaSeeking：： GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) 方法。</span><span class="sxs-lookup"><span data-stu-id="d94ff-106">This method implements the [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d94ff-107">語法</span><span class="sxs-lookup"><span data-stu-id="d94ff-107">Syntax</span></span>


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="d94ff-108">參數</span><span class="sxs-lookup"><span data-stu-id="d94ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d94ff-109">*Pformatetc 架構*</span><span class="sxs-lookup"><span data-stu-id="d94ff-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="d94ff-110">接收時間格式 GUID 之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="d94ff-110">Pointer to a variable that receives a time format GUID.</span></span> <span data-ttu-id="d94ff-111">請參閱 [**時間格式 guid**](time-format-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="d94ff-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d94ff-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d94ff-112">Return value</span></span>

<span data-ttu-id="d94ff-113">傳回下表所列的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="d94ff-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="d94ff-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d94ff-114">Return code</span></span>                                                                               | <span data-ttu-id="d94ff-115">Description</span><span class="sxs-lookup"><span data-stu-id="d94ff-115">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="d94ff-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d94ff-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="d94ff-117">Success</span><span class="sxs-lookup"><span data-stu-id="d94ff-117">Success</span></span><br/>                |
| <dl> <span data-ttu-id="d94ff-118"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="d94ff-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="d94ff-119">**Null** 指標值</span><span class="sxs-lookup"><span data-stu-id="d94ff-119">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d94ff-120">備註</span><span class="sxs-lookup"><span data-stu-id="d94ff-120">Remarks</span></span>

<span data-ttu-id="d94ff-121">基類所支援的唯一時間格式是時間 \_ 格式 \_ 媒體 \_ 時間 (100-毫微秒單位) 。</span><span class="sxs-lookup"><span data-stu-id="d94ff-121">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="d94ff-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="d94ff-122">Requirements</span></span>



| <span data-ttu-id="d94ff-123">需求</span><span class="sxs-lookup"><span data-stu-id="d94ff-123">Requirement</span></span> | <span data-ttu-id="d94ff-124">值</span><span class="sxs-lookup"><span data-stu-id="d94ff-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d94ff-125">標頭</span><span class="sxs-lookup"><span data-stu-id="d94ff-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d94ff-126"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d94ff-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d94ff-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="d94ff-127">Library</span></span><br/> | <dl> <span data-ttu-id="d94ff-128"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d94ff-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d94ff-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d94ff-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d94ff-130">**CSourceSeeking 類別**</span><span class="sxs-lookup"><span data-stu-id="d94ff-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




