---
description: IsUsingTimeFormat 方法會判斷指定的時間格式是否為目前使用中的格式。
ms.assetid: 86965bfc-fc9f-42d3-bcaa-2049195b98bd
title: 'CSourceSeeking. IsUsingTimeFormat 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.IsUsingTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8229387364a061febc7bd825e7bc76ee5d9b4a2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978764"
---
# <a name="csourceseekingisusingtimeformat-method"></a><span data-ttu-id="c5171-103">CSourceSeeking. IsUsingTimeFormat 方法</span><span class="sxs-lookup"><span data-stu-id="c5171-103">CSourceSeeking.IsUsingTimeFormat method</span></span>

<span data-ttu-id="c5171-104">`IsUsingTimeFormat`方法會判斷指定的時間格式是否為目前使用中的格式。</span><span class="sxs-lookup"><span data-stu-id="c5171-104">The `IsUsingTimeFormat` method determines whether a specified time format is the format currently in use.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5171-105">語法</span><span class="sxs-lookup"><span data-stu-id="c5171-105">Syntax</span></span>


```C++
HRESULT IsUsingTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="c5171-106">參數</span><span class="sxs-lookup"><span data-stu-id="c5171-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5171-107">*Pformatetc 架構*</span><span class="sxs-lookup"><span data-stu-id="c5171-107">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="c5171-108">時間格式 GUID 的指標。</span><span class="sxs-lookup"><span data-stu-id="c5171-108">Pointer to a time format GUID.</span></span> <span data-ttu-id="c5171-109">請參閱 [**時間格式 guid**](time-format-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="c5171-109">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5171-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5171-110">Return value</span></span>

<span data-ttu-id="c5171-111">傳回下表所列的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="c5171-111">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="c5171-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c5171-112">Return code</span></span>                                                                               | <span data-ttu-id="c5171-113">Description</span><span class="sxs-lookup"><span data-stu-id="c5171-113">Description</span></span>                                                |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="c5171-114"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="c5171-114"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="c5171-115">指定的格式不是目前的格式。</span><span class="sxs-lookup"><span data-stu-id="c5171-115">The specified format is not the current format.</span></span><br/> |
| <dl> <span data-ttu-id="c5171-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c5171-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="c5171-117">指定的格式為目前的格式。</span><span class="sxs-lookup"><span data-stu-id="c5171-117">The specified format is the current format.</span></span><br/>     |
| <dl> <span data-ttu-id="c5171-118"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="c5171-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="c5171-119">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="c5171-119">**NULL** pointer argument.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="c5171-120">備註</span><span class="sxs-lookup"><span data-stu-id="c5171-120">Remarks</span></span>

<span data-ttu-id="c5171-121">基類所支援的唯一時間格式是時間 \_ 格式 \_ 媒體 \_ 時間 (100-毫微秒單位) 。</span><span class="sxs-lookup"><span data-stu-id="c5171-121">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5171-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5171-122">Requirements</span></span>



| <span data-ttu-id="c5171-123">需求</span><span class="sxs-lookup"><span data-stu-id="c5171-123">Requirement</span></span> | <span data-ttu-id="c5171-124">值</span><span class="sxs-lookup"><span data-stu-id="c5171-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5171-125">標頭</span><span class="sxs-lookup"><span data-stu-id="c5171-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c5171-126"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c5171-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c5171-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="c5171-127">Library</span></span><br/> | <dl> <span data-ttu-id="c5171-128"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c5171-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5171-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5171-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5171-130">**CSourceSeeking 類別**</span><span class="sxs-lookup"><span data-stu-id="c5171-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




