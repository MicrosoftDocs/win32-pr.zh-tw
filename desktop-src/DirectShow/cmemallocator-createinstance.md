---
description: CreateInstance 方法會建立 CMemAllocator 類別的新實例。
ms.assetid: 87a831a4-2414-4240-8448-c5d90f130470
title: CMemAllocator (Amfilter) 的 CreateInstance 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ef85de95db74e8a9d7aa6a7b1ba977620a29826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993322"
---
# <a name="cmemallocatorcreateinstance-method"></a><span data-ttu-id="b2761-103">CMemAllocator CreateInstance 方法</span><span class="sxs-lookup"><span data-stu-id="b2761-103">CMemAllocator.CreateInstance method</span></span>

<span data-ttu-id="b2761-104">`CreateInstance`方法會建立 **CMemAllocator** 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="b2761-104">The `CreateInstance` method creates a new instance of the **CMemAllocator** class.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2761-105">語法</span><span class="sxs-lookup"><span data-stu-id="b2761-105">Syntax</span></span>


```C++
static CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="b2761-106">參數</span><span class="sxs-lookup"><span data-stu-id="b2761-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2761-107">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="b2761-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="b2761-108">這個物件之擁有者的指標。</span><span class="sxs-lookup"><span data-stu-id="b2761-108">Pointer to the owner of this object.</span></span> <span data-ttu-id="b2761-109">如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="b2761-109">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="b2761-110">否則，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b2761-110">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b2761-111">*phr*</span><span class="sxs-lookup"><span data-stu-id="b2761-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="b2761-112">變數的指標，此變數會接收 **HRESULT** 值，指出方法的成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="b2761-112">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2761-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b2761-113">Return value</span></span>

<span data-ttu-id="b2761-114">傳回新的 **CMemAllocator** 物件的指標，其類型為 **CUnknown** 物件。</span><span class="sxs-lookup"><span data-stu-id="b2761-114">Returns a pointer to a new **CMemAllocator** object, typed as a **CUnknown** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2761-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2761-115">Requirements</span></span>



| <span data-ttu-id="b2761-116">需求</span><span class="sxs-lookup"><span data-stu-id="b2761-116">Requirement</span></span> | <span data-ttu-id="b2761-117">值</span><span class="sxs-lookup"><span data-stu-id="b2761-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2761-118">標頭</span><span class="sxs-lookup"><span data-stu-id="b2761-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b2761-119"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b2761-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b2761-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="b2761-120">Library</span></span><br/> | <dl> <span data-ttu-id="b2761-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b2761-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2761-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2761-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2761-123">**CMemAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="b2761-123">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




