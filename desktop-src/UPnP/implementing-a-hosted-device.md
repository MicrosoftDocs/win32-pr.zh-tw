---
title: 執行託管裝置
description: 具有 UPnP 技術的裝置主機會實行核心的 UPnP 通訊協定探索、描述、控制和事件。
ms.assetid: ab113d76-5fc9-4be2-a814-8772dd1e9600
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172e9935dcbca73dbb285ba73270375fb5bfb6cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675251"
---
# <a name="implementing-a-hosted-device"></a><span data-ttu-id="dcf74-103">執行託管裝置</span><span class="sxs-lookup"><span data-stu-id="dcf74-103">Implementing a Hosted Device</span></span>

<span data-ttu-id="dcf74-104">具有 UPnP 技術的裝置主機會實行核心的 UPnP 通訊協定：探索、描述、控制和事件。</span><span class="sxs-lookup"><span data-stu-id="dcf74-104">The device host with UPnP technology implements the core UPnP protocols: discovery, description, control, and eventing.</span></span> <span data-ttu-id="dcf74-105">執行託管裝置的開發人員只需要提供：</span><span class="sxs-lookup"><span data-stu-id="dcf74-105">The developer who implements a hosted device only needs to provide:</span></span>

-   <span data-ttu-id="dcf74-106">裝置及其服務的描述。</span><span class="sxs-lookup"><span data-stu-id="dcf74-106">A description of the device and its services.</span></span>
-   <span data-ttu-id="dcf74-107">裝置功能的實作為。</span><span class="sxs-lookup"><span data-stu-id="dcf74-107">An implementation of the device's functionality.</span></span>

<span data-ttu-id="dcf74-108">例如，時鐘裝置的開發人員必須為其提供以 UPnP 為基礎的裝置和服務描述，並可執行時鐘函式 (例如維持時間、設定時間，以及回應目前時間) 的查詢。</span><span class="sxs-lookup"><span data-stu-id="dcf74-108">For example, the developer of a clock device must provide UPnP-based device and service descriptions for it, and an implementation of the clock functions (such as keeping time, setting time, and responding to queries for the current time).</span></span> <span data-ttu-id="dcf74-109">裝置主機：</span><span class="sxs-lookup"><span data-stu-id="dcf74-109">The device host:</span></span>

-   <span data-ttu-id="dcf74-110">根據 UPnP 探索通訊協定宣佈裝置。</span><span class="sxs-lookup"><span data-stu-id="dcf74-110">Announces the device according to the UPnP discovery protocol.</span></span>
-   <span data-ttu-id="dcf74-111">回應裝置描述的查詢。</span><span class="sxs-lookup"><span data-stu-id="dcf74-111">Responds to queries for the device's description.</span></span>
-   <span data-ttu-id="dcf74-112">將控制權要求路由至裝置程式碼中執行時鐘函數的部分。</span><span class="sxs-lookup"><span data-stu-id="dcf74-112">Routes control requests to the part of the device's code that implements the clock functions.</span></span>
-   <span data-ttu-id="dcf74-113">維護服務的事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="dcf74-113">Maintains event subscriptions to services.</span></span>
-   <span data-ttu-id="dcf74-114">當服務的狀態變更時，將事件通知傳送給訂閱者。</span><span class="sxs-lookup"><span data-stu-id="dcf74-114">Sends event notifications to subscribers when the service's state changes.</span></span>

 

 




