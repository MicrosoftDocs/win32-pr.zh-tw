---
description: 函式方法。
ms.assetid: 2340b39a-cab6-4524-b8cd-b22d4bdd24d0
title: 'CMemAllocator. CMemAllocator (Amfilter. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b650e23761c3fe5b3f5014666f90c679f088c4a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989790"
---
# <a name="cmemallocatorcmemallocator-constructor"></a><span data-ttu-id="075c9-103">CMemAllocator. CMemAllocator 函數</span><span class="sxs-lookup"><span data-stu-id="075c9-103">CMemAllocator.CMemAllocator constructor</span></span>

<span data-ttu-id="075c9-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="075c9-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="075c9-105">語法</span><span class="sxs-lookup"><span data-stu-id="075c9-105">Syntax</span></span>


```C++
CMemAllocator(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="075c9-106">參數</span><span class="sxs-lookup"><span data-stu-id="075c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="075c9-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="075c9-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="075c9-108">包含配置器名稱之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="075c9-108">Pointer to a string containing the name of the allocator.</span></span>

</dd> <dt>

<span data-ttu-id="075c9-109">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="075c9-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="075c9-110">這個物件之擁有者的指標。</span><span class="sxs-lookup"><span data-stu-id="075c9-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="075c9-111">如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="075c9-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="075c9-112">否則，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="075c9-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="075c9-113">*phr*</span><span class="sxs-lookup"><span data-stu-id="075c9-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="075c9-114">變數的指標，此變數會接收 **HRESULT** 值，指出方法的成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="075c9-114">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="075c9-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="075c9-115">Requirements</span></span>



| <span data-ttu-id="075c9-116">需求</span><span class="sxs-lookup"><span data-stu-id="075c9-116">Requirement</span></span> | <span data-ttu-id="075c9-117">值</span><span class="sxs-lookup"><span data-stu-id="075c9-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="075c9-118">標頭</span><span class="sxs-lookup"><span data-stu-id="075c9-118">Header</span></span><br/>  | <dl> <span data-ttu-id="075c9-119"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="075c9-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="075c9-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="075c9-120">Library</span></span><br/> | <dl> <span data-ttu-id="075c9-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="075c9-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="075c9-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="075c9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="075c9-123">**CMemAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="075c9-123">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




