---
description: 如果有的話，ConnectionMediaType 方法會抓取目前 pin 連接的媒體類型。 這個方法會實 IPin：： ConnectionMediaType 方法。
ms.assetid: 57d100ba-4171-4caa-ab98-66a0a327a53b
title: 'CBasePin. ConnectionMediaType 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ConnectionMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62bd211b6c93e44c571d822ccc86104a5a6fdcab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998699"
---
# <a name="cbasepinconnectionmediatype-method"></a><span data-ttu-id="93467-104">CBasePin. ConnectionMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="93467-104">CBasePin.ConnectionMediaType method</span></span>

<span data-ttu-id="93467-105">如果有的話， **ConnectionMediaType** 方法會抓取目前 pin 連接的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="93467-105">The **ConnectionMediaType** method retrieves the media type for the current pin connection, if any.</span></span> <span data-ttu-id="93467-106">這個方法會實 [**IPin：： ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) 方法。</span><span class="sxs-lookup"><span data-stu-id="93467-106">This method implements the [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="93467-107">語法</span><span class="sxs-lookup"><span data-stu-id="93467-107">Syntax</span></span>


```C++
HRESULT ConnectionMediaType(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="93467-108">參數</span><span class="sxs-lookup"><span data-stu-id="93467-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93467-109">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="93467-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="93467-110">接收媒體類型的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="93467-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93467-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="93467-111">Return value</span></span>

<span data-ttu-id="93467-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="93467-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="93467-113">可能的值包括下表中的值。</span><span class="sxs-lookup"><span data-stu-id="93467-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="93467-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="93467-114">Return code</span></span>                                                                                           | <span data-ttu-id="93467-115">Description</span><span class="sxs-lookup"><span data-stu-id="93467-115">Description</span></span>                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="93467-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="93467-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="93467-117">成功。</span><span class="sxs-lookup"><span data-stu-id="93467-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="93467-118"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="93467-118"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="93467-119">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="93467-119">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="93467-120"><dt>**VFW \_ E \_ 未 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="93467-120"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="93467-121">Pin 未連接。</span><span class="sxs-lookup"><span data-stu-id="93467-121">Pin is not connected.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="93467-122">備註</span><span class="sxs-lookup"><span data-stu-id="93467-122">Remarks</span></span>

<span data-ttu-id="93467-123">如果連接釘選，這個方法會將媒體類型複製到由 *pmt* 指定的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構中。呼叫端必須釋放媒體類型的格式區塊。</span><span class="sxs-lookup"><span data-stu-id="93467-123">If the pin is connected, this method copies the media type into the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure specified by *pmt*. The caller must free the media type's format block.</span></span> <span data-ttu-id="93467-124">您可以使用 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) 函數或 [**FreeMediaType**](freemediatype.md) helper 函數。</span><span class="sxs-lookup"><span data-stu-id="93467-124">You can use the [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) function, or the [**FreeMediaType**](freemediatype.md) helper function.</span></span>

<span data-ttu-id="93467-125">如果未連接到 pin，這個方法會將 *pmt* 指定的記憶體區塊零零，並傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="93467-125">If the pin is not connected, this method zeroes the memory block specified by *pmt* and returns an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="93467-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="93467-126">Requirements</span></span>



| <span data-ttu-id="93467-127">需求</span><span class="sxs-lookup"><span data-stu-id="93467-127">Requirement</span></span> | <span data-ttu-id="93467-128">值</span><span class="sxs-lookup"><span data-stu-id="93467-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93467-129">標頭</span><span class="sxs-lookup"><span data-stu-id="93467-129">Header</span></span><br/>  | <dl> <span data-ttu-id="93467-130"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="93467-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="93467-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="93467-131">Library</span></span><br/> | <dl> <span data-ttu-id="93467-132"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="93467-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93467-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93467-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93467-134">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="93467-134">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

