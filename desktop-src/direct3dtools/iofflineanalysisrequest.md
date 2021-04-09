---
description: 離線分析資料的要求。
MS-HAID: vspixengine.IOfflineAnalysisRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IOfflineAnalysisRequest 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1E438545-D4C4-45A7-918E-D3D9DC06BA08
api_name:
- IOfflineAnalysisRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 980c4d9f3b745d197789e5e450e0bf782127ca0a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846587"
---
# <a name="span-idvspixengineiofflineanalysisrequestspaniofflineanalysisrequest-interface"></a><span data-ttu-id="39bff-103"><span id="vspixengine.iofflineanalysisrequest"></span>IOfflineAnalysisRequest 介面</span><span class="sxs-lookup"><span data-stu-id="39bff-103"><span id="vspixengine.iofflineanalysisrequest"></span>IOfflineAnalysisRequest interface</span></span>

<span data-ttu-id="39bff-104">離線分析資料的要求。</span><span class="sxs-lookup"><span data-stu-id="39bff-104">Request for offline analysis data.</span></span>

## <a name="members"></a><span data-ttu-id="39bff-105">成員</span><span class="sxs-lookup"><span data-stu-id="39bff-105">Members</span></span>

<span data-ttu-id="39bff-106">**IOfflineAnalysisRequest** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="39bff-106">The **IOfflineAnalysisRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="39bff-107">**IOfflineAnalysisRequest** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="39bff-107">**IOfflineAnalysisRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="39bff-108">方法</span><span class="sxs-lookup"><span data-stu-id="39bff-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="39bff-109"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="39bff-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="39bff-110">**IOfflineAnalysisRequest** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="39bff-110">The **IOfflineAnalysisRequest** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="39bff-111">方法</span><span class="sxs-lookup"><span data-stu-id="39bff-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="39bff-112">描述</span><span class="sxs-lookup"><span data-stu-id="39bff-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="39bff-113"><a href="/windows/desktop/direct3dtools/iofflineanalysisrequest-cancelofflineanalysisasync-dword"><strong>CancelOfflineAnalysisAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="39bff-113"><a href="/windows/desktop/direct3dtools/iofflineanalysisrequest-cancelofflineanalysisasync-dword"><strong>CancelOfflineAnalysisAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="39bff-114">在離線分析要求中取消離線分析的要求。</span><span class="sxs-lookup"><span data-stu-id="39bff-114">Requests to cancel offline analysis in an offline analysis request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="39bff-115"><a href="/windows/desktop/direct3dtools/iofflineanalysisrequest-requestofflineanalysisasync-enumofflineanalysissource-bstr-bstr-dword-bstr-dword-bstr-iofflineanalysiscallback-ptr"><strong>RequestOfflineAnalysisAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="39bff-115"><a href="/windows/desktop/direct3dtools/iofflineanalysisrequest-requestofflineanalysisasync-enumofflineanalysissource-bstr-bstr-dword-bstr-dword-bstr-iofflineanalysiscallback-ptr"><strong>RequestOfflineAnalysisAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="39bff-116">要求以指定的來源、資訊清單、參數和指定的框架執行離線分析。</span><span class="sxs-lookup"><span data-stu-id="39bff-116">Requests to run offline analysis with the specified source, manifest, parameters and of the specified frame.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="39bff-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="39bff-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="39bff-118">標頭</span><span class="sxs-lookup"><span data-stu-id="39bff-118">Header</span></span></p></td><td><span data-ttu-id="39bff-119">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="39bff-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
