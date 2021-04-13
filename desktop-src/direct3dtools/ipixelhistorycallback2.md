---
description: 回呼會傳回圖元歷程記錄交集 (繪製呼叫層級) 和基本 (三角形層級) 在兩個不同的結果中。
MS-HAID: vspixengine.IPixelHistoryCallback2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixelHistoryCallback2 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0111482E-B66A-4763-8890-85B1711F38B2
api_name:
- IPixelHistoryCallback2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 473f3540ad9c6a16659a6e43c3aa31eef706ec59
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510051"
---
# <a name="span-idvspixengineipixelhistorycallback2spanipixelhistorycallback2-interface"></a><span data-ttu-id="1ee92-103"><span id="vspixengine.ipixelhistorycallback2"></span>IPixelHistoryCallback2 介面</span><span class="sxs-lookup"><span data-stu-id="1ee92-103"><span id="vspixengine.ipixelhistorycallback2"></span>IPixelHistoryCallback2 interface</span></span>

<span data-ttu-id="1ee92-104">回呼會傳回圖元歷程記錄交集 (繪製呼叫層級) 和基本 (三角形層級) 在兩個不同的結果中。</span><span class="sxs-lookup"><span data-stu-id="1ee92-104">Callback to return pixel history intersections (draw call level) and primitives (triangle level) in two different results.</span></span>

## <a name="members"></a><span data-ttu-id="1ee92-105">成員</span><span class="sxs-lookup"><span data-stu-id="1ee92-105">Members</span></span>

<span data-ttu-id="1ee92-106">**IPixelHistoryCallback2** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="1ee92-106">The **IPixelHistoryCallback2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1ee92-107">**IPixelHistoryCallback2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1ee92-107">**IPixelHistoryCallback2** also has these types of members:</span></span>

-   [<span data-ttu-id="1ee92-108">方法</span><span class="sxs-lookup"><span data-stu-id="1ee92-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="1ee92-109"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="1ee92-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="1ee92-110">**IPixelHistoryCallback2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="1ee92-110">The **IPixelHistoryCallback2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="1ee92-111">方法</span><span class="sxs-lookup"><span data-stu-id="1ee92-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="1ee92-112">描述</span><span class="sxs-lookup"><span data-stu-id="1ee92-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="1ee92-113"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-intersectionscallback-dword-pixelhistoryintersection-arr"><strong>IntersectionsCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="1ee92-113"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-intersectionscallback-dword-pixelhistoryintersection-arr"><strong>IntersectionsCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="1ee92-114">回呼，會通知主機 assocaited 要求所傳回的圖元歷程記錄交集資訊。</span><span class="sxs-lookup"><span data-stu-id="1ee92-114">A callback that notifies the host of pixel history intersection information returned by the assocaited request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="1ee92-115"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-primitivescallback-dword-pixelhistoryoperation-arr"><strong>PrimitivesCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="1ee92-115"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-primitivescallback-dword-pixelhistoryoperation-arr"><strong>PrimitivesCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="1ee92-116">回呼，會通知主機相關聯的要求所傳回的圖元歷程記錄基本作業資訊。</span><span class="sxs-lookup"><span data-stu-id="1ee92-116">A callback that notifies the host of pixel history primitive operation information returned by the associated request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="1ee92-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ee92-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1ee92-118">標頭</span><span class="sxs-lookup"><span data-stu-id="1ee92-118">Header</span></span></p></td><td><span data-ttu-id="1ee92-119">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="1ee92-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
