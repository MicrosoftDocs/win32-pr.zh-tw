---
description: StartAt 方法會在開始傳遞資料時通知 pin。 這個方法會實 IAMStreamControl：： StartAt 方法。
ms.assetid: fd2943e8-8d35-4122-a99e-96d12459b335
title: 'CBaseStreamControl. StartAt 方法 (Strmctl .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.StartAt
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7adcf7cbd435992333bb8ae59d5ab1674056223
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993937"
---
# <a name="cbasestreamcontrolstartat-method"></a><span data-ttu-id="cdefb-104">CBaseStreamControl. StartAt 方法</span><span class="sxs-lookup"><span data-stu-id="cdefb-104">CBaseStreamControl.StartAt method</span></span>

<span data-ttu-id="cdefb-105">`StartAt`方法會在開始傳遞資料時通知 pin。</span><span class="sxs-lookup"><span data-stu-id="cdefb-105">The `StartAt` method informs the pin when to start delivering data.</span></span> <span data-ttu-id="cdefb-106">這個方法會實 [**IAMStreamControl：： StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) 方法。</span><span class="sxs-lookup"><span data-stu-id="cdefb-106">This method implements the [**IAMStreamControl::StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdefb-107">語法</span><span class="sxs-lookup"><span data-stu-id="cdefb-107">Syntax</span></span>


```C++
HRESULT StartAt(
   const REFERENCE_TIME *ptStart = NULL,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a><span data-ttu-id="cdefb-108">參數</span><span class="sxs-lookup"><span data-stu-id="cdefb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdefb-109">*ptStart*</span><span class="sxs-lookup"><span data-stu-id="cdefb-109">*ptStart*</span></span> 
</dt> <dd>

<span data-ttu-id="cdefb-110">[**參考 \_ 時間**](reference-time.md)值的指標，此值會指定 pin 應開始傳遞資料的時間。</span><span class="sxs-lookup"><span data-stu-id="cdefb-110">Pointer to a [**REFERENCE\_TIME**](reference-time.md) value that specifies when the pin should start delivering data.</span></span>

</dd> <dt>

<span data-ttu-id="cdefb-111">*dwCookie*</span><span class="sxs-lookup"><span data-stu-id="cdefb-111">*dwCookie*</span></span> 
</dt> <dd>

<span data-ttu-id="cdefb-112">指定要連同開始通知一起傳送的值。</span><span class="sxs-lookup"><span data-stu-id="cdefb-112">Specifies a value to send along with the start notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdefb-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="cdefb-113">Return value</span></span>

<span data-ttu-id="cdefb-114">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="cdefb-114">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdefb-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="cdefb-115">Requirements</span></span>



| <span data-ttu-id="cdefb-116">需求</span><span class="sxs-lookup"><span data-stu-id="cdefb-116">Requirement</span></span> | <span data-ttu-id="cdefb-117">值</span><span class="sxs-lookup"><span data-stu-id="cdefb-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdefb-118">標頭</span><span class="sxs-lookup"><span data-stu-id="cdefb-118">Header</span></span><br/>  | <dl> <span data-ttu-id="cdefb-119"><dt>Strmctl (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="cdefb-119"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cdefb-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="cdefb-120">Library</span></span><br/> | <dl> <span data-ttu-id="cdefb-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="cdefb-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdefb-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cdefb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdefb-123">**CBaseStreamControl 類別**</span><span class="sxs-lookup"><span data-stu-id="cdefb-123">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




