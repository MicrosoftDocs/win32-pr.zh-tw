---
description: CTransformOutputPin. QueryId 方法-QueryId 方法會抓取 pin 的識別碼。 這個方法會實 IPin：： QueryId 方法。
ms.assetid: 3d83db3a-b919-454d-a91a-91f33a952a22
title: 'CTransformOutputPin. QueryId 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d4c2d222ca4dd184adfe41f9f610b10f15ee9f02
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094846"
---
# <a name="ctransformoutputpinqueryid-method"></a><span data-ttu-id="b6bfd-104">CTransformOutputPin. QueryId 方法</span><span class="sxs-lookup"><span data-stu-id="b6bfd-104">CTransformOutputPin.QueryId method</span></span>

<span data-ttu-id="b6bfd-105">方法會抓取 `QueryId` pin 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b6bfd-105">The `QueryId` method retrieves an identifier for the pin.</span></span> <span data-ttu-id="b6bfd-106">這個方法會實 [**IPin：： QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) 方法。</span><span class="sxs-lookup"><span data-stu-id="b6bfd-106">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6bfd-107">語法</span><span class="sxs-lookup"><span data-stu-id="b6bfd-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="b6bfd-108">參數</span><span class="sxs-lookup"><span data-stu-id="b6bfd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6bfd-109">*識別碼*</span><span class="sxs-lookup"><span data-stu-id="b6bfd-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="b6bfd-110">接收包含 pin 識別碼的字串。</span><span class="sxs-lookup"><span data-stu-id="b6bfd-110">Receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6bfd-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b6bfd-111">Return value</span></span>

<span data-ttu-id="b6bfd-112">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="b6bfd-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="b6bfd-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b6bfd-113">Return code</span></span>                                                                                   | <span data-ttu-id="b6bfd-114">Description</span><span class="sxs-lookup"><span data-stu-id="b6bfd-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="b6bfd-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="b6bfd-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b6bfd-116">Success</span><span class="sxs-lookup"><span data-stu-id="b6bfd-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="b6bfd-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b6bfd-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b6bfd-118">記憶體不足</span><span class="sxs-lookup"><span data-stu-id="b6bfd-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="b6bfd-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="b6bfd-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b6bfd-120">**Null** 指標引數</span><span class="sxs-lookup"><span data-stu-id="b6bfd-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b6bfd-121">備註</span><span class="sxs-lookup"><span data-stu-id="b6bfd-121">Remarks</span></span>

<span data-ttu-id="b6bfd-122">Pin 識別碼會用於圖形持續性。</span><span class="sxs-lookup"><span data-stu-id="b6bfd-122">The pin identifier is used for graph persistence.</span></span> <span data-ttu-id="b6bfd-123">此類別的 pin 識別碼為 Out。這個類別會覆寫 [**CBasePin**](cbasepin.md) 類別的行為。</span><span class="sxs-lookup"><span data-stu-id="b6bfd-123">The pin identifier for this class is Out. This class overrides the behavior of the [**CBasePin**](cbasepin.md) class.</span></span> <span data-ttu-id="b6bfd-124">在 **CBasePin** 類別中，pin 識別碼與在類別的函式中指定的 pin 碼名稱相同。</span><span class="sxs-lookup"><span data-stu-id="b6bfd-124">In the **CBasePin** class, the pin identifier is the same as the pin name, specified in the class constructor.</span></span> <span data-ttu-id="b6bfd-125">在 **CTransformInputPin** 類別中，pin 識別碼和 pin 名稱不相同。</span><span class="sxs-lookup"><span data-stu-id="b6bfd-125">In the **CTransformInputPin** class, the pin identifier and the pin name are not the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6bfd-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6bfd-126">Requirements</span></span>



| <span data-ttu-id="b6bfd-127">需求</span><span class="sxs-lookup"><span data-stu-id="b6bfd-127">Requirement</span></span> | <span data-ttu-id="b6bfd-128">值</span><span class="sxs-lookup"><span data-stu-id="b6bfd-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6bfd-129">標頭</span><span class="sxs-lookup"><span data-stu-id="b6bfd-129">Header</span></span><br/>  | <dl> <span data-ttu-id="b6bfd-130"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b6bfd-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b6bfd-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="b6bfd-131">Library</span></span><br/> | <dl> <span data-ttu-id="b6bfd-132"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b6bfd-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




