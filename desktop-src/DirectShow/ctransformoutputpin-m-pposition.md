---
description: CTransformOutputPin：： m_pPosition 成員協助程式物件，以傳送上游的搜尋命令。
ms.assetid: 2ca9bae7-a133-4e09-8aa7-1c4601ec5db0
title: 'CTransformOutputPin：： m_pPosition 成員 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pPosition
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9c5a1b5d5ced7a9f3985ceebdd2bdcb8e491d2e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084856"
---
# <a name="ctransformoutputpinm_pposition-member"></a><span data-ttu-id="7139d-103">CTransformOutputPin：： m \_ pPosition 成員</span><span class="sxs-lookup"><span data-stu-id="7139d-103">CTransformOutputPin::m\_pPosition member</span></span>

<span data-ttu-id="7139d-104">要傳遞向上游傳遞搜尋命令的 Helper 物件。</span><span class="sxs-lookup"><span data-stu-id="7139d-104">Helper object to pass seek commands upstream.</span></span>

## <a name="syntax"></a><span data-ttu-id="7139d-105">語法</span><span class="sxs-lookup"><span data-stu-id="7139d-105">Syntax</span></span>


```C++
IUnknown *m_pPosition;
```



## <a name="remarks"></a><span data-ttu-id="7139d-106">備註</span><span class="sxs-lookup"><span data-stu-id="7139d-106">Remarks</span></span>

<span data-ttu-id="7139d-107">第一次查詢 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) 或 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 介面的 pin 時，它會建立並匯總 [**CPosPassThru**](cpospassthru.md) helper 物件。</span><span class="sxs-lookup"><span data-stu-id="7139d-107">When the pin is first queried for the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) or [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, it creates and aggregates a [**CPosPassThru**](cpospassthru.md) helper object.</span></span>

## <a name="requirements"></a><span data-ttu-id="7139d-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="7139d-108">Requirements</span></span>



| <span data-ttu-id="7139d-109">需求</span><span class="sxs-lookup"><span data-stu-id="7139d-109">Requirement</span></span> | <span data-ttu-id="7139d-110">值</span><span class="sxs-lookup"><span data-stu-id="7139d-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7139d-111">標頭</span><span class="sxs-lookup"><span data-stu-id="7139d-111">Header</span></span><br/>  | <dl> <span data-ttu-id="7139d-112"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7139d-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7139d-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="7139d-113">Library</span></span><br/> | <dl> <span data-ttu-id="7139d-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7139d-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




