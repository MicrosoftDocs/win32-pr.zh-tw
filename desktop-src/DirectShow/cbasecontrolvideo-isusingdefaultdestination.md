---
description: IsUsingDefaultDestination 方法會判斷轉譯器是否使用預設的目的地視窗。
ms.assetid: 0b956575-4cf0-4f1f-9223-bb1ec3ae8b10
title: 'CBaseControlVideo. IsUsingDefaultDestination 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsUsingDefaultDestination
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 88168442cf741e5997c2b66fc4b83bf8205e694f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982691"
---
# <a name="cbasecontrolvideoisusingdefaultdestination-method"></a><span data-ttu-id="55fcb-103">CBaseControlVideo. IsUsingDefaultDestination 方法</span><span class="sxs-lookup"><span data-stu-id="55fcb-103">CBaseControlVideo.IsUsingDefaultDestination method</span></span>

<span data-ttu-id="55fcb-104">`IsUsingDefaultDestination`方法會判斷轉譯器是否使用預設的目的地視窗。</span><span class="sxs-lookup"><span data-stu-id="55fcb-104">The `IsUsingDefaultDestination` method determines if the renderer is using the default destination window.</span></span>

## <a name="syntax"></a><span data-ttu-id="55fcb-105">語法</span><span class="sxs-lookup"><span data-stu-id="55fcb-105">Syntax</span></span>


```C++
virtual HRESULT IsUsingDefaultDestination() = 0;
```



## <a name="parameters"></a><span data-ttu-id="55fcb-106">參數</span><span class="sxs-lookup"><span data-stu-id="55fcb-106">Parameters</span></span>

<span data-ttu-id="55fcb-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="55fcb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="55fcb-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="55fcb-108">Return value</span></span>

<span data-ttu-id="55fcb-109">\_如果使用預設目的地，則傳回 [確定]，否則傳回 \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="55fcb-109">Returns S\_OK if using the default destination; otherwise, returns S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="55fcb-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="55fcb-110">Requirements</span></span>



| <span data-ttu-id="55fcb-111">需求</span><span class="sxs-lookup"><span data-stu-id="55fcb-111">Requirement</span></span> | <span data-ttu-id="55fcb-112">值</span><span class="sxs-lookup"><span data-stu-id="55fcb-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55fcb-113">標頭</span><span class="sxs-lookup"><span data-stu-id="55fcb-113">Header</span></span><br/>  | <dl> <span data-ttu-id="55fcb-114"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="55fcb-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="55fcb-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="55fcb-115">Library</span></span><br/> | <dl> <span data-ttu-id="55fcb-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="55fcb-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55fcb-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55fcb-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55fcb-118">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="55fcb-118">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




