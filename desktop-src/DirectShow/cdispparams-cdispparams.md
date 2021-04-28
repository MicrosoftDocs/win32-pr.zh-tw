---
description: CDispParams。 CDispParams 函式-函數方法。
ms.assetid: da67a5e4-b4a1-4a38-93fe-0965695e93f5
title: 'CDispParams. CDispParams (Ctlutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDispParams.CDispParams
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 42f55a57a0f9e06d3001c2638d457fe0b82a914d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095786"
---
# <a name="cdispparamscdispparams-constructor"></a><span data-ttu-id="36593-103">CDispParams. CDispParams 函數</span><span class="sxs-lookup"><span data-stu-id="36593-103">CDispParams.CDispParams constructor</span></span>

<span data-ttu-id="36593-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="36593-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="36593-105">語法</span><span class="sxs-lookup"><span data-stu-id="36593-105">Syntax</span></span>


```C++
CDispParams(
   UINT    nArgs,
   VARIANT *pArgs
);
```



## <a name="parameters"></a><span data-ttu-id="36593-106">參數</span><span class="sxs-lookup"><span data-stu-id="36593-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36593-107">*nArgs*</span><span class="sxs-lookup"><span data-stu-id="36593-107">*nArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="36593-108">傳遞給方法或屬性的引數數目。</span><span class="sxs-lookup"><span data-stu-id="36593-108">Number of arguments passed to the method or property.</span></span>

</dd> <dt>

<span data-ttu-id="36593-109">*pArgs*</span><span class="sxs-lookup"><span data-stu-id="36593-109">*pArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="36593-110">引數清單的指標。</span><span class="sxs-lookup"><span data-stu-id="36593-110">Pointer to the list of arguments.</span></span> <span data-ttu-id="36593-111">在清單中，每個引數都會儲存其 variant 類型。</span><span class="sxs-lookup"><span data-stu-id="36593-111">In the list, each argument is stored with its variant type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="36593-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="36593-112">Requirements</span></span>



| <span data-ttu-id="36593-113">需求</span><span class="sxs-lookup"><span data-stu-id="36593-113">Requirement</span></span> | <span data-ttu-id="36593-114">值</span><span class="sxs-lookup"><span data-stu-id="36593-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36593-115">標頭</span><span class="sxs-lookup"><span data-stu-id="36593-115">Header</span></span><br/>  | <dl> <span data-ttu-id="36593-116"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="36593-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="36593-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="36593-117">Library</span></span><br/> | <dl> <span data-ttu-id="36593-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="36593-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36593-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36593-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36593-120">**CDispParams 類別**</span><span class="sxs-lookup"><span data-stu-id="36593-120">**CDispParams Class**</span></span>](cdispparams.md)
</dt> </dl>

 

 




