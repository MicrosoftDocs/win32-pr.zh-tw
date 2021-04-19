---
description: = 運算子會指派新的參考時間。 這個方法使用 *ll* 參數。
ms.assetid: 556c2e8a-4726-42ab-949d-9a028ebb1b95
title: CRefTime. operator = method (Reftime. h) -ll 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d09cb957e06d8b075cff3d831a7f68fbbdf662a8
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106993704"
---
# <a name="creftimeoperator-method-reftimeh---ll-parameter"></a><span data-ttu-id="dcc42-104">CRefTime. operator = method (Reftime. h) -ll 參數</span><span class="sxs-lookup"><span data-stu-id="dcc42-104">CRefTime.operator= method (Reftime.h) - ll parameter</span></span>

<span data-ttu-id="dcc42-105">= 運算子會指派新的參考時間。</span><span class="sxs-lookup"><span data-stu-id="dcc42-105">The = operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcc42-106">語法</span><span class="sxs-lookup"><span data-stu-id="dcc42-106">Syntax</span></span>


```C++
CRefTime& operator=(
   const LONGLONG ll
);
```



## <a name="parameters"></a><span data-ttu-id="dcc42-107">參數</span><span class="sxs-lookup"><span data-stu-id="dcc42-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcc42-108">*將*</span><span class="sxs-lookup"><span data-stu-id="dcc42-108">*ll*</span></span> 
</dt> <dd>

<span data-ttu-id="dcc42-109">新的參考時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="dcc42-109">New reference time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcc42-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="dcc42-110">Return value</span></span>

<span data-ttu-id="dcc42-111">傳回物件的參考。</span><span class="sxs-lookup"><span data-stu-id="dcc42-111">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcc42-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="dcc42-112">Requirements</span></span>



| <span data-ttu-id="dcc42-113">需求</span><span class="sxs-lookup"><span data-stu-id="dcc42-113">Requirement</span></span> | <span data-ttu-id="dcc42-114">值</span><span class="sxs-lookup"><span data-stu-id="dcc42-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcc42-115">標頭</span><span class="sxs-lookup"><span data-stu-id="dcc42-115">Header</span></span>  | <span data-ttu-id="dcc42-116">Reftime (包含： .h) </span><span class="sxs-lookup"><span data-stu-id="dcc42-116">Reftime.h (include Streams.h)</span></span>                                                                                   |
| <span data-ttu-id="dcc42-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="dcc42-117">Library</span></span> | <span data-ttu-id="dcc42-118"> (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建) </span><span class="sxs-lookup"><span data-stu-id="dcc42-118">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |



 

 




