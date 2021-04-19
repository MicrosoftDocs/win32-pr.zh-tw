---
description: 這個運算子會測試某個參考時間是否小於另一個。
ms.assetid: 709fb861-a836-4a20-8c93-c0e8ab79f377
title: COARefTime (Ctlutil) 的運算子< 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator<
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c61403b959f8b5ee19e9ba0d9cd0ab4db54c124
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979452"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="fa0ca-103">COARefTime 運算子< 方法</span><span class="sxs-lookup"><span data-stu-id="fa0ca-103">COARefTime.operator< method</span></span>

<span data-ttu-id="fa0ca-104">這個運算子會測試某個參考時間是否小於另一個。</span><span class="sxs-lookup"><span data-stu-id="fa0ca-104">This operator tests if one reference time is less than another.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa0ca-105">語法</span><span class="sxs-lookup"><span data-stu-id="fa0ca-105">Syntax</span></span>


```C++
BOOL operator<(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="fa0ca-106">參數</span><span class="sxs-lookup"><span data-stu-id="fa0ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa0ca-107">*rt* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="fa0ca-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="fa0ca-108">要比較的 **COARefTime** 物件參考。</span><span class="sxs-lookup"><span data-stu-id="fa0ca-108">Reference to the **COARefTime** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa0ca-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="fa0ca-109">Return value</span></span>

<span data-ttu-id="fa0ca-110">如果此物件嚴格小於 *rt*，則傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="fa0ca-110">Returns **TRUE** if this object is strictly less than *rt*.</span></span> <span data-ttu-id="fa0ca-111">否則，會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="fa0ca-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa0ca-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa0ca-112">Requirements</span></span>



| <span data-ttu-id="fa0ca-113">需求</span><span class="sxs-lookup"><span data-stu-id="fa0ca-113">Requirement</span></span> | <span data-ttu-id="fa0ca-114">值</span><span class="sxs-lookup"><span data-stu-id="fa0ca-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa0ca-115">標頭</span><span class="sxs-lookup"><span data-stu-id="fa0ca-115">Header</span></span><br/>  | <dl> <span data-ttu-id="fa0ca-116"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="fa0ca-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fa0ca-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="fa0ca-117">Library</span></span><br/> | <dl> <span data-ttu-id="fa0ca-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="fa0ca-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa0ca-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa0ca-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa0ca-120">**COARefTime 類別**</span><span class="sxs-lookup"><span data-stu-id="fa0ca-120">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




