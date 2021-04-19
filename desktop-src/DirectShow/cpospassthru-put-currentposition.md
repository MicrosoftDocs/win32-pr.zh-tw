---
description: Put \_ CurrentPosition 方法會設定目前的位置，相對於資料流程的總持續時間。 這個方法會實 IMediaPosition：:p 的 \_ CurrentPosition 方法。
ms.assetid: 22d7e9e4-47da-45b5-9be0-3c5128f90353
title: 'CPosPassThru.put_CurrentPosition 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_CurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85426636a34d0e197b36496d5a38a847c61b9501
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991020"
---
# <a name="cpospassthruput_currentposition-method"></a><span data-ttu-id="e4f81-104">CPosPassThru. put \_ CurrentPosition 方法</span><span class="sxs-lookup"><span data-stu-id="e4f81-104">CPosPassThru.put\_CurrentPosition method</span></span>

<span data-ttu-id="e4f81-105">`put_CurrentPosition`方法會設定目前的位置，相對於資料流程的總持續時間。</span><span class="sxs-lookup"><span data-stu-id="e4f81-105">The `put_CurrentPosition` method sets the current position, relative to the total duration of the stream.</span></span> <span data-ttu-id="e4f81-106">這個方法會實 [**IMediaPosition：:p 的 \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition) 方法。</span><span class="sxs-lookup"><span data-stu-id="e4f81-106">This method implements the [**IMediaPosition::put\_CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4f81-107">語法</span><span class="sxs-lookup"><span data-stu-id="e4f81-107">Syntax</span></span>


```C++
HRESULT put_CurrentPosition(
   REFTIME llTime
);
```



## <a name="parameters"></a><span data-ttu-id="e4f81-108">參數</span><span class="sxs-lookup"><span data-stu-id="e4f81-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4f81-109">*llTime*</span><span class="sxs-lookup"><span data-stu-id="e4f81-109">*llTime*</span></span> 
</dt> <dd>

<span data-ttu-id="e4f81-110">新位置（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e4f81-110">New position, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4f81-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e4f81-111">Return value</span></span>

<span data-ttu-id="e4f81-112">從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="e4f81-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4f81-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4f81-113">Requirements</span></span>



| <span data-ttu-id="e4f81-114">需求</span><span class="sxs-lookup"><span data-stu-id="e4f81-114">Requirement</span></span> | <span data-ttu-id="e4f81-115">值</span><span class="sxs-lookup"><span data-stu-id="e4f81-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4f81-116">標頭</span><span class="sxs-lookup"><span data-stu-id="e4f81-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e4f81-117"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e4f81-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e4f81-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="e4f81-118">Library</span></span><br/> | <dl> <span data-ttu-id="e4f81-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e4f81-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4f81-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e4f81-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4f81-121">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="e4f81-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




