---
description: 回呼，以使用其事件識別碼和框架編號傳回框架清單。
MS-HAID: vspixengine.IFrameListCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IFrameListCallback 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 16318DBE-4126-4331-B726-DCF929F712DA
api_name:
- IFrameListCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a4fe281584a9ca51d18eee22f7e9fd4a92e48f88
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385831"
---
# <a name="span-idvspixengineiframelistcallbackspaniframelistcallback-interface"></a><span data-ttu-id="0663b-103"><span id="vspixengine.iframelistcallback"></span>IFrameListCallback 介面</span><span class="sxs-lookup"><span data-stu-id="0663b-103"><span id="vspixengine.iframelistcallback"></span>IFrameListCallback interface</span></span>

<span data-ttu-id="0663b-104">回呼，以使用其事件識別碼和框架編號傳回框架清單。</span><span class="sxs-lookup"><span data-stu-id="0663b-104">Callback to return the list of frames with their event id and frame number.</span></span>

## <a name="members"></a><span data-ttu-id="0663b-105">成員</span><span class="sxs-lookup"><span data-stu-id="0663b-105">Members</span></span>

<span data-ttu-id="0663b-106">**IFrameListCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="0663b-106">The **IFrameListCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0663b-107">**IFrameListCallback** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0663b-107">**IFrameListCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="0663b-108">方法</span><span class="sxs-lookup"><span data-stu-id="0663b-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="0663b-109"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="0663b-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="0663b-110">**IFrameListCallback** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="0663b-110">The **IFrameListCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="0663b-111">方法</span><span class="sxs-lookup"><span data-stu-id="0663b-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="0663b-112">描述</span><span class="sxs-lookup"><span data-stu-id="0663b-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="0663b-113"><a href="/windows/desktop/direct3dtools/iframelistcallback-resultcallback-dword-dword-arr-dword-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="0663b-113"><a href="/windows/desktop/direct3dtools/iframelistcallback-resultcallback-dword-dword-arr-dword-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="0663b-114">回呼函式，用來通知主控制項已被捕獲的框架。</span><span class="sxs-lookup"><span data-stu-id="0663b-114">A callback function used to notify the host of which frames were captured.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="0663b-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="0663b-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="0663b-116">標頭</span><span class="sxs-lookup"><span data-stu-id="0663b-116">Header</span></span></p></td><td><span data-ttu-id="0663b-117">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="0663b-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
