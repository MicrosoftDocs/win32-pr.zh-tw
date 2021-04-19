---
description: ResetStreamingTimes 方法會重設控制串流的所有時間。
ms.assetid: 8a596760-a45a-4486-bb91-aab10bbf927f
title: 'CBaseVideoRenderer. ResetStreamingTimes 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ResetStreamingTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d887ca9e246d5e3fb746c119b1ed6784201ec702
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990524"
---
# <a name="cbasevideorendererresetstreamingtimes-method"></a><span data-ttu-id="3de3b-103">CBaseVideoRenderer. ResetStreamingTimes 方法</span><span class="sxs-lookup"><span data-stu-id="3de3b-103">CBaseVideoRenderer.ResetStreamingTimes method</span></span>

<span data-ttu-id="3de3b-104">`ResetStreamingTimes`方法會重設控制串流的所有時間。</span><span class="sxs-lookup"><span data-stu-id="3de3b-104">The `ResetStreamingTimes` method resets all times that control the streaming.</span></span>

## <a name="syntax"></a><span data-ttu-id="3de3b-105">語法</span><span class="sxs-lookup"><span data-stu-id="3de3b-105">Syntax</span></span>


```C++
virtual HRESULT ResetStreamingTimes();
```



## <a name="parameters"></a><span data-ttu-id="3de3b-106">參數</span><span class="sxs-lookup"><span data-stu-id="3de3b-106">Parameters</span></span>

<span data-ttu-id="3de3b-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="3de3b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3de3b-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="3de3b-108">Return value</span></span>

<span data-ttu-id="3de3b-109">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="3de3b-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3de3b-110">備註</span><span class="sxs-lookup"><span data-stu-id="3de3b-110">Remarks</span></span>

<span data-ttu-id="3de3b-111">系統會設定時間，讓框架一開始不會被捨棄，因此會繪製第一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="3de3b-111">The times are set so that frames will not be initially dropped and so that the first frame will be drawn.</span></span>

## <a name="requirements"></a><span data-ttu-id="3de3b-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="3de3b-112">Requirements</span></span>



| <span data-ttu-id="3de3b-113">需求</span><span class="sxs-lookup"><span data-stu-id="3de3b-113">Requirement</span></span> | <span data-ttu-id="3de3b-114">值</span><span class="sxs-lookup"><span data-stu-id="3de3b-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3de3b-115">標頭</span><span class="sxs-lookup"><span data-stu-id="3de3b-115">Header</span></span><br/>  | <dl> <span data-ttu-id="3de3b-116"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3de3b-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3de3b-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="3de3b-117">Library</span></span><br/> | <dl> <span data-ttu-id="3de3b-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3de3b-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3de3b-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3de3b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3de3b-120">**CBaseVideoRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="3de3b-120">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




