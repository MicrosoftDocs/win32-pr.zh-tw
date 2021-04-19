---
description: 這個運算子會測試某個參考時間是否大於另一個參考時間。
ms.assetid: db281040-9bcf-41fc-95b4-5481ffc5061f
title: COARefTime (Ctlutil) 的運算子> 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator>
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7c796bd5194c5bdb2dcbe260b803274962f81347
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991023"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="31c57-103">COARefTime 運算子> 方法</span><span class="sxs-lookup"><span data-stu-id="31c57-103">COARefTime.operator> method</span></span>

<span data-ttu-id="31c57-104">這個運算子會測試某個參考時間是否大於另一個參考時間。</span><span class="sxs-lookup"><span data-stu-id="31c57-104">This operator tests if one reference time is greater than another.</span></span>

## <a name="syntax"></a><span data-ttu-id="31c57-105">語法</span><span class="sxs-lookup"><span data-stu-id="31c57-105">Syntax</span></span>


```C++
BOOL operator>(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="31c57-106">參數</span><span class="sxs-lookup"><span data-stu-id="31c57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31c57-107">*rt* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="31c57-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="31c57-108">要比較的 **COARefTime** 物件參考。</span><span class="sxs-lookup"><span data-stu-id="31c57-108">Reference to the **COARefTime** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31c57-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="31c57-109">Return value</span></span>

<span data-ttu-id="31c57-110">如果此物件嚴格大於 *rt*，則傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="31c57-110">Returns **TRUE** if this object is strictly greater than *rt*.</span></span> <span data-ttu-id="31c57-111">否則，會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="31c57-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="31c57-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="31c57-112">Requirements</span></span>



| <span data-ttu-id="31c57-113">需求</span><span class="sxs-lookup"><span data-stu-id="31c57-113">Requirement</span></span> | <span data-ttu-id="31c57-114">值</span><span class="sxs-lookup"><span data-stu-id="31c57-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31c57-115">標頭</span><span class="sxs-lookup"><span data-stu-id="31c57-115">Header</span></span><br/>  | <dl> <span data-ttu-id="31c57-116"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="31c57-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="31c57-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="31c57-117">Library</span></span><br/> | <dl> <span data-ttu-id="31c57-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="31c57-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31c57-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31c57-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31c57-120">**COARefTime 類別**</span><span class="sxs-lookup"><span data-stu-id="31c57-120">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




