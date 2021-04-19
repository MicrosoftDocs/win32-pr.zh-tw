---
description: AMOVIESETUP \_ 篩選結構的指標。
ms.assetid: 72db601b-78a3-484a-a27f-147ec36022ab
title: 'CFactoryTemplate：： m_pAMovieSetup_Filter 成員 (Combase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAMovieSetup_Filter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 087612acf99a41966ccd98d3b41d2b83255a86f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993416"
---
# <a name="cfactorytemplatem_pamoviesetup_filter-member"></a><span data-ttu-id="6e0ce-103">CFactoryTemplate：： m \_ pAMovieSetup \_ 篩選成員</span><span class="sxs-lookup"><span data-stu-id="6e0ce-103">CFactoryTemplate::m\_pAMovieSetup\_Filter member</span></span>

<span data-ttu-id="6e0ce-104">[**AMOVIESETUP \_ 篩選**](amoviesetup-filter.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="6e0ce-104">Pointer to an [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e0ce-105">語法</span><span class="sxs-lookup"><span data-stu-id="6e0ce-105">Syntax</span></span>


```C++
const AMOVIESETUP_FILTER *m_pAMovieSetup_Filter;
```



## <a name="remarks"></a><span data-ttu-id="6e0ce-106">備註</span><span class="sxs-lookup"><span data-stu-id="6e0ce-106">Remarks</span></span>

<span data-ttu-id="6e0ce-107">您可以使用此結構來讓篩選自我註冊。</span><span class="sxs-lookup"><span data-stu-id="6e0ce-107">Use this structure to make a filter self-registering.</span></span> <span data-ttu-id="6e0ce-108">如果您的元件不是篩選準則，此成員變數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6e0ce-108">If your component is not a filter, this member variable can be **NULL**.</span></span> <span data-ttu-id="6e0ce-109">如需詳細資訊，請參閱如何註冊 DirectShow 篩選。</span><span class="sxs-lookup"><span data-stu-id="6e0ce-109">For more information, see How to Register DirectShow Filters.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e0ce-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e0ce-110">Requirements</span></span>



| <span data-ttu-id="6e0ce-111">需求</span><span class="sxs-lookup"><span data-stu-id="6e0ce-111">Requirement</span></span> | <span data-ttu-id="6e0ce-112">值</span><span class="sxs-lookup"><span data-stu-id="6e0ce-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e0ce-113">標頭</span><span class="sxs-lookup"><span data-stu-id="6e0ce-113">Header</span></span><br/>  | <dl> <span data-ttu-id="6e0ce-114"><dt>Combase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6e0ce-114"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6e0ce-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="6e0ce-115">Library</span></span><br/> | <dl> <span data-ttu-id="6e0ce-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6e0ce-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e0ce-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e0ce-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e0ce-118">**CFactoryTemplate 類別**</span><span class="sxs-lookup"><span data-stu-id="6e0ce-118">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




