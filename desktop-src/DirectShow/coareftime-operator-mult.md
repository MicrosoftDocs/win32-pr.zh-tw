---
description: 這個運算子會將參考時間乘以某個值。
ms.assetid: f575fd41-1d3e-43a6-abf8-8e64093e408e
title: 'COARefTime. operator * 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator*
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c62a4282f7a43ba3d7ba35daf81530f8b246be32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983117"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="9cab1-103">COARefTime 運算子 \* 方法</span><span class="sxs-lookup"><span data-stu-id="9cab1-103">COARefTime.operator\* method</span></span>

<span data-ttu-id="9cab1-104">這個運算子會將參考時間乘以某個值。</span><span class="sxs-lookup"><span data-stu-id="9cab1-104">This operator multiplies a reference time by a value.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cab1-105">語法</span><span class="sxs-lookup"><span data-stu-id="9cab1-105">Syntax</span></span>


```C++
COARefTime operator*(
   LONG l
);
```



## <a name="parameters"></a><span data-ttu-id="9cab1-106">參數</span><span class="sxs-lookup"><span data-stu-id="9cab1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cab1-107">*l*</span><span class="sxs-lookup"><span data-stu-id="9cab1-107">*l*</span></span> 
</dt> <dd>

<span data-ttu-id="9cab1-108">乘數。</span><span class="sxs-lookup"><span data-stu-id="9cab1-108">Multiplier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cab1-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="9cab1-109">Return value</span></span>

<span data-ttu-id="9cab1-110">傳回新的 **COARefTime** 物件，這個物件等於這個物件和 **l** 的乘積。</span><span class="sxs-lookup"><span data-stu-id="9cab1-110">Returns a new **COARefTime** object equal to the product of this object and **l**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cab1-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="9cab1-111">Requirements</span></span>



| <span data-ttu-id="9cab1-112">需求</span><span class="sxs-lookup"><span data-stu-id="9cab1-112">Requirement</span></span> | <span data-ttu-id="9cab1-113">值</span><span class="sxs-lookup"><span data-stu-id="9cab1-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cab1-114">標頭</span><span class="sxs-lookup"><span data-stu-id="9cab1-114">Header</span></span><br/>  | <dl> <span data-ttu-id="9cab1-115"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9cab1-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9cab1-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="9cab1-116">Library</span></span><br/> | <dl> <span data-ttu-id="9cab1-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9cab1-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cab1-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9cab1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cab1-119">**COARefTime 類別**</span><span class="sxs-lookup"><span data-stu-id="9cab1-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




