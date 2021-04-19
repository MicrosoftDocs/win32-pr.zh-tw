---
description: IsActive 方法會判斷物件是否為作用中， (執行中或已暫停) 。
ms.assetid: 6531cf1f-e057-4094-9354-d5a32371c83c
title: 'CBaseMediaFilter. IsActive 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.IsActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6438850b90309b47fbe1fb76b1fd4f7baea8f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992818"
---
# <a name="cbasemediafilterisactive-method"></a><span data-ttu-id="a7cc9-103">CBaseMediaFilter. IsActive 方法</span><span class="sxs-lookup"><span data-stu-id="a7cc9-103">CBaseMediaFilter.IsActive method</span></span>

<span data-ttu-id="a7cc9-104">`IsActive`方法會判斷物件是否為作用中， (執行中或已暫停) 。</span><span class="sxs-lookup"><span data-stu-id="a7cc9-104">The `IsActive` method determines whether the object is active (running or paused).</span></span>

## <a name="syntax"></a><span data-ttu-id="a7cc9-105">語法</span><span class="sxs-lookup"><span data-stu-id="a7cc9-105">Syntax</span></span>


```C++
BOOL IsActive();
```



## <a name="parameters"></a><span data-ttu-id="a7cc9-106">參數</span><span class="sxs-lookup"><span data-stu-id="a7cc9-106">Parameters</span></span>

<span data-ttu-id="a7cc9-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="a7cc9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a7cc9-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="a7cc9-108">Return value</span></span>

<span data-ttu-id="a7cc9-109">如果物件已暫停或正在執行，則傳回 **TRUE** ; 如果已停止，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="a7cc9-109">Returns **TRUE** if the object is paused or running, or **FALSE** if it is stopped.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7cc9-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7cc9-110">Requirements</span></span>



| <span data-ttu-id="a7cc9-111">需求</span><span class="sxs-lookup"><span data-stu-id="a7cc9-111">Requirement</span></span> | <span data-ttu-id="a7cc9-112">值</span><span class="sxs-lookup"><span data-stu-id="a7cc9-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7cc9-113">標頭</span><span class="sxs-lookup"><span data-stu-id="a7cc9-113">Header</span></span><br/>  | <dl> <span data-ttu-id="a7cc9-114"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a7cc9-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a7cc9-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="a7cc9-115">Library</span></span><br/> | <dl> <span data-ttu-id="a7cc9-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a7cc9-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7cc9-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7cc9-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7cc9-118">**CBaseMediaFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="a7cc9-118">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




