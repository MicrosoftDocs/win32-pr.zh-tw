---
description: Invoke 方法會提供物件所公開之方法和屬性的存取權。
ms.assetid: d9539b89-b7c2-4b4d-b6d6-6275cc6d7e7c
title: 'CDeferredCommand： Invoke 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 268cfc3d4665eeacafbd695b974f55445747e151
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990677"
---
# <a name="cdeferredcommandinvoke-method"></a><span data-ttu-id="3c447-103">CDeferredCommand 方法</span><span class="sxs-lookup"><span data-stu-id="3c447-103">CDeferredCommand.Invoke method</span></span>

<span data-ttu-id="3c447-104">`Invoke`方法會提供物件所公開之方法和屬性的存取權。</span><span class="sxs-lookup"><span data-stu-id="3c447-104">The `Invoke` method provides access to methods and properties exposed by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c447-105">語法</span><span class="sxs-lookup"><span data-stu-id="3c447-105">Syntax</span></span>


```C++
HRESULT Invoke();
```



## <a name="parameters"></a><span data-ttu-id="3c447-106">參數</span><span class="sxs-lookup"><span data-stu-id="3c447-106">Parameters</span></span>

<span data-ttu-id="3c447-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="3c447-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3c447-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="3c447-108">Return value</span></span>

<span data-ttu-id="3c447-109">\_ \_ \_ 如果 **m \_ pQueue** 為 **Null**，則傳回 VFW E 已取消。</span><span class="sxs-lookup"><span data-stu-id="3c447-109">Returns VFW\_E\_ALREADY\_CANCELLED if **m\_pQueue** is **NULL**.</span></span> <span data-ttu-id="3c447-110">否則，會傳回對 **IDispatch：： GetTypeInfo** 或 **IUnknown：： QueryInterface** 的呼叫所產生的 **HRESULT** 。</span><span class="sxs-lookup"><span data-stu-id="3c447-110">Otherwise, returns the **HRESULT** resulting from a call to **IDispatch::GetTypeInfo** or **IUnknown::QueryInterface**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c447-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c447-111">Requirements</span></span>



| <span data-ttu-id="3c447-112">需求</span><span class="sxs-lookup"><span data-stu-id="3c447-112">Requirement</span></span> | <span data-ttu-id="3c447-113">值</span><span class="sxs-lookup"><span data-stu-id="3c447-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c447-114">標頭</span><span class="sxs-lookup"><span data-stu-id="3c447-114">Header</span></span><br/>  | <dl> <span data-ttu-id="3c447-115"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3c447-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3c447-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="3c447-116">Library</span></span><br/> | <dl> <span data-ttu-id="3c447-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3c447-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c447-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c447-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c447-119">**CDeferredCommand 類別**</span><span class="sxs-lookup"><span data-stu-id="3c447-119">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




