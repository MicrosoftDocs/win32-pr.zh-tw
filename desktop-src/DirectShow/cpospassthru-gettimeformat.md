---
description: GetTimeFormat 方法會抓取目前的時間格式。 這個方法會實 IMediaSeeking：： GetTimeFormat 方法。
ms.assetid: 445c1873-da6f-42be-a4cf-0c475c5f0723
title: 'CPosPassThru. GetTimeFormat 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7db1b46cfe2ac06dc43b52009043ae32676f154
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995970"
---
# <a name="cpospassthrugettimeformat-method"></a><span data-ttu-id="34bf0-104">CPosPassThru. GetTimeFormat 方法</span><span class="sxs-lookup"><span data-stu-id="34bf0-104">CPosPassThru.GetTimeFormat method</span></span>

<span data-ttu-id="34bf0-105">方法會抓取 `GetTimeFormat` 目前的時間格式。</span><span class="sxs-lookup"><span data-stu-id="34bf0-105">The `GetTimeFormat` method retrieves the current time format.</span></span> <span data-ttu-id="34bf0-106">這個方法會實 [**IMediaSeeking：： GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) 方法。</span><span class="sxs-lookup"><span data-stu-id="34bf0-106">This method implements the [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="34bf0-107">語法</span><span class="sxs-lookup"><span data-stu-id="34bf0-107">Syntax</span></span>


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="34bf0-108">參數</span><span class="sxs-lookup"><span data-stu-id="34bf0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34bf0-109">*Pformatetc 架構*</span><span class="sxs-lookup"><span data-stu-id="34bf0-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="34bf0-110">接收時間格式 GUID 之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="34bf0-110">Pointer to a variable that receives a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34bf0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="34bf0-111">Return value</span></span>

<span data-ttu-id="34bf0-112">從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="34bf0-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="34bf0-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="34bf0-113">Requirements</span></span>



| <span data-ttu-id="34bf0-114">需求</span><span class="sxs-lookup"><span data-stu-id="34bf0-114">Requirement</span></span> | <span data-ttu-id="34bf0-115">值</span><span class="sxs-lookup"><span data-stu-id="34bf0-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34bf0-116">標頭</span><span class="sxs-lookup"><span data-stu-id="34bf0-116">Header</span></span><br/>  | <dl> <span data-ttu-id="34bf0-117"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="34bf0-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="34bf0-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="34bf0-118">Library</span></span><br/> | <dl> <span data-ttu-id="34bf0-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="34bf0-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34bf0-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="34bf0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34bf0-121">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="34bf0-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="34bf0-122">**時間格式 Guid**</span><span class="sxs-lookup"><span data-stu-id="34bf0-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




