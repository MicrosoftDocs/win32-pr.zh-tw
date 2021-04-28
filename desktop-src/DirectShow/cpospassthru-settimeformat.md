---
description: CPosPassThru. SetTimeFormat 方法-SetTimeFormat 方法會設定時間格式。 這個方法會實 IMediaSeeking：： SetTimeFormat 方法。
ms.assetid: f6fc456d-51cf-4b2e-9248-afed9073d440
title: 'CPosPassThru. SetTimeFormat 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 81798ccbb51056353c62cd94f821b3567d78a484
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085466"
---
# <a name="cpospassthrusettimeformat-method"></a><span data-ttu-id="976eb-104">CPosPassThru. SetTimeFormat 方法</span><span class="sxs-lookup"><span data-stu-id="976eb-104">CPosPassThru.SetTimeFormat method</span></span>

<span data-ttu-id="976eb-105">SetTimeFormat 方法會設定時間格式。</span><span class="sxs-lookup"><span data-stu-id="976eb-105">The SetTimeFormat method sets the time format.</span></span> <span data-ttu-id="976eb-106">這個方法會實 [**IMediaSeeking：： SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) 方法。</span><span class="sxs-lookup"><span data-stu-id="976eb-106">This method implements the [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="976eb-107">語法</span><span class="sxs-lookup"><span data-stu-id="976eb-107">Syntax</span></span>


```C++
HRESULT SetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="976eb-108">參數</span><span class="sxs-lookup"><span data-stu-id="976eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="976eb-109">*Pformatetc 架構*</span><span class="sxs-lookup"><span data-stu-id="976eb-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="976eb-110">時間格式 GUID 的指標。</span><span class="sxs-lookup"><span data-stu-id="976eb-110">Pointer to a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="976eb-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="976eb-111">Return value</span></span>

<span data-ttu-id="976eb-112">從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="976eb-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="976eb-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="976eb-113">Requirements</span></span>



| <span data-ttu-id="976eb-114">需求</span><span class="sxs-lookup"><span data-stu-id="976eb-114">Requirement</span></span> | <span data-ttu-id="976eb-115">值</span><span class="sxs-lookup"><span data-stu-id="976eb-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="976eb-116">標頭</span><span class="sxs-lookup"><span data-stu-id="976eb-116">Header</span></span><br/>  | <dl> <span data-ttu-id="976eb-117"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="976eb-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="976eb-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="976eb-118">Library</span></span><br/> | <dl> <span data-ttu-id="976eb-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="976eb-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="976eb-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="976eb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="976eb-121">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="976eb-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="976eb-122">**時間格式 Guid**</span><span class="sxs-lookup"><span data-stu-id="976eb-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




