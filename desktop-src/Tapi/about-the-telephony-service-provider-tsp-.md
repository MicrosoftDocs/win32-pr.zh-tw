---
description: TAPI 電話語音服務提供者 (TSP) 是動態連結程式庫 (DLL) ，可透過一組匯出的服務功能來支援通訊裝置控制。
ms.assetid: 6e4fb295-940e-4f76-ad43-fad7da90094a
title: '關於電話語音服務提供者 (TSP) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5200a4291bdd91aba9f93a5552fecf4b52d24ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690072"
---
# <a name="about-the-telephony-service-provider-tsp"></a><span data-ttu-id="54f48-103">關於電話語音服務提供者 (TSP) </span><span class="sxs-lookup"><span data-stu-id="54f48-103">About the Telephony Service Provider (TSP)</span></span>

<span data-ttu-id="54f48-104">\[ H323 和 IPConf Tsp 無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="54f48-104">\[ The H323 and IPConf TSPs are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="54f48-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="54f48-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="54f48-106">TAPI 電話語音服務提供者 (TSP) 是動態連結程式庫 (DLL) ，可透過一組匯出的服務功能來支援通訊裝置控制。</span><span class="sxs-lookup"><span data-stu-id="54f48-106">A TAPI telephony service provider (TSP) is a dynamic-link library (DLL) that supports communications device control through a set of exported service functions.</span></span> <span data-ttu-id="54f48-107">TAPI 應用程式使用標準化命令、TAPI 傳遞給電話語音服務提供者，而 TSP 則處理必須與裝置交換的特定命令。</span><span class="sxs-lookup"><span data-stu-id="54f48-107">A TAPI application uses standardized commands, TAPI passes in formation to the telephony service provider, and the TSP handles the specific commands that must be exchanged with the device.</span></span>

<span data-ttu-id="54f48-108">下列各節簡要說明 Microsoft Windows 所提供的 Tsp：</span><span class="sxs-lookup"><span data-stu-id="54f48-108">The following sections briefly describe the TSPs provided with Microsoft Windows:</span></span>

-   [<span data-ttu-id="54f48-109">H323 TSP</span><span class="sxs-lookup"><span data-stu-id="54f48-109">H323 TSP</span></span>](h323-tsp.md)
-   [<span data-ttu-id="54f48-110">IPConf TSP</span><span class="sxs-lookup"><span data-stu-id="54f48-110">IPConf TSP</span></span>](ipconf-tsp.md)
-   [<span data-ttu-id="54f48-111">核心模式設備磁碟機 TSP</span><span class="sxs-lookup"><span data-stu-id="54f48-111">Kernel-Mode Device Driver TSP</span></span>](kernel-mode-device-driver-tsp.md)
-   [<span data-ttu-id="54f48-112">NDIS Proxy TSP</span><span class="sxs-lookup"><span data-stu-id="54f48-112">NDIS Proxy TSP</span></span>](ndis-proxy-tsp.md)
-   [<span data-ttu-id="54f48-113">遠端 TSP</span><span class="sxs-lookup"><span data-stu-id="54f48-113">Remote TSP</span></span>](remote-tsp.md)
-   [<span data-ttu-id="54f48-114">協力廠商 TSP</span><span class="sxs-lookup"><span data-stu-id="54f48-114">Third-Party TSP</span></span>](third-party-tsp.md)
-   [<span data-ttu-id="54f48-115">Unimodem TSP</span><span class="sxs-lookup"><span data-stu-id="54f48-115">Unimodem TSP</span></span>](unimodem-tsp.md)

<span data-ttu-id="54f48-116">如需詳細資訊，請參閱目標作業系統的資源套件。</span><span class="sxs-lookup"><span data-stu-id="54f48-116">For detailed information, please see the Resource Kit for the target operating system.</span></span> <span data-ttu-id="54f48-117">專用通訊裝置的協力廠商 Tsp 通常會由製造商提供，並會與裝置一起安裝。</span><span class="sxs-lookup"><span data-stu-id="54f48-117">Third-party TSPs for specialized communications devices will typically be provided by the manufacturer and will be installed with the device.</span></span>

<span data-ttu-id="54f48-118">下列主題說明如何建立可在 Microsoft 電話語音環境內正常運作的 TSP，以及如何建立 TSP/MSP 組：</span><span class="sxs-lookup"><span data-stu-id="54f48-118">The following topics describe how to create a TSP that will function properly within the Microsoft Telephony environment, and how to create a TSP/MSP pair:</span></span>

-   [<span data-ttu-id="54f48-119">電話語音服務提供者介面 (TSPI) </span><span class="sxs-lookup"><span data-stu-id="54f48-119">Telephony Service Provider Interface (TSPI)</span></span>](telephony-service-provider-interface-tspi-.md)
-   [<span data-ttu-id="54f48-120">TSPI 參考</span><span class="sxs-lookup"><span data-stu-id="54f48-120">TSPI Reference</span></span>](tspi-reference.md)
-   [<span data-ttu-id="54f48-121">媒體服務提供者</span><span class="sxs-lookup"><span data-stu-id="54f48-121">Media Service Providers</span></span>](./media-service-providers-start-page.md)

> [!Note]  
> <span data-ttu-id="54f48-122">TSP 是使用者建立的 DLL。</span><span class="sxs-lookup"><span data-stu-id="54f48-122">A TSP is a user-created DLL.</span></span> <span data-ttu-id="54f48-123">如果您要建立64位 Windows 平臺的 TSP，您必須將它編譯為64位 DLL 或 Dll。</span><span class="sxs-lookup"><span data-stu-id="54f48-123">If you are creating a TSP for a 64-bit Windows platform, you must compile it as a 64-bit DLL or DLLs.</span></span>

 

 

 
