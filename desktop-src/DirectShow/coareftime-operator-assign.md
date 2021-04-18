---
description: 這個運算子會指派新的參考時間。
ms.assetid: ae6a33ab-f4e0-4f1c-80a0-8a25ee1e9dc5
title: 'COARefTime： operator = 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f5a051cea555975fd8606c3693d4b7d63cb9ce4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996399"
---
# <a name="coareftimeoperator-method-ctlutilh"></a><span data-ttu-id="3487e-103">COARefTime： operator = 方法 (Ctlutil .h) </span><span class="sxs-lookup"><span data-stu-id="3487e-103">COARefTime.operator= method (Ctlutil.h)</span></span>

<span data-ttu-id="3487e-104">這個運算子會指派新的參考時間。</span><span class="sxs-lookup"><span data-stu-id="3487e-104">This operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="3487e-105">語法</span><span class="sxs-lookup"><span data-stu-id="3487e-105">Syntax</span></span>


```C++
COARefTime& operator=(
  [ref] const double &rd
);
```



## <a name="parameters"></a><span data-ttu-id="3487e-106">參數</span><span class="sxs-lookup"><span data-stu-id="3487e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3487e-107">*rd* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="3487e-107">*rd* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="3487e-108">參考 **雙精度浮點數** ，指定新的參考時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="3487e-108">Reference to a **double** value that specifies the new reference time in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3487e-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="3487e-109">Return value</span></span>

<span data-ttu-id="3487e-110">傳回物件的參考。</span><span class="sxs-lookup"><span data-stu-id="3487e-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="3487e-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="3487e-111">Requirements</span></span>



| <span data-ttu-id="3487e-112">需求</span><span class="sxs-lookup"><span data-stu-id="3487e-112">Requirement</span></span> | <span data-ttu-id="3487e-113">值</span><span class="sxs-lookup"><span data-stu-id="3487e-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3487e-114">標頭</span><span class="sxs-lookup"><span data-stu-id="3487e-114">Header</span></span><br/>  | <dl> <span data-ttu-id="3487e-115"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3487e-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3487e-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="3487e-116">Library</span></span><br/> | <dl> <span data-ttu-id="3487e-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3487e-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3487e-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3487e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3487e-119">**COARefTime 類別**</span><span class="sxs-lookup"><span data-stu-id="3487e-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




