---
description: IsFixedSize 方法會判斷樣本的大小是否固定或變數大小。
ms.assetid: bd49f01a-21bb-48a2-aa9e-94ea0d2dbab3
title: 'CMediaType. IsFixedSize 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsFixedSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5016b38139165cb3714bc9ad2630dcc0483545cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106974908"
---
# <a name="cmediatypeisfixedsize-method"></a><span data-ttu-id="e808f-103">CMediaType. IsFixedSize 方法</span><span class="sxs-lookup"><span data-stu-id="e808f-103">CMediaType.IsFixedSize method</span></span>

<span data-ttu-id="e808f-104">`IsFixedSize`方法會判斷樣本的大小是否固定或變數大小。</span><span class="sxs-lookup"><span data-stu-id="e808f-104">The `IsFixedSize` method determines if the samples have a fixed size or a variable size.</span></span>

## <a name="syntax"></a><span data-ttu-id="e808f-105">語法</span><span class="sxs-lookup"><span data-stu-id="e808f-105">Syntax</span></span>


```C++
BOOL IsFixedSize() const;
```



## <a name="parameters"></a><span data-ttu-id="e808f-106">參數</span><span class="sxs-lookup"><span data-stu-id="e808f-106">Parameters</span></span>

<span data-ttu-id="e808f-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e808f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e808f-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="e808f-108">Return value</span></span>

<span data-ttu-id="e808f-109">傳回 **bFixedSizeSamples** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="e808f-109">Returns the value of the **bFixedSizeSamples** member.</span></span>

## <a name="requirements"></a><span data-ttu-id="e808f-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="e808f-110">Requirements</span></span>



| <span data-ttu-id="e808f-111">需求</span><span class="sxs-lookup"><span data-stu-id="e808f-111">Requirement</span></span> | <span data-ttu-id="e808f-112">值</span><span class="sxs-lookup"><span data-stu-id="e808f-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e808f-113">標頭</span><span class="sxs-lookup"><span data-stu-id="e808f-113">Header</span></span><br/>  | <dl> <span data-ttu-id="e808f-114"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e808f-114"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="e808f-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="e808f-115">Library</span></span><br/> | <dl> <span data-ttu-id="e808f-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e808f-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e808f-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e808f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e808f-118">**CMediaType 類別**</span><span class="sxs-lookup"><span data-stu-id="e808f-118">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




