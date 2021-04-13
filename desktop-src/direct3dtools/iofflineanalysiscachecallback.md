---
description: 回呼，傳回是否快取離線要求的資訊。
MS-HAID: vspixengine.IOfflineAnalysisCacheCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IOfflineAnalysisCacheCallback 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E226B1A6-D028-4562-9C8C-D25EC91A2DB2
api_name:
- IOfflineAnalysisCacheCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e0107f97353bf7ad5b62472bc54a2b8388fb6aff
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510253"
---
# <a name="span-idvspixengineiofflineanalysiscachecallbackspaniofflineanalysiscachecallback-interface"></a><span data-ttu-id="0bb9e-103"><span id="vspixengine.iofflineanalysiscachecallback"></span>IOfflineAnalysisCacheCallback 介面</span><span class="sxs-lookup"><span data-stu-id="0bb9e-103"><span id="vspixengine.iofflineanalysiscachecallback"></span>IOfflineAnalysisCacheCallback interface</span></span>

<span data-ttu-id="0bb9e-104">回呼，傳回是否快取離線要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="0bb9e-104">Callback to return information on whether an offline request is cached or not.</span></span>

## <a name="members"></a><span data-ttu-id="0bb9e-105">成員</span><span class="sxs-lookup"><span data-stu-id="0bb9e-105">Members</span></span>

<span data-ttu-id="0bb9e-106">**IOfflineAnalysisCacheCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="0bb9e-106">The **IOfflineAnalysisCacheCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0bb9e-107">**IOfflineAnalysisCacheCallback** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0bb9e-107">**IOfflineAnalysisCacheCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="0bb9e-108">方法</span><span class="sxs-lookup"><span data-stu-id="0bb9e-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="0bb9e-109"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="0bb9e-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="0bb9e-110">**IOfflineAnalysisCacheCallback** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="0bb9e-110">The **IOfflineAnalysisCacheCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="0bb9e-111">方法</span><span class="sxs-lookup"><span data-stu-id="0bb9e-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="0bb9e-112">描述</span><span class="sxs-lookup"><span data-stu-id="0bb9e-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="0bb9e-113"><a href="/windows/desktop/direct3dtools/iofflineanalysiscachecallback-offlineanalaysisreportavailabilitycallback-dword-dword-arr"><strong>OfflineAnalaysisReportAvailabilityCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="0bb9e-113"><a href="/windows/desktop/direct3dtools/iofflineanalysiscachecallback-offlineanalaysisreportavailabilitycallback-dword-dword-arr"><strong>OfflineAnalaysisReportAvailabilityCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="0bb9e-114">回呼函式，用來通知主機有哪些框架有離線分析報表可用。</span><span class="sxs-lookup"><span data-stu-id="0bb9e-114">A callback function used to notify the host about which frames have offline analysis reports available.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="0bb9e-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="0bb9e-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="0bb9e-116">標頭</span><span class="sxs-lookup"><span data-stu-id="0bb9e-116">Header</span></span></p></td><td><span data-ttu-id="0bb9e-117">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="0bb9e-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
