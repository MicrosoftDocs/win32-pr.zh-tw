---
description: IsFormatSupported 方法會判斷是否支援指定的時間格式。 這個方法會實 IMediaSeeking：： IsFormatSupported 方法。
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
ms.openlocfilehash: 85bdbef2315bd2c9e2bc92f639a7d328f1f17ce0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001209"
---
# <a name="cpospassthruisformatsupported-method"></a><span data-ttu-id="92262-104">CPosPassThru. IsFormatSupported 方法</span><span class="sxs-lookup"><span data-stu-id="92262-104">CPosPassThru.IsFormatSupported method</span></span>

<span data-ttu-id="92262-105">`IsFormatSupported`方法會判斷是否支援指定的時間格式。</span><span class="sxs-lookup"><span data-stu-id="92262-105">The `IsFormatSupported` method determines whether a specified time format is supported.</span></span> <span data-ttu-id="92262-106">這個方法會實 [**IMediaSeeking：： IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) 方法。</span><span class="sxs-lookup"><span data-stu-id="92262-106">This method implements the [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="92262-107">語法</span><span class="sxs-lookup"><span data-stu-id="92262-107">Syntax</span></span>


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="92262-108">參數</span><span class="sxs-lookup"><span data-stu-id="92262-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92262-109">*Pformatetc 架構*</span><span class="sxs-lookup"><span data-stu-id="92262-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="92262-110">時間格式 GUID 的指標。</span><span class="sxs-lookup"><span data-stu-id="92262-110">Pointer to a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92262-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="92262-111">Return value</span></span>

<span data-ttu-id="92262-112">從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="92262-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="92262-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="92262-113">Requirements</span></span>



| <span data-ttu-id="92262-114">需求</span><span class="sxs-lookup"><span data-stu-id="92262-114">Requirement</span></span> | <span data-ttu-id="92262-115">值</span><span class="sxs-lookup"><span data-stu-id="92262-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92262-116">標頭</span><span class="sxs-lookup"><span data-stu-id="92262-116">Header</span></span><br/>  | <dl> <span data-ttu-id="92262-117"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="92262-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="92262-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="92262-118">Library</span></span><br/> | <dl> <span data-ttu-id="92262-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="92262-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92262-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="92262-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92262-121">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="92262-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="92262-122">**時間格式 Guid**</span><span class="sxs-lookup"><span data-stu-id="92262-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




