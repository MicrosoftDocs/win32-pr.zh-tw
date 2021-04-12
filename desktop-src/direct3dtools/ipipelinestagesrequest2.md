---
description: 未使用。 先前是管線階段資料的要求。
MS-HAID: vspixengine.IPipeLineStagesRequest2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesRequest2 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B40E0701-3F17-4B3A-B150-D4B243662042
api_name:
- IPipeLineStagesRequest2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9d344b7e128adf344f50a99ba41a420ca794baec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108825"
---
# <a name="span-idvspixengineipipelinestagesrequest2spanipipelinestagesrequest2-interface"></a><span data-ttu-id="5d0ae-104"><span id="vspixengine.ipipelinestagesrequest2"></span>IPipeLineStagesRequest2 介面</span><span class="sxs-lookup"><span data-stu-id="5d0ae-104"><span id="vspixengine.ipipelinestagesrequest2"></span>IPipeLineStagesRequest2 interface</span></span>

<span data-ttu-id="5d0ae-105">未使用。</span><span class="sxs-lookup"><span data-stu-id="5d0ae-105">Not used.</span></span> <span data-ttu-id="5d0ae-106">先前是管線階段資料的要求。</span><span class="sxs-lookup"><span data-stu-id="5d0ae-106">Formerly a request for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="5d0ae-107">成員</span><span class="sxs-lookup"><span data-stu-id="5d0ae-107">Members</span></span>

<span data-ttu-id="5d0ae-108">**IPipeLineStagesRequest2** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="5d0ae-108">The **IPipeLineStagesRequest2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5d0ae-109">**IPipeLineStagesRequest2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5d0ae-109">**IPipeLineStagesRequest2** also has these types of members:</span></span>

-   [<span data-ttu-id="5d0ae-110">方法</span><span class="sxs-lookup"><span data-stu-id="5d0ae-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="5d0ae-111"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="5d0ae-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="5d0ae-112">**IPipeLineStagesRequest2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="5d0ae-112">The **IPipeLineStagesRequest2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="5d0ae-113">方法</span><span class="sxs-lookup"><span data-stu-id="5d0ae-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="5d0ae-114">描述</span><span class="sxs-lookup"><span data-stu-id="5d0ae-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="5d0ae-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderdataasync-eventid-ipipelinestagescallback2-ptr-dword-dword"><strong>RequestComputeShaderDataAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d0ae-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderdataasync-eventid-ipipelinestagescallback2-ptr-dword-dword"><strong>RequestComputeShaderDataAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="5d0ae-116">針對指定分派取得計算著色器資料的非同步要求。</span><span class="sxs-lookup"><span data-stu-id="5d0ae-116">An asynchronous request to get compute shader data for the specified dispatch.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="5d0ae-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderstageasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>RequestComputeShaderStageAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d0ae-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderstageasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>RequestComputeShaderStageAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="5d0ae-118">非同步要求，以取得是否針對指定的框架和事件使用計算著色器階段。</span><span class="sxs-lookup"><span data-stu-id="5d0ae-118">An asynchronous request to get whether the compute shader stage was used for the specified frame and event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="5d0ae-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d0ae-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5d0ae-120">標頭</span><span class="sxs-lookup"><span data-stu-id="5d0ae-120">Header</span></span></p></td><td><span data-ttu-id="5d0ae-121">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="5d0ae-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
