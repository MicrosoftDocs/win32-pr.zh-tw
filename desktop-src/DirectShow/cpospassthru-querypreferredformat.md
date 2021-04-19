---
description: QueryPreferredFormat 方法會抓取資料流程的慣用時間格式。 這個方法會實 IMediaSeeking：： QueryPreferredFormat 方法。
ms.assetid: 8637448f-6b53-4ec9-9671-43bc8b713668
title: 'CPosPassThru. QueryPreferredFormat 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.QueryPreferredFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c22348a10e8b9e5f241e06252c025e2ec9593486
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995751"
---
# <a name="cpospassthruquerypreferredformat-method"></a><span data-ttu-id="2a561-104">CPosPassThru. QueryPreferredFormat 方法</span><span class="sxs-lookup"><span data-stu-id="2a561-104">CPosPassThru.QueryPreferredFormat method</span></span>

<span data-ttu-id="2a561-105">方法會抓取 `QueryPreferredFormat` 資料流程的慣用時間格式。</span><span class="sxs-lookup"><span data-stu-id="2a561-105">The `QueryPreferredFormat` method retrieves the preferred time format for the stream.</span></span> <span data-ttu-id="2a561-106">這個方法會實 [**IMediaSeeking：： QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) 方法。</span><span class="sxs-lookup"><span data-stu-id="2a561-106">This method implements the [**IMediaSeeking::QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a561-107">語法</span><span class="sxs-lookup"><span data-stu-id="2a561-107">Syntax</span></span>


```C++
HRESULT QueryPreferredFormat(
   GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="2a561-108">參數</span><span class="sxs-lookup"><span data-stu-id="2a561-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a561-109">*Pformatetc 架構*</span><span class="sxs-lookup"><span data-stu-id="2a561-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="2a561-110">接收時間格式 GUID 之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="2a561-110">Pointer to a variable that receives a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a561-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2a561-111">Return value</span></span>

<span data-ttu-id="2a561-112">從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="2a561-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a561-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a561-113">Requirements</span></span>



| <span data-ttu-id="2a561-114">需求</span><span class="sxs-lookup"><span data-stu-id="2a561-114">Requirement</span></span> | <span data-ttu-id="2a561-115">值</span><span class="sxs-lookup"><span data-stu-id="2a561-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a561-116">標頭</span><span class="sxs-lookup"><span data-stu-id="2a561-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2a561-117"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2a561-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2a561-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="2a561-118">Library</span></span><br/> | <dl> <span data-ttu-id="2a561-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="2a561-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a561-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a561-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a561-121">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="2a561-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="2a561-122">**時間格式 Guid**</span><span class="sxs-lookup"><span data-stu-id="2a561-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




