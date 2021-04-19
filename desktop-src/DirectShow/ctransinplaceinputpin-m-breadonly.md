---
Description: 指定輸入資料流程是否為唯讀的旗標。 上游篩選器會在呼叫 NotifyAllocator 方法時指定此資訊。 依預設，此值為 FALSE。
ms.assetid: d5a71c00-326c-45b4-b9c5-b67a0fe71bf5
title: 'CTransInPlaceInputPin：： m_bReadOnly 成員 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bReadOnly
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ac2f66296c08b2461440e0615b225c62405fd99a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989535"
---
# <a name="ctransinplaceinputpinm_breadonly-member"></a><span data-ttu-id="53152-105">CTransInPlaceInputPin：： m \_ bReadOnly 成員</span><span class="sxs-lookup"><span data-stu-id="53152-105">CTransInPlaceInputPin::m\_bReadOnly member</span></span>

<span data-ttu-id="53152-106">指定輸入資料流程是否為唯讀的旗標。</span><span class="sxs-lookup"><span data-stu-id="53152-106">Flag that specifies whether the input stream is read-only.</span></span> <span data-ttu-id="53152-107">上游篩選器會在呼叫 [**NotifyAllocator**](ctransinplaceinputpin-notifyallocator.md) 方法時指定此資訊。</span><span class="sxs-lookup"><span data-stu-id="53152-107">The upstream filter specifies this information when it calls the [**NotifyAllocator**](ctransinplaceinputpin-notifyallocator.md) method.</span></span> <span data-ttu-id="53152-108">依預設，此值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="53152-108">By default, the value is **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="53152-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="53152-109">Syntax</span></span>


```C++
BOOL m_bReadOnly;
```



## <a name="requirements"></a><span data-ttu-id="53152-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="53152-110">Requirements</span></span>



| <span data-ttu-id="53152-111">需求</span><span class="sxs-lookup"><span data-stu-id="53152-111">Requirement</span></span> | <span data-ttu-id="53152-112">值</span><span class="sxs-lookup"><span data-stu-id="53152-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53152-113">標頭</span><span class="sxs-lookup"><span data-stu-id="53152-113">Header</span></span><br/>  | <dl> <span data-ttu-id="53152-114"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="53152-114"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="53152-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="53152-115">Library</span></span><br/> | <dl> <span data-ttu-id="53152-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="53152-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53152-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53152-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53152-118">**CTransInPlaceInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="53152-118">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




