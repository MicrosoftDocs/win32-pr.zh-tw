---
description: Microsoft 電話語音程式設計模型將通訊控制項從裝置控制抽象化，釋出使用者的應用程式和裝置製造商，從密集建置到三月的需要。
ms.assetid: 07dd8447-08dc-4ae3-9a22-70e914c392db
title: Microsoft 電話語音程式設計模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0efb8947f3b428ab4a252301e3fdd5f94e29f6ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986285"
---
# <a name="microsoft-telephony-programming-model"></a><span data-ttu-id="0c725-103">Microsoft 電話語音程式設計模型</span><span class="sxs-lookup"><span data-stu-id="0c725-103">Microsoft Telephony Programming Model</span></span>

<span data-ttu-id="0c725-104">Microsoft 電話語音程式設計模型將通訊控制項從裝置控制抽象化，釋出使用者的應用程式和裝置製造商，從密集建置到三月的需要。</span><span class="sxs-lookup"><span data-stu-id="0c725-104">The Microsoft Telephony programming model abstracts communications control from device control, freeing end-user applications and device manufacturers from the need to march in lockstep.</span></span> <span data-ttu-id="0c725-105">使用此模型時，使用者或伺服器應用程式不需要裝置控制的詳細資訊，且裝置不需要針對應用程式量身打造。</span><span class="sxs-lookup"><span data-stu-id="0c725-105">Using this model, an end-user or server application does not require detailed information on device control and the device does not need to be tailored to the application.</span></span> <span data-ttu-id="0c725-106">應用程式和裝置可以進行創新和變更，而不會對客戶呈現彼此的效用。</span><span class="sxs-lookup"><span data-stu-id="0c725-106">Applications and devices can undergo innovation and change without rendering each other useless to customers.</span></span>

<span data-ttu-id="0c725-107">下圖說明如何完成此抽象概念。</span><span class="sxs-lookup"><span data-stu-id="0c725-107">The following diagram illustrates how this abstraction is accomplished.</span></span>

![tapi 如何從裝置控制將通訊控制抽象化](images/tapicomp.png)

<span data-ttu-id="0c725-109">您可以將這些元件視為專門知識的儲存機制。</span><span class="sxs-lookup"><span data-stu-id="0c725-109">These components can be viewed as repositories of specialized knowledge.</span></span> <span data-ttu-id="0c725-110">電話語音應用程式開發介面 (TAPI) 應用程式知道使用者需求、TAPI DLL 和 TAPISRV 瞭解一般電話語音，而服務提供者 (TSP 和 MSP) 瞭解詳細的裝置控制項。</span><span class="sxs-lookup"><span data-stu-id="0c725-110">The Telephony Application Programming Interface (TAPI) application knows user needs, the TAPI DLL and TAPISRV understand general telephony, and the service providers (TSP and MSP) know detailed device control.</span></span> <span data-ttu-id="0c725-111">應用程式撰寫者和裝置製造商只需要對彼此需求的一般知識。</span><span class="sxs-lookup"><span data-stu-id="0c725-111">Application writers and device manufacturers require only general knowledge of each other's requirements.</span></span>

-   <span data-ttu-id="0c725-112">應用程式會將 TAPI DLL 載入其進程空間，並使用 TAPI 來溝通需求。</span><span class="sxs-lookup"><span data-stu-id="0c725-112">An application loads the TAPI DLL into its process space and uses TAPI to communicate needs.</span></span>
-   <span data-ttu-id="0c725-113">TAPI 會建立與 TAPI 伺服器的 RPC 連結通訊。</span><span class="sxs-lookup"><span data-stu-id="0c725-113">TAPI establishes an RPC link communications with the TAPI Server.</span></span>
-   <span data-ttu-id="0c725-114">此外，TAPI 3.x 會建立 MSP 物件，並使用一組已定義的命令、媒體服務提供者介面 (MSPI) 來與其通訊。</span><span class="sxs-lookup"><span data-stu-id="0c725-114">In addition, TAPI 3.x creates an MSP object and communicates with it using a defined set of commands, the Media Service Provider Interface (MSPI).</span></span>
-   <span data-ttu-id="0c725-115">當應用程式呼叫 TAPI 操作時，TAPI 動態連結程式庫會驗證並封送處理參數，然後將資訊轉送至 TAPISRV。</span><span class="sxs-lookup"><span data-stu-id="0c725-115">When an application calls a TAPI operation, the TAPI dynamic-link library validates and marshals the parameters, then forwards the information to TAPISRV.</span></span>
-   <span data-ttu-id="0c725-116">TAPISRV 會使用電話語音服務提供者 (TSPI)  (Tsp) ，追蹤本機電腦可用的通訊資源，以及與電話語音服務提供者的介面。</span><span class="sxs-lookup"><span data-stu-id="0c725-116">TAPISRV tracks communications resources available to the local machine and interfaces with the Telephony Service Providers (TSPs) using the Telephony Service Provider Interface (TSPI).</span></span>
-   <span data-ttu-id="0c725-117">TSP 和 MSP 之間的通訊會使用透過 TAPI DLL 和 TAPISRV 傳遞的虛擬連線進行。</span><span class="sxs-lookup"><span data-stu-id="0c725-117">Communications between a TSP and an MSP take place using a virtual connection that passes through the TAPI DLL and TAPISRV.</span></span>
-   <span data-ttu-id="0c725-118">TSP/MSP 組會提供裝置狀態和功能的相關資訊，並執行所需回應所需的特定命令。</span><span class="sxs-lookup"><span data-stu-id="0c725-118">The TSP/MSP pair supplies information on device state and capabilities and implements the specific commands required for a desired response.</span></span>

<span data-ttu-id="0c725-119">使用此程式設計模型的結果是應用程式可以忽略或調整裝置變更，而新的裝置可以立即使用，而不是等候程式碼基底變更。</span><span class="sxs-lookup"><span data-stu-id="0c725-119">The result of using this programming model is that applications can ignore or adjust to device changes and new devices can be instantly useful instead of waiting on code base changes.</span></span> <span data-ttu-id="0c725-120">應用程式撰寫者和裝置製造商都能擴展潛在的市場佔有率。</span><span class="sxs-lookup"><span data-stu-id="0c725-120">Potential market share is expanded for both application writers and device manufacturers.</span></span>

<span data-ttu-id="0c725-121">下列主題會更詳細地說明 Microsoft 電話語音元件：</span><span class="sxs-lookup"><span data-stu-id="0c725-121">The following topics describe the Microsoft Telephony components in more detail:</span></span>

-   [<span data-ttu-id="0c725-122">TAPI 應用程式</span><span class="sxs-lookup"><span data-stu-id="0c725-122">TAPI Applications</span></span>](tapi-applications.md)
-   [<span data-ttu-id="0c725-123">TAPI DLL</span><span class="sxs-lookup"><span data-stu-id="0c725-123">TAPI DLL</span></span>](tapi-dll.md)
-   [<span data-ttu-id="0c725-124">TAPI 伺服器</span><span class="sxs-lookup"><span data-stu-id="0c725-124">TAPI Server</span></span>](tapi-server.md)
-   [<span data-ttu-id="0c725-125">服務提供者</span><span class="sxs-lookup"><span data-stu-id="0c725-125">Service Providers</span></span>](service-providers.md)
-   [<span data-ttu-id="0c725-126">同步/非同步模型</span><span class="sxs-lookup"><span data-stu-id="0c725-126">Synchronous/Asynchronous Model</span></span>](synchronous-asynchronous-model.md)
-   [<span data-ttu-id="0c725-127">TAPI 資料結構</span><span class="sxs-lookup"><span data-stu-id="0c725-127">TAPI Data Structures</span></span>](tapi-data-structures.md)
-   [<span data-ttu-id="0c725-128">服務的 TAPI 等級</span><span class="sxs-lookup"><span data-stu-id="0c725-128">TAPI Levels of Service</span></span>](tapi-levels-of-service.md)

 

 



