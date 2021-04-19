---
description: GetInterface 函式會捕獲介面指標。
ms.assetid: 75fe8849-c779-4d47-a5ff-5a23308c8a21
title: 'GetInterface 函式 (Combase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetInterface
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 317f08af2a4ff0e9410c61da8b19d14735a14f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979502"
---
# <a name="getinterface-function"></a><span data-ttu-id="206a8-103">GetInterface 函式</span><span class="sxs-lookup"><span data-stu-id="206a8-103">GetInterface function</span></span>

<span data-ttu-id="206a8-104">函 `GetInterface` 式會捕獲介面指標。</span><span class="sxs-lookup"><span data-stu-id="206a8-104">The `GetInterface` function retrieves an interface pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="206a8-105">語法</span><span class="sxs-lookup"><span data-stu-id="206a8-105">Syntax</span></span>


```C++
HRESULT GetInterface(
   LPUNKNOWN pUnk,
   void      **ppv
);
```



## <a name="parameters"></a><span data-ttu-id="206a8-106">參數</span><span class="sxs-lookup"><span data-stu-id="206a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="206a8-107">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="206a8-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="206a8-108">**IUnknown** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="206a8-108">Pointer to the **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="206a8-109">*Ppv*</span><span class="sxs-lookup"><span data-stu-id="206a8-109">*ppv*</span></span> 
</dt> <dd>

<span data-ttu-id="206a8-110">已抓取介面之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="206a8-110">Address of a pointer to the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="206a8-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="206a8-111">Return value</span></span>

<span data-ttu-id="206a8-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="206a8-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="206a8-113">備註</span><span class="sxs-lookup"><span data-stu-id="206a8-113">Remarks</span></span>

<span data-ttu-id="206a8-114">此成員函式會執行參考計數的安全線程增量。</span><span class="sxs-lookup"><span data-stu-id="206a8-114">This member function performs a thread-safe increment of the reference count.</span></span> <span data-ttu-id="206a8-115">若要取出介面並加入參考，請從 **INonDelegatingUnknown：： NonDelegatingQueryInterface** 方法的覆寫執行呼叫這個函式。</span><span class="sxs-lookup"><span data-stu-id="206a8-115">To retrieve the interface and add a reference, call this function from your overriding implementation of the **INonDelegatingUnknown::NonDelegatingQueryInterface** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="206a8-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="206a8-116">Requirements</span></span>



| <span data-ttu-id="206a8-117">需求</span><span class="sxs-lookup"><span data-stu-id="206a8-117">Requirement</span></span> | <span data-ttu-id="206a8-118">值</span><span class="sxs-lookup"><span data-stu-id="206a8-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="206a8-119">標頭</span><span class="sxs-lookup"><span data-stu-id="206a8-119">Header</span></span><br/>  | <dl> <span data-ttu-id="206a8-120"><dt>Combase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="206a8-120"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="206a8-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="206a8-121">Library</span></span><br/> | <dl> <span data-ttu-id="206a8-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="206a8-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="206a8-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="206a8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="206a8-124">**COM Helper 函數**</span><span class="sxs-lookup"><span data-stu-id="206a8-124">**COM Helper Functions**</span></span>](com-helper-functions.md)
</dt> <dt>

[<span data-ttu-id="206a8-125">**INonDelegatingUnknown**</span><span class="sxs-lookup"><span data-stu-id="206a8-125">**INonDelegatingUnknown**</span></span>](inondelegatingunknown.md)
</dt> </dl>

 

 




