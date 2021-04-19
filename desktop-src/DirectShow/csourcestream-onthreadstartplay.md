---
description: 在 CSourceStream：:D oBufferProcessingLoop 方法的開頭呼叫 OnThreadStartPlay 方法。
ms.assetid: 16d3b28f-bfae-49af-b8e4-8cc8cb15ecab
title: 'CSourceStream. OnThreadStartPlay 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadStartPlay
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 857f27ad39fb9169e1ef67253d5232c7cbc3dbb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999292"
---
# <a name="csourcestreamonthreadstartplay-method"></a><span data-ttu-id="b1486-103">CSourceStream. OnThreadStartPlay 方法</span><span class="sxs-lookup"><span data-stu-id="b1486-103">CSourceStream.OnThreadStartPlay method</span></span>

<span data-ttu-id="b1486-104">`OnThreadStartPlay`方法是在 [**CSourceStream：:D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md)方法的開頭呼叫。</span><span class="sxs-lookup"><span data-stu-id="b1486-104">The `OnThreadStartPlay` method is called at the start of the [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1486-105">語法</span><span class="sxs-lookup"><span data-stu-id="b1486-105">Syntax</span></span>


```C++
virtual HRESULT OnThreadStartPlay();
```



## <a name="parameters"></a><span data-ttu-id="b1486-106">參數</span><span class="sxs-lookup"><span data-stu-id="b1486-106">Parameters</span></span>

<span data-ttu-id="b1486-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="b1486-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b1486-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="b1486-108">Return value</span></span>

<span data-ttu-id="b1486-109">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="b1486-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1486-110">備註</span><span class="sxs-lookup"><span data-stu-id="b1486-110">Remarks</span></span>

<span data-ttu-id="b1486-111">這個方法不會在基類中執行任何動作;它可供衍生類別覆寫。</span><span class="sxs-lookup"><span data-stu-id="b1486-111">This method does nothing in the base class; it is available for the derived class to override.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1486-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1486-112">Requirements</span></span>



| <span data-ttu-id="b1486-113">需求</span><span class="sxs-lookup"><span data-stu-id="b1486-113">Requirement</span></span> | <span data-ttu-id="b1486-114">值</span><span class="sxs-lookup"><span data-stu-id="b1486-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1486-115">標頭</span><span class="sxs-lookup"><span data-stu-id="b1486-115">Header</span></span><br/>  | <dl> <span data-ttu-id="b1486-116"><dt>來源 .h (包含) 的資料流程 </dt></span><span class="sxs-lookup"><span data-stu-id="b1486-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b1486-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="b1486-117">Library</span></span><br/> | <dl> <span data-ttu-id="b1486-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b1486-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1486-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1486-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1486-120">**CSourceStream 類別**</span><span class="sxs-lookup"><span data-stu-id="b1486-120">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




