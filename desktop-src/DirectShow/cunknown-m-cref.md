---
description: 參考計數。
ms.assetid: be619a85-ca73-4cee-9df7-20e7be21853b
title: 'CUnknown：： m_cRef 成員 (Combase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_cRef
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94ff5d88ca48feeb46a8b0411a55d6261aefcf6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984383"
---
# <a name="cunknownm_cref-member"></a><span data-ttu-id="3ddae-103">CUnknown：： m \_ cRef 成員</span><span class="sxs-lookup"><span data-stu-id="3ddae-103">CUnknown::m\_cRef member</span></span>

<span data-ttu-id="3ddae-104">參考計數。</span><span class="sxs-lookup"><span data-stu-id="3ddae-104">Reference count.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ddae-105">語法</span><span class="sxs-lookup"><span data-stu-id="3ddae-105">Syntax</span></span>


```C++
LONG m_cRef;
```



## <a name="remarks"></a><span data-ttu-id="3ddae-106">備註</span><span class="sxs-lookup"><span data-stu-id="3ddae-106">Remarks</span></span>

<span data-ttu-id="3ddae-107">如果您覆寫 [**NonDelegatingAddRef**](cunknown-nondelegatingaddref.md) 或 [**NonDelegatingRelease**](cunknown-nondelegatingrelease.md) 方法，請使用這個成員變數。</span><span class="sxs-lookup"><span data-stu-id="3ddae-107">Use this member variable if you override the [**NonDelegatingAddRef**](cunknown-nondelegatingaddref.md) or [**NonDelegatingRelease**](cunknown-nondelegatingrelease.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ddae-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ddae-108">Requirements</span></span>



| <span data-ttu-id="3ddae-109">需求</span><span class="sxs-lookup"><span data-stu-id="3ddae-109">Requirement</span></span> | <span data-ttu-id="3ddae-110">值</span><span class="sxs-lookup"><span data-stu-id="3ddae-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ddae-111">標頭</span><span class="sxs-lookup"><span data-stu-id="3ddae-111">Header</span></span><br/>  | <dl> <span data-ttu-id="3ddae-112"><dt>Combase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3ddae-112"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3ddae-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="3ddae-113">Library</span></span><br/> | <dl> <span data-ttu-id="3ddae-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3ddae-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




