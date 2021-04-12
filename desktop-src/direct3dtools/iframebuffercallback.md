---
description: 回呼，以傳回轉譯目標。 不論引擎內 rendertarget 的格式為何，傳回轉譯目標的格式都是 R8G8B8A8 \_ UNORM。
MS-HAID: vspixengine.IFrameBufferCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IFrameBufferCallback 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 613AD7AC-0732-49E2-8155-AE0A76597BE9
api_name:
- IFrameBufferCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 565813999cda898f693aab37b24f7979896a8497
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385727"
---
# <a name="span-idvspixengineiframebuffercallbackspaniframebuffercallback-interface"></a><span data-ttu-id="3ebac-104"><span id="vspixengine.iframebuffercallback"></span>IFrameBufferCallback 介面</span><span class="sxs-lookup"><span data-stu-id="3ebac-104"><span id="vspixengine.iframebuffercallback"></span>IFrameBufferCallback interface</span></span>

<span data-ttu-id="3ebac-105">回呼，以傳回轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="3ebac-105">Callback to return a render target.</span></span> <span data-ttu-id="3ebac-106">不論引擎內 rendertarget 的格式為何，傳回轉譯目標的格式都是 R8G8B8A8 \_ UNORM。</span><span class="sxs-lookup"><span data-stu-id="3ebac-106">The format of the returned render target is R8G8B8A8\_UNORM regardless of the format of the in-engine rendertarget.</span></span>

## <a name="members"></a><span data-ttu-id="3ebac-107">成員</span><span class="sxs-lookup"><span data-stu-id="3ebac-107">Members</span></span>

<span data-ttu-id="3ebac-108">**IFrameBufferCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="3ebac-108">The **IFrameBufferCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3ebac-109">**IFrameBufferCallback** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3ebac-109">**IFrameBufferCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="3ebac-110">方法</span><span class="sxs-lookup"><span data-stu-id="3ebac-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="3ebac-111"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="3ebac-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="3ebac-112">**IFrameBufferCallback** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3ebac-112">The **IFrameBufferCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="3ebac-113">方法</span><span class="sxs-lookup"><span data-stu-id="3ebac-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="3ebac-114">描述</span><span class="sxs-lookup"><span data-stu-id="3ebac-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="3ebac-115"><a href="/windows/desktop/direct3dtools/iframebuffercallback-resultcallback-dword-dword-dword-dword-double-dword-byte-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ebac-115"><a href="/windows/desktop/direct3dtools/iframebuffercallback-resultcallback-dword-dword-dword-dword-double-dword-byte-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="3ebac-116">回呼，會通知主機相關要求所傳回的畫面格緩衝區資訊。</span><span class="sxs-lookup"><span data-stu-id="3ebac-116">A callback that notifies the host of framebuffer information returned by the associated request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="3ebac-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ebac-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="3ebac-118">標頭</span><span class="sxs-lookup"><span data-stu-id="3ebac-118">Header</span></span></p></td><td><span data-ttu-id="3ebac-119">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="3ebac-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
