---
description: FindPinNumber 方法會抓取篩選上指定的 pin 數目。
ms.assetid: c9366fcc-7b13-4e43-883e-6003c32fadec
title: 'CSource. FindPinNumber 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPinNumber
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6a71c65efd97c48eed58fb7d0b5aa8fcc2f178e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982076"
---
# <a name="csourcefindpinnumber-method"></a><span data-ttu-id="8c9d3-103">CSource. FindPinNumber 方法</span><span class="sxs-lookup"><span data-stu-id="8c9d3-103">CSource.FindPinNumber method</span></span>

<span data-ttu-id="8c9d3-104">方法會抓取 `FindPinNumber` 篩選上指定的 pin 數目。</span><span class="sxs-lookup"><span data-stu-id="8c9d3-104">The `FindPinNumber` method retrieves the number of a specified pin on the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c9d3-105">語法</span><span class="sxs-lookup"><span data-stu-id="8c9d3-105">Syntax</span></span>


```C++
int FindPinNumber(
   IPin *iPin
);
```



## <a name="parameters"></a><span data-ttu-id="8c9d3-106">參數</span><span class="sxs-lookup"><span data-stu-id="8c9d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c9d3-107">*iPin*</span><span class="sxs-lookup"><span data-stu-id="8c9d3-107">*iPin*</span></span> 
</dt> <dd>

<span data-ttu-id="8c9d3-108">釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="8c9d3-108">Pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c9d3-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="8c9d3-109">Return value</span></span>

<span data-ttu-id="8c9d3-110">傳回 pin 碼，如果在此篩選器上找不到 pin，則傳回1。</span><span class="sxs-lookup"><span data-stu-id="8c9d3-110">Returns the pin number, or  1 if the pin is not found on this filter.</span></span> <span data-ttu-id="8c9d3-111">第一個 pin 的編號為零。</span><span class="sxs-lookup"><span data-stu-id="8c9d3-111">The first pin is numbered zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c9d3-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c9d3-112">Requirements</span></span>



| <span data-ttu-id="8c9d3-113">需求</span><span class="sxs-lookup"><span data-stu-id="8c9d3-113">Requirement</span></span> | <span data-ttu-id="8c9d3-114">值</span><span class="sxs-lookup"><span data-stu-id="8c9d3-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c9d3-115">標頭</span><span class="sxs-lookup"><span data-stu-id="8c9d3-115">Header</span></span><br/>  | <dl> <span data-ttu-id="8c9d3-116"><dt>來源 .h (包含) 的資料流程 </dt></span><span class="sxs-lookup"><span data-stu-id="8c9d3-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="8c9d3-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="8c9d3-117">Library</span></span><br/> | <dl> <span data-ttu-id="8c9d3-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8c9d3-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c9d3-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c9d3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c9d3-120">**CSource 類別**</span><span class="sxs-lookup"><span data-stu-id="8c9d3-120">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




