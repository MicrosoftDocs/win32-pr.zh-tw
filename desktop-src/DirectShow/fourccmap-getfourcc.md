---
description: '\#從 FOURCCMap 物件中抓取 FOURCC&160; DWORD。'
ms.assetid: bb382a57-8499-44c0-b287-2d31f5f5d1d0
title: 'FOURCCMap：： GetFOURCC 方法 (Fourcc .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.GetFOURCC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c76493ff172f7a5611367fd50aa3b7957cf5441b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995223"
---
# <a name="fourccmapgetfourcc-method"></a><span data-ttu-id="17d49-103">FOURCCMap：： GetFOURCC 方法</span><span class="sxs-lookup"><span data-stu-id="17d49-103">FOURCCMap::GetFOURCC method</span></span>

<span data-ttu-id="17d49-104">從 [**FOURCCMap**](fourccmap.md)物件中抓取 **FOURCC** 的 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="17d49-104">Retrieves the **FOURCC** **DWORD** from the [**FOURCCMap**](fourccmap.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="17d49-105">語法</span><span class="sxs-lookup"><span data-stu-id="17d49-105">Syntax</span></span>


```C++
DWORD GetFOURCC();
```



## <a name="parameters"></a><span data-ttu-id="17d49-106">參數</span><span class="sxs-lookup"><span data-stu-id="17d49-106">Parameters</span></span>

<span data-ttu-id="17d49-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="17d49-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="17d49-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="17d49-108">Return value</span></span>

<span data-ttu-id="17d49-109">傳回 **FOURCC** **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="17d49-109">Returns the **FOURCC** **DWORD** value.</span></span> <span data-ttu-id="17d49-110">請注意，如果您所建立的 **GUID** 原本並非衍生自 **FOURCC**，則傳回值基本上會是隨機的。</span><span class="sxs-lookup"><span data-stu-id="17d49-110">Note that if you construct a **GUID** that was not originally derived from a **FOURCC**, the return value will be essentially random.</span></span>

## <a name="requirements"></a><span data-ttu-id="17d49-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="17d49-111">Requirements</span></span>



| <span data-ttu-id="17d49-112">需求</span><span class="sxs-lookup"><span data-stu-id="17d49-112">Requirement</span></span> | <span data-ttu-id="17d49-113">值</span><span class="sxs-lookup"><span data-stu-id="17d49-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17d49-114">標頭</span><span class="sxs-lookup"><span data-stu-id="17d49-114">Header</span></span><br/>  | <dl> <span data-ttu-id="17d49-115"><dt>Fourcc (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="17d49-115"><dt>Fourcc.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="17d49-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="17d49-116">Library</span></span><br/> | <dl> <span data-ttu-id="17d49-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="17d49-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17d49-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17d49-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17d49-119">**FOURCCMap 類別**</span><span class="sxs-lookup"><span data-stu-id="17d49-119">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




