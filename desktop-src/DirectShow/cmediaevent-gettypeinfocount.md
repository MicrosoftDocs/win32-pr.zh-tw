---
description: 抓取物件所提供的類型資訊介面數目。
ms.assetid: e16bc324-bb49-4df2-afeb-2c2cd1620693
title: 'CMediaEvent. GetTypeInfoCount 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4de7a79251f2d25c1c55642050ad06513a1bfe6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990159"
---
# <a name="cmediaeventgettypeinfocount-method"></a><span data-ttu-id="f853f-103">CMediaEvent. GetTypeInfoCount 方法</span><span class="sxs-lookup"><span data-stu-id="f853f-103">CMediaEvent.GetTypeInfoCount method</span></span>

<span data-ttu-id="f853f-104">抓取物件所提供的類型資訊介面數目。</span><span class="sxs-lookup"><span data-stu-id="f853f-104">Retrieves the number of type-information interfaces provided by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f853f-105">語法</span><span class="sxs-lookup"><span data-stu-id="f853f-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="f853f-106">參數</span><span class="sxs-lookup"><span data-stu-id="f853f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f853f-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="f853f-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="f853f-108">物件提供的類型資訊介面數目的指標。</span><span class="sxs-lookup"><span data-stu-id="f853f-108">Pointer to number of type-information interfaces that the object provides.</span></span> <span data-ttu-id="f853f-109">如果物件提供型別資訊，這個數位就是 1;否則，此數目為0。</span><span class="sxs-lookup"><span data-stu-id="f853f-109">If the object provides type information, this number is 1; otherwise, the number is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f853f-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="f853f-110">Return value</span></span>

<span data-ttu-id="f853f-111">\_如果 *pctinfo* 無效，則傳回 E 指標，否則傳回 S \_ 。</span><span class="sxs-lookup"><span data-stu-id="f853f-111">Returns E\_POINTER if *pctinfo* is invalid; otherwise, returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="f853f-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="f853f-112">Requirements</span></span>



| <span data-ttu-id="f853f-113">需求</span><span class="sxs-lookup"><span data-stu-id="f853f-113">Requirement</span></span> | <span data-ttu-id="f853f-114">值</span><span class="sxs-lookup"><span data-stu-id="f853f-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f853f-115">標頭</span><span class="sxs-lookup"><span data-stu-id="f853f-115">Header</span></span><br/>  | <dl> <span data-ttu-id="f853f-116"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f853f-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f853f-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="f853f-117">Library</span></span><br/> | <dl> <span data-ttu-id="f853f-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f853f-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f853f-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f853f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f853f-120">**CMediaEvent 類別**</span><span class="sxs-lookup"><span data-stu-id="f853f-120">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




