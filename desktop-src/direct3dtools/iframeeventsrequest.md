---
description: 要求傳回框架中的事件清單。
MS-HAID: vspixengine.IFrameEventsRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IFrameEventsRequest 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E171A94C-012F-4296-B1EC-2E814F977565
api_name:
- IFrameEventsRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a66c098c8808eadcf31d39d76a48b6185871aded
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935742"
---
# <a name="span-idvspixengineiframeeventsrequestspaniframeeventsrequest-interface"></a><span data-ttu-id="bd060-103"><span id="vspixengine.iframeeventsrequest"></span>IFrameEventsRequest 介面</span><span class="sxs-lookup"><span data-stu-id="bd060-103"><span id="vspixengine.iframeeventsrequest"></span>IFrameEventsRequest interface</span></span>

<span data-ttu-id="bd060-104">要求傳回框架中的事件清單。</span><span class="sxs-lookup"><span data-stu-id="bd060-104">Request for returning the list of events in a frame.</span></span>

## <a name="members"></a><span data-ttu-id="bd060-105">成員</span><span class="sxs-lookup"><span data-stu-id="bd060-105">Members</span></span>

<span data-ttu-id="bd060-106">**IFrameEventsRequest** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="bd060-106">The **IFrameEventsRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bd060-107">**IFrameEventsRequest** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bd060-107">**IFrameEventsRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="bd060-108">方法</span><span class="sxs-lookup"><span data-stu-id="bd060-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="bd060-109"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="bd060-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="bd060-110">**IFrameEventsRequest** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="bd060-110">The **IFrameEventsRequest** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="bd060-111">方法</span><span class="sxs-lookup"><span data-stu-id="bd060-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="bd060-112">描述</span><span class="sxs-lookup"><span data-stu-id="bd060-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="bd060-113"><a href="/windows/desktop/direct3dtools/iframeeventsrequest-requestasync-dword-dword-dword-arr-iframeeventscallback-ptr-dword-dword"><strong>RequestAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="bd060-113"><a href="/windows/desktop/direct3dtools/iframeeventsrequest-requestasync-dword-dword-dword-arr-iframeeventscallback-ptr-dword-dword"><strong>RequestAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="bd060-114">非同步要求，以取得單一指定框架的指定資訊。</span><span class="sxs-lookup"><span data-stu-id="bd060-114">An asynchronous request to get specified information about a single specified frame.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="bd060-115"><a href="/windows/desktop/direct3dtools/iframeeventsrequest-requestsupportedcolumnsasync-iframeeventscallback-ptr-dword"><strong>RequestSupportedColumnsAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="bd060-115"><a href="/windows/desktop/direct3dtools/iframeeventsrequest-requestsupportedcolumnsasync-iframeeventscallback-ptr-dword"><strong>RequestSupportedColumnsAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="bd060-116">非同步要求，以取得) 此框架事件要求類型所支援之資料行 (欄位的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bd060-116">An asynchronous request to get information about what columns (fields) this frame events request type supports.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="bd060-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd060-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="bd060-118">標頭</span><span class="sxs-lookup"><span data-stu-id="bd060-118">Header</span></span></p></td><td><span data-ttu-id="bd060-119">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="bd060-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
