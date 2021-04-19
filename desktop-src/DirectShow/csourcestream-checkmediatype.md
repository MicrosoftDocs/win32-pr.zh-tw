---
description: CheckMediaType 方法會判斷 pin 是否接受特定的媒體類型。 這個方法會實作為純虛擬 CBasePin：： CheckMediaType 方法。
ms.assetid: 3db7c74c-a6aa-4b49-b2a5-9bf8db35fd7e
title: 'CSourceStream. CheckMediaType 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62f8b6c18613f5c187fc637febd08b74260a1e44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990254"
---
# <a name="csourcestreamcheckmediatype-method"></a><span data-ttu-id="7c629-104">CSourceStream. CheckMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="7c629-104">CSourceStream.CheckMediaType method</span></span>

<span data-ttu-id="7c629-105">`CheckMediaType`方法會判斷 pin 是否接受特定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="7c629-105">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span> <span data-ttu-id="7c629-106">這個方法會實作為純虛擬 [**CBasePin：： CheckMediaType**](cbasepin-checkmediatype.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="7c629-106">This method implements the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c629-107">語法</span><span class="sxs-lookup"><span data-stu-id="7c629-107">Syntax</span></span>


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="7c629-108">參數</span><span class="sxs-lookup"><span data-stu-id="7c629-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c629-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="7c629-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="7c629-110">[**CMediaType**](cmediatype.md)物件的指標，該物件包含建議的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="7c629-110">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c629-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7c629-111">Return value</span></span>

<span data-ttu-id="7c629-112">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="7c629-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="7c629-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="7c629-113">Return code</span></span>                                                                            | <span data-ttu-id="7c629-114">Description</span><span class="sxs-lookup"><span data-stu-id="7c629-114">Description</span></span>                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="7c629-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="7c629-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="7c629-116">此 pin 支援此媒體類型。</span><span class="sxs-lookup"><span data-stu-id="7c629-116">This pin supports this media type.</span></span><br/>        |
| <dl> <span data-ttu-id="7c629-117"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="7c629-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="7c629-118">Pin 不支援此媒體類型。</span><span class="sxs-lookup"><span data-stu-id="7c629-118">The pin does not support this media type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7c629-119">備註</span><span class="sxs-lookup"><span data-stu-id="7c629-119">Remarks</span></span>

<span data-ttu-id="7c629-120">根據預設，pin 支援單一媒體類型。</span><span class="sxs-lookup"><span data-stu-id="7c629-120">By default, the pin supports a single media type.</span></span> <span data-ttu-id="7c629-121">這個方法會呼叫 [**CSourceStream：： GetMediaType**](csourcestream-getmediatype.md) 方法的單一參數版本，以抓取支援的型別，並將它與建議的型別進行比較。</span><span class="sxs-lookup"><span data-stu-id="7c629-121">This method retrieves the supported type by calling the single-parameter version of the [**CSourceStream::GetMediaType**](csourcestream-getmediatype.md) method, and compares it to the proposed type.</span></span> <span data-ttu-id="7c629-122">如果您的 pin 支援一個以上的媒體類型，請覆寫這個方法。</span><span class="sxs-lookup"><span data-stu-id="7c629-122">If your pin supports more than one media type, override this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c629-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c629-123">Requirements</span></span>



| <span data-ttu-id="7c629-124">需求</span><span class="sxs-lookup"><span data-stu-id="7c629-124">Requirement</span></span> | <span data-ttu-id="7c629-125">值</span><span class="sxs-lookup"><span data-stu-id="7c629-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c629-126">標頭</span><span class="sxs-lookup"><span data-stu-id="7c629-126">Header</span></span><br/>  | <dl> <span data-ttu-id="7c629-127"><dt>來源 .h (包含) 的資料流程 </dt></span><span class="sxs-lookup"><span data-stu-id="7c629-127"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7c629-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="7c629-128">Library</span></span><br/> | <dl> <span data-ttu-id="7c629-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7c629-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c629-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c629-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c629-131">**CSourceStream 類別**</span><span class="sxs-lookup"><span data-stu-id="7c629-131">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




