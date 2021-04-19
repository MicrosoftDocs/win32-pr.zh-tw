---
description: CreateInstance 方法會呼叫類別的物件建立函數。
ms.assetid: 8a7d5c56-867d-432d-a0c2-97b8e3cf8a69
title: CFactoryTemplate (Combase) 的 CreateInstance 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0f67ba528943bc2a468419fc84db44359745d4a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995357"
---
# <a name="cfactorytemplatecreateinstance-method"></a><span data-ttu-id="55380-103">CFactoryTemplate CreateInstance 方法</span><span class="sxs-lookup"><span data-stu-id="55380-103">CFactoryTemplate.CreateInstance method</span></span>

<span data-ttu-id="55380-104">`CreateInstance`方法會呼叫類別的物件建立函數。</span><span class="sxs-lookup"><span data-stu-id="55380-104">The `CreateInstance` method calls the object-creation function for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="55380-105">語法</span><span class="sxs-lookup"><span data-stu-id="55380-105">Syntax</span></span>


```C++
CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="55380-106">參數</span><span class="sxs-lookup"><span data-stu-id="55380-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55380-107">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="55380-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="55380-108">匯總 **IUnknown** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="55380-108">Pointer to the aggregating **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="55380-109">*phr*</span><span class="sxs-lookup"><span data-stu-id="55380-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="55380-110">變數的指標，此變數會接收 **HRESULT** 值，指出方法的成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="55380-110">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55380-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="55380-111">Return value</span></span>

<span data-ttu-id="55380-112">傳回類別物件的實例。</span><span class="sxs-lookup"><span data-stu-id="55380-112">Returns an instance of the class object.</span></span>

## <a name="remarks"></a><span data-ttu-id="55380-113">備註</span><span class="sxs-lookup"><span data-stu-id="55380-113">Remarks</span></span>

<span data-ttu-id="55380-114">**IClassFactory：： CreateInstance** 方法會呼叫這個類別方法。</span><span class="sxs-lookup"><span data-stu-id="55380-114">The **IClassFactory::CreateInstance** method calls this class method.</span></span> <span data-ttu-id="55380-115">這個方法會呼叫 [**CFactoryTemplate：： m \_ lpfnNew**](cfactorytemplate-m-lpfnnew.md) 成員變數所指向的函式。</span><span class="sxs-lookup"><span data-stu-id="55380-115">This method calls the function pointed to by the [**CFactoryTemplate::m\_lpfnNew**](cfactorytemplate-m-lpfnnew.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="55380-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="55380-116">Requirements</span></span>



| <span data-ttu-id="55380-117">需求</span><span class="sxs-lookup"><span data-stu-id="55380-117">Requirement</span></span> | <span data-ttu-id="55380-118">值</span><span class="sxs-lookup"><span data-stu-id="55380-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55380-119">標頭</span><span class="sxs-lookup"><span data-stu-id="55380-119">Header</span></span><br/>  | <dl> <span data-ttu-id="55380-120"><dt>Combase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="55380-120"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="55380-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="55380-121">Library</span></span><br/> | <dl> <span data-ttu-id="55380-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="55380-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55380-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55380-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55380-124">**CFactoryTemplate 類別**</span><span class="sxs-lookup"><span data-stu-id="55380-124">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




