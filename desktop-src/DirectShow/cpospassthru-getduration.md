---
description: GetDuration 方法會捕獲資料流程的持續時間。 這個方法會實 IMediaSeeking：： GetDuration 方法。
ms.assetid: 0552e7bb-4d7e-40a8-a8ad-89ae6fff8ccb
title: 'CPosPassThru. GetDuration 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9b533537c36ac7ec4c76289307368539482aa47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977148"
---
# <a name="cpospassthrugetduration-method"></a><span data-ttu-id="9b13b-104">CPosPassThru. GetDuration 方法</span><span class="sxs-lookup"><span data-stu-id="9b13b-104">CPosPassThru.GetDuration method</span></span>

<span data-ttu-id="9b13b-105">`GetDuration`方法會捕獲資料流程的持續時間。</span><span class="sxs-lookup"><span data-stu-id="9b13b-105">The `GetDuration` method retrieves the duration of the stream.</span></span> <span data-ttu-id="9b13b-106">這個方法會實 [**IMediaSeeking：： GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) 方法。</span><span class="sxs-lookup"><span data-stu-id="9b13b-106">This method implements the [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b13b-107">語法</span><span class="sxs-lookup"><span data-stu-id="9b13b-107">Syntax</span></span>


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="9b13b-108">參數</span><span class="sxs-lookup"><span data-stu-id="9b13b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b13b-109">*pDuration*</span><span class="sxs-lookup"><span data-stu-id="9b13b-109">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="9b13b-110">接收持續時間之變數的指標，以目前時間格式的單位為單位。</span><span class="sxs-lookup"><span data-stu-id="9b13b-110">Pointer to a variable that receives the duration, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b13b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9b13b-111">Return value</span></span>

<span data-ttu-id="9b13b-112">從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="9b13b-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b13b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b13b-113">Requirements</span></span>



| <span data-ttu-id="9b13b-114">需求</span><span class="sxs-lookup"><span data-stu-id="9b13b-114">Requirement</span></span> | <span data-ttu-id="9b13b-115">值</span><span class="sxs-lookup"><span data-stu-id="9b13b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b13b-116">標頭</span><span class="sxs-lookup"><span data-stu-id="9b13b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="9b13b-117"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9b13b-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9b13b-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="9b13b-118">Library</span></span><br/> | <dl> <span data-ttu-id="9b13b-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9b13b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b13b-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b13b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b13b-121">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="9b13b-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




