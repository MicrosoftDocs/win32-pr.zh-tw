---
description: SetAbortSignal 方法會設定旗標，指出是否要停止轉譯和拒絕進一步的範例。
ms.assetid: 2dbf3b4d-e285-4d17-a77c-01a16c09d148
title: 'CBaseRenderer. SetAbortSignal 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetAbortSignal
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70527d5e43ccab4df7b2110a33df8d813bd16d28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977574"
---
# <a name="cbaserenderersetabortsignal-method"></a><span data-ttu-id="d6ee3-103">CBaseRenderer. SetAbortSignal 方法</span><span class="sxs-lookup"><span data-stu-id="d6ee3-103">CBaseRenderer.SetAbortSignal method</span></span>

<span data-ttu-id="d6ee3-104">`SetAbortSignal`方法會設定旗標，指出是否要停止轉譯和拒絕進一步的範例。</span><span class="sxs-lookup"><span data-stu-id="d6ee3-104">The `SetAbortSignal` method sets a flag which indicates whether to stop rendering and reject further samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6ee3-105">語法</span><span class="sxs-lookup"><span data-stu-id="d6ee3-105">Syntax</span></span>


```C++
void SetAbortSignal(
   BOOL bAbort
);
```



## <a name="parameters"></a><span data-ttu-id="d6ee3-106">參數</span><span class="sxs-lookup"><span data-stu-id="d6ee3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6ee3-107">*bAbort*</span><span class="sxs-lookup"><span data-stu-id="d6ee3-107">*bAbort*</span></span> 
</dt> <dd>

<span data-ttu-id="d6ee3-108">指出是否要停止轉譯的布林值。</span><span class="sxs-lookup"><span data-stu-id="d6ee3-108">Boolean value indicating whether to stop rendering.</span></span> <span data-ttu-id="d6ee3-109">若 **為 TRUE**，則篩選不會再轉譯任何範例。</span><span class="sxs-lookup"><span data-stu-id="d6ee3-109">If **TRUE**, the filter will not render any more samples.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6ee3-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6ee3-110">Return value</span></span>

<span data-ttu-id="d6ee3-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d6ee3-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6ee3-112">備註</span><span class="sxs-lookup"><span data-stu-id="d6ee3-112">Remarks</span></span>

<span data-ttu-id="d6ee3-113">這個方法會設定 [**CBaseRenderer：： m \_ bAbort**](cbaserenderer-m-babort.md) 旗標。</span><span class="sxs-lookup"><span data-stu-id="d6ee3-113">This method sets the [**CBaseRenderer::m\_bAbort**](cbaserenderer-m-babort.md) flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6ee3-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6ee3-114">Requirements</span></span>



| <span data-ttu-id="d6ee3-115">需求</span><span class="sxs-lookup"><span data-stu-id="d6ee3-115">Requirement</span></span> | <span data-ttu-id="d6ee3-116">值</span><span class="sxs-lookup"><span data-stu-id="d6ee3-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6ee3-117">標頭</span><span class="sxs-lookup"><span data-stu-id="d6ee3-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d6ee3-118"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d6ee3-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d6ee3-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="d6ee3-119">Library</span></span><br/> | <dl> <span data-ttu-id="d6ee3-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d6ee3-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6ee3-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6ee3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6ee3-122">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="d6ee3-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




