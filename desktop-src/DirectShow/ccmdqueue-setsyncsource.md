---
description: SetSyncSource 方法會設定計時所使用的時鐘。
ms.assetid: 646d4d24-f9b7-438a-b842-58e90eb6a945
title: 'CCmdQueue. SetSyncSource 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 995df3afa5185d8f50278899ac6a5d67dc6d230e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992373"
---
# <a name="ccmdqueuesetsyncsource-method"></a><span data-ttu-id="06b8b-103">CCmdQueue. SetSyncSource 方法</span><span class="sxs-lookup"><span data-stu-id="06b8b-103">CCmdQueue.SetSyncSource method</span></span>

<span data-ttu-id="06b8b-104">`SetSyncSource`方法會設定計時所使用的時鐘。</span><span class="sxs-lookup"><span data-stu-id="06b8b-104">The `SetSyncSource` method sets the clock used for timing.</span></span>

## <a name="syntax"></a><span data-ttu-id="06b8b-105">語法</span><span class="sxs-lookup"><span data-stu-id="06b8b-105">Syntax</span></span>


```C++
virtual HRESULT SetSyncSource(
   IReferenceClock *pIrc
);
```



## <a name="parameters"></a><span data-ttu-id="06b8b-106">參數</span><span class="sxs-lookup"><span data-stu-id="06b8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06b8b-107">*pIrc*</span><span class="sxs-lookup"><span data-stu-id="06b8b-107">*pIrc*</span></span> 
</dt> <dd>

<span data-ttu-id="06b8b-108">[**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="06b8b-108">Pointer to the [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06b8b-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="06b8b-109">Return value</span></span>

<span data-ttu-id="06b8b-110">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="06b8b-110">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="06b8b-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="06b8b-111">Requirements</span></span>



| <span data-ttu-id="06b8b-112">需求</span><span class="sxs-lookup"><span data-stu-id="06b8b-112">Requirement</span></span> | <span data-ttu-id="06b8b-113">值</span><span class="sxs-lookup"><span data-stu-id="06b8b-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06b8b-114">標頭</span><span class="sxs-lookup"><span data-stu-id="06b8b-114">Header</span></span><br/>  | <dl> <span data-ttu-id="06b8b-115"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="06b8b-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="06b8b-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="06b8b-116">Library</span></span><br/> | <dl> <span data-ttu-id="06b8b-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="06b8b-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06b8b-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06b8b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06b8b-119">**CCmdQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="06b8b-119">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




