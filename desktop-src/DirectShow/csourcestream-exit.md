---
description: Exit 方法會通知串流執行緒結束。
ms.assetid: 1bb59848-e405-40f9-87ec-33de8754e2dd
title: CSourceStream， (Source. h) 的 Exit 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Exit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1ede6cf2318fa9226b8e220ff526f411def9b0f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994345"
---
# <a name="csourcestreamexit-method"></a><span data-ttu-id="c134a-103">CSourceStream. Exit 方法</span><span class="sxs-lookup"><span data-stu-id="c134a-103">CSourceStream.Exit method</span></span>

<span data-ttu-id="c134a-104">`Exit`方法會通知串流執行緒結束。</span><span class="sxs-lookup"><span data-stu-id="c134a-104">The `Exit` method signals the streaming thread to exit.</span></span>

## <a name="syntax"></a><span data-ttu-id="c134a-105">語法</span><span class="sxs-lookup"><span data-stu-id="c134a-105">Syntax</span></span>


```C++
HRESULT Exit();
```



## <a name="parameters"></a><span data-ttu-id="c134a-106">參數</span><span class="sxs-lookup"><span data-stu-id="c134a-106">Parameters</span></span>

<span data-ttu-id="c134a-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c134a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c134a-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="c134a-108">Return value</span></span>

<span data-ttu-id="c134a-109">傳回 \_ [OK] 或 [E 未 \_ 預期]。</span><span class="sxs-lookup"><span data-stu-id="c134a-109">Returns S\_OK or E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="c134a-110">備註</span><span class="sxs-lookup"><span data-stu-id="c134a-110">Remarks</span></span>

<span data-ttu-id="c134a-111">[**CSourceStream：：非**](csourcestream-inactive.md)使用中的方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="c134a-111">The [**CSourceStream::Inactive**](csourcestream-inactive.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c134a-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="c134a-112">Requirements</span></span>



| <span data-ttu-id="c134a-113">需求</span><span class="sxs-lookup"><span data-stu-id="c134a-113">Requirement</span></span> | <span data-ttu-id="c134a-114">值</span><span class="sxs-lookup"><span data-stu-id="c134a-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c134a-115">標頭</span><span class="sxs-lookup"><span data-stu-id="c134a-115">Header</span></span><br/>  | <dl> <span data-ttu-id="c134a-116"><dt>來源 .h (包含) 的資料流程 </dt></span><span class="sxs-lookup"><span data-stu-id="c134a-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c134a-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="c134a-117">Library</span></span><br/> | <dl> <span data-ttu-id="c134a-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c134a-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c134a-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c134a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c134a-120">**CSourceStream 類別**</span><span class="sxs-lookup"><span data-stu-id="c134a-120">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




