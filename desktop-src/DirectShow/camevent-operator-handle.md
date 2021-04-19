---
description: 捕獲事件控制碼。 這個運算子不支援做為左值。
ms.assetid: 9000d6d1-bbca-44ac-8808-0b3b827086c5
title: 'CAMEvent 處理方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.operator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72193e89f415aabebfea4288fcdb986ccf8d73bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994035"
---
# <a name="cameventoperator-handle-method"></a><span data-ttu-id="bf343-104">CAMEvent 運算子控制碼方法</span><span class="sxs-lookup"><span data-stu-id="bf343-104">CAMEvent.operator HANDLE method</span></span>

<span data-ttu-id="bf343-105">捕獲事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="bf343-105">Retrieves the event handle.</span></span> <span data-ttu-id="bf343-106">這個運算子不支援做為左值。</span><span class="sxs-lookup"><span data-stu-id="bf343-106">This operator is not supported as an L-value.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf343-107">語法</span><span class="sxs-lookup"><span data-stu-id="bf343-107">Syntax</span></span>


```C++
 operator HANDLE() const;
```



## <a name="parameters"></a><span data-ttu-id="bf343-108">參數</span><span class="sxs-lookup"><span data-stu-id="bf343-108">Parameters</span></span>

<span data-ttu-id="bf343-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="bf343-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bf343-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="bf343-110">Return value</span></span>

<span data-ttu-id="bf343-111">傳回 [**CAMEvent：： m \_ hEvent**](camevent-m-hevent.md) 成員變數。</span><span class="sxs-lookup"><span data-stu-id="bf343-111">Returns the [**CAMEvent::m\_hEvent**](camevent-m-hevent.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf343-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf343-112">Requirements</span></span>



| <span data-ttu-id="bf343-113">需求</span><span class="sxs-lookup"><span data-stu-id="bf343-113">Requirement</span></span> | <span data-ttu-id="bf343-114">值</span><span class="sxs-lookup"><span data-stu-id="bf343-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf343-115">標頭</span><span class="sxs-lookup"><span data-stu-id="bf343-115">Header</span></span><br/>  | <dl> <span data-ttu-id="bf343-116"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="bf343-116"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="bf343-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="bf343-117">Library</span></span><br/> | <dl> <span data-ttu-id="bf343-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="bf343-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf343-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf343-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf343-120">**CAMEvent 類別**</span><span class="sxs-lookup"><span data-stu-id="bf343-120">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




