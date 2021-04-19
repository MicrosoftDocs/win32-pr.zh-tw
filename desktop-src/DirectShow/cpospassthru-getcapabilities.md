---
description: GetCapabilities 方法會抓取資料流程的所有搜尋功能。 這個方法會實 IMediaSeeking：： GetCapabilities 方法。
ms.assetid: c60c4f47-48de-47d0-9b87-589b84df842c
title: 'CPosPassThru. GetCapabilities 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f896adbc1015cb34e6f9063cb5ebf73e5cdb441c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984042"
---
# <a name="cpospassthrugetcapabilities-method"></a><span data-ttu-id="aa685-104">CPosPassThru. GetCapabilities 方法</span><span class="sxs-lookup"><span data-stu-id="aa685-104">CPosPassThru.GetCapabilities method</span></span>

<span data-ttu-id="aa685-105">**GetCapabilities** 方法會抓取資料流程的所有搜尋功能。</span><span class="sxs-lookup"><span data-stu-id="aa685-105">The **GetCapabilities** method retrieves all the seeking capabilities of the stream.</span></span> <span data-ttu-id="aa685-106">這個方法會實 [**IMediaSeeking：： GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) 方法。</span><span class="sxs-lookup"><span data-stu-id="aa685-106">This method implements the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa685-107">語法</span><span class="sxs-lookup"><span data-stu-id="aa685-107">Syntax</span></span>


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="aa685-108">參數</span><span class="sxs-lookup"><span data-stu-id="aa685-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa685-109">*pCapabilities*</span><span class="sxs-lookup"><span data-stu-id="aa685-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="aa685-110">變數的指標，此變數會接收搜尋 [**\_ \_ \_ 功能**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) 旗標之 AM 的位元組合。</span><span class="sxs-lookup"><span data-stu-id="aa685-110">Pointer to a variable that receives a bitwise combination of [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa685-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="aa685-111">Return value</span></span>

<span data-ttu-id="aa685-112">從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="aa685-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa685-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa685-113">Requirements</span></span>



| <span data-ttu-id="aa685-114">需求</span><span class="sxs-lookup"><span data-stu-id="aa685-114">Requirement</span></span> | <span data-ttu-id="aa685-115">值</span><span class="sxs-lookup"><span data-stu-id="aa685-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa685-116">標頭</span><span class="sxs-lookup"><span data-stu-id="aa685-116">Header</span></span><br/>  | <dl> <span data-ttu-id="aa685-117"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="aa685-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="aa685-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="aa685-118">Library</span></span><br/> | <dl> <span data-ttu-id="aa685-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="aa685-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa685-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa685-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa685-121">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="aa685-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




