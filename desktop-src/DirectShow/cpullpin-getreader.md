---
description: System.diagnostics.symbolstore.isymbolbinder1.getreader 方法會傳回輸出釘選的 IAsyncReader 介面指標。
ms.assetid: bb7ed3f2-a5bc-496c-8a52-f9915a75105e
title: 'CPullPin. System.diagnostics.symbolstore.isymbolbinder1.getreader 方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.GetReader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a20bbb689c4ee5e3ac12c510098163d9fbb224e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996003"
---
# <a name="cpullpingetreader-method"></a><span data-ttu-id="44b79-103">CPullPin. System.diagnostics.symbolstore.isymbolbinder1.getreader 方法</span><span class="sxs-lookup"><span data-stu-id="44b79-103">CPullPin.GetReader method</span></span>

<span data-ttu-id="44b79-104">方法會傳回 `GetReader` 輸出釘選 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="44b79-104">The `GetReader` method returns a pointer to the output pin's [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="44b79-105">語法</span><span class="sxs-lookup"><span data-stu-id="44b79-105">Syntax</span></span>


```C++
IAsyncReader* GetReader();
```



## <a name="parameters"></a><span data-ttu-id="44b79-106">參數</span><span class="sxs-lookup"><span data-stu-id="44b79-106">Parameters</span></span>

<span data-ttu-id="44b79-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="44b79-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="44b79-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="44b79-108">Return value</span></span>

<span data-ttu-id="44b79-109">傳回 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="44b79-109">Returns a pointer to the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="44b79-110">備註</span><span class="sxs-lookup"><span data-stu-id="44b79-110">Remarks</span></span>

<span data-ttu-id="44b79-111">傳回的介面具有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="44b79-111">The returned interface has an outstanding reference count.</span></span> <span data-ttu-id="44b79-112">呼叫端必須釋放介面。</span><span class="sxs-lookup"><span data-stu-id="44b79-112">The caller must release the interface.</span></span>

<span data-ttu-id="44b79-113">在呼叫 **AddRef** 之前，方法不會檢查介面指標的值，因此，除非您已成功呼叫 [**CPullPin：： Connect**](cpullpin-connect.md) 方法，否則請不要呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="44b79-113">The method does not check the value of the interface pointer before calling **AddRef**, so do not call this until you have successfully called the [**CPullPin::Connect**](cpullpin-connect.md) method.</span></span> <span data-ttu-id="44b79-114">否則，介面指標可能是 **Null** ，而且呼叫 **AddRef** 將會擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="44b79-114">Otherwise, the interface pointer might be **NULL** and calling **AddRef** will throw an exception.</span></span>

## <a name="requirements"></a><span data-ttu-id="44b79-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="44b79-115">Requirements</span></span>



| <span data-ttu-id="44b79-116">需求</span><span class="sxs-lookup"><span data-stu-id="44b79-116">Requirement</span></span> | <span data-ttu-id="44b79-117">值</span><span class="sxs-lookup"><span data-stu-id="44b79-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44b79-118">標頭</span><span class="sxs-lookup"><span data-stu-id="44b79-118">Header</span></span><br/>  | <dl> <span data-ttu-id="44b79-119"><dt>Pullpin。h</dt></span><span class="sxs-lookup"><span data-stu-id="44b79-119"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="44b79-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="44b79-120">Library</span></span><br/> | <dl> <span data-ttu-id="44b79-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="44b79-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44b79-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44b79-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44b79-123">**CPullPin 類別**</span><span class="sxs-lookup"><span data-stu-id="44b79-123">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




