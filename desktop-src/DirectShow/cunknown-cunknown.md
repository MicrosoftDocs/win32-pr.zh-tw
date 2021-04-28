---
description: CUnknown。 CUnknown 函式-函數方法。
ms.assetid: dafe0d5c-b4c8-4efb-8c47-a8c5db6e8aed
title: 'CUnknown. CUnknown (Combase. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.CUnknown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32859871f8ef69ce357fe204f0741356314fbb06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084606"
---
# <a name="cunknowncunknown-constructor"></a><span data-ttu-id="07d0b-103">CUnknown. CUnknown 函數</span><span class="sxs-lookup"><span data-stu-id="07d0b-103">CUnknown.CUnknown constructor</span></span>

<span data-ttu-id="07d0b-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="07d0b-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="07d0b-105">語法</span><span class="sxs-lookup"><span data-stu-id="07d0b-105">Syntax</span></span>


```C++
CUnknown(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="07d0b-106">參數</span><span class="sxs-lookup"><span data-stu-id="07d0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07d0b-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="07d0b-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="07d0b-108">包含物件名稱的字串;用於 [**CBaseObject**](cbaseobject.md) 的函式以進行調試。</span><span class="sxs-lookup"><span data-stu-id="07d0b-108">String containing the name of the object; used in the [**CBaseObject**](cbaseobject.md) constructor for debugging.</span></span>

</dd> <dt>

<span data-ttu-id="07d0b-109">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="07d0b-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="07d0b-110">這個物件之擁有者的指標。</span><span class="sxs-lookup"><span data-stu-id="07d0b-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="07d0b-111">如果物件已匯總，請將指標傳遞至匯總物件的 IUnknown 介面。</span><span class="sxs-lookup"><span data-stu-id="07d0b-111">If the object is aggregated, pass a pointer to the aggregating object's IUnknown interface.</span></span> <span data-ttu-id="07d0b-112">否則，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="07d0b-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07d0b-113">備註</span><span class="sxs-lookup"><span data-stu-id="07d0b-113">Remarks</span></span>

<span data-ttu-id="07d0b-114">以零的參考計數來初始化物件。</span><span class="sxs-lookup"><span data-stu-id="07d0b-114">The object is initialized with a reference count of zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="07d0b-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="07d0b-115">Requirements</span></span>



| <span data-ttu-id="07d0b-116">需求</span><span class="sxs-lookup"><span data-stu-id="07d0b-116">Requirement</span></span> | <span data-ttu-id="07d0b-117">值</span><span class="sxs-lookup"><span data-stu-id="07d0b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07d0b-118">標頭</span><span class="sxs-lookup"><span data-stu-id="07d0b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="07d0b-119"><dt>Combase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="07d0b-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="07d0b-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="07d0b-120">Library</span></span><br/> | <dl> <span data-ttu-id="07d0b-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="07d0b-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




