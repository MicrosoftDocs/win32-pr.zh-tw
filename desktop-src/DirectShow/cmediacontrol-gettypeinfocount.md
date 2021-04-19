---
description: 抓取物件所提供的類型資訊介面數目。
ms.assetid: 29575325-8f97-4f39-8272-86a917d9144f
title: 'CMediaControl. GetTypeInfoCount 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2454e503a045a02db20c0dc457b6367f6d3b427
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000960"
---
# <a name="cmediacontrolgettypeinfocount-method"></a><span data-ttu-id="08f1c-103">CMediaControl. GetTypeInfoCount 方法</span><span class="sxs-lookup"><span data-stu-id="08f1c-103">CMediaControl.GetTypeInfoCount method</span></span>

<span data-ttu-id="08f1c-104">抓取物件所提供的類型資訊介面數目。</span><span class="sxs-lookup"><span data-stu-id="08f1c-104">Retrieves the number of type-information interfaces provided by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="08f1c-105">語法</span><span class="sxs-lookup"><span data-stu-id="08f1c-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="08f1c-106">參數</span><span class="sxs-lookup"><span data-stu-id="08f1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08f1c-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="08f1c-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="08f1c-108">物件提供的類型資訊介面數目的指標。</span><span class="sxs-lookup"><span data-stu-id="08f1c-108">Pointer to the number of type-information interfaces that the object provides.</span></span> <span data-ttu-id="08f1c-109">如果物件提供型別資訊，這個數位就是 1;否則，此數目為0。</span><span class="sxs-lookup"><span data-stu-id="08f1c-109">If the object provides type information, this number is 1; otherwise, the number is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08f1c-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="08f1c-110">Return value</span></span>

<span data-ttu-id="08f1c-111">\_如果 *pctinfo* 無效，則傳回 E 指標，否則傳回 S \_ 。</span><span class="sxs-lookup"><span data-stu-id="08f1c-111">Returns E\_POINTER if *pctinfo* is invalid; otherwise, returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="08f1c-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="08f1c-112">Requirements</span></span>



| <span data-ttu-id="08f1c-113">需求</span><span class="sxs-lookup"><span data-stu-id="08f1c-113">Requirement</span></span> | <span data-ttu-id="08f1c-114">值</span><span class="sxs-lookup"><span data-stu-id="08f1c-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08f1c-115">標頭</span><span class="sxs-lookup"><span data-stu-id="08f1c-115">Header</span></span><br/>  | <dl> <span data-ttu-id="08f1c-116"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="08f1c-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="08f1c-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="08f1c-117">Library</span></span><br/> | <dl> <span data-ttu-id="08f1c-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="08f1c-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08f1c-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08f1c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08f1c-120">**CMediaControl 類別**</span><span class="sxs-lookup"><span data-stu-id="08f1c-120">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




