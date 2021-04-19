---
description: Get \_ PrerollTime 方法會抓取在開始位置之前將排入佇列的資料量。 這個方法會實 IMediaPosition：： get \_ PrerollTime 方法。
ms.assetid: 37c12798-eb0d-4859-8b2e-52d6ae147863
title: 'CPosPassThru.get_PrerollTime 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_PrerollTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55cb2cc37a18c9ea00b4eb7115590f472b8d467e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992578"
---
# <a name="cpospassthruget_prerolltime-method"></a><span data-ttu-id="1b568-104">CPosPassThru. 取得 \_ PrerollTime 方法</span><span class="sxs-lookup"><span data-stu-id="1b568-104">CPosPassThru.get\_PrerollTime method</span></span>

<span data-ttu-id="1b568-105">`get_PrerollTime`方法會抓取在開始位置之前將排入佇列的資料量。</span><span class="sxs-lookup"><span data-stu-id="1b568-105">The `get_PrerollTime` method retrieves the amount of data that will be queued before the start position.</span></span> <span data-ttu-id="1b568-106">這個方法會實 [**IMediaPosition：： get \_ PrerollTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_prerolltime) 方法。</span><span class="sxs-lookup"><span data-stu-id="1b568-106">This method implements the [**IMediaPosition::get\_PrerollTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_prerolltime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b568-107">語法</span><span class="sxs-lookup"><span data-stu-id="1b568-107">Syntax</span></span>


```C++
HRESULT get_PrerollTime(
   REFTIME *pllTime
);
```



## <a name="parameters"></a><span data-ttu-id="1b568-108">參數</span><span class="sxs-lookup"><span data-stu-id="1b568-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b568-109">*pllTime*</span><span class="sxs-lookup"><span data-stu-id="1b568-109">*pllTime*</span></span> 
</dt> <dd>

<span data-ttu-id="1b568-110">變數的指標，此變數會接收預先計算的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="1b568-110">Pointer to a variable that receives the preroll time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b568-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1b568-111">Return value</span></span>

<span data-ttu-id="1b568-112">從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="1b568-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b568-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="1b568-113">Requirements</span></span>



| <span data-ttu-id="1b568-114">需求</span><span class="sxs-lookup"><span data-stu-id="1b568-114">Requirement</span></span> | <span data-ttu-id="1b568-115">值</span><span class="sxs-lookup"><span data-stu-id="1b568-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b568-116">標頭</span><span class="sxs-lookup"><span data-stu-id="1b568-116">Header</span></span><br/>  | <dl> <span data-ttu-id="1b568-117"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1b568-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1b568-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="1b568-118">Library</span></span><br/> | <dl> <span data-ttu-id="1b568-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="1b568-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b568-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1b568-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b568-121">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="1b568-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




