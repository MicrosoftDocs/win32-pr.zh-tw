---
description: M \_ bModifiesData 成員變數會指出篩選準則是否修改接收的範例資料。 值是在 CTransInPlaceFilter 的函式中設定，但預設為 TRUE。
ms.assetid: 8ccdba46-315f-4519-b363-6870d1217f98
title: 'CTransInPlaceFilter：： m_bModifiesData 成員 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bModifiesData
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5bc0d630fd0eda6e9915f8c11f5b15d21b725ce8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989821"
---
# <a name="ctransinplacefilterm_bmodifiesdata-member"></a><span data-ttu-id="1697c-104">CTransInPlaceFilter：： m \_ bModifiesData 成員</span><span class="sxs-lookup"><span data-stu-id="1697c-104">CTransInPlaceFilter::m\_bModifiesData member</span></span>

<span data-ttu-id="1697c-105">`m_bModifiesData`成員變數會指出篩選準則是否修改接收的範例資料。</span><span class="sxs-lookup"><span data-stu-id="1697c-105">The `m_bModifiesData` member variable indicates whether the filter modifies the sample data that is receives.</span></span> <span data-ttu-id="1697c-106">值是在 **CTransInPlaceFilter** 的函式中設定，但預設為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="1697c-106">The value is set in the **CTransInPlaceFilter** constructor, but defaults to **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1697c-107">語法</span><span class="sxs-lookup"><span data-stu-id="1697c-107">Syntax</span></span>


```C++
bool m_bModifiesData;
```



## <a name="remarks"></a><span data-ttu-id="1697c-108">備註</span><span class="sxs-lookup"><span data-stu-id="1697c-108">Remarks</span></span>

<span data-ttu-id="1697c-109">這個變數會影響篩選器如何協調配置器。</span><span class="sxs-lookup"><span data-stu-id="1697c-109">This variable affects how the filter negotiates the allocator.</span></span> <span data-ttu-id="1697c-110">如果值為 **TRUE**，則篩選器無法針對這兩個 pin 連線使用唯讀配置器。</span><span class="sxs-lookup"><span data-stu-id="1697c-110">If the value is **TRUE**, the filter cannot use a read-only allocator for both pin connections.</span></span>

## <a name="requirements"></a><span data-ttu-id="1697c-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="1697c-111">Requirements</span></span>



| <span data-ttu-id="1697c-112">需求</span><span class="sxs-lookup"><span data-stu-id="1697c-112">Requirement</span></span> | <span data-ttu-id="1697c-113">值</span><span class="sxs-lookup"><span data-stu-id="1697c-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1697c-114">標頭</span><span class="sxs-lookup"><span data-stu-id="1697c-114">Header</span></span><br/>  | <dl> <span data-ttu-id="1697c-115"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1697c-115"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1697c-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="1697c-116">Library</span></span><br/> | <dl> <span data-ttu-id="1697c-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="1697c-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1697c-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1697c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1697c-119">**CTransInPlaceFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="1697c-119">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




