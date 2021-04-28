---
description: CTransformInputPin. QueryId 方法-QueryId 方法會抓取 pin 的識別碼。 這個方法會實 IPin：： QueryId 方法。
ms.assetid: 91fde383-0288-4307-9ca8-e117b6111769
title: 'CTransformInputPin. QueryId 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8407e649814fcb12f699c2362f0f89137e941d19
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095006"
---
# <a name="ctransforminputpinqueryid-method"></a><span data-ttu-id="484ae-104">CTransformInputPin. QueryId 方法</span><span class="sxs-lookup"><span data-stu-id="484ae-104">CTransformInputPin.QueryId method</span></span>

<span data-ttu-id="484ae-105">方法會抓取 `QueryId` pin 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="484ae-105">The `QueryId` method retrieves an identifier for the pin.</span></span> <span data-ttu-id="484ae-106">這個方法會實 [**IPin：： QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) 方法。</span><span class="sxs-lookup"><span data-stu-id="484ae-106">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="484ae-107">語法</span><span class="sxs-lookup"><span data-stu-id="484ae-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="484ae-108">參數</span><span class="sxs-lookup"><span data-stu-id="484ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="484ae-109">*識別碼*</span><span class="sxs-lookup"><span data-stu-id="484ae-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="484ae-110">接收包含 pin 識別碼的字串。</span><span class="sxs-lookup"><span data-stu-id="484ae-110">Receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="484ae-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="484ae-111">Return value</span></span>

<span data-ttu-id="484ae-112">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="484ae-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="484ae-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="484ae-113">Return code</span></span>                                                                                   | <span data-ttu-id="484ae-114">Description</span><span class="sxs-lookup"><span data-stu-id="484ae-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="484ae-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="484ae-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="484ae-116">Success</span><span class="sxs-lookup"><span data-stu-id="484ae-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="484ae-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="484ae-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="484ae-118">記憶體不足</span><span class="sxs-lookup"><span data-stu-id="484ae-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="484ae-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="484ae-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="484ae-120">**Null** 指標引數</span><span class="sxs-lookup"><span data-stu-id="484ae-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="484ae-121">備註</span><span class="sxs-lookup"><span data-stu-id="484ae-121">Remarks</span></span>

<span data-ttu-id="484ae-122">Pin 識別碼會用於圖形持續性。</span><span class="sxs-lookup"><span data-stu-id="484ae-122">The pin identifier is used for graph persistence.</span></span> <span data-ttu-id="484ae-123">此類別的 pin 識別碼在中。</span><span class="sxs-lookup"><span data-stu-id="484ae-123">The pin identifier for this class is In.</span></span> <span data-ttu-id="484ae-124">這個類別會覆寫 [**CBasePin**](cbasepin.md) 類別的行為。</span><span class="sxs-lookup"><span data-stu-id="484ae-124">This class overrides the behavior of the [**CBasePin**](cbasepin.md) class.</span></span> <span data-ttu-id="484ae-125">在 **CBasePin** 類別中，pin 識別碼與在類別的函式中指定的 pin 碼名稱相同。</span><span class="sxs-lookup"><span data-stu-id="484ae-125">In the **CBasePin** class, the pin identifier is the same as the pin name, specified in the class constructor.</span></span> <span data-ttu-id="484ae-126">在 **CTransformInputPin** 類別中，pin 識別碼和 pin 名稱不相同。</span><span class="sxs-lookup"><span data-stu-id="484ae-126">In the **CTransformInputPin** class, the pin identifier and the pin name are not the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="484ae-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="484ae-127">Requirements</span></span>



| <span data-ttu-id="484ae-128">需求</span><span class="sxs-lookup"><span data-stu-id="484ae-128">Requirement</span></span> | <span data-ttu-id="484ae-129">值</span><span class="sxs-lookup"><span data-stu-id="484ae-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="484ae-130">標頭</span><span class="sxs-lookup"><span data-stu-id="484ae-130">Header</span></span><br/>  | <dl> <span data-ttu-id="484ae-131"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="484ae-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="484ae-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="484ae-132">Library</span></span><br/> | <dl> <span data-ttu-id="484ae-133"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="484ae-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




