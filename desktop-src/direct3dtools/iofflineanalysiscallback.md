---
description: 回呼，以傳回離線分析資料。
MS-HAID: vspixengine.IOfflineAnalysisCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IOfflineAnalysisCallback 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 39E6B9CA-C17A-42C8-AC6D-118DC8DE3AD9
api_name:
- IOfflineAnalysisCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 496ca07544cdc38ff9f0e3f29c0ebbd2b9e8753c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106985385"
---
# <a name="span-idvspixengineiofflineanalysiscallbackspaniofflineanalysiscallback-interface"></a><span data-ttu-id="fc40e-103"><span id="vspixengine.iofflineanalysiscallback"></span>IOfflineAnalysisCallback 介面</span><span class="sxs-lookup"><span data-stu-id="fc40e-103"><span id="vspixengine.iofflineanalysiscallback"></span>IOfflineAnalysisCallback interface</span></span>

<span data-ttu-id="fc40e-104">回呼，以傳回離線分析資料。</span><span class="sxs-lookup"><span data-stu-id="fc40e-104">Callback to returns offline analysis data.</span></span>

## <a name="members"></a><span data-ttu-id="fc40e-105">成員</span><span class="sxs-lookup"><span data-stu-id="fc40e-105">Members</span></span>

<span data-ttu-id="fc40e-106">**IOfflineAnalysisCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="fc40e-106">The **IOfflineAnalysisCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fc40e-107">**IOfflineAnalysisCallback** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fc40e-107">**IOfflineAnalysisCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="fc40e-108">方法</span><span class="sxs-lookup"><span data-stu-id="fc40e-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="fc40e-109"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="fc40e-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="fc40e-110">**IOfflineAnalysisCallback** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="fc40e-110">The **IOfflineAnalysisCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="fc40e-111">方法</span><span class="sxs-lookup"><span data-stu-id="fc40e-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="fc40e-112">描述</span><span class="sxs-lookup"><span data-stu-id="fc40e-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="fc40e-113"><a href="/windows/desktop/direct3dtools/iofflineanalysiscallback-offlineanalysiscomplete-dword-hresult-bstr"><strong>OfflineAnalysisComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc40e-113"><a href="/windows/desktop/direct3dtools/iofflineanalysiscallback-offlineanalysiscomplete-dword-hresult-bstr"><strong>OfflineAnalysisComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="fc40e-114">用來通知主機離線分析已完成的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="fc40e-114">A callback function used to notify the host that offline analysis has completed.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="fc40e-115"><a href="/windows/desktop/direct3dtools/iofflineanalysiscallback-offlineanalysisprogress-dword-double"><strong>OfflineAnalysisProgress</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc40e-115"><a href="/windows/desktop/direct3dtools/iofflineanalysiscallback-offlineanalysisprogress-dword-double"><strong>OfflineAnalysisProgress</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="fc40e-116">用來通知主機離線分析進度的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="fc40e-116">A callback function used to notify the host of offline analysis progress.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="fc40e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc40e-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="fc40e-118">標頭</span><span class="sxs-lookup"><span data-stu-id="fc40e-118">Header</span></span></p></td><td><span data-ttu-id="fc40e-119">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="fc40e-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
