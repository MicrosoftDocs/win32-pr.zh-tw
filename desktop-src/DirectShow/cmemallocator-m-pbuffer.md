---
description: 包含緩衝區之記憶體區塊的指標。
ms.assetid: b9d08f5b-8616-4f68-869a-e8ebb77ccdc1
title: 'CMemAllocator：： m_pBuffer 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pBuffer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ae988474196e323cde24305b0e389ac69f0f10d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984471"
---
# <a name="cmemallocatorm_pbuffer-member"></a><span data-ttu-id="e007b-103">CMemAllocator：： m \_ pBuffer 成員</span><span class="sxs-lookup"><span data-stu-id="e007b-103">CMemAllocator::m\_pBuffer member</span></span>

<span data-ttu-id="e007b-104">包含緩衝區之記憶體區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="e007b-104">Pointer to the memory block that contains the buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="e007b-105">語法</span><span class="sxs-lookup"><span data-stu-id="e007b-105">Syntax</span></span>


```C++
LPBYTE m_pBuffer;
```



## <a name="remarks"></a><span data-ttu-id="e007b-106">備註</span><span class="sxs-lookup"><span data-stu-id="e007b-106">Remarks</span></span>

<span data-ttu-id="e007b-107">範例緩衝區會計算為此指標的位移。</span><span class="sxs-lookup"><span data-stu-id="e007b-107">Sample buffers are calculated as offsets from this pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="e007b-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="e007b-108">Requirements</span></span>



| <span data-ttu-id="e007b-109">需求</span><span class="sxs-lookup"><span data-stu-id="e007b-109">Requirement</span></span> | <span data-ttu-id="e007b-110">值</span><span class="sxs-lookup"><span data-stu-id="e007b-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e007b-111">標頭</span><span class="sxs-lookup"><span data-stu-id="e007b-111">Header</span></span><br/>  | <dl> <span data-ttu-id="e007b-112"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e007b-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e007b-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="e007b-113">Library</span></span><br/> | <dl> <span data-ttu-id="e007b-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e007b-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e007b-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e007b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e007b-116">**CMemAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="e007b-116">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




