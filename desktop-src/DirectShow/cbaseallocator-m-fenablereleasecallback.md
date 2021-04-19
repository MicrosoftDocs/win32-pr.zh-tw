---
description: 指出是否已啟用發行回呼的旗標。 此旗標是在函式方法中設定。 如果值為 FALSE，則呼叫 CBaseAllocator：： SetNotify 方法會導致判斷提示 (在) 的 debug 組建中引發。
ms.assetid: cc9adc7c-ec44-41e7-875a-b3e553120804
title: 'CBaseAllocator：： m_fEnableReleaseCallback 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_fEnableReleaseCallback
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 626f1e8f4101eb48e79bc1cf679d1b91be9b2b31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995088"
---
# <a name="cbaseallocatorm_fenablereleasecallback-member"></a><span data-ttu-id="68b6b-105">CBaseAllocator：： m \_ fEnableReleaseCallback 成員</span><span class="sxs-lookup"><span data-stu-id="68b6b-105">CBaseAllocator::m\_fEnableReleaseCallback member</span></span>

<span data-ttu-id="68b6b-106">指出是否已啟用發行回呼的旗標。</span><span class="sxs-lookup"><span data-stu-id="68b6b-106">Flag indicating whether the release callback is enabled.</span></span> <span data-ttu-id="68b6b-107">此旗標是在函式方法中設定。</span><span class="sxs-lookup"><span data-stu-id="68b6b-107">This flag is set in the constructor method.</span></span> <span data-ttu-id="68b6b-108">如果值為 FALSE，則呼叫 [**CBaseAllocator：： SetNotify**](cbaseallocator-setnotify.md)方法會導致 **判斷** 提示 (在) 的 debug 組建中引發。</span><span class="sxs-lookup"><span data-stu-id="68b6b-108">If the value is **FALSE**, calling the [**CBaseAllocator::SetNotify**](cbaseallocator-setnotify.md) method causes an assertion to fire (in debug builds).</span></span>

## <a name="syntax"></a><span data-ttu-id="68b6b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="68b6b-109">Syntax</span></span>


```C++
BOOL m_fEnableReleaseCallback;
```



## <a name="requirements"></a><span data-ttu-id="68b6b-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="68b6b-110">Requirements</span></span>



| <span data-ttu-id="68b6b-111">需求</span><span class="sxs-lookup"><span data-stu-id="68b6b-111">Requirement</span></span> | <span data-ttu-id="68b6b-112">值</span><span class="sxs-lookup"><span data-stu-id="68b6b-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68b6b-113">標頭</span><span class="sxs-lookup"><span data-stu-id="68b6b-113">Header</span></span><br/>  | <dl> <span data-ttu-id="68b6b-114"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="68b6b-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="68b6b-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="68b6b-115">Library</span></span><br/> | <dl> <span data-ttu-id="68b6b-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="68b6b-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68b6b-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68b6b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68b6b-118">**CBaseAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="68b6b-118">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




