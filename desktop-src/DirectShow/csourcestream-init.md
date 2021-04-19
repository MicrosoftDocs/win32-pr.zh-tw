---
description: Init 方法會初始化串流執行緒。
ms.assetid: c746e595-de97-478c-8b22-5c4dd5594a8f
title: 'CSourceStream.Init 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Init
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a3abf2b4637385616862c0613f72afd676f5b79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998894"
---
# <a name="csourcestreaminit-method"></a><span data-ttu-id="13705-103">CSourceStream.Init 方法</span><span class="sxs-lookup"><span data-stu-id="13705-103">CSourceStream.Init method</span></span>

<span data-ttu-id="13705-104">`Init`方法會初始化串流執行緒。</span><span class="sxs-lookup"><span data-stu-id="13705-104">The `Init` method initializes the streaming thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="13705-105">語法</span><span class="sxs-lookup"><span data-stu-id="13705-105">Syntax</span></span>


```C++
HRESULT Init();
```



## <a name="parameters"></a><span data-ttu-id="13705-106">參數</span><span class="sxs-lookup"><span data-stu-id="13705-106">Parameters</span></span>

<span data-ttu-id="13705-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="13705-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="13705-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="13705-108">Return value</span></span>

<span data-ttu-id="13705-109">傳回 S \_ OK，或另一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="13705-109">Returns S\_OK, or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="13705-110">備註</span><span class="sxs-lookup"><span data-stu-id="13705-110">Remarks</span></span>

<span data-ttu-id="13705-111">這個方法必須是傳送至 [**CSourceStream：： ThreadProc**](csourcestream-threadproc.md) 方法的第一個執行緒要求。</span><span class="sxs-lookup"><span data-stu-id="13705-111">This method must be the first thread request sent to the [**CSourceStream::ThreadProc**](csourcestream-threadproc.md) method.</span></span> <span data-ttu-id="13705-112">[**CSourceStream：： Active**](csourcestream-active.md)方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="13705-112">The [**CSourceStream::Active**](csourcestream-active.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="13705-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="13705-113">Requirements</span></span>



| <span data-ttu-id="13705-114">需求</span><span class="sxs-lookup"><span data-stu-id="13705-114">Requirement</span></span> | <span data-ttu-id="13705-115">值</span><span class="sxs-lookup"><span data-stu-id="13705-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13705-116">標頭</span><span class="sxs-lookup"><span data-stu-id="13705-116">Header</span></span><br/>  | <dl> <span data-ttu-id="13705-117"><dt>來源 .h (包含) 的資料流程 </dt></span><span class="sxs-lookup"><span data-stu-id="13705-117"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="13705-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="13705-118">Library</span></span><br/> | <dl> <span data-ttu-id="13705-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="13705-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13705-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13705-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13705-121">**CSourceStream 類別**</span><span class="sxs-lookup"><span data-stu-id="13705-121">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




