---
description: 這個運算子會將參考時間除以某個值。
ms.assetid: fb2e2a4b-dc0b-42e3-86c7-8aa2c60daedc
title: 'COARefTime. operator/方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator/
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e1e4d7b7adb881ac11988a2d2c46946ff6cddcc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999415"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="faeed-103">COARefTime. operator/方法</span><span class="sxs-lookup"><span data-stu-id="faeed-103">COARefTime.operator/ method</span></span>

<span data-ttu-id="faeed-104">這個運算子會將參考時間除以某個值。</span><span class="sxs-lookup"><span data-stu-id="faeed-104">This operator divides a reference time by a value.</span></span>

## <a name="syntax"></a><span data-ttu-id="faeed-105">語法</span><span class="sxs-lookup"><span data-stu-id="faeed-105">Syntax</span></span>


```C++
COARefTime operator/(
   LONG l
);
```



## <a name="parameters"></a><span data-ttu-id="faeed-106">參數</span><span class="sxs-lookup"><span data-stu-id="faeed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="faeed-107">*l*</span><span class="sxs-lookup"><span data-stu-id="faeed-107">*l*</span></span> 
</dt> <dd>

<span data-ttu-id="faeed-108">因數。</span><span class="sxs-lookup"><span data-stu-id="faeed-108">Divisor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="faeed-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="faeed-109">Return value</span></span>

<span data-ttu-id="faeed-110">傳回新的 **COARefTime** 物件，等於這個物件和 **l** 的商。</span><span class="sxs-lookup"><span data-stu-id="faeed-110">Returns a new **COARefTime** object equal to the quotient of this object and **l**.</span></span>

## <a name="requirements"></a><span data-ttu-id="faeed-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="faeed-111">Requirements</span></span>



| <span data-ttu-id="faeed-112">需求</span><span class="sxs-lookup"><span data-stu-id="faeed-112">Requirement</span></span> | <span data-ttu-id="faeed-113">值</span><span class="sxs-lookup"><span data-stu-id="faeed-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="faeed-114">標頭</span><span class="sxs-lookup"><span data-stu-id="faeed-114">Header</span></span><br/>  | <dl> <span data-ttu-id="faeed-115"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="faeed-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="faeed-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="faeed-116">Library</span></span><br/> | <dl> <span data-ttu-id="faeed-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="faeed-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faeed-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="faeed-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faeed-119">**COARefTime 類別**</span><span class="sxs-lookup"><span data-stu-id="faeed-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




