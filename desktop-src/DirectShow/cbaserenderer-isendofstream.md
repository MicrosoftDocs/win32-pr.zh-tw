---
description: IsEndOfStream 方法會查詢是否已收到資料流程結尾通知。
ms.assetid: 44f9b740-ff7d-4387-9c2c-a5b6b90f3295
title: 'CBaseRenderer. IsEndOfStream 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.IsEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e07afb4dfb10e38d90184ba5747f200d1bc716d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984023"
---
# <a name="cbaserendererisendofstream-method"></a><span data-ttu-id="b9eda-103">CBaseRenderer. IsEndOfStream 方法</span><span class="sxs-lookup"><span data-stu-id="b9eda-103">CBaseRenderer.IsEndOfStream method</span></span>

<span data-ttu-id="b9eda-104">`IsEndOfStream`方法會查詢是否已收到資料流程結尾通知。</span><span class="sxs-lookup"><span data-stu-id="b9eda-104">The `IsEndOfStream` method queries whether the end-of-stream notification was received.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9eda-105">語法</span><span class="sxs-lookup"><span data-stu-id="b9eda-105">Syntax</span></span>


```C++
BOOL IsEndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="b9eda-106">參數</span><span class="sxs-lookup"><span data-stu-id="b9eda-106">Parameters</span></span>

<span data-ttu-id="b9eda-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="b9eda-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b9eda-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="b9eda-108">Return value</span></span>

<span data-ttu-id="b9eda-109">傳回 [**CBaseRenderer：： m \_ bEOS**](cbaserenderer-m-beos.md) 旗標。</span><span class="sxs-lookup"><span data-stu-id="b9eda-109">Returns the [**CBaseRenderer::m\_bEOS**](cbaserenderer-m-beos.md) flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9eda-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9eda-110">Requirements</span></span>



| <span data-ttu-id="b9eda-111">需求</span><span class="sxs-lookup"><span data-stu-id="b9eda-111">Requirement</span></span> | <span data-ttu-id="b9eda-112">值</span><span class="sxs-lookup"><span data-stu-id="b9eda-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9eda-113">標頭</span><span class="sxs-lookup"><span data-stu-id="b9eda-113">Header</span></span><br/>  | <dl> <span data-ttu-id="b9eda-114"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b9eda-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b9eda-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="b9eda-115">Library</span></span><br/> | <dl> <span data-ttu-id="b9eda-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b9eda-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9eda-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9eda-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9eda-118">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="b9eda-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




