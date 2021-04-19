---
description: CheckRequest 方法會檢查是否有線程要求，而不會封鎖。
ms.assetid: b4691dde-abec-4671-bea6-0f22cc4e7c61
title: 'CSourceStream. CheckRequest 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3100d449d2f29b2080541c5968cad6abc5643b26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982646"
---
# <a name="csourcestreamcheckrequest-method"></a><span data-ttu-id="af376-103">CSourceStream. CheckRequest 方法</span><span class="sxs-lookup"><span data-stu-id="af376-103">CSourceStream.CheckRequest method</span></span>

<span data-ttu-id="af376-104">`CheckRequest`方法會檢查是否有線程要求，而不會封鎖。</span><span class="sxs-lookup"><span data-stu-id="af376-104">The `CheckRequest` method checks if there is a thread request, without blocking.</span></span>

## <a name="syntax"></a><span data-ttu-id="af376-105">語法</span><span class="sxs-lookup"><span data-stu-id="af376-105">Syntax</span></span>


```C++
BOOL CheckRequest(
   Command *pCom
);
```



## <a name="parameters"></a><span data-ttu-id="af376-106">參數</span><span class="sxs-lookup"><span data-stu-id="af376-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af376-107">*pCom*</span><span class="sxs-lookup"><span data-stu-id="af376-107">*pCom*</span></span> 
</dt> <dd>

<span data-ttu-id="af376-108">變數的指標，此變數會接收最後呼叫 [**CAMThread：： CallWorker**](camthread-callworker.md) 方法時所傳遞的值。</span><span class="sxs-lookup"><span data-stu-id="af376-108">Pointer to a variable that receives the value passed in the last call to the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af376-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="af376-109">Return value</span></span>

<span data-ttu-id="af376-110">如果有暫止的要求，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="af376-110">Returns **TRUE** if there is a pending request, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="af376-111">備註</span><span class="sxs-lookup"><span data-stu-id="af376-111">Remarks</span></span>

<span data-ttu-id="af376-112">這個方法會覆寫 [**CAMThread：： CheckRequest**](camthread-checkrequest.md) 方法，以執行類型檢查。</span><span class="sxs-lookup"><span data-stu-id="af376-112">This method overrides the [**CAMThread::CheckRequest**](camthread-checkrequest.md) method to perform type-checking.</span></span> <span data-ttu-id="af376-113">**CSourceStream** 類別會定義 *pCom* 參數的下列列舉型別：</span><span class="sxs-lookup"><span data-stu-id="af376-113">The **CSourceStream** class defines the following enumerated type for the *pCom* parameter:</span></span>


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a><span data-ttu-id="af376-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="af376-114">Requirements</span></span>



| <span data-ttu-id="af376-115">需求</span><span class="sxs-lookup"><span data-stu-id="af376-115">Requirement</span></span> | <span data-ttu-id="af376-116">值</span><span class="sxs-lookup"><span data-stu-id="af376-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af376-117">標頭</span><span class="sxs-lookup"><span data-stu-id="af376-117">Header</span></span><br/>  | <dl> <span data-ttu-id="af376-118"><dt>來源 .h (包含) 的資料流程 </dt></span><span class="sxs-lookup"><span data-stu-id="af376-118"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="af376-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="af376-119">Library</span></span><br/> | <dl> <span data-ttu-id="af376-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="af376-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af376-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af376-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af376-122">**CSourceStream 類別**</span><span class="sxs-lookup"><span data-stu-id="af376-122">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




