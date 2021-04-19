---
description: 封鎖狀態。
ms.assetid: 55afd314-efd3-47bf-80e3-e17c1332a4cf
title: 'CDynamicOutputPin：： m_BlockState 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_BlockState
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f02a59854b381db5e7b13a85ccca0754cc38f51d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980230"
---
# <a name="cdynamicoutputpinm_blockstate-member"></a><span data-ttu-id="a691a-103">CDynamicOutputPin：： m \_ BlockState 成員</span><span class="sxs-lookup"><span data-stu-id="a691a-103">CDynamicOutputPin::m\_BlockState member</span></span>

<span data-ttu-id="a691a-104">封鎖狀態。</span><span class="sxs-lookup"><span data-stu-id="a691a-104">Blocking state.</span></span>

## <a name="syntax"></a><span data-ttu-id="a691a-105">語法</span><span class="sxs-lookup"><span data-stu-id="a691a-105">Syntax</span></span>


```C++
BLOCK_STATE m_BlockState;
```



## <a name="remarks"></a><span data-ttu-id="a691a-106">備註</span><span class="sxs-lookup"><span data-stu-id="a691a-106">Remarks</span></span>

<span data-ttu-id="a691a-107">下列為定義的狀態：</span><span class="sxs-lookup"><span data-stu-id="a691a-107">The following states are defined:</span></span>

-   <span data-ttu-id="a691a-108">未 \_ 封鎖</span><span class="sxs-lookup"><span data-stu-id="a691a-108">NOT\_BLOCKED</span></span>
-   <span data-ttu-id="a691a-109">PENDING</span><span class="sxs-lookup"><span data-stu-id="a691a-109">PENDING</span></span>
-   <span data-ttu-id="a691a-110">封鎖</span><span class="sxs-lookup"><span data-stu-id="a691a-110">BLOCKED</span></span>

<span data-ttu-id="a691a-111">存取此變數之前，請先保留 [**CDynamicOutputPin：： m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) 重要區段。</span><span class="sxs-lookup"><span data-stu-id="a691a-111">Before accessing this variable, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="a691a-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="a691a-112">Requirements</span></span>



| <span data-ttu-id="a691a-113">需求</span><span class="sxs-lookup"><span data-stu-id="a691a-113">Requirement</span></span> | <span data-ttu-id="a691a-114">值</span><span class="sxs-lookup"><span data-stu-id="a691a-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a691a-115">標頭</span><span class="sxs-lookup"><span data-stu-id="a691a-115">Header</span></span><br/>  | <dl> <span data-ttu-id="a691a-116"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a691a-116"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a691a-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="a691a-117">Library</span></span><br/> | <dl> <span data-ttu-id="a691a-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a691a-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a691a-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a691a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a691a-120">**CDynamicOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="a691a-120">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




