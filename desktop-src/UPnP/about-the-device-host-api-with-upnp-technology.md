---
title: 關於裝置主機 API
description: 具有 UPnP 技術的裝置主機 API 是在 Windows 平臺上執行以 UPnP 為基礎之裝置功能的架構。
ms.assetid: fa716c59-d3f0-4cd4-b92d-939b258b0102
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c751328696d6524208dc95a0b7961829f8ee231c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372526"
---
# <a name="about-the-device-host-api"></a><span data-ttu-id="c1902-103">關於裝置主機 API</span><span class="sxs-lookup"><span data-stu-id="c1902-103">About the Device Host API</span></span>

<span data-ttu-id="c1902-104">具有 UPnP 技術的裝置主機 API 是在 Windows 平臺上執行以 UPnP 為基礎之裝置功能的架構。</span><span class="sxs-lookup"><span data-stu-id="c1902-104">The Device Host API with UPnP technology is a framework for implementing UPnP-based device functionality on the Windows platform.</span></span> <span data-ttu-id="c1902-105">使用裝置主機 API 搭配 UPnP 技術來建立裝置 (稱為「 [*託管裝置*](h-gly.md) 」的開發人員) 只需要執行裝置的核心功能。</span><span class="sxs-lookup"><span data-stu-id="c1902-105">Developers who are creating devices by using the Device Host API with UPnP technology (referred to as [*hosted devices*](h-gly.md)) need only implement the device's core functionality.</span></span> <span data-ttu-id="c1902-106">開發人員可以依賴裝置主機來處理探索、描述、控制、事件和簡報的 UPnP 特定詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c1902-106">Developers can rely on the device host to handle the UPnP-specific details of discovery, description, control, eventing, and presentation.</span></span> <span data-ttu-id="c1902-107">裝置主機會驗證來自 UPnP 型用戶端的傳入資料，並根據 UPnP 裝置架構來格式化託管裝置上的所有傳出資料。</span><span class="sxs-lookup"><span data-stu-id="c1902-107">The device host validates incoming data from UPnP-based clients and formats all outgoing data from hosted devices according to the UPnP device architecture.</span></span>

<span data-ttu-id="c1902-108">下列各節將說明一般情況下，UPnP 裝置主機的運作方式：</span><span class="sxs-lookup"><span data-stu-id="c1902-108">The following sections explain, in general, how the UPnP device host works:</span></span>

-   [<span data-ttu-id="c1902-109">執行託管裝置</span><span class="sxs-lookup"><span data-stu-id="c1902-109">Implementing a Hosted Device</span></span>](implementing-a-hosted-device.md)
-   [<span data-ttu-id="c1902-110">向裝置主機註冊託管裝置</span><span class="sxs-lookup"><span data-stu-id="c1902-110">Registering a Hosted Device with the Device Host</span></span>](registering-a-hosted-device-with-the-device-host.md)
-   [<span data-ttu-id="c1902-111">裝置提供者</span><span class="sxs-lookup"><span data-stu-id="c1902-111">Device Providers</span></span>](device-providers.md)
-   [<span data-ttu-id="c1902-112">事件</span><span class="sxs-lookup"><span data-stu-id="c1902-112">Eventing</span></span>](eventing.md)
-   [<span data-ttu-id="c1902-113">展示</span><span class="sxs-lookup"><span data-stu-id="c1902-113">Presentation</span></span>](presentation.md)

 

 




