---
description: SetSampleSize 方法會指定固定樣本大小，或指定樣本具有變數大小。
ms.assetid: b0f9dd7b-4ff9-4d11-9c13-b52d7b1549b5
title: 'CMediaType. SetSampleSize 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSampleSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0992afd0576c1039397e6ecaa2119a989283136e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001896"
---
# <a name="cmediatypesetsamplesize-method"></a><span data-ttu-id="458ac-103">CMediaType. SetSampleSize 方法</span><span class="sxs-lookup"><span data-stu-id="458ac-103">CMediaType.SetSampleSize method</span></span>

<span data-ttu-id="458ac-104">`SetSampleSize`方法會指定固定樣本大小，或指定樣本具有變數大小。</span><span class="sxs-lookup"><span data-stu-id="458ac-104">The `SetSampleSize` method specifies a fixed sample size, or specifies that samples have a variable size.</span></span>

## <a name="syntax"></a><span data-ttu-id="458ac-105">語法</span><span class="sxs-lookup"><span data-stu-id="458ac-105">Syntax</span></span>


```C++
void SetSampleSize(
   ULONG sz
);
```



## <a name="parameters"></a><span data-ttu-id="458ac-106">參數</span><span class="sxs-lookup"><span data-stu-id="458ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="458ac-107">*深圳*</span><span class="sxs-lookup"><span data-stu-id="458ac-107">*sz*</span></span> 
</dt> <dd>

<span data-ttu-id="458ac-108">樣本大小（以位元組為單位）或零。</span><span class="sxs-lookup"><span data-stu-id="458ac-108">Sample size, in bytes, or zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="458ac-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="458ac-109">Return value</span></span>

<span data-ttu-id="458ac-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="458ac-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="458ac-111">備註</span><span class="sxs-lookup"><span data-stu-id="458ac-111">Remarks</span></span>

<span data-ttu-id="458ac-112">如果 *sz* 的值為零，則媒體類型會使用變數樣本大小。</span><span class="sxs-lookup"><span data-stu-id="458ac-112">If value of *sz* is zero, the media type uses variable sample sizes.</span></span> <span data-ttu-id="458ac-113">否則，範例大小會固定為 *sz* 個位元組。</span><span class="sxs-lookup"><span data-stu-id="458ac-113">Otherwise, the sample size is fixed at *sz* bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="458ac-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="458ac-114">Requirements</span></span>



| <span data-ttu-id="458ac-115">需求</span><span class="sxs-lookup"><span data-stu-id="458ac-115">Requirement</span></span> | <span data-ttu-id="458ac-116">值</span><span class="sxs-lookup"><span data-stu-id="458ac-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="458ac-117">標頭</span><span class="sxs-lookup"><span data-stu-id="458ac-117">Header</span></span><br/>  | <dl> <span data-ttu-id="458ac-118"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="458ac-118"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="458ac-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="458ac-119">Library</span></span><br/> | <dl> <span data-ttu-id="458ac-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="458ac-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="458ac-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="458ac-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="458ac-122">**CMediaType 類別**</span><span class="sxs-lookup"><span data-stu-id="458ac-122">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




