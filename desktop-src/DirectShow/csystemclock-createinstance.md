---
description: CreateInstance 方法會建立這個物件的新實例。
ms.assetid: 5c62f781-0f22-4d8f-8517-272405dd07c5
title: CSystemClock (Sysclock) 的 CreateInstance 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 264997448aea028c5725d207ce4b301d369a092c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979479"
---
# <a name="csystemclockcreateinstance-method"></a><span data-ttu-id="a531a-103">CSystemClock CreateInstance 方法</span><span class="sxs-lookup"><span data-stu-id="a531a-103">CSystemClock.CreateInstance method</span></span>

<span data-ttu-id="a531a-104">`CreateInstance`方法會建立這個物件的新實例。</span><span class="sxs-lookup"><span data-stu-id="a531a-104">The `CreateInstance` method creates a new instance of this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a531a-105">語法</span><span class="sxs-lookup"><span data-stu-id="a531a-105">Syntax</span></span>


```C++
static CUnknown* WINAPI CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="a531a-106">參數</span><span class="sxs-lookup"><span data-stu-id="a531a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a531a-107">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="a531a-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="a531a-108">匯總 **IUnknown** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="a531a-108">Pointer to the aggregating **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="a531a-109">*phr*</span><span class="sxs-lookup"><span data-stu-id="a531a-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="a531a-110">變數的指標，此變數會接收 **HRESULT** 值，指出方法的成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="a531a-110">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a531a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a531a-111">Return value</span></span>

<span data-ttu-id="a531a-112">傳回這個物件之新實例的指標。</span><span class="sxs-lookup"><span data-stu-id="a531a-112">Returns a pointer to a new instance of this object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a531a-113">備註</span><span class="sxs-lookup"><span data-stu-id="a531a-113">Remarks</span></span>

<span data-ttu-id="a531a-114">Class factory 會呼叫這個方法來建立物件。</span><span class="sxs-lookup"><span data-stu-id="a531a-114">The class factory calls this method to create the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="a531a-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="a531a-115">Requirements</span></span>



| <span data-ttu-id="a531a-116">需求</span><span class="sxs-lookup"><span data-stu-id="a531a-116">Requirement</span></span> | <span data-ttu-id="a531a-117">值</span><span class="sxs-lookup"><span data-stu-id="a531a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a531a-118">標頭</span><span class="sxs-lookup"><span data-stu-id="a531a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a531a-119"><dt>Sysclock (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a531a-119"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a531a-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="a531a-120">Library</span></span><br/> | <dl> <span data-ttu-id="a531a-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a531a-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




