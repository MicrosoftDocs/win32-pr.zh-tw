---
description: 這個運算子會從另一個參考時間減去另一個參考時間。
ms.assetid: 5691cd76-0d25-45c0-bb58-6668abe1db01
title: COARefTime) 方法 (Ctlutil
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator-
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e51ee8aaed69830a498d1d22cebdc3927987f045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999346"
---
# <a name="coareftimeoperator--method"></a><span data-ttu-id="8c244-103">COARefTime 運算子-方法</span><span class="sxs-lookup"><span data-stu-id="8c244-103">COARefTime.operator- method</span></span>

<span data-ttu-id="8c244-104">這個運算子會從另一個參考時間減去另一個參考時間。</span><span class="sxs-lookup"><span data-stu-id="8c244-104">This operator subtracts one reference time from another.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c244-105">語法</span><span class="sxs-lookup"><span data-stu-id="8c244-105">Syntax</span></span>


```C++
COARefTime operator-(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="8c244-106">參數</span><span class="sxs-lookup"><span data-stu-id="8c244-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c244-107">*rt* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="8c244-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="8c244-108">要減去之 **COARefTime** 物件的參考。</span><span class="sxs-lookup"><span data-stu-id="8c244-108">Reference to the **COARefTime** object to subtract.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c244-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="8c244-109">Return value</span></span>

<span data-ttu-id="8c244-110">傳回等於參考時間差異的新 **COARefTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="8c244-110">Returns a new **COARefTime** object equal to the difference of the reference times.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c244-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c244-111">Requirements</span></span>



| <span data-ttu-id="8c244-112">需求</span><span class="sxs-lookup"><span data-stu-id="8c244-112">Requirement</span></span> | <span data-ttu-id="8c244-113">值</span><span class="sxs-lookup"><span data-stu-id="8c244-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c244-114">標頭</span><span class="sxs-lookup"><span data-stu-id="8c244-114">Header</span></span><br/>  | <dl> <span data-ttu-id="8c244-115"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="8c244-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8c244-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="8c244-116">Library</span></span><br/> | <dl> <span data-ttu-id="8c244-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8c244-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c244-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c244-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c244-119">**COARefTime 類別**</span><span class="sxs-lookup"><span data-stu-id="8c244-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




