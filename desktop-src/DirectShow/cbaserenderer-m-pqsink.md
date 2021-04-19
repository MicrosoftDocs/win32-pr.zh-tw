---
description: 物件的指標，該物件會接收品質控制訊息。
ms.assetid: bf4fd84c-9522-4686-9fb1-17a2ce3e5a16
title: 'CBaseRenderer：： m_pQSink 成員 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pQSink
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 331504ffaeb74d84382b65d1332f6dbe7c9556dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000423"
---
# <a name="cbaserendererm_pqsink-member"></a><span data-ttu-id="1ff85-103">CBaseRenderer：： m \_ pQSink 成員</span><span class="sxs-lookup"><span data-stu-id="1ff85-103">CBaseRenderer::m\_pQSink member</span></span>

<span data-ttu-id="1ff85-104">物件的指標，該物件會接收品質控制訊息。</span><span class="sxs-lookup"><span data-stu-id="1ff85-104">Pointer to the object that receives quality-control messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ff85-105">語法</span><span class="sxs-lookup"><span data-stu-id="1ff85-105">Syntax</span></span>


```C++
IQualityControl *m_pQSink;
```



## <a name="remarks"></a><span data-ttu-id="1ff85-106">備註</span><span class="sxs-lookup"><span data-stu-id="1ff85-106">Remarks</span></span>

<span data-ttu-id="1ff85-107">基類不會執行品質控制項。</span><span class="sxs-lookup"><span data-stu-id="1ff85-107">The base class does not implement quality control.</span></span> <span data-ttu-id="1ff85-108">此成員變數預設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1ff85-108">This member variable defaults to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ff85-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ff85-109">Requirements</span></span>



| <span data-ttu-id="1ff85-110">需求</span><span class="sxs-lookup"><span data-stu-id="1ff85-110">Requirement</span></span> | <span data-ttu-id="1ff85-111">值</span><span class="sxs-lookup"><span data-stu-id="1ff85-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ff85-112">標頭</span><span class="sxs-lookup"><span data-stu-id="1ff85-112">Header</span></span><br/>  | <dl> <span data-ttu-id="1ff85-113"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1ff85-113"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1ff85-114">程式庫</span><span class="sxs-lookup"><span data-stu-id="1ff85-114">Library</span></span><br/> | <dl> <span data-ttu-id="1ff85-115"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="1ff85-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ff85-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ff85-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ff85-117">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="1ff85-117">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




