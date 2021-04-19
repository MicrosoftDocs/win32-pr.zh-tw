---
description: DumpGraph 函式會將篩選圖形的相關資訊傳送至偵錯工具的輸出位置。 在零售組建中略過。
ms.assetid: c78f86bb-44d0-4904-b7f8-e756bda0151d
title: 'DumpGraph 函式 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DumpGraph
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55c3adf793982b7b00ab44e26e7c34e08a1ac42b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994344"
---
# <a name="dumpgraph-function"></a><span data-ttu-id="e2aca-104">DumpGraph 函式</span><span class="sxs-lookup"><span data-stu-id="e2aca-104">DumpGraph function</span></span>

<span data-ttu-id="e2aca-105">`DumpGraph`函數會將篩選圖形的相關資訊傳送至偵錯工具輸出位置。</span><span class="sxs-lookup"><span data-stu-id="e2aca-105">The `DumpGraph` function sends information about a filter graph to the debug output location.</span></span> <span data-ttu-id="e2aca-106">在零售組建中略過。</span><span class="sxs-lookup"><span data-stu-id="e2aca-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2aca-107">語法</span><span class="sxs-lookup"><span data-stu-id="e2aca-107">Syntax</span></span>


```C++
void DumpGraph(
   IFilterGraph *pGraph,
   DWORD        dwLevel
);
```



## <a name="parameters"></a><span data-ttu-id="e2aca-108">參數</span><span class="sxs-lookup"><span data-stu-id="e2aca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2aca-109">*pGraph*</span><span class="sxs-lookup"><span data-stu-id="e2aca-109">*pGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="e2aca-110">篩選圖形管理員上 [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="e2aca-110">Pointer to the [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) interface on the filter graph manager.</span></span>

</dd> <dt>

<span data-ttu-id="e2aca-111">*dwLevel*</span><span class="sxs-lookup"><span data-stu-id="e2aca-111">*dwLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="e2aca-112">記錄層級。</span><span class="sxs-lookup"><span data-stu-id="e2aca-112">Logging level.</span></span> <span data-ttu-id="e2aca-113">函數會產生 \_ 具有指定記錄層級的記錄追蹤訊息。</span><span class="sxs-lookup"><span data-stu-id="e2aca-113">The function generates a LOG\_TRACE message with the specified logging level.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2aca-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="e2aca-114">Return value</span></span>

<span data-ttu-id="e2aca-115">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e2aca-115">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2aca-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2aca-116">Requirements</span></span>



| <span data-ttu-id="e2aca-117">需求</span><span class="sxs-lookup"><span data-stu-id="e2aca-117">Requirement</span></span> | <span data-ttu-id="e2aca-118">值</span><span class="sxs-lookup"><span data-stu-id="e2aca-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2aca-119">標頭</span><span class="sxs-lookup"><span data-stu-id="e2aca-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e2aca-120"><dt>Wxdebug (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e2aca-120"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e2aca-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="e2aca-121">Library</span></span><br/> | <dl> <span data-ttu-id="e2aca-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e2aca-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2aca-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2aca-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2aca-124">Debug Output 函數</span><span class="sxs-lookup"><span data-stu-id="e2aca-124">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




