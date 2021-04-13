---
description: 從引擎回呼，表示它已完成剖析新增至記錄檔的任何新框架。
MS-HAID: vspixengine.INewFramesCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: INewFramesCallback 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A73E1EA4-F9D5-43F1-B363-20B3F7B3D8B0
api_name:
- INewFramesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 134de14d95ceb625f1c5d4461c0b379b7f9e8a0a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385828"
---
# <a name="span-idvspixengineinewframescallbackspaninewframescallback-interface"></a><span data-ttu-id="91283-103"><span id="vspixengine.inewframescallback"></span>INewFramesCallback 介面</span><span class="sxs-lookup"><span data-stu-id="91283-103"><span id="vspixengine.inewframescallback"></span>INewFramesCallback interface</span></span>

<span data-ttu-id="91283-104">從引擎回呼，表示它已完成剖析新增至記錄檔的任何新框架。</span><span class="sxs-lookup"><span data-stu-id="91283-104">Callback from engine indicating that it is done parsing any new frames added to the log.</span></span>

## <a name="members"></a><span data-ttu-id="91283-105">成員</span><span class="sxs-lookup"><span data-stu-id="91283-105">Members</span></span>

<span data-ttu-id="91283-106">**INewFramesCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="91283-106">The **INewFramesCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="91283-107">**INewFramesCallback** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="91283-107">**INewFramesCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="91283-108">方法</span><span class="sxs-lookup"><span data-stu-id="91283-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="91283-109"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="91283-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="91283-110">**INewFramesCallback** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="91283-110">The **INewFramesCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="91283-111">方法</span><span class="sxs-lookup"><span data-stu-id="91283-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="91283-112">描述</span><span class="sxs-lookup"><span data-stu-id="91283-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="91283-113"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelall"><strong>CancelAll</strong></a></span><span class="sxs-lookup"><span data-stu-id="91283-113"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelall"><strong>CancelAll</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="91283-114">通知主機所有要求都已取消的回呼。</span><span class="sxs-lookup"><span data-stu-id="91283-114">A callback that notifies the host that all requests have been cancelled.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="91283-115"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcallback-iunknown-ptr"><strong>CancelUsingCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="91283-115"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcallback-iunknown-ptr"><strong>CancelUsingCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="91283-116">通知主機已取消要求的回呼。</span><span class="sxs-lookup"><span data-stu-id="91283-116">A callback that notifies the host of a canceled request.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="91283-117"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcookie-dword"><strong>CancelUsingCookie</strong></a></span><span class="sxs-lookup"><span data-stu-id="91283-117"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcookie-dword"><strong>CancelUsingCookie</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="91283-118">回呼，使用可唯一識別要求的 cookie 來通知主機已取消的要求。</span><span class="sxs-lookup"><span data-stu-id="91283-118">A callback that notifies the host of a canceled request by using a cookie that uniquely identifies the request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="91283-119"><a href="/windows/desktop/direct3dtools/inewframescallback-newframesavailable"><strong>NewFramesAvailable</strong></a></span><span class="sxs-lookup"><span data-stu-id="91283-119"><a href="/windows/desktop/direct3dtools/inewframescallback-newframesavailable"><strong>NewFramesAvailable</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="91283-120">回呼，會通知主機有新的框架可供處理。</span><span class="sxs-lookup"><span data-stu-id="91283-120">A callback that notifies the host that new frames are available to be processed.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="91283-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="91283-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="91283-122">標頭</span><span class="sxs-lookup"><span data-stu-id="91283-122">Header</span></span></p></td><td><span data-ttu-id="91283-123">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="91283-123">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
