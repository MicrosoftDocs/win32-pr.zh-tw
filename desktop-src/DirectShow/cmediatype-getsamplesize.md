---
description: GetSampleSize 方法會抓取樣本大小。
ms.assetid: 5cc98556-cca6-46ca-ad33-cd40011ff6f4
title: 'CMediaType. GetSampleSize 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.GetSampleSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc5b80e20ad2a16af9c25c68499348ffa744c0fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001525"
---
# <a name="cmediatypegetsamplesize-method"></a><span data-ttu-id="cec44-103">CMediaType. GetSampleSize 方法</span><span class="sxs-lookup"><span data-stu-id="cec44-103">CMediaType.GetSampleSize method</span></span>

<span data-ttu-id="cec44-104">方法會抓取 `GetSampleSize` 範例大小。</span><span class="sxs-lookup"><span data-stu-id="cec44-104">The `GetSampleSize` method retrieves the sample size.</span></span>

## <a name="syntax"></a><span data-ttu-id="cec44-105">語法</span><span class="sxs-lookup"><span data-stu-id="cec44-105">Syntax</span></span>


```C++
ULONG GetSampleSize() const;
```



## <a name="parameters"></a><span data-ttu-id="cec44-106">參數</span><span class="sxs-lookup"><span data-stu-id="cec44-106">Parameters</span></span>

<span data-ttu-id="cec44-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="cec44-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cec44-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="cec44-108">Return value</span></span>

<span data-ttu-id="cec44-109">如果範例大小是固定的，則傳回範例大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="cec44-109">If the sample size is fixed, returns the sample size in bytes.</span></span> <span data-ttu-id="cec44-110">否則，會傳回零。</span><span class="sxs-lookup"><span data-stu-id="cec44-110">Otherwise, returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="cec44-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="cec44-111">Requirements</span></span>



| <span data-ttu-id="cec44-112">需求</span><span class="sxs-lookup"><span data-stu-id="cec44-112">Requirement</span></span> | <span data-ttu-id="cec44-113">值</span><span class="sxs-lookup"><span data-stu-id="cec44-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cec44-114">標頭</span><span class="sxs-lookup"><span data-stu-id="cec44-114">Header</span></span><br/>  | <dl> <span data-ttu-id="cec44-115"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="cec44-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="cec44-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="cec44-116">Library</span></span><br/> | <dl> <span data-ttu-id="cec44-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="cec44-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cec44-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cec44-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cec44-119">**CMediaType 類別**</span><span class="sxs-lookup"><span data-stu-id="cec44-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




