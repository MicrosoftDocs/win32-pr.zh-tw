---
description: 用於傳達 vsglog 相關資料的原始介面。
MS-HAID: vspixengine.IPixEngine
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 87AB1D07-8E90-49F0-B44D-F6185923B8D4
api_name:
- IPixEngine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2f02538f7acbd88daf166af657382e507a4e5661
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467922"
---
# <a name="span-idvspixengineipixenginespanipixengine-interface"></a><span data-ttu-id="410bd-103"><span id="vspixengine.ipixengine"></span>IPixEngine 介面</span><span class="sxs-lookup"><span data-stu-id="410bd-103"><span id="vspixengine.ipixengine"></span>IPixEngine interface</span></span>

<span data-ttu-id="410bd-104">用於傳達 vsglog 相關資料的原始介面。</span><span class="sxs-lookup"><span data-stu-id="410bd-104">Original interface for communicating data about a vsglog .</span></span>

## <a name="members"></a><span data-ttu-id="410bd-105">成員</span><span class="sxs-lookup"><span data-stu-id="410bd-105">Members</span></span>

<span data-ttu-id="410bd-106">**IPixEngine** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="410bd-106">The **IPixEngine** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="410bd-107">**IPixEngine** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="410bd-107">**IPixEngine** also has these types of members:</span></span>

-   [<span data-ttu-id="410bd-108">方法</span><span class="sxs-lookup"><span data-stu-id="410bd-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="410bd-109"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="410bd-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="410bd-110">**IPixEngine** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="410bd-110">The **IPixEngine** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="410bd-111">方法</span><span class="sxs-lookup"><span data-stu-id="410bd-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="410bd-112">描述</span><span class="sxs-lookup"><span data-stu-id="410bd-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="410bd-113"><a href="/windows/desktop/direct3dtools/ipixengine-openfile-bstr-bstr-inewframescallback-ptr-ifileiocallback-ptr-lcid"><strong>OpenFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="410bd-113"><a href="/windows/desktop/direct3dtools/ipixengine-openfile-bstr-bstr-inewframescallback-ptr-ifileiocallback-ptr-lcid"><strong>OpenFile</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="410bd-114">開啟圖形記錄檔。</span><span class="sxs-lookup"><span data-stu-id="410bd-114">Opens a graphics log.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="410bd-115"><a href="/windows/desktop/direct3dtools/ipixengine-runexperiment-experiment-irunexperimentcallback-ptr-inewframescallback-ptr-ifileiocallback-ptr-dword-experimenttrigger-arr"><strong>RunExperiment</strong></a></span><span class="sxs-lookup"><span data-stu-id="410bd-115"><a href="/windows/desktop/direct3dtools/ipixengine-runexperiment-experiment-irunexperimentcallback-ptr-inewframescallback-ptr-ifileiocallback-ptr-dword-experimenttrigger-arr"><strong>RunExperiment</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="410bd-116">執行實驗。</span><span class="sxs-lookup"><span data-stu-id="410bd-116">Runs an experiment.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="410bd-117"><a href="/windows/desktop/direct3dtools/ipixengine-savefile-bstr-ifileiocallback-ptr"><strong>SaveFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="410bd-117"><a href="/windows/desktop/direct3dtools/ipixengine-savefile-bstr-ifileiocallback-ptr"><strong>SaveFile</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="410bd-118">將圖形記錄檔儲存至指定的位置。</span><span class="sxs-lookup"><span data-stu-id="410bd-118">Saves the graphics log to the specified location.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="410bd-119"><a href="/windows/desktop/direct3dtools/ipixengine-setparentprocess-dword"><strong>SetParentProcess</strong></a></span><span class="sxs-lookup"><span data-stu-id="410bd-119"><a href="/windows/desktop/direct3dtools/ipixengine-setparentprocess-dword"><strong>SetParentProcess</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="410bd-120">未使用。</span><span class="sxs-lookup"><span data-stu-id="410bd-120">Not used.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="410bd-121"><a href="/windows/desktop/direct3dtools/ipixengine-shutdown"><strong>關閉</strong></a></span><span class="sxs-lookup"><span data-stu-id="410bd-121"><a href="/windows/desktop/direct3dtools/ipixengine-shutdown"><strong>ShutDown</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="410bd-122">關閉引擎。</span><span class="sxs-lookup"><span data-stu-id="410bd-122">Shuts down the engine.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="410bd-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="410bd-123">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="410bd-124">標頭</span><span class="sxs-lookup"><span data-stu-id="410bd-124">Header</span></span></p></td><td><span data-ttu-id="410bd-125">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="410bd-125">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
