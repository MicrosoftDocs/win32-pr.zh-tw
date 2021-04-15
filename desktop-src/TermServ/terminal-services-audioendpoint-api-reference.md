---
title: 遠端桌面服務 AudioEndpoint API 參考
description: 支援用於音訊端點註冊和資料傳輸的介面。
ms.assetid: 0e3ea0e7-8c61-400e-b8ef-8a0403aedafa
ms.tgt_platform: multiple
keywords:
- 遠端桌面服務遠端桌面服務 AudioEndpoint API 參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1958b21643083a14110ddad77f68024cc464dd36
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372440"
---
# <a name="remote-desktop-services-audioendpoint-api-reference"></a><span data-ttu-id="b6b17-104">遠端桌面服務 AudioEndpoint API 參考</span><span class="sxs-lookup"><span data-stu-id="b6b17-104">Remote Desktop Services AudioEndpoint API reference</span></span>

<span data-ttu-id="b6b17-105">*音訊端點* 代表音訊裝置、音訊 API 或任何其他音訊來源或接收器，可用來將資料傳送到音訊引擎或從中取用資料。</span><span class="sxs-lookup"><span data-stu-id="b6b17-105">An *audio endpoint* represents an audio device, audio API, or any other audio source or sink, and is used to send data to or consume data from the audio engine.</span></span> <span data-ttu-id="b6b17-106">音訊端點必須透過 *連線連接到音訊引擎，而且* 每個連接只能有一個連接到的端點。</span><span class="sxs-lookup"><span data-stu-id="b6b17-106">An audio endpoint must be connected to the audio engine through a *connection*, and each connection can have only one endpoint connected to it.</span></span> <span data-ttu-id="b6b17-107">註冊端點之後，音訊引擎會將端點附加至連接。</span><span class="sxs-lookup"><span data-stu-id="b6b17-107">After an endpoint is registered, the audio engine attaches the endpoint to the connection.</span></span>

<span data-ttu-id="b6b17-108">每個端點物件都必須執行下列介面：</span><span class="sxs-lookup"><span data-stu-id="b6b17-108">Each endpoint object must implement the following interfaces:</span></span>

-   <span data-ttu-id="b6b17-109">[**IAudioEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint) 可讓音訊引擎取得端點的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b6b17-109">[**IAudioEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint) to enable the audio engine to get information about the endpoint.</span></span>
-   <span data-ttu-id="b6b17-110">[**IAudioEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt) 可在執行處理行程之前取得資料緩衝區的相關資訊，並在傳遞完成時通知端點。</span><span class="sxs-lookup"><span data-stu-id="b6b17-110">[**IAudioEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt) to get information about the data buffer before performing a processing pass and notifying the endpoint when the pass is complete.</span></span>
-   <span data-ttu-id="b6b17-111">[**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt)或 [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt)介面，取決於端點物件是否正在捕捉或轉譯音訊。</span><span class="sxs-lookup"><span data-stu-id="b6b17-111">Either the [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt) or [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) interface, depending on whether the endpoint object is capturing or rendering audio.</span></span>
-   [<span data-ttu-id="b6b17-112">**IAudioDeviceEndpoint**</span><span class="sxs-lookup"><span data-stu-id="b6b17-112">**IAudioDeviceEndpoint**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
-   [<span data-ttu-id="b6b17-113">**IAudioEndpointControl**</span><span class="sxs-lookup"><span data-stu-id="b6b17-113">**IAudioEndpointControl**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)

<span data-ttu-id="b6b17-114">音訊引擎會使用這些介面來取得附加至引擎之端點的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b6b17-114">The audio engine uses these interfaces to get information about the endpoints that are attached to the engine.</span></span> <span data-ttu-id="b6b17-115">端點執行必須提供機制，以便將資料傳遞至或取用來自引擎的資料（如這些介面所指定）。</span><span class="sxs-lookup"><span data-stu-id="b6b17-115">The endpoint implementation must provide the mechanism to deliver data to or consume data from the engine as specified by these interfaces.</span></span>

<span data-ttu-id="b6b17-116">遠端桌面服務 AudioEndpoint API 支援列舉類型、介面和結構。</span><span class="sxs-lookup"><span data-stu-id="b6b17-116">The Remote Desktop Services AudioEndpoint API supports enumeration types, interfaces, and structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b6b17-117">本節內容</span><span class="sxs-lookup"><span data-stu-id="b6b17-117">In this section</span></span>

-   [<span data-ttu-id="b6b17-118">遠端桌面服務 AudioEndpoint 列舉類型</span><span class="sxs-lookup"><span data-stu-id="b6b17-118">Remote Desktop Services AudioEndpoint Enumeration Types</span></span>](terminal-services-audioendpoint-enumeration-types.md)
-   [<span data-ttu-id="b6b17-119">遠端桌面服務 AudioEndpoint 函式</span><span class="sxs-lookup"><span data-stu-id="b6b17-119">Remote Desktop Services AudioEndpoint Functions</span></span>](remote-desktop-services-audioendpoint-functions.md)
-   [<span data-ttu-id="b6b17-120">遠端桌面服務 AudioEndpoint 介面</span><span class="sxs-lookup"><span data-stu-id="b6b17-120">Remote Desktop Services AudioEndpoint Interfaces</span></span>](terminal-services-audioendpoint-interfaces.md)
-   [<span data-ttu-id="b6b17-121">遠端桌面服務 AudioEndpoint 結構</span><span class="sxs-lookup"><span data-stu-id="b6b17-121">Remote Desktop Services AudioEndpoint Structures</span></span>](terminal-services-audioendpoint-structures.md)

## <a name="remarks"></a><span data-ttu-id="b6b17-122">備註</span><span class="sxs-lookup"><span data-stu-id="b6b17-122">Remarks</span></span>

<span data-ttu-id="b6b17-123">遠端桌面服務 AudioEndpoint API 適用于遠端桌面案例;它不適用於用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="b6b17-123">The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.</span></span>

 

 




