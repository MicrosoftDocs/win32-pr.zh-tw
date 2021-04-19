---
description: StopAt 方法會通知 pin 何時停止傳遞資料。 這個方法會實 IAMStreamControl：： StopAt 方法。
ms.assetid: cc9f0fdc-253b-4feb-95ce-56ebc575a49b
title: 'CBaseStreamControl. StopAt 方法 (Strmctl .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.StopAt
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e6b794f5f05721f403d943252c2aabd48614519
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985931"
---
# <a name="cbasestreamcontrolstopat-method"></a><span data-ttu-id="67e38-104">CBaseStreamControl. StopAt 方法</span><span class="sxs-lookup"><span data-stu-id="67e38-104">CBaseStreamControl.StopAt method</span></span>

<span data-ttu-id="67e38-105">`StopAt`方法會在停止傳遞資料時通知 pin。</span><span class="sxs-lookup"><span data-stu-id="67e38-105">The `StopAt` method informs the pin when to stop delivering data.</span></span> <span data-ttu-id="67e38-106">這個方法會實 [**IAMStreamControl：： StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) 方法。</span><span class="sxs-lookup"><span data-stu-id="67e38-106">This method implements the [**IAMStreamControl::StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="67e38-107">語法</span><span class="sxs-lookup"><span data-stu-id="67e38-107">Syntax</span></span>


```C++
HRESULT StopAt(
   const REFERENCE_TIME *ptStop = NULL,
         BOOL           bSendExtra = FALSE,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a><span data-ttu-id="67e38-108">參數</span><span class="sxs-lookup"><span data-stu-id="67e38-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67e38-109">*ptStop*</span><span class="sxs-lookup"><span data-stu-id="67e38-109">*ptStop*</span></span> 
</dt> <dd>

<span data-ttu-id="67e38-110">[**參考 \_ 時間**](reference-time.md)值的指標，此值會指定 pin 應停止傳遞資料的時間。</span><span class="sxs-lookup"><span data-stu-id="67e38-110">Pointer to a [**REFERENCE\_TIME**](reference-time.md) value that specifies when the pin should stop delivering data.</span></span>

</dd> <dt>

<span data-ttu-id="67e38-111">*bSendExtra*</span><span class="sxs-lookup"><span data-stu-id="67e38-111">*bSendExtra*</span></span> 
</dt> <dd>

<span data-ttu-id="67e38-112">指定布林值，指出是否要在排定的停止時間之後傳送額外的範例。</span><span class="sxs-lookup"><span data-stu-id="67e38-112">Specifies a Boolean value that indicates whether to send an extra sample after the scheduled stop time.</span></span> <span data-ttu-id="67e38-113">若 **為 TRUE**，則會傳送一個額外的範例給 pin。</span><span class="sxs-lookup"><span data-stu-id="67e38-113">If **TRUE**, the pin sends one extra sample.</span></span>

</dd> <dt>

<span data-ttu-id="67e38-114">*dwCookie*</span><span class="sxs-lookup"><span data-stu-id="67e38-114">*dwCookie*</span></span> 
</dt> <dd>

<span data-ttu-id="67e38-115">指定要連同開始通知一起傳送的值。</span><span class="sxs-lookup"><span data-stu-id="67e38-115">Specifies a value to send along with the start notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67e38-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="67e38-116">Return value</span></span>

<span data-ttu-id="67e38-117">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="67e38-117">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="67e38-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="67e38-118">Requirements</span></span>



| <span data-ttu-id="67e38-119">需求</span><span class="sxs-lookup"><span data-stu-id="67e38-119">Requirement</span></span> | <span data-ttu-id="67e38-120">值</span><span class="sxs-lookup"><span data-stu-id="67e38-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67e38-121">標頭</span><span class="sxs-lookup"><span data-stu-id="67e38-121">Header</span></span><br/>  | <dl> <span data-ttu-id="67e38-122"><dt>Strmctl (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="67e38-122"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="67e38-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="67e38-123">Library</span></span><br/> | <dl> <span data-ttu-id="67e38-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="67e38-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67e38-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67e38-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67e38-126">**CBaseStreamControl 類別**</span><span class="sxs-lookup"><span data-stu-id="67e38-126">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




