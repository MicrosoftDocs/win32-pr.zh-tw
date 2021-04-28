---
description: CPosPassThru. IsFormatSupported 方法-IsFormatSupported 方法會判斷是否支援指定的時間格式。 這個方法會實 IMediaSeeking：： IsFormatSupported 方法。
ms.assetid: dd8751d6-8439-4155-bdaf-b152a7c6cad4
title: 'CPosPassThru. IsFormatSupported 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.IsFormatSupported
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bd4b90bbe86e7ba05aa48fb7888c946babd8ed9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095246"
---
# <a name="cpospassthruisformatsupported-method"></a><span data-ttu-id="426d1-104">CPosPassThru. IsFormatSupported 方法</span><span class="sxs-lookup"><span data-stu-id="426d1-104">CPosPassThru.IsFormatSupported method</span></span>

<span data-ttu-id="426d1-105">`IsFormatSupported`方法會判斷是否支援指定的時間格式。</span><span class="sxs-lookup"><span data-stu-id="426d1-105">The `IsFormatSupported` method determines whether a specified time format is supported.</span></span> <span data-ttu-id="426d1-106">這個方法會實 [**IMediaSeeking：： IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) 方法。</span><span class="sxs-lookup"><span data-stu-id="426d1-106">This method implements the [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="426d1-107">語法</span><span class="sxs-lookup"><span data-stu-id="426d1-107">Syntax</span></span>


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="426d1-108">參數</span><span class="sxs-lookup"><span data-stu-id="426d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="426d1-109">*Pformatetc 架構*</span><span class="sxs-lookup"><span data-stu-id="426d1-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="426d1-110">時間格式 GUID 的指標。</span><span class="sxs-lookup"><span data-stu-id="426d1-110">Pointer to a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="426d1-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="426d1-111">Return value</span></span>

<span data-ttu-id="426d1-112">從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="426d1-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="426d1-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="426d1-113">Requirements</span></span>



| <span data-ttu-id="426d1-114">需求</span><span class="sxs-lookup"><span data-stu-id="426d1-114">Requirement</span></span> | <span data-ttu-id="426d1-115">值</span><span class="sxs-lookup"><span data-stu-id="426d1-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="426d1-116">標頭</span><span class="sxs-lookup"><span data-stu-id="426d1-116">Header</span></span><br/>  | <dl> <span data-ttu-id="426d1-117"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="426d1-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="426d1-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="426d1-118">Library</span></span><br/> | <dl> <span data-ttu-id="426d1-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="426d1-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="426d1-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="426d1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="426d1-121">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="426d1-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="426d1-122">**時間格式 Guid**</span><span class="sxs-lookup"><span data-stu-id="426d1-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




