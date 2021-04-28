---
description: <span id="vspixengine.ipipelinestagescallback2"></span>IPipeLineStagesCallback2 介面-未使用。 先前是管線階段資料的回呼。
MS-HAID: vspixengine.IPipeLineStagesCallback2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesCallback2 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C27F94D2-D038-4D4E-9445-D0FF4C17F769
api_name:
- IPipeLineStagesCallback2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 941a056a5c2af00cfa1bb53f038cbeb923a777bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097386"
---
# <a name="span-idvspixengineipipelinestagescallback2spanipipelinestagescallback2-interface"></a><span data-ttu-id="f8084-104"><span id="vspixengine.ipipelinestagescallback2"></span>IPipeLineStagesCallback2 介面</span><span class="sxs-lookup"><span data-stu-id="f8084-104"><span id="vspixengine.ipipelinestagescallback2"></span>IPipeLineStagesCallback2 interface</span></span>

<span data-ttu-id="f8084-105">未使用。</span><span class="sxs-lookup"><span data-stu-id="f8084-105">Not used.</span></span> <span data-ttu-id="f8084-106">先前是管線階段資料的回呼。</span><span class="sxs-lookup"><span data-stu-id="f8084-106">Formerly a callback for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="f8084-107">成員</span><span class="sxs-lookup"><span data-stu-id="f8084-107">Members</span></span>

<span data-ttu-id="f8084-108">**IPipeLineStagesCallback2** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="f8084-108">The **IPipeLineStagesCallback2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f8084-109">**IPipeLineStagesCallback2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f8084-109">**IPipeLineStagesCallback2** also has these types of members:</span></span>

-   [<span data-ttu-id="f8084-110">方法</span><span class="sxs-lookup"><span data-stu-id="f8084-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="f8084-111"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="f8084-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="f8084-112">**IPipeLineStagesCallback2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="f8084-112">The **IPipeLineStagesCallback2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="f8084-113">方法</span><span class="sxs-lookup"><span data-stu-id="f8084-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="f8084-114">描述</span><span class="sxs-lookup"><span data-stu-id="f8084-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="f8084-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatadimensioncallback-threaddata3d-threaddata3d"><strong>ThreadDataDimensionCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="f8084-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatadimensioncallback-threaddata3d-threaddata3d"><strong>ThreadDataDimensionCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="f8084-116">回呼，會通知主機相關要求中計算著色器的執行緒和群組數目。</span><span class="sxs-lookup"><span data-stu-id="f8084-116">A callback that notifies the host of the number of threads and groups of the compute shader in the associated request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="f8084-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatanotavailablecallback-pipelinestageerror-eventid"><strong>ThreadDataNotAvailableCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="f8084-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatanotavailablecallback-pipelinestageerror-eventid"><strong>ThreadDataNotAvailableCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="f8084-118">通知主機 ThreadData 無法用於特定管線階段和事件的回呼。</span><span class="sxs-lookup"><span data-stu-id="f8084-118">A callback that notifies the host that ThreadData is unavailable for a particular pipeline stage and event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="f8084-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8084-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f8084-120">標頭</span><span class="sxs-lookup"><span data-stu-id="f8084-120">Header</span></span></p></td><td><span data-ttu-id="f8084-121">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="f8084-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
