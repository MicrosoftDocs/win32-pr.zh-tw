---
description: 原始 IPixEngine 介面的延伸模組。
MS-HAID: vspixengine.IPixEngine2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine2 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D650FB4C-C332-4E2E-85EB-DDCE3DA87B0C
api_name:
- IPixEngine2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bf8fe4537a6f4c8703482289302ffa8f3a645903
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467575"
---
# <a name="span-idvspixengineipixengine2spanipixengine2-interface"></a><span data-ttu-id="c43c7-103"><span id="vspixengine.ipixengine2"></span>IPixEngine2 介面</span><span class="sxs-lookup"><span data-stu-id="c43c7-103"><span id="vspixengine.ipixengine2"></span>IPixEngine2 interface</span></span>

<span data-ttu-id="c43c7-104">原始 IPixEngine 介面的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="c43c7-104">Extensions to the original IPixEngine interface.</span></span>

## <a name="members"></a><span data-ttu-id="c43c7-105">成員</span><span class="sxs-lookup"><span data-stu-id="c43c7-105">Members</span></span>

<span data-ttu-id="c43c7-106">**IPixEngine2** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="c43c7-106">The **IPixEngine2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c43c7-107">**IPixEngine2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c43c7-107">**IPixEngine2** also has these types of members:</span></span>

-   [<span data-ttu-id="c43c7-108">方法</span><span class="sxs-lookup"><span data-stu-id="c43c7-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="c43c7-109"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="c43c7-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="c43c7-110">**IPixEngine2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c43c7-110">The **IPixEngine2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="c43c7-111">方法</span><span class="sxs-lookup"><span data-stu-id="c43c7-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="c43c7-112">描述</span><span class="sxs-lookup"><span data-stu-id="c43c7-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="c43c7-113"><a href="/windows/desktop/direct3dtools/ipixengine2-endexperiment-bstr-ifileiocallback-ptr"><strong>EndExperiment</strong></a></span><span class="sxs-lookup"><span data-stu-id="c43c7-113"><a href="/windows/desktop/direct3dtools/ipixengine2-endexperiment-bstr-ifileiocallback-ptr"><strong>EndExperiment</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c43c7-114">結束 experiement 並完成圖形記錄檔。</span><span class="sxs-lookup"><span data-stu-id="c43c7-114">Ends the experiement and completes the graphics log.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="c43c7-115"><a href="/windows/desktop/direct3dtools/ipixengine2-getplaybackmachine-bstr-bool-ptr-bstr-ptr"><strong>GetPlaybackMachine</strong></a></span><span class="sxs-lookup"><span data-stu-id="c43c7-115"><a href="/windows/desktop/direct3dtools/ipixengine2-getplaybackmachine-bstr-bool-ptr-bstr-ptr"><strong>GetPlaybackMachine</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c43c7-116">取得目前播放電腦的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c43c7-116">Gets information about the current playback machine.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="c43c7-117"><a href="/windows/desktop/direct3dtools/ipixengine2-onnewdataavailable-bool-bool-int64-int64-int32-byte-arr"><strong>OnNewDataAvailable</strong></a></span><span class="sxs-lookup"><span data-stu-id="c43c7-117"><a href="/windows/desktop/direct3dtools/ipixengine2-onnewdataavailable-bool-bool-int64-int64-int32-byte-arr"><strong>OnNewDataAvailable</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c43c7-118">要求指出圖形記錄檔中有新的資料。</span><span class="sxs-lookup"><span data-stu-id="c43c7-118">Requests to indicate that the graphics log has new data inside of it.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="c43c7-119"><a href="/windows/desktop/direct3dtools/ipixengine2-setplaybackmachine-bstr-bool-bstr"><strong>SetPlaybackMachine</strong></a></span><span class="sxs-lookup"><span data-stu-id="c43c7-119"><a href="/windows/desktop/direct3dtools/ipixengine2-setplaybackmachine-bstr-bool-bstr"><strong>SetPlaybackMachine</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c43c7-120">設定指定之圖形記錄檔的目前播放電腦。</span><span class="sxs-lookup"><span data-stu-id="c43c7-120">Sets the current playback machine for the specified graphics log.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="c43c7-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="c43c7-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c43c7-122">標頭</span><span class="sxs-lookup"><span data-stu-id="c43c7-122">Header</span></span></p></td><td><span data-ttu-id="c43c7-123">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="c43c7-123">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
