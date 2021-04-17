---
description: WIA 會實作為元件物件模型 (COM) 跨進程伺服器，以確保用戶端應用程式的健全運作。
ms.assetid: 9f3d1848-36ab-4e0f-a7f4-312bc85ecc00
title: WIA 架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09652258ee249fb3c68e65472e863ccd35154ee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570028"
---
# <a name="wia-architecture"></a><span data-ttu-id="b5bfa-103">WIA 架構</span><span class="sxs-lookup"><span data-stu-id="b5bfa-103">WIA Architecture</span></span>

<span data-ttu-id="b5bfa-104">WIA 會實作為元件物件模型 (COM) 跨進程伺服器，以確保用戶端應用程式的健全運作。</span><span class="sxs-lookup"><span data-stu-id="b5bfa-104">WIA is implemented as a Component Object Model (COM) out-of-process server to ensure the robust operation of client applications.</span></span> <span data-ttu-id="b5bfa-105">與大部分進程伺服器應用程式不同的是，Windows 映像取得 (WIA) 可提供自己的資料傳輸機制 [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer)，以避免在映射資料傳輸期間發生效能下降。</span><span class="sxs-lookup"><span data-stu-id="b5bfa-105">Unlike most out of process server applications, Windows Image Acquisition (WIA) avoids performance penalties during image data transfer by providing its own data transfer mechanism, [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span></span> <span data-ttu-id="b5bfa-106">這個高效能介面會使用共用記憶體視窗，將資料傳輸至用戶端。</span><span class="sxs-lookup"><span data-stu-id="b5bfa-106">This high performance interface uses a shared memory window to transfer data to the client.</span></span>

<span data-ttu-id="b5bfa-107">WIA 有三個主要元件：裝置管理員、迷你驅動程式的服務程式庫和裝置迷你驅動程式。</span><span class="sxs-lookup"><span data-stu-id="b5bfa-107">WIA has three main components: a Device Manager, a Minidriver Service Library, and a Device Minidriver.</span></span>

-   <span data-ttu-id="b5bfa-108">裝置管理員會列舉映射裝置、抓取裝置屬性、設定裝置的事件，以及建立裝置物件。</span><span class="sxs-lookup"><span data-stu-id="b5bfa-108">The Device Manager enumerates imaging devices, retrieves device properties, sets up events for devices, and creates device objects.</span></span>
-   <span data-ttu-id="b5bfa-109">迷你驅動程式服務程式庫會執行與裝置無關的所有服務。</span><span class="sxs-lookup"><span data-stu-id="b5bfa-109">The Minidriver Service Library implements all services that are device independent.</span></span>
-   <span data-ttu-id="b5bfa-110">裝置迷你驅動程式會將 WIA 屬性和命令對應到特定裝置。</span><span class="sxs-lookup"><span data-stu-id="b5bfa-110">The Device Minidriver maps WIA properties and commands to the specific device.</span></span>

<span data-ttu-id="b5bfa-111">下圖說明 WIA 架構：</span><span class="sxs-lookup"><span data-stu-id="b5bfa-111">The following diagram illustrates the WIA architecture:</span></span>

![wia 架構](images/wiarch.gif)

 

 



