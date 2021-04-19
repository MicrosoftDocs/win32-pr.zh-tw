---
description: GetPreroll 方法會抓取在開始位置之前將排入佇列的資料量。 這個方法會實 IMediaSeeking：： GetPreroll 方法。
ms.assetid: b00de2fa-ba3c-4a16-ad67-adf3df52ef9a
title: 'CPosPassThru. GetPreroll 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e72d7c83c8cdb0fa08a4b395fd65c80edbe3fb05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997714"
---
# <a name="cpospassthrugetpreroll-method"></a><span data-ttu-id="d5b5e-104">CPosPassThru. GetPreroll 方法</span><span class="sxs-lookup"><span data-stu-id="d5b5e-104">CPosPassThru.GetPreroll method</span></span>

<span data-ttu-id="d5b5e-105">`GetPreroll`方法會抓取在開始位置之前將排入佇列的資料量。</span><span class="sxs-lookup"><span data-stu-id="d5b5e-105">The `GetPreroll` method retrieves the amount of data that will be queued before the start position.</span></span> <span data-ttu-id="d5b5e-106">這個方法會實 [**IMediaSeeking：： GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) 方法。</span><span class="sxs-lookup"><span data-stu-id="d5b5e-106">This method implements the [**IMediaSeeking::GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5b5e-107">語法</span><span class="sxs-lookup"><span data-stu-id="d5b5e-107">Syntax</span></span>


```C++
HRESULT GetPreroll(
   LONGLONG *pllPreroll
);
```



## <a name="parameters"></a><span data-ttu-id="d5b5e-108">參數</span><span class="sxs-lookup"><span data-stu-id="d5b5e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5b5e-109">*pllPreroll*</span><span class="sxs-lookup"><span data-stu-id="d5b5e-109">*pllPreroll*</span></span> 
</dt> <dd>

<span data-ttu-id="d5b5e-110">變數的指標，此變數會接收預先計算的時間，以目前時間格式的單位為單位。</span><span class="sxs-lookup"><span data-stu-id="d5b5e-110">Pointer to a variable that receives the preroll time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5b5e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d5b5e-111">Return value</span></span>

<span data-ttu-id="d5b5e-112">從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="d5b5e-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5b5e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5b5e-113">Requirements</span></span>



| <span data-ttu-id="d5b5e-114">需求</span><span class="sxs-lookup"><span data-stu-id="d5b5e-114">Requirement</span></span> | <span data-ttu-id="d5b5e-115">值</span><span class="sxs-lookup"><span data-stu-id="d5b5e-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5b5e-116">標頭</span><span class="sxs-lookup"><span data-stu-id="d5b5e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d5b5e-117"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d5b5e-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d5b5e-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="d5b5e-118">Library</span></span><br/> | <dl> <span data-ttu-id="d5b5e-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d5b5e-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5b5e-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5b5e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5b5e-121">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="d5b5e-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




