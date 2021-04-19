---
description: GetResult 方法會抓取產生的引數清單（如果有的話）。
ms.assetid: a2a8b17c-3dcf-4f59-89c3-f42070d2a8eb
title: 'CDeferredCommand. GetResult 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetResult
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e8c1638dc33be6457dd682f37e2ddd49e73a111a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999401"
---
# <a name="cdeferredcommandgetresult-method"></a><span data-ttu-id="e194e-103">CDeferredCommand. GetResult 方法</span><span class="sxs-lookup"><span data-stu-id="e194e-103">CDeferredCommand.GetResult method</span></span>

<span data-ttu-id="e194e-104">方法會抓取 `GetResult` 產生的引數清單（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="e194e-104">The `GetResult` method retrieves the resulting argument list, if one exists.</span></span>

## <a name="syntax"></a><span data-ttu-id="e194e-105">語法</span><span class="sxs-lookup"><span data-stu-id="e194e-105">Syntax</span></span>


```C++
VARIANT* GetResult();
```



## <a name="parameters"></a><span data-ttu-id="e194e-106">參數</span><span class="sxs-lookup"><span data-stu-id="e194e-106">Parameters</span></span>

<span data-ttu-id="e194e-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e194e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e194e-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="e194e-108">Return value</span></span>

<span data-ttu-id="e194e-109">傳回 **變數** 的指標，其中包含方法的引數清單（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="e194e-109">Returns a pointer to a **VARIANT** containing the method's argument list, if it exists.</span></span>

## <a name="requirements"></a><span data-ttu-id="e194e-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="e194e-110">Requirements</span></span>



| <span data-ttu-id="e194e-111">需求</span><span class="sxs-lookup"><span data-stu-id="e194e-111">Requirement</span></span> | <span data-ttu-id="e194e-112">值</span><span class="sxs-lookup"><span data-stu-id="e194e-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e194e-113">標頭</span><span class="sxs-lookup"><span data-stu-id="e194e-113">Header</span></span><br/>  | <dl> <span data-ttu-id="e194e-114"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e194e-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e194e-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="e194e-115">Library</span></span><br/> | <dl> <span data-ttu-id="e194e-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e194e-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e194e-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e194e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e194e-118">**CDeferredCommand 類別**</span><span class="sxs-lookup"><span data-stu-id="e194e-118">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




