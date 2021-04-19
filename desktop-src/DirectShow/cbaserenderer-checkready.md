---
description: CheckReady 方法會查詢狀態轉換是否已完成。
ms.assetid: dfa669ed-a5ab-498e-9fc2-ff15d6ddbc13
title: 'CBaseRenderer. CheckReady 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CheckReady
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 28c0c8bcb6efb0e3cbd648c1e45d36e8b18d4b74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994130"
---
# <a name="cbaserenderercheckready-method"></a><span data-ttu-id="d7c1e-103">CBaseRenderer. CheckReady 方法</span><span class="sxs-lookup"><span data-stu-id="d7c1e-103">CBaseRenderer.CheckReady method</span></span>

<span data-ttu-id="d7c1e-104">`CheckReady`方法會查詢狀態轉換是否已完成。</span><span class="sxs-lookup"><span data-stu-id="d7c1e-104">The `CheckReady` method queries whether a state transition is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7c1e-105">語法</span><span class="sxs-lookup"><span data-stu-id="d7c1e-105">Syntax</span></span>


```C++
BOOL CheckReady();
```



## <a name="parameters"></a><span data-ttu-id="d7c1e-106">參數</span><span class="sxs-lookup"><span data-stu-id="d7c1e-106">Parameters</span></span>

<span data-ttu-id="d7c1e-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d7c1e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d7c1e-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="d7c1e-108">Return value</span></span>

<span data-ttu-id="d7c1e-109">如果狀態轉換完成，則傳回 **TRUE** ; 如果篩選仍在轉換成新狀態，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="d7c1e-109">Returns **TRUE** if the state transition is complete, or **FALSE** if the filter is still transitioning to a new state.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7c1e-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7c1e-110">Requirements</span></span>



| <span data-ttu-id="d7c1e-111">需求</span><span class="sxs-lookup"><span data-stu-id="d7c1e-111">Requirement</span></span> | <span data-ttu-id="d7c1e-112">值</span><span class="sxs-lookup"><span data-stu-id="d7c1e-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7c1e-113">標頭</span><span class="sxs-lookup"><span data-stu-id="d7c1e-113">Header</span></span><br/>  | <dl> <span data-ttu-id="d7c1e-114"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d7c1e-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d7c1e-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="d7c1e-115">Library</span></span><br/> | <dl> <span data-ttu-id="d7c1e-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d7c1e-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7c1e-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7c1e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7c1e-118">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="d7c1e-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="d7c1e-119">**CBaseRenderer：： NotReady**</span><span class="sxs-lookup"><span data-stu-id="d7c1e-119">**CBaseRenderer::NotReady**</span></span>](cbaserenderer-notready.md)
</dt> <dt>

[<span data-ttu-id="d7c1e-120">**CBaseRenderer：： Ready**</span><span class="sxs-lookup"><span data-stu-id="d7c1e-120">**CBaseRenderer::Ready**</span></span>](cbaserenderer-ready.md)
</dt> </dl>

 

 




