---
description: SampleProps 方法會在 AM \_ Sample2.xml 屬性結構中，抓取最新範例的屬性 \_ 。
ms.assetid: d4c98c35-f8b2-4111-bae9-4e0f58a0cc8a
title: 'CBaseInputPin. SampleProps 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.SampleProps
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 45663cfd221c7a31abe5f85a494869b24d1ddd8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983224"
---
# <a name="cbaseinputpinsampleprops-method"></a><span data-ttu-id="e9aed-103">CBaseInputPin. SampleProps 方法</span><span class="sxs-lookup"><span data-stu-id="e9aed-103">CBaseInputPin.SampleProps method</span></span>

<span data-ttu-id="e9aed-104">`SampleProps`方法會在 [**AM \_ sample2.xml \_ 屬性**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)結構中，捕獲最新範例的屬性。</span><span class="sxs-lookup"><span data-stu-id="e9aed-104">The `SampleProps` method retrieves the properties of the most recent sample, in an [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9aed-105">語法</span><span class="sxs-lookup"><span data-stu-id="e9aed-105">Syntax</span></span>


```C++
AM_SAMPLE2_PROPERTIES* SampleProps();
```



## <a name="parameters"></a><span data-ttu-id="e9aed-106">參數</span><span class="sxs-lookup"><span data-stu-id="e9aed-106">Parameters</span></span>

<span data-ttu-id="e9aed-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e9aed-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e9aed-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="e9aed-108">Return value</span></span>

<span data-ttu-id="e9aed-109">傳回 [**CBaseInputPin：： m \_ SampleProps**](cbaseinputpin-m-sampleprops.md) 成員變數的位址。</span><span class="sxs-lookup"><span data-stu-id="e9aed-109">Returns the address of the [**CBaseInputPin::m\_SampleProps**](cbaseinputpin-m-sampleprops.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9aed-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9aed-110">Requirements</span></span>



| <span data-ttu-id="e9aed-111">需求</span><span class="sxs-lookup"><span data-stu-id="e9aed-111">Requirement</span></span> | <span data-ttu-id="e9aed-112">值</span><span class="sxs-lookup"><span data-stu-id="e9aed-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9aed-113">標頭</span><span class="sxs-lookup"><span data-stu-id="e9aed-113">Header</span></span><br/>  | <dl> <span data-ttu-id="e9aed-114"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e9aed-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e9aed-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="e9aed-115">Library</span></span><br/> | <dl> <span data-ttu-id="e9aed-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e9aed-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9aed-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9aed-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9aed-118">**CBaseInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="e9aed-118">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




