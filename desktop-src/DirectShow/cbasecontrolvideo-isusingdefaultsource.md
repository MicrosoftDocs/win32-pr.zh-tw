---
description: IsUsingDefaultSource 方法會判斷轉譯器是否使用預設的來源視窗。
ms.assetid: f68d47e7-6602-4321-8e9e-373d354077a1
title: 'CBaseControlVideo. IsUsingDefaultSource 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsUsingDefaultSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94768cb098183654b7a0fa9464221989b407d880
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991248"
---
# <a name="cbasecontrolvideoisusingdefaultsource-method"></a><span data-ttu-id="209bd-103">CBaseControlVideo. IsUsingDefaultSource 方法</span><span class="sxs-lookup"><span data-stu-id="209bd-103">CBaseControlVideo.IsUsingDefaultSource method</span></span>

<span data-ttu-id="209bd-104">`IsUsingDefaultSource`方法會判斷轉譯器是否使用預設的來源視窗。</span><span class="sxs-lookup"><span data-stu-id="209bd-104">The `IsUsingDefaultSource` method determines if the renderer is using the default source window.</span></span>

## <a name="syntax"></a><span data-ttu-id="209bd-105">語法</span><span class="sxs-lookup"><span data-stu-id="209bd-105">Syntax</span></span>


```C++
virtual HRESULT IsUsingDefaultSource() = 0;
```



## <a name="parameters"></a><span data-ttu-id="209bd-106">參數</span><span class="sxs-lookup"><span data-stu-id="209bd-106">Parameters</span></span>

<span data-ttu-id="209bd-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="209bd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="209bd-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="209bd-108">Return value</span></span>

<span data-ttu-id="209bd-109">如果轉譯器 \_ 使用預設來源，則傳回 [確定]，否則傳回 \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="209bd-109">Returns S\_OK if the renderer is using the default source; otherwise, returns S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="209bd-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="209bd-110">Requirements</span></span>



| <span data-ttu-id="209bd-111">需求</span><span class="sxs-lookup"><span data-stu-id="209bd-111">Requirement</span></span> | <span data-ttu-id="209bd-112">值</span><span class="sxs-lookup"><span data-stu-id="209bd-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="209bd-113">標頭</span><span class="sxs-lookup"><span data-stu-id="209bd-113">Header</span></span><br/>  | <dl> <span data-ttu-id="209bd-114"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="209bd-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="209bd-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="209bd-115">Library</span></span><br/> | <dl> <span data-ttu-id="209bd-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="209bd-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="209bd-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="209bd-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="209bd-118">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="209bd-118">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




