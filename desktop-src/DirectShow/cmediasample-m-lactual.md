---
description: 緩衝區中有效資料的長度（以位元組為單位）。 值必須等於或小於 CMediaSample：： m cbBuffer 成員變數所指定的緩衝區大小 \_ 。
ms.assetid: 75610043-fe0b-4cd0-9fd6-292f25040d72
title: 'CMediaSample：： m_lActual 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lActual
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69d7abd5eb64db0ab5801de9b7e27b84a991ae06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983964"
---
# <a name="cmediasamplem_lactual-member"></a><span data-ttu-id="0a4f8-104">CMediaSample：： m \_ lActual 成員</span><span class="sxs-lookup"><span data-stu-id="0a4f8-104">CMediaSample::m\_lActual member</span></span>

<span data-ttu-id="0a4f8-105">緩衝區中有效資料的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="0a4f8-105">Length of the valid data in the buffer, in bytes.</span></span> <span data-ttu-id="0a4f8-106">值必須等於或小於 [**CMediaSample：： m \_ cbBuffer**](cmediasample-m-cbbuffer.md) 成員變數所指定的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="0a4f8-106">The value must be equal to or less than the size of the buffer, specified by the [**CMediaSample::m\_cbBuffer**](cmediasample-m-cbbuffer.md) member variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a4f8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a4f8-107">Syntax</span></span>


```C++
LONG m_lActual;
```



## <a name="requirements"></a><span data-ttu-id="0a4f8-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a4f8-108">Requirements</span></span>



| <span data-ttu-id="0a4f8-109">需求</span><span class="sxs-lookup"><span data-stu-id="0a4f8-109">Requirement</span></span> | <span data-ttu-id="0a4f8-110">值</span><span class="sxs-lookup"><span data-stu-id="0a4f8-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a4f8-111">標頭</span><span class="sxs-lookup"><span data-stu-id="0a4f8-111">Header</span></span><br/>  | <dl> <span data-ttu-id="0a4f8-112"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0a4f8-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0a4f8-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="0a4f8-113">Library</span></span><br/> | <dl> <span data-ttu-id="0a4f8-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0a4f8-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a4f8-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a4f8-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a4f8-116">**CMediaSample 類別**</span><span class="sxs-lookup"><span data-stu-id="0a4f8-116">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




