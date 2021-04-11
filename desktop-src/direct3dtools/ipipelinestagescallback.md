---
description: 未使用。 先前是管線階段資料的回呼。
MS-HAID: vspixengine.IPipeLineStagesCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesCallback 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2F5B84DB-3D06-4D82-BF1D-E5853CC4B835
api_name:
- IPipeLineStagesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 93a00815fc42f4ac7b56e310fafedc0561f40233
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846764"
---
# <a name="span-idvspixengineipipelinestagescallbackspanipipelinestagescallback-interface"></a><span data-ttu-id="79620-104"><span id="vspixengine.ipipelinestagescallback"></span>IPipeLineStagesCallback 介面</span><span class="sxs-lookup"><span data-stu-id="79620-104"><span id="vspixengine.ipipelinestagescallback"></span>IPipeLineStagesCallback interface</span></span>

<span data-ttu-id="79620-105">未使用。</span><span class="sxs-lookup"><span data-stu-id="79620-105">Not used.</span></span> <span data-ttu-id="79620-106">先前是管線階段資料的回呼。</span><span class="sxs-lookup"><span data-stu-id="79620-106">Formerly a callback for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="79620-107">成員</span><span class="sxs-lookup"><span data-stu-id="79620-107">Members</span></span>

<span data-ttu-id="79620-108">**IPipeLineStagesCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="79620-108">The **IPipeLineStagesCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="79620-109">**IPipeLineStagesCallback** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="79620-109">**IPipeLineStagesCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="79620-110">方法</span><span class="sxs-lookup"><span data-stu-id="79620-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="79620-111"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="79620-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="79620-112">**IPipeLineStagesCallback** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="79620-112">The **IPipeLineStagesCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="79620-113">方法</span><span class="sxs-lookup"><span data-stu-id="79620-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="79620-114">描述</span><span class="sxs-lookup"><span data-stu-id="79620-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="79620-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-getsupportedstages-dword-pipelinestage-arr-uint-uint"><strong>GetSupportedStages</strong></a></span><span class="sxs-lookup"><span data-stu-id="79620-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-getsupportedstages-dword-pipelinestage-arr-uint-uint"><strong>GetSupportedStages</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="79620-116">回呼，會通知主機 assocaited 要求的繪製呼叫所使用的管線階段。</span><span class="sxs-lookup"><span data-stu-id="79620-116">A callback that notifies the host of which pipeline stages are used by the draw call of the assocaited request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="79620-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatanotavailablecallback-uint-pipelinestageerror-arr-uint-uint-eventid"><strong>MeshDataNotAvailableCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="79620-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatanotavailablecallback-uint-pipelinestageerror-arr-uint-uint-eventid"><strong>MeshDataNotAvailableCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="79620-118">回呼，通知主機哪些管線階段無法針對相關要求中所指定的事件傳回網格資料。</span><span class="sxs-lookup"><span data-stu-id="79620-118">A callback that notifies the host of which pipeline stages are not able to return mesh data for the event specified in the associated request.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="79620-119"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatavertcallback-uint-uint-meshdatabufferlayoutentry-arr-uint-uint-byte-arr-uint-byte-arr-uint-uint-uint-uint-bool-uint-uint"><strong>MeshDataVertCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="79620-119"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatavertcallback-uint-uint-meshdatabufferlayoutentry-arr-uint-uint-byte-arr-uint-byte-arr-uint-uint-uint-uint-bool-uint-uint"><strong>MeshDataVertCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="79620-120">回呼，會通知主機 assocaited 要求所傳回的管線階段網格資訊。</span><span class="sxs-lookup"><span data-stu-id="79620-120">A callback that notifies the host of pipeline stages mesh information returned by the assocaited request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="79620-121"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-resultcallback-pipelinestagesid-eventid-dword-dword-dword-dword-byte-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="79620-121"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-resultcallback-pipelinestagesid-eventid-dword-dword-dword-dword-byte-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="79620-122">回呼，會通知主機 assocaited 要求所傳回的管線階段影像資訊。</span><span class="sxs-lookup"><span data-stu-id="79620-122">A callback that notifies the host of pipeline stages image information returned by the assocaited request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="79620-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="79620-123">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="79620-124">標頭</span><span class="sxs-lookup"><span data-stu-id="79620-124">Header</span></span></p></td><td><span data-ttu-id="79620-125">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="79620-125">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
