---
description: CEnumPins。 CEnumPins 函式-函數方法。
ms.assetid: f696e433-b051-4de0-80e5-f9cd31fd0f23
title: 'CEnumPins. CEnumPins (Amfilter. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.CEnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: caa27dfe0190df15be1e41b7128c06249f1ae2b8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099226"
---
# <a name="cenumpinscenumpins-constructor"></a><span data-ttu-id="983e5-103">CEnumPins. CEnumPins 函數</span><span class="sxs-lookup"><span data-stu-id="983e5-103">CEnumPins.CEnumPins constructor</span></span>

<span data-ttu-id="983e5-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="983e5-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="983e5-105">語法</span><span class="sxs-lookup"><span data-stu-id="983e5-105">Syntax</span></span>


```C++
CEnumPins(
   CBaseFilter *pFilter,
   CEnumPins   *pEnumPins
);
```



## <a name="parameters"></a><span data-ttu-id="983e5-106">參數</span><span class="sxs-lookup"><span data-stu-id="983e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="983e5-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="983e5-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="983e5-108">要列舉釘選之篩選準則的指標。</span><span class="sxs-lookup"><span data-stu-id="983e5-108">Pointer to the filter on which to enumerate the pins.</span></span>

</dd> <dt>

<span data-ttu-id="983e5-109">*pEnumPins*</span><span class="sxs-lookup"><span data-stu-id="983e5-109">*pEnumPins*</span></span> 
</dt> <dd>

<span data-ttu-id="983e5-110">要複製之列舉值的 [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) 介面指標，或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="983e5-110">Pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface of an enumerator to clone, or **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="983e5-111">備註</span><span class="sxs-lookup"><span data-stu-id="983e5-111">Remarks</span></span>

<span data-ttu-id="983e5-112">如果 *pEnumPins* 是 **Null**，這個方法會將列舉值初始化為列舉序列的開頭。</span><span class="sxs-lookup"><span data-stu-id="983e5-112">If *pEnumPins* is **NULL**, this method initializes the enumerator to the beginning of the enumeration sequence.</span></span> <span data-ttu-id="983e5-113">否則，它會複製 *pEnumPins* 所指定之列舉值的內部狀態。</span><span class="sxs-lookup"><span data-stu-id="983e5-113">Otherwise, it duplicates the internal state of the enumerator specified by *pEnumPins*.</span></span>

## <a name="requirements"></a><span data-ttu-id="983e5-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="983e5-114">Requirements</span></span>



| <span data-ttu-id="983e5-115">需求</span><span class="sxs-lookup"><span data-stu-id="983e5-115">Requirement</span></span> | <span data-ttu-id="983e5-116">值</span><span class="sxs-lookup"><span data-stu-id="983e5-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="983e5-117">標頭</span><span class="sxs-lookup"><span data-stu-id="983e5-117">Header</span></span><br/>  | <dl> <span data-ttu-id="983e5-118"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="983e5-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="983e5-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="983e5-119">Library</span></span><br/> | <dl> <span data-ttu-id="983e5-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="983e5-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="983e5-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="983e5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="983e5-122">**CEnumPins 類別**</span><span class="sxs-lookup"><span data-stu-id="983e5-122">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 




