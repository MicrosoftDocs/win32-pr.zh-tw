---
description: 未使用。
MS-HAID: vspixengine.IServerConnectionCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IServerConnectionCallback 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E140C0EA-2DAB-4F86-B1AE-4AE9214DE40A
api_name:
- IServerConnectionCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bdced979ce18a3a6cbb37bebf84efdfe1112d71b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109049"
---
# <a name="span-idvspixengineiserverconnectioncallbackspaniserverconnectioncallback-interface"></a><span data-ttu-id="52ed3-103"><span id="vspixengine.iserverconnectioncallback"></span>IServerConnectionCallback 介面</span><span class="sxs-lookup"><span data-stu-id="52ed3-103"><span id="vspixengine.iserverconnectioncallback"></span>IServerConnectionCallback interface</span></span>

<span data-ttu-id="52ed3-104">未使用。</span><span class="sxs-lookup"><span data-stu-id="52ed3-104">Not used.</span></span>

## <a name="members"></a><span data-ttu-id="52ed3-105">成員</span><span class="sxs-lookup"><span data-stu-id="52ed3-105">Members</span></span>

<span data-ttu-id="52ed3-106">**IServerConnectionCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="52ed3-106">The **IServerConnectionCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="52ed3-107">**IServerConnectionCallback** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="52ed3-107">**IServerConnectionCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="52ed3-108">方法</span><span class="sxs-lookup"><span data-stu-id="52ed3-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="52ed3-109"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="52ed3-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="52ed3-110">**IServerConnectionCallback** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="52ed3-110">The **IServerConnectionCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="52ed3-111">方法</span><span class="sxs-lookup"><span data-stu-id="52ed3-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="52ed3-112">描述</span><span class="sxs-lookup"><span data-stu-id="52ed3-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="52ed3-113"><a href="/windows/desktop/direct3dtools/iserverconnectioncallback-connecttoengine-bool-bstr-ipixengine-ptr-ptr"><strong>ConnectToEngine</strong></a></span><span class="sxs-lookup"><span data-stu-id="52ed3-113"><a href="/windows/desktop/direct3dtools/iserverconnectioncallback-connecttoengine-bool-bstr-ipixengine-ptr-ptr"><strong>ConnectToEngine</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="52ed3-114">連接到本機電腦上遠端引擎的另一個實例。</span><span class="sxs-lookup"><span data-stu-id="52ed3-114">Connect to another instance of a remote engine on the local machine.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="52ed3-115"><a href="/windows/desktop/direct3dtools/iserverconnectioncallback-waitforshutdown-ipixengine-ptr"><strong>WaitForShutdown</strong></a></span><span class="sxs-lookup"><span data-stu-id="52ed3-115"><a href="/windows/desktop/direct3dtools/iserverconnectioncallback-waitforshutdown-ipixengine-ptr"><strong>WaitForShutdown</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="52ed3-116">等候指定引擎的關機 (封鎖呼叫) 。</span><span class="sxs-lookup"><span data-stu-id="52ed3-116">Wait for shutdown of the specified engine (Blocking call).</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="52ed3-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="52ed3-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="52ed3-118">標頭</span><span class="sxs-lookup"><span data-stu-id="52ed3-118">Header</span></span></p></td><td><span data-ttu-id="52ed3-119">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="52ed3-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
