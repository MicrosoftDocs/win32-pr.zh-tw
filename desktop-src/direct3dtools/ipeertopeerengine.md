---
description: 遠端通訊 vsglog 相關資料的介面。
MS-HAID: vspixengine.IPeerToPeerEngine
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPeerToPeerEngine 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C6C4783F-ED46-47C2-98BB-C618897F8FF8
api_name:
- IPeerToPeerEngine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 899e5eea28ffb769e082b2e0bd7bc165889b2d37
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973349"
---
# <a name="span-idvspixengineipeertopeerenginespanipeertopeerengine-interface"></a><span data-ttu-id="ecad5-103"><span id="vspixengine.ipeertopeerengine"></span>IPeerToPeerEngine 介面</span><span class="sxs-lookup"><span data-stu-id="ecad5-103"><span id="vspixengine.ipeertopeerengine"></span>IPeerToPeerEngine interface</span></span>

<span data-ttu-id="ecad5-104">遠端通訊 vsglog 相關資料的介面。</span><span class="sxs-lookup"><span data-stu-id="ecad5-104">Interface for remote communicating data about a vsglog.</span></span>

## <a name="members"></a><span data-ttu-id="ecad5-105">成員</span><span class="sxs-lookup"><span data-stu-id="ecad5-105">Members</span></span>

<span data-ttu-id="ecad5-106">**IPeerToPeerEngine** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="ecad5-106">The **IPeerToPeerEngine** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ecad5-107">**IPeerToPeerEngine** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ecad5-107">**IPeerToPeerEngine** also has these types of members:</span></span>

-   [<span data-ttu-id="ecad5-108">方法</span><span class="sxs-lookup"><span data-stu-id="ecad5-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="ecad5-109"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="ecad5-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="ecad5-110">**IPeerToPeerEngine** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="ecad5-110">The **IPeerToPeerEngine** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="ecad5-111">方法</span><span class="sxs-lookup"><span data-stu-id="ecad5-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="ecad5-112">描述</span><span class="sxs-lookup"><span data-stu-id="ecad5-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="ecad5-113"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-cancelsetplaybackendpoint"><strong>CancelSetPlaybackEndpoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="ecad5-113"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-cancelsetplaybackendpoint"><strong>CancelSetPlaybackEndpoint</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ecad5-114">取消先前的要求以設定遠端連線。</span><span class="sxs-lookup"><span data-stu-id="ecad5-114">Cancels a previous request to set up a remote connection.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="ecad5-115"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-getplaybackendpoint-bool-bstr-ptr-bstr-ptr-remotingversion-ptr"><strong>GetPlaybackEndpoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="ecad5-115"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-getplaybackendpoint-bool-bstr-ptr-bstr-ptr-remotingversion-ptr"><strong>GetPlaybackEndpoint</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ecad5-116">取得遠端引擎的端點位址。</span><span class="sxs-lookup"><span data-stu-id="ecad5-116">Gets the endpoint address of a remote engine.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="ecad5-117"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-setplaybackendpoint-bool-bstr-bstr-remotingversion"><strong>SetPlaybackEndpoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="ecad5-117"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-setplaybackendpoint-bool-bstr-bstr-remotingversion"><strong>SetPlaybackEndpoint</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ecad5-118">設定用來連接到遠端引擎的端點位址。</span><span class="sxs-lookup"><span data-stu-id="ecad5-118">Sets the endpoint address used to connect to a remote engine.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="ecad5-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="ecad5-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ecad5-120">標頭</span><span class="sxs-lookup"><span data-stu-id="ecad5-120">Header</span></span></p></td><td><span data-ttu-id="ecad5-121">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="ecad5-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
