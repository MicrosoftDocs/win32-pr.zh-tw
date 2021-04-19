---
description: InitMediaType 方法會初始化媒體類型。
ms.assetid: 141ced68-11ed-4567-b2e1-82c040d3b4a4
title: " (Mtype 的 CMediaType.InitMediaType 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.InitMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c3bbe170c6d896f3b28d9b85cf49f18269341d50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999070"
---
# <a name="cmediatypeinitmediatype-method"></a><span data-ttu-id="5c2dc-103">CMediaType.InitMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="5c2dc-103">CMediaType.InitMediaType method</span></span>

<span data-ttu-id="5c2dc-104">`InitMediaType`方法會初始化媒體類型。</span><span class="sxs-lookup"><span data-stu-id="5c2dc-104">The `InitMediaType` method initializes the media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c2dc-105">語法</span><span class="sxs-lookup"><span data-stu-id="5c2dc-105">Syntax</span></span>


```C++
void InitMediaType();
```



## <a name="parameters"></a><span data-ttu-id="5c2dc-106">參數</span><span class="sxs-lookup"><span data-stu-id="5c2dc-106">Parameters</span></span>

<span data-ttu-id="5c2dc-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="5c2dc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5c2dc-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="5c2dc-108">Return value</span></span>

<span data-ttu-id="5c2dc-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5c2dc-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c2dc-110">備註</span><span class="sxs-lookup"><span data-stu-id="5c2dc-110">Remarks</span></span>

<span data-ttu-id="5c2dc-111">這個方法會將物件的記憶體設為零，將固定大小樣本大小的屬性設定為 **TRUE**，並將樣本大小設定為1。</span><span class="sxs-lookup"><span data-stu-id="5c2dc-111">This method zeroes the object's memory, sets the fixed-sample-size property to **TRUE**, and sets the sample size to 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c2dc-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c2dc-112">Requirements</span></span>



| <span data-ttu-id="5c2dc-113">需求</span><span class="sxs-lookup"><span data-stu-id="5c2dc-113">Requirement</span></span> | <span data-ttu-id="5c2dc-114">值</span><span class="sxs-lookup"><span data-stu-id="5c2dc-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c2dc-115">標頭</span><span class="sxs-lookup"><span data-stu-id="5c2dc-115">Header</span></span><br/>  | <dl> <span data-ttu-id="5c2dc-116"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="5c2dc-116"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="5c2dc-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="5c2dc-117">Library</span></span><br/> | <dl> <span data-ttu-id="5c2dc-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="5c2dc-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c2dc-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c2dc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c2dc-120">**CMediaType 類別**</span><span class="sxs-lookup"><span data-stu-id="5c2dc-120">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




