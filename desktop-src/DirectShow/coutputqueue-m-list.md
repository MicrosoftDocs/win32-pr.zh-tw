---
description: 媒體範例佇列。
ms.assetid: 910f1c0c-2ce9-452f-a97b-aa424da9a93e
title: 'COutputQueue：： m_List 成員 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_List
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32840ed0ed9f976cceb1e0dc6dc8debc3f774377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994297"
---
# <a name="coutputqueuem_list-member"></a><span data-ttu-id="ee9cb-103">COutputQueue：： m \_ List 成員</span><span class="sxs-lookup"><span data-stu-id="ee9cb-103">COutputQueue::m\_List member</span></span>

<span data-ttu-id="ee9cb-104">媒體範例佇列。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-104">Media sample queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee9cb-105">語法</span><span class="sxs-lookup"><span data-stu-id="ee9cb-105">Syntax</span></span>


```C++
CSampleList *m_List;
```



## <a name="remarks"></a><span data-ttu-id="ee9cb-106">備註</span><span class="sxs-lookup"><span data-stu-id="ee9cb-106">Remarks</span></span>

<span data-ttu-id="ee9cb-107">這個成員變數是 [**CGenericList**](cgenericlist.md) 物件的指標，該物件會保存 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 指標。</span><span class="sxs-lookup"><span data-stu-id="ee9cb-107">This member variable is a pointer to a [**CGenericList**](cgenericlist.md) object that holds [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) pointers.</span></span> <span data-ttu-id="ee9cb-108">**CSampleList** 類型的定義如下：</span><span class="sxs-lookup"><span data-stu-id="ee9cb-108">The **CSampleList** type is defined as follows:</span></span>

``` syntax
typedef CGenericList<IMediaSample> CSampleList;
```

## <a name="requirements"></a><span data-ttu-id="ee9cb-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee9cb-109">Requirements</span></span>



| <span data-ttu-id="ee9cb-110">需求</span><span class="sxs-lookup"><span data-stu-id="ee9cb-110">Requirement</span></span> | <span data-ttu-id="ee9cb-111">值</span><span class="sxs-lookup"><span data-stu-id="ee9cb-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee9cb-112">標頭</span><span class="sxs-lookup"><span data-stu-id="ee9cb-112">Header</span></span><br/>  | <dl> <span data-ttu-id="ee9cb-113"><dt>Outputq (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ee9cb-113"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ee9cb-114">程式庫</span><span class="sxs-lookup"><span data-stu-id="ee9cb-114">Library</span></span><br/> | <dl> <span data-ttu-id="ee9cb-115"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ee9cb-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee9cb-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee9cb-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee9cb-117">**COutputQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="ee9cb-117">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




