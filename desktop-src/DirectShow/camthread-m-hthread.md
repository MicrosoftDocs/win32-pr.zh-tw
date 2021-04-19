---
description: 執行緒的控制碼。
ms.assetid: 93d1182a-58f0-4570-8568-fe0fded762cb
title: 'CAMThread：： m_hThread 成員 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hThread
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e83dd225da0c3673f9c7f423e0bf56da7431b097
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984462"
---
# <a name="camthreadm_hthread-member"></a><span data-ttu-id="3840d-103">CAMThread：： m \_ hThread 成員</span><span class="sxs-lookup"><span data-stu-id="3840d-103">CAMThread::m\_hThread member</span></span>

<span data-ttu-id="3840d-104">執行緒的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3840d-104">Handle to the thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="3840d-105">語法</span><span class="sxs-lookup"><span data-stu-id="3840d-105">Syntax</span></span>


```C++
HANDLE m_hThread;
```



## <a name="remarks"></a><span data-ttu-id="3840d-106">備註</span><span class="sxs-lookup"><span data-stu-id="3840d-106">Remarks</span></span>

<span data-ttu-id="3840d-107">這個變數會初始化為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="3840d-107">This variable is initialized as **NULL**.</span></span> <span data-ttu-id="3840d-108">[**CAMThread：： Create**](camthread-create.md)方法會將這個變數設定為執行緒控制碼。</span><span class="sxs-lookup"><span data-stu-id="3840d-108">The [**CAMThread::Create**](camthread-create.md) method sets this variable to the thread handle.</span></span> <span data-ttu-id="3840d-109">若要判斷線程是否存在，請呼叫 [**CAMThread：： ThreadExists**](camthread-threadexists.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="3840d-109">To determine whether the thread exists, call the [**CAMThread::ThreadExists**](camthread-threadexists.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3840d-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="3840d-110">Requirements</span></span>



| <span data-ttu-id="3840d-111">需求</span><span class="sxs-lookup"><span data-stu-id="3840d-111">Requirement</span></span> | <span data-ttu-id="3840d-112">值</span><span class="sxs-lookup"><span data-stu-id="3840d-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3840d-113">標頭</span><span class="sxs-lookup"><span data-stu-id="3840d-113">Header</span></span><br/>  | <dl> <span data-ttu-id="3840d-114"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3840d-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3840d-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="3840d-115">Library</span></span><br/> | <dl> <span data-ttu-id="3840d-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3840d-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3840d-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3840d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3840d-118">**CAMThread 類別**</span><span class="sxs-lookup"><span data-stu-id="3840d-118">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




