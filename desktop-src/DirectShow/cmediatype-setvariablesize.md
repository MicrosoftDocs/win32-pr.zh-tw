---
description: SetVariableSize 方法指定範例沒有固定的大小。
ms.assetid: 2a207cdb-f8e6-44aa-8bf6-868267aeb42d
title: 'CMediaType. SetVariableSize 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetVariableSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4621a639b3bc18382bc41ae9425c4de50db920ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987962"
---
# <a name="cmediatypesetvariablesize-method"></a><span data-ttu-id="6ea7c-103">CMediaType. SetVariableSize 方法</span><span class="sxs-lookup"><span data-stu-id="6ea7c-103">CMediaType.SetVariableSize method</span></span>

<span data-ttu-id="6ea7c-104">`SetVariableSize`方法指定範例沒有固定的大小。</span><span class="sxs-lookup"><span data-stu-id="6ea7c-104">The `SetVariableSize` method specifies that samples do not have a fixed size.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ea7c-105">語法</span><span class="sxs-lookup"><span data-stu-id="6ea7c-105">Syntax</span></span>


```C++
void SetVariableSize();
```



## <a name="parameters"></a><span data-ttu-id="6ea7c-106">參數</span><span class="sxs-lookup"><span data-stu-id="6ea7c-106">Parameters</span></span>

<span data-ttu-id="6ea7c-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="6ea7c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6ea7c-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="6ea7c-108">Return value</span></span>

<span data-ttu-id="6ea7c-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6ea7c-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ea7c-110">備註</span><span class="sxs-lookup"><span data-stu-id="6ea7c-110">Remarks</span></span>

<span data-ttu-id="6ea7c-111">這個方法會將 **bFixedSizeSamples** 成員設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="6ea7c-111">This method sets the **bFixedSizeSamples** member to **FALSE**.</span></span> <span data-ttu-id="6ea7c-112">[**CMediaType：： GetSampleSize**](cmediatype-getsamplesize.md)方法的後續呼叫會傳回零。</span><span class="sxs-lookup"><span data-stu-id="6ea7c-112">Subsequent calls to the [**CMediaType::GetSampleSize**](cmediatype-getsamplesize.md) method return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ea7c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ea7c-113">Requirements</span></span>



| <span data-ttu-id="6ea7c-114">需求</span><span class="sxs-lookup"><span data-stu-id="6ea7c-114">Requirement</span></span> | <span data-ttu-id="6ea7c-115">值</span><span class="sxs-lookup"><span data-stu-id="6ea7c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ea7c-116">標頭</span><span class="sxs-lookup"><span data-stu-id="6ea7c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6ea7c-117"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6ea7c-117"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="6ea7c-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="6ea7c-118">Library</span></span><br/> | <dl> <span data-ttu-id="6ea7c-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6ea7c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ea7c-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ea7c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ea7c-121">**CMediaType 類別**</span><span class="sxs-lookup"><span data-stu-id="6ea7c-121">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




