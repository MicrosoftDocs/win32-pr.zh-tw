---
description: 分別要求圖元歷程記錄交集和基本類型。
MS-HAID: vspixengine.IPixelHistoryRequest2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixelHistoryRequest2 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B62A9EBA-4497-4825-A2F1-285A4AD45012
api_name:
- IPixelHistoryRequest2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e789829d85f4cb986de694470a8cebddf3f26675
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317819"
---
# <a name="span-idvspixengineipixelhistoryrequest2spanipixelhistoryrequest2-interface"></a><span data-ttu-id="fcec4-103"><span id="vspixengine.ipixelhistoryrequest2"></span>IPixelHistoryRequest2 介面</span><span class="sxs-lookup"><span data-stu-id="fcec4-103"><span id="vspixengine.ipixelhistoryrequest2"></span>IPixelHistoryRequest2 interface</span></span>

<span data-ttu-id="fcec4-104">分別要求圖元歷程記錄交集和基本類型。</span><span class="sxs-lookup"><span data-stu-id="fcec4-104">Request for pixel history intersections and primitives separately.</span></span>

## <a name="members"></a><span data-ttu-id="fcec4-105">成員</span><span class="sxs-lookup"><span data-stu-id="fcec4-105">Members</span></span>

<span data-ttu-id="fcec4-106">**IPixelHistoryRequest2** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="fcec4-106">The **IPixelHistoryRequest2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fcec4-107">**IPixelHistoryRequest2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fcec4-107">**IPixelHistoryRequest2** also has these types of members:</span></span>

-   [<span data-ttu-id="fcec4-108">方法</span><span class="sxs-lookup"><span data-stu-id="fcec4-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="fcec4-109"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="fcec4-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="fcec4-110">**IPixelHistoryRequest2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="fcec4-110">The **IPixelHistoryRequest2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="fcec4-111">方法</span><span class="sxs-lookup"><span data-stu-id="fcec4-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="fcec4-112">描述</span><span class="sxs-lookup"><span data-stu-id="fcec4-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="fcec4-113"><a href="/windows/desktop/direct3dtools/ipixelhistoryrequest2-requestintersections-dword-point2d-dword-ipixelhistorycallback2-ptr-dword-dword"><strong>RequestIntersections</strong></a></span><span class="sxs-lookup"><span data-stu-id="fcec4-113"><a href="/windows/desktop/direct3dtools/ipixelhistoryrequest2-requestintersections-dword-point2d-dword-ipixelhistorycallback2-ptr-dword-dword"><strong>RequestIntersections</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="fcec4-114">要求會導致指定圖元、轉譯目標/UAV 和框架變更的事件清單。</span><span class="sxs-lookup"><span data-stu-id="fcec4-114">Requests a list of events that cause a change in the specified pixel, render target / UAV, and frame.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="fcec4-115"><a href="/windows/desktop/direct3dtools/ipixelhistoryrequest2-requestprimitives-pixelhistoryintersection-ptr-ipixelhistorycallback2-ptr-dword-dword"><strong>RequestPrimitives</strong></a></span><span class="sxs-lookup"><span data-stu-id="fcec4-115"><a href="/windows/desktop/direct3dtools/ipixelhistoryrequest2-requestprimitives-pixelhistoryintersection-ptr-ipixelhistorycallback2-ptr-dword-dword"><strong>RequestPrimitives</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="fcec4-116">要求特定交集的基本欄表。</span><span class="sxs-lookup"><span data-stu-id="fcec4-116">Requests a list of primitives from a particular intersection.</span></span> <span data-ttu-id="fcec4-117">如需詳細資訊，請參閱 RequestIntersections 成員函式。</span><span class="sxs-lookup"><span data-stu-id="fcec4-117">For more information, see the RequestIntersections member function.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="fcec4-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="fcec4-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="fcec4-119">標頭</span><span class="sxs-lookup"><span data-stu-id="fcec4-119">Header</span></span></p></td><td><span data-ttu-id="fcec4-120">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="fcec4-120">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
