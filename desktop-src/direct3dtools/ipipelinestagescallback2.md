---
description: 未使用。 先前是管線階段資料的回呼。
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
ms.openlocfilehash: 9d14e080d4381405f32c6def51d8c64d78aaa422
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935740"
---
# <a name="span-idvspixengineipipelinestagescallback2spanipipelinestagescallback2-interface"></a><span data-ttu-id="af143-104"><span id="vspixengine.ipipelinestagescallback2"></span>IPipeLineStagesCallback2 介面</span><span class="sxs-lookup"><span data-stu-id="af143-104"><span id="vspixengine.ipipelinestagescallback2"></span>IPipeLineStagesCallback2 interface</span></span>

<span data-ttu-id="af143-105">未使用。</span><span class="sxs-lookup"><span data-stu-id="af143-105">Not used.</span></span> <span data-ttu-id="af143-106">先前是管線階段資料的回呼。</span><span class="sxs-lookup"><span data-stu-id="af143-106">Formerly a callback for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="af143-107">成員</span><span class="sxs-lookup"><span data-stu-id="af143-107">Members</span></span>

<span data-ttu-id="af143-108">**IPipeLineStagesCallback2** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="af143-108">The **IPipeLineStagesCallback2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="af143-109">**IPipeLineStagesCallback2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="af143-109">**IPipeLineStagesCallback2** also has these types of members:</span></span>

-   [<span data-ttu-id="af143-110">方法</span><span class="sxs-lookup"><span data-stu-id="af143-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="af143-111"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="af143-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="af143-112">**IPipeLineStagesCallback2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="af143-112">The **IPipeLineStagesCallback2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="af143-113">方法</span><span class="sxs-lookup"><span data-stu-id="af143-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="af143-114">描述</span><span class="sxs-lookup"><span data-stu-id="af143-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="af143-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatadimensioncallback-threaddata3d-threaddata3d"><strong>ThreadDataDimensionCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="af143-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatadimensioncallback-threaddata3d-threaddata3d"><strong>ThreadDataDimensionCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="af143-116">回呼，會通知主機相關要求中計算著色器的執行緒和群組數目。</span><span class="sxs-lookup"><span data-stu-id="af143-116">A callback that notifies the host of the number of threads and groups of the compute shader in the associated request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="af143-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatanotavailablecallback-pipelinestageerror-eventid"><strong>ThreadDataNotAvailableCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="af143-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatanotavailablecallback-pipelinestageerror-eventid"><strong>ThreadDataNotAvailableCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="af143-118">通知主機 ThreadData 無法用於特定管線階段和事件的回呼。</span><span class="sxs-lookup"><span data-stu-id="af143-118">A callback that notifies the host that ThreadData is unavailable for a particular pipeline stage and event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="af143-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="af143-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="af143-120">標頭</span><span class="sxs-lookup"><span data-stu-id="af143-120">Header</span></span></p></td><td><span data-ttu-id="af143-121">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="af143-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
