---
title: 委派
description: 媒體串流 API 提供下列事件處理常式函數。
ms.assetid: CDE7B829-D0D1-479D-9B35-4445E711AF58
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23fbf0f44a0822fd0c8914833b0696fcb9aacad
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507884"
---
# <a name="delegates"></a><span data-ttu-id="2925d-103">委派</span><span class="sxs-lookup"><span data-stu-id="2925d-103">Delegates</span></span>

<span data-ttu-id="2925d-104">[媒體串流 API](media-streaming-api-portal.md)提供下列事件處理常式函數。</span><span class="sxs-lookup"><span data-stu-id="2925d-104">The [Media Streaming API](media-streaming-api-portal.md) provides the following event handler functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2925d-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="2925d-105">In this section</span></span>



| <span data-ttu-id="2925d-106">主題</span><span class="sxs-lookup"><span data-stu-id="2925d-106">Topic</span></span>                                                                                   | <span data-ttu-id="2925d-107">描述</span><span class="sxs-lookup"><span data-stu-id="2925d-107">Description</span></span>                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2925d-108">[**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2925d-108">[**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85))</span></span><br/>                   | <span data-ttu-id="2925d-109">代表將處理 [**ConnectionStatusChanged**](connectionstatuschanged.md) 事件的函式，該事件會通知用戶端裝置網路線上狀態中的變更。</span><span class="sxs-lookup"><span data-stu-id="2925d-109">Represents the function that will handle the [**ConnectionStatusChanged**](connectionstatuschanged.md) event which notifies the client of changes in the device s network connection status.</span></span><br/>               |
| <span data-ttu-id="2925d-110">[**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2925d-110">[**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85))</span></span><br/>       | <span data-ttu-id="2925d-111">代表將處理 [**DeviceArrival**](devicearrival.md) 和 [**DeviceDeparture**](devicedeparture.md) 事件的函式，這些事件會通知用戶端快取裝置清單中的變更。</span><span class="sxs-lookup"><span data-stu-id="2925d-111">Represents the function that will handle the [**DeviceArrival**](devicearrival.md) and [**DeviceDeparture**](devicedeparture.md) events which notify the client of changes in the list of cached devices.</span></span><br/> |
| <span data-ttu-id="2925d-112">[**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2925d-112">[**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85))</span></span><br/> | <span data-ttu-id="2925d-113">表示將處理 [**RenderingParametersUpdate**](renderingparametersupdate.md) 事件的函式，該事件會通知用戶端任何 DMR 轉譯控制項參數的更新。</span><span class="sxs-lookup"><span data-stu-id="2925d-113">Represents the function that will handle the [**RenderingParametersUpdate**](renderingparametersupdate.md) event which notifies the client of an update to any of the DMR s rendering control parameters.</span></span><br/>  |
| <span data-ttu-id="2925d-114">[**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2925d-114">[**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85))</span></span><br/> | <span data-ttu-id="2925d-115">表示將處理 [**TransportParametersUpdate**](transportparametersupdate.md) 事件的函式，該事件會通知用戶端對任何 DMR 的傳輸參數進行更新。</span><span class="sxs-lookup"><span data-stu-id="2925d-115">Represents the function that will handle the [**TransportParametersUpdate**](transportparametersupdate.md) event which notifies the client of an update to any of the DMR s transport parameters.</span></span><br/>          |



 

 

