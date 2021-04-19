---
description: GetRequest 方法會等候下一個執行緒要求。
ms.assetid: 2938374b-174f-4276-98a2-20a084bd9bbd
title: 'CSourceStream. GetRequest 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.GetRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f45e6f6cf269f7aca6741d8e1c150c7054b07f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981307"
---
# <a name="csourcestreamgetrequest-method"></a><span data-ttu-id="c7f6e-103">CSourceStream. GetRequest 方法</span><span class="sxs-lookup"><span data-stu-id="c7f6e-103">CSourceStream.GetRequest method</span></span>

<span data-ttu-id="c7f6e-104">`GetRequest`方法會等候下一個執行緒要求。</span><span class="sxs-lookup"><span data-stu-id="c7f6e-104">The `GetRequest` method waits for the next thread request.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7f6e-105">語法</span><span class="sxs-lookup"><span data-stu-id="c7f6e-105">Syntax</span></span>


```C++
Command GetRequest();
```



## <a name="parameters"></a><span data-ttu-id="c7f6e-106">參數</span><span class="sxs-lookup"><span data-stu-id="c7f6e-106">Parameters</span></span>

<span data-ttu-id="c7f6e-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c7f6e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c7f6e-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="c7f6e-108">Return value</span></span>

<span data-ttu-id="c7f6e-109">傳回下一個執行緒要求。</span><span class="sxs-lookup"><span data-stu-id="c7f6e-109">Returns the next thread request.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7f6e-110">備註</span><span class="sxs-lookup"><span data-stu-id="c7f6e-110">Remarks</span></span>

<span data-ttu-id="c7f6e-111">這個方法會覆寫 [**CAMThread：： GetRequest**](camthread-getrequest.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="c7f6e-111">This method overrides the [**CAMThread::GetRequest**](camthread-getrequest.md) method.</span></span> <span data-ttu-id="c7f6e-112">傳回值會轉換成下列列舉型別：</span><span class="sxs-lookup"><span data-stu-id="c7f6e-112">The return value is cast to the following enumerated type:</span></span>


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a><span data-ttu-id="c7f6e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7f6e-113">Requirements</span></span>



| <span data-ttu-id="c7f6e-114">需求</span><span class="sxs-lookup"><span data-stu-id="c7f6e-114">Requirement</span></span> | <span data-ttu-id="c7f6e-115">值</span><span class="sxs-lookup"><span data-stu-id="c7f6e-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7f6e-116">標頭</span><span class="sxs-lookup"><span data-stu-id="c7f6e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c7f6e-117"><dt>來源 .h (包含) 的資料流程 </dt></span><span class="sxs-lookup"><span data-stu-id="c7f6e-117"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c7f6e-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="c7f6e-118">Library</span></span><br/> | <dl> <span data-ttu-id="c7f6e-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c7f6e-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7f6e-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7f6e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7f6e-121">**CSourceStream 類別**</span><span class="sxs-lookup"><span data-stu-id="c7f6e-121">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




