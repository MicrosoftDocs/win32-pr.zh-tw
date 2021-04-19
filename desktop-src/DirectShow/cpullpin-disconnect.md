---
description: 中斷連接方法會中斷與輸出 pin 的連接。
ms.assetid: 6e362e32-7b74-4392-b46f-1ab47a30a07b
title: 'CPullPin 連接方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec13a7f29a06bab4f79ddb58932796f8363adadc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995413"
---
# <a name="cpullpindisconnect-method"></a><span data-ttu-id="799f9-103">CPullPin 中斷方法</span><span class="sxs-lookup"><span data-stu-id="799f9-103">CPullPin.Disconnect method</span></span>

<span data-ttu-id="799f9-104">方法會將 `Disconnect` 連接與輸出釘選中斷。</span><span class="sxs-lookup"><span data-stu-id="799f9-104">The `Disconnect` method breaks the connection with the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="799f9-105">語法</span><span class="sxs-lookup"><span data-stu-id="799f9-105">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="799f9-106">參數</span><span class="sxs-lookup"><span data-stu-id="799f9-106">Parameters</span></span>

<span data-ttu-id="799f9-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="799f9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="799f9-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="799f9-108">Return value</span></span>

<span data-ttu-id="799f9-109">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="799f9-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="799f9-110">備註</span><span class="sxs-lookup"><span data-stu-id="799f9-110">Remarks</span></span>

<span data-ttu-id="799f9-111">這個方法會中斷 [**CPullPin：： Connect**](cpullpin-connect.md) 方法中所做的任何連接。</span><span class="sxs-lookup"><span data-stu-id="799f9-111">This method breaks any connection made in the [**CPullPin::Connect**](cpullpin-connect.md) method.</span></span> <span data-ttu-id="799f9-112">在您的 [**IPin：:D isconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) 方法內呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="799f9-112">Call this method inside your [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span> <span data-ttu-id="799f9-113"> (如果您的 pin 衍生自 [**CBasePin**](cbasepin.md)，請覆寫 [**CBasePin：： BreakConnect**](cbasepin-breakconnect.md) 以呼叫這個方法。 ) </span><span class="sxs-lookup"><span data-stu-id="799f9-113">(If your pin derives from [**CBasePin**](cbasepin.md), override [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) to call this method.)</span></span>

## <a name="requirements"></a><span data-ttu-id="799f9-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="799f9-114">Requirements</span></span>



| <span data-ttu-id="799f9-115">需求</span><span class="sxs-lookup"><span data-stu-id="799f9-115">Requirement</span></span> | <span data-ttu-id="799f9-116">值</span><span class="sxs-lookup"><span data-stu-id="799f9-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="799f9-117">標頭</span><span class="sxs-lookup"><span data-stu-id="799f9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="799f9-118"><dt>Pullpin。h</dt></span><span class="sxs-lookup"><span data-stu-id="799f9-118"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="799f9-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="799f9-119">Library</span></span><br/> | <dl> <span data-ttu-id="799f9-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="799f9-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="799f9-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="799f9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="799f9-122">**CPullPin 類別**</span><span class="sxs-lookup"><span data-stu-id="799f9-122">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




