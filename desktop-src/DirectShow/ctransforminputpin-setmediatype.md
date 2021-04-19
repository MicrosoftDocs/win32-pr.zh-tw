---
description: SetMediaType 方法會設定連接的媒體類型。
ms.assetid: 8e83380f-ba38-4fb8-ac32-40d68a4efea6
title: 'CTransformInputPin. SetMediaType 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b42531a003fbad1a2a08864390a512296c440e64
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994895"
---
# <a name="ctransforminputpinsetmediatype-method"></a><span data-ttu-id="81ad9-103">CTransformInputPin. SetMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="81ad9-103">CTransformInputPin.SetMediaType method</span></span>

<span data-ttu-id="81ad9-104">`SetMediaType`方法會設定連接的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="81ad9-104">The `SetMediaType` method sets the media type for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="81ad9-105">語法</span><span class="sxs-lookup"><span data-stu-id="81ad9-105">Syntax</span></span>


```C++
HRESULT SetMediaType(
   const CMediaType *mt
);
```



## <a name="parameters"></a><span data-ttu-id="81ad9-106">參數</span><span class="sxs-lookup"><span data-stu-id="81ad9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81ad9-107">*mt*</span><span class="sxs-lookup"><span data-stu-id="81ad9-107">*mt*</span></span> 
</dt> <dd>

<span data-ttu-id="81ad9-108">指定媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="81ad9-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81ad9-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="81ad9-109">Return value</span></span>

<span data-ttu-id="81ad9-110">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="81ad9-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="81ad9-111">備註</span><span class="sxs-lookup"><span data-stu-id="81ad9-111">Remarks</span></span>

<span data-ttu-id="81ad9-112">這個方法會覆寫 [**CBasePin：： SetMediaType**](cbasepin-setmediatype.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="81ad9-112">This method overrides the [**CBasePin::SetMediaType**](cbasepin-setmediatype.md) method.</span></span> <span data-ttu-id="81ad9-113">它會呼叫篩選器的 [**CTransformFilter：： SetMediaType**](ctransformfilter-setmediatype.md) 方法來通知篩選。</span><span class="sxs-lookup"><span data-stu-id="81ad9-113">It calls the filter's [**CTransformFilter::SetMediaType**](ctransformfilter-setmediatype.md) method to inform the filter.</span></span>

<span data-ttu-id="81ad9-114">Pin 必須在呼叫這個方法之前，先確認媒體類型是可接受的。</span><span class="sxs-lookup"><span data-stu-id="81ad9-114">The pin must verify that the media type is acceptable before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="81ad9-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="81ad9-115">Requirements</span></span>



| <span data-ttu-id="81ad9-116">需求</span><span class="sxs-lookup"><span data-stu-id="81ad9-116">Requirement</span></span> | <span data-ttu-id="81ad9-117">值</span><span class="sxs-lookup"><span data-stu-id="81ad9-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81ad9-118">標頭</span><span class="sxs-lookup"><span data-stu-id="81ad9-118">Header</span></span><br/>  | <dl> <span data-ttu-id="81ad9-119"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="81ad9-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="81ad9-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="81ad9-120">Library</span></span><br/> | <dl> <span data-ttu-id="81ad9-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="81ad9-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




