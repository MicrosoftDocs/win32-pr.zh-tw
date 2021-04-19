---
description: BeginFlush 方法會開始進行清除作業。
ms.assetid: dc652394-c24e-4cea-ac28-30a1e6de205f
title: 'CBaseRenderer. BeginFlush 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e218e3b2d9c0cef8ce0fe052ad1b3c4b6f786858
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997768"
---
# <a name="cbaserendererbeginflush-method"></a><span data-ttu-id="17dee-103">CBaseRenderer. BeginFlush 方法</span><span class="sxs-lookup"><span data-stu-id="17dee-103">CBaseRenderer.BeginFlush method</span></span>

<span data-ttu-id="17dee-104">`BeginFlush`方法會開始清除作業。</span><span class="sxs-lookup"><span data-stu-id="17dee-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="17dee-105">語法</span><span class="sxs-lookup"><span data-stu-id="17dee-105">Syntax</span></span>


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="17dee-106">參數</span><span class="sxs-lookup"><span data-stu-id="17dee-106">Parameters</span></span>

<span data-ttu-id="17dee-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="17dee-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="17dee-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="17dee-108">Return value</span></span>

<span data-ttu-id="17dee-109">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="17dee-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="17dee-110">備註</span><span class="sxs-lookup"><span data-stu-id="17dee-110">Remarks</span></span>

<span data-ttu-id="17dee-111">當篩選準則的輸入 pin 收到 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 方法的呼叫時，會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="17dee-111">The filter's input pin calls this method when it receives a call to the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span> <span data-ttu-id="17dee-112">此篩選會釋放串流執行緒，並釋放其保留的任何範例以供轉譯。</span><span class="sxs-lookup"><span data-stu-id="17dee-112">The filter releases the streaming thread, and releases any sample that it was holding for rendering.</span></span>

## <a name="requirements"></a><span data-ttu-id="17dee-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="17dee-113">Requirements</span></span>



| <span data-ttu-id="17dee-114">需求</span><span class="sxs-lookup"><span data-stu-id="17dee-114">Requirement</span></span> | <span data-ttu-id="17dee-115">值</span><span class="sxs-lookup"><span data-stu-id="17dee-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17dee-116">標頭</span><span class="sxs-lookup"><span data-stu-id="17dee-116">Header</span></span><br/>  | <dl> <span data-ttu-id="17dee-117"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="17dee-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="17dee-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="17dee-118">Library</span></span><br/> | <dl> <span data-ttu-id="17dee-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="17dee-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17dee-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17dee-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17dee-121">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="17dee-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




