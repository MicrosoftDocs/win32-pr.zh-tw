---
description: M \_ pAlloc 成員變數是記憶體配置器的 IMemAllocator 介面指標。
ms.assetid: a3be5982-83f0-4552-9bcd-85da4a4918ff
title: 'CPullPin：： m_pAlloc 成員 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAlloc
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e9945bd7b5f3c5b54f0ef578c2b012d0e56935d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999652"
---
# <a name="cpullpinm_palloc-member"></a><span data-ttu-id="b7302-103">CPullPin：： m \_ pAlloc 成員</span><span class="sxs-lookup"><span data-stu-id="b7302-103">CPullPin::m\_pAlloc member</span></span>

<span data-ttu-id="b7302-104">`m_pAlloc`成員變數是記憶體配置器之 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="b7302-104">The `m_pAlloc` member variable is a pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface of the memory allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7302-105">語法</span><span class="sxs-lookup"><span data-stu-id="b7302-105">Syntax</span></span>


```C++
IMemAllocator *m_pAlloc;
```



## <a name="remarks"></a><span data-ttu-id="b7302-106">備註</span><span class="sxs-lookup"><span data-stu-id="b7302-106">Remarks</span></span>

<span data-ttu-id="b7302-107">[**CPullPin：:D ecideallocator**](cpullpin-decideallocator.md)方法會設定這個成員變數。</span><span class="sxs-lookup"><span data-stu-id="b7302-107">The [**CPullPin::DecideAllocator**](cpullpin-decideallocator.md) method sets this member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7302-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7302-108">Requirements</span></span>



| <span data-ttu-id="b7302-109">需求</span><span class="sxs-lookup"><span data-stu-id="b7302-109">Requirement</span></span> | <span data-ttu-id="b7302-110">值</span><span class="sxs-lookup"><span data-stu-id="b7302-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7302-111">標頭</span><span class="sxs-lookup"><span data-stu-id="b7302-111">Header</span></span><br/>  | <dl> <span data-ttu-id="b7302-112"><dt>Pullpin。h</dt></span><span class="sxs-lookup"><span data-stu-id="b7302-112"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="b7302-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="b7302-113">Library</span></span><br/> | <dl> <span data-ttu-id="b7302-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b7302-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7302-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7302-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7302-116">**CPullPin 類別**</span><span class="sxs-lookup"><span data-stu-id="b7302-116">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




