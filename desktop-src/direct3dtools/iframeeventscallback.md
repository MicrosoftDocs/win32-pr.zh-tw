---
description: 回呼，以傳回框架中的事件清單。
MS-HAID: vspixengine.IFrameEventsCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IFrameEventsCallback 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F40DD5DC-E78E-41F3-9D25-4D7CAE27DE45
api_name:
- IFrameEventsCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 98815681db182c99a86c05c1ea22eaad41526438
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "107001321"
---
# <a name="span-idvspixengineiframeeventscallbackspaniframeeventscallback-interface"></a><span data-ttu-id="fbfeb-103"><span id="vspixengine.iframeeventscallback"></span>IFrameEventsCallback 介面</span><span class="sxs-lookup"><span data-stu-id="fbfeb-103"><span id="vspixengine.iframeeventscallback"></span>IFrameEventsCallback interface</span></span>

<span data-ttu-id="fbfeb-104">回呼，以傳回框架中的事件清單。</span><span class="sxs-lookup"><span data-stu-id="fbfeb-104">Callback to return the list of events in a frame.</span></span>

## <a name="members"></a><span data-ttu-id="fbfeb-105">成員</span><span class="sxs-lookup"><span data-stu-id="fbfeb-105">Members</span></span>

<span data-ttu-id="fbfeb-106">**IFrameEventsCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="fbfeb-106">The **IFrameEventsCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fbfeb-107">**IFrameEventsCallback** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fbfeb-107">**IFrameEventsCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="fbfeb-108">方法</span><span class="sxs-lookup"><span data-stu-id="fbfeb-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="fbfeb-109"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="fbfeb-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="fbfeb-110">**IFrameEventsCallback** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="fbfeb-110">The **IFrameEventsCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="fbfeb-111">方法</span><span class="sxs-lookup"><span data-stu-id="fbfeb-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="fbfeb-112">描述</span><span class="sxs-lookup"><span data-stu-id="fbfeb-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="fbfeb-113"><a href="/windows/desktop/direct3dtools/iframeeventscallback-getsupportedeventcolumns-dword-eventcolumnid-arr-bstr-arr"><strong>GetSupportedEventColumns</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbfeb-113"><a href="/windows/desktop/direct3dtools/iframeeventscallback-getsupportedeventcolumns-dword-eventcolumnid-arr-bstr-arr"><strong>GetSupportedEventColumns</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="fbfeb-114">取得事件清單) 支援的事件資料行 (類型相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fbfeb-114">Gets information about which columns (types of event data) are supported by the event list.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="fbfeb-115"><a href="/windows/desktop/direct3dtools/iframeeventscallback-resultcallback-dword-dword-dword-dword-variant-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbfeb-115"><a href="/windows/desktop/direct3dtools/iframeeventscallback-resultcallback-dword-dword-dword-dword-variant-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="fbfeb-116">回呼函數，用來通知主機事件清單中事件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fbfeb-116">A callback function used to notify the host of information about events in the event list.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="fbfeb-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="fbfeb-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="fbfeb-118">標頭</span><span class="sxs-lookup"><span data-stu-id="fbfeb-118">Header</span></span></p></td><td><span data-ttu-id="fbfeb-119">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="fbfeb-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
