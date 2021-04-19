---
description: 鎖定以保護在篩選內建立物件。
ms.assetid: ad1d2584-0d9e-42a8-83ea-0c1907ddcf33
title: 'CBaseRenderer：： m_ObjectCreationLock 成員 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ObjectCreationLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e344b20b4924ac26ebe6253f5388136b350abefe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976221"
---
# <a name="cbaserendererm_objectcreationlock-member"></a><span data-ttu-id="e3a2e-103">CBaseRenderer：： m \_ ObjectCreationLock 成員</span><span class="sxs-lookup"><span data-stu-id="e3a2e-103">CBaseRenderer::m\_ObjectCreationLock member</span></span>

<span data-ttu-id="e3a2e-104">鎖定以保護在篩選內建立物件。</span><span class="sxs-lookup"><span data-stu-id="e3a2e-104">Lock to protect the creation of objects inside the filter.</span></span> <span data-ttu-id="e3a2e-105">當篩選建立輸入 pin ([**CBaseRenderer：： m \_ PInputPin**](cbaserenderer-m-pinputpin.md)) 或 [**CRendererPosPassThru**](crendererpospassthru.md) 物件 ([**CBaseRenderer：： m \_ pPosition**](cbaserenderer-m-pposition.md)) 時，會保留這個鎖定。</span><span class="sxs-lookup"><span data-stu-id="e3a2e-105">The filter holds this lock when it creates the input pin ([**CBaseRenderer::m\_pInputPin**](cbaserenderer-m-pinputpin.md)) or the [**CRendererPosPassThru**](crendererpospassthru.md) object ([**CBaseRenderer::m\_pPosition**](cbaserenderer-m-pposition.md)).</span></span> <span data-ttu-id="e3a2e-106">此鎖定可防止多個執行緒同時嘗試建立這些物件的其中一個。</span><span class="sxs-lookup"><span data-stu-id="e3a2e-106">This lock prevents multiple threads from attempting to create one of these objects at the same time.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3a2e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3a2e-107">Syntax</span></span>


```C++
CCritSec m_ObjectCreationLock;
```



## <a name="requirements"></a><span data-ttu-id="e3a2e-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3a2e-108">Requirements</span></span>



| <span data-ttu-id="e3a2e-109">需求</span><span class="sxs-lookup"><span data-stu-id="e3a2e-109">Requirement</span></span> | <span data-ttu-id="e3a2e-110">值</span><span class="sxs-lookup"><span data-stu-id="e3a2e-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3a2e-111">標頭</span><span class="sxs-lookup"><span data-stu-id="e3a2e-111">Header</span></span><br/>  | <dl> <span data-ttu-id="e3a2e-112"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e3a2e-112"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e3a2e-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="e3a2e-113">Library</span></span><br/> | <dl> <span data-ttu-id="e3a2e-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e3a2e-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3a2e-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3a2e-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3a2e-116">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="e3a2e-116">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




