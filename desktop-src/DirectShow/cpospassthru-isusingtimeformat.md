---
description: IsUsingTimeFormat 方法會判斷指定的時間格式是否為目前使用中的格式。 這個方法會實 IMediaSeeking：： IsUsingTimeFormat 方法。
ms.assetid: e377bcf0-0518-42b2-8975-e4c345e3fed4
title: 'CPosPassThru. IsUsingTimeFormat 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.IsUsingTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 012a9487f5840117edb9f8bc0afa1d9388b4bce0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000995"
---
# <a name="cpospassthruisusingtimeformat-method"></a><span data-ttu-id="35d8b-104">CPosPassThru. IsUsingTimeFormat 方法</span><span class="sxs-lookup"><span data-stu-id="35d8b-104">CPosPassThru.IsUsingTimeFormat method</span></span>

<span data-ttu-id="35d8b-105">`IsUsingTimeFormat`方法會判斷指定的時間格式是否為目前使用中的格式。</span><span class="sxs-lookup"><span data-stu-id="35d8b-105">The `IsUsingTimeFormat` method determines whether a specified time format is the format currently in use.</span></span> <span data-ttu-id="35d8b-106">這個方法會實 [**IMediaSeeking：： IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat) 方法。</span><span class="sxs-lookup"><span data-stu-id="35d8b-106">This method implements the [**IMediaSeeking::IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="35d8b-107">語法</span><span class="sxs-lookup"><span data-stu-id="35d8b-107">Syntax</span></span>


```C++
HRESULT IsUsingTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="35d8b-108">參數</span><span class="sxs-lookup"><span data-stu-id="35d8b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35d8b-109">*Pformatetc 架構*</span><span class="sxs-lookup"><span data-stu-id="35d8b-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="35d8b-110">時間格式 GUID 的指標。</span><span class="sxs-lookup"><span data-stu-id="35d8b-110">Pointer to a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35d8b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="35d8b-111">Return value</span></span>

<span data-ttu-id="35d8b-112">從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="35d8b-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="35d8b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="35d8b-113">Requirements</span></span>



| <span data-ttu-id="35d8b-114">需求</span><span class="sxs-lookup"><span data-stu-id="35d8b-114">Requirement</span></span> | <span data-ttu-id="35d8b-115">值</span><span class="sxs-lookup"><span data-stu-id="35d8b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35d8b-116">標頭</span><span class="sxs-lookup"><span data-stu-id="35d8b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="35d8b-117"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="35d8b-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="35d8b-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="35d8b-118">Library</span></span><br/> | <dl> <span data-ttu-id="35d8b-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="35d8b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35d8b-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35d8b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35d8b-121">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="35d8b-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="35d8b-122">**時間格式 Guid**</span><span class="sxs-lookup"><span data-stu-id="35d8b-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




