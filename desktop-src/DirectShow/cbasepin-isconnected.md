---
description: IsConnected 方法會判斷釘選是否連接到另一個 pin。
ms.assetid: d8b9b43b-6f8d-4d75-9688-f0cee3794a78
title: 'CBasePin. IsConnected 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IsConnected
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b857e1ceff4844d66c55cf729a3d2b9771d48846
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983211"
---
# <a name="cbasepinisconnected-method"></a><span data-ttu-id="d6dbf-103">CBasePin. IsConnected 方法</span><span class="sxs-lookup"><span data-stu-id="d6dbf-103">CBasePin.IsConnected method</span></span>

<span data-ttu-id="d6dbf-104">`IsConnected`方法會判斷 pin 是否已連接到另一個 pin。</span><span class="sxs-lookup"><span data-stu-id="d6dbf-104">The `IsConnected` method determines whether the pin is connected to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6dbf-105">語法</span><span class="sxs-lookup"><span data-stu-id="d6dbf-105">Syntax</span></span>


```C++
BOOL IsConnected();
```



## <a name="parameters"></a><span data-ttu-id="d6dbf-106">參數</span><span class="sxs-lookup"><span data-stu-id="d6dbf-106">Parameters</span></span>

<span data-ttu-id="d6dbf-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d6dbf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d6dbf-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6dbf-108">Return value</span></span>

<span data-ttu-id="d6dbf-109">如果釘選連接，則傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="d6dbf-109">Returns **TRUE** if the pin is connected.</span></span> <span data-ttu-id="d6dbf-110">否則，會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="d6dbf-110">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6dbf-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6dbf-111">Requirements</span></span>



| <span data-ttu-id="d6dbf-112">需求</span><span class="sxs-lookup"><span data-stu-id="d6dbf-112">Requirement</span></span> | <span data-ttu-id="d6dbf-113">值</span><span class="sxs-lookup"><span data-stu-id="d6dbf-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6dbf-114">標頭</span><span class="sxs-lookup"><span data-stu-id="d6dbf-114">Header</span></span><br/>  | <dl> <span data-ttu-id="d6dbf-115"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d6dbf-115"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d6dbf-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="d6dbf-116">Library</span></span><br/> | <dl> <span data-ttu-id="d6dbf-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d6dbf-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6dbf-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6dbf-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6dbf-119">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="d6dbf-119">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




