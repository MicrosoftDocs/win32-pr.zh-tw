---
description: 建立此範例的配置器指標。
ms.assetid: b4faccec-9124-4ae6-8662-ac5eb017328a
title: 'CMediaSample：： m_pAllocator 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAllocator
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ac2943c08b881badd8e15ea0633952ccc973a534
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991540"
---
# <a name="cmediasamplem_pallocator-member"></a><span data-ttu-id="a5406-103">CMediaSample：： m \_ pAllocator 成員</span><span class="sxs-lookup"><span data-stu-id="a5406-103">CMediaSample::m\_pAllocator member</span></span>

<span data-ttu-id="a5406-104">建立此範例的配置器指標。</span><span class="sxs-lookup"><span data-stu-id="a5406-104">Pointer to the allocator that created this sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5406-105">語法</span><span class="sxs-lookup"><span data-stu-id="a5406-105">Syntax</span></span>


```C++
CBaseAllocator *m_pAllocator;
```



## <a name="remarks"></a><span data-ttu-id="a5406-106">備註</span><span class="sxs-lookup"><span data-stu-id="a5406-106">Remarks</span></span>

<span data-ttu-id="a5406-107">雖然此範例會保留配置器的指標，但不會保留參考計數。</span><span class="sxs-lookup"><span data-stu-id="a5406-107">Although the sample keeps a pointer to the allocator, it does not hold a reference count.</span></span> <span data-ttu-id="a5406-108">取而代之的是，配置器會在 [**IMemAllocator：： GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) 方法中遞增自己的參考計數，並在 [**IMemAllocator：： ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) 方法中自行發行。</span><span class="sxs-lookup"><span data-stu-id="a5406-108">Instead, the allocator increments its own reference count in the [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) method, and releases itself in the [**IMemAllocator::ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) method.</span></span> <span data-ttu-id="a5406-109">這可保證配置器將可供使用，只要另一個物件正在使用範例即可。</span><span class="sxs-lookup"><span data-stu-id="a5406-109">This guarantees that the allocator will be available as long as another object is using the sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5406-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5406-110">Requirements</span></span>



| <span data-ttu-id="a5406-111">需求</span><span class="sxs-lookup"><span data-stu-id="a5406-111">Requirement</span></span> | <span data-ttu-id="a5406-112">值</span><span class="sxs-lookup"><span data-stu-id="a5406-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5406-113">標頭</span><span class="sxs-lookup"><span data-stu-id="a5406-113">Header</span></span><br/>  | <dl> <span data-ttu-id="a5406-114"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a5406-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a5406-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="a5406-115">Library</span></span><br/> | <dl> <span data-ttu-id="a5406-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a5406-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5406-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5406-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5406-118">**CMediaSample 類別**</span><span class="sxs-lookup"><span data-stu-id="a5406-118">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




