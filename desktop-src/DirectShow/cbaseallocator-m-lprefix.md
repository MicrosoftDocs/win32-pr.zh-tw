---
description: 每個緩衝區的前置詞（以位元組為單位）。
ms.assetid: 471b73bf-f959-41aa-84ba-324a2738dd0e
title: 'CBaseAllocator：： m_lPrefix 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lPrefix
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc52db44dcdfa050cf8bc7faf57cb7094d8cac91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993260"
---
# <a name="cbaseallocatorm_lprefix-member"></a><span data-ttu-id="71b30-103">CBaseAllocator：： m \_ lPrefix 成員</span><span class="sxs-lookup"><span data-stu-id="71b30-103">CBaseAllocator::m\_lPrefix member</span></span>

<span data-ttu-id="71b30-104">每個緩衝區的前置詞（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="71b30-104">Prefix of each buffer, in bytes.</span></span> <span data-ttu-id="71b30-105">如果此值不是零， [**CBaseAllocator：： GetBuffer**](cbaseallocator-getbuffer.md) 方法所傳回的每個緩衝區指標前面都會加上大小為 *m \_ lPrefix* 的位元組區塊。</span><span class="sxs-lookup"><span data-stu-id="71b30-105">If the value is non-zero, each buffer pointer returned by the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method is preceded by a block of bytes of size *m\_lPrefix*.</span></span> <span data-ttu-id="71b30-106">這個記憶體區塊稱為 *前置* 詞。</span><span class="sxs-lookup"><span data-stu-id="71b30-106">This memory block is called the *prefix*.</span></span> <span data-ttu-id="71b30-107">[**CBaseAllocator：： m \_ lSize**](cbaseallocator-m-lsize.md)成員變數不包含前置詞值。</span><span class="sxs-lookup"><span data-stu-id="71b30-107">The [**CBaseAllocator::m\_lSize**](cbaseallocator-m-lsize.md) member variable does not include the prefix value.</span></span>

## <a name="syntax"></a><span data-ttu-id="71b30-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="71b30-108">Syntax</span></span>


```C++
long m_lPrefix;
```



## <a name="requirements"></a><span data-ttu-id="71b30-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="71b30-109">Requirements</span></span>



| <span data-ttu-id="71b30-110">需求</span><span class="sxs-lookup"><span data-stu-id="71b30-110">Requirement</span></span> | <span data-ttu-id="71b30-111">值</span><span class="sxs-lookup"><span data-stu-id="71b30-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71b30-112">標頭</span><span class="sxs-lookup"><span data-stu-id="71b30-112">Header</span></span><br/>  | <dl> <span data-ttu-id="71b30-113"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="71b30-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="71b30-114">程式庫</span><span class="sxs-lookup"><span data-stu-id="71b30-114">Library</span></span><br/> | <dl> <span data-ttu-id="71b30-115"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="71b30-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71b30-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71b30-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71b30-117">**CBaseAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="71b30-117">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




