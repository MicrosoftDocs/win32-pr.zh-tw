---
title: 關於 Windows 部署服務 API
description: Windows 部署服務 (WDS) 是一套可讓您部署 Windows 作業系統（特別是 Windows Vista 和更新版本以及 Windows Server 2008 和更新版本）的元件。
ms.assetid: 5742e51a-70e3-4607-bfb7-181362dfb168
keywords:
- Windows 部署服務 Windows 部署服務，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac4a904765f58ccf995c5bbc0a9413f8eb4d13c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933300"
---
# <a name="about-the-windows-deployment-services-api"></a><span data-ttu-id="67b29-104">關於 Windows 部署服務 API</span><span class="sxs-lookup"><span data-stu-id="67b29-104">About the Windows Deployment Services API</span></span>

<span data-ttu-id="67b29-105">Windows 部署服務 (WDS) 是一套可讓您部署 Windows 作業系統（特別是 Windows Vista 和更新版本以及 Windows Server 2008 和更新版本）的元件。</span><span class="sxs-lookup"><span data-stu-id="67b29-105">Windows Deployment Services (WDS) is a suite of components that enable the deployment of Windows operating systems, particularly Windows Vista and later and Windows Server 2008 and later.</span></span> <span data-ttu-id="67b29-106">您可以使用它來設定使用以網路為基礎之安裝的新電腦。</span><span class="sxs-lookup"><span data-stu-id="67b29-106">You can use it to set up new computers using network-based installations.</span></span>

<span data-ttu-id="67b29-107">Oem、系統建造商和企業 IT 專業人員，想要瞭解如何將 Windows 部署到新電腦上的詳細資訊，請參閱 [Windows 部署服務更新逐步指南](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) 和 [Windows 自動化安裝套件 (WAIK) ](https://www.microsoft.com/download/details.aspx?id=10333)中的標準 WDS 解決方案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="67b29-107">OEMs, system builders, and corporate IT professionals looking for information on how to deploy Windows onto new computers, should see the information about the standard WDS solution in the [Windows Deployment Services Update Step-by-Step Guide](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) and the [Windows Automated Installation Kit (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333).</span></span>

<span data-ttu-id="67b29-108">在無法使用標準 WDS 解決方案的環境中，WDS API 可讓您以程式設計方式存取某些 WDS 元件。</span><span class="sxs-lookup"><span data-stu-id="67b29-108">In environments where the standard WDS solution cannot be used, the WDS API enables programmatic access to some WDS components.</span></span>

-   <span data-ttu-id="67b29-109">[Windows 部署服務伺服器函數](windows-deployment-services-server-functions.md)可讓您以程式設計方式存取 WDS 開機前執行環境 (PXE) 伺服器。</span><span class="sxs-lookup"><span data-stu-id="67b29-109">The [Windows Deployment Services Server Functions](windows-deployment-services-server-functions.md) provide programmatic access to the WDS Pre-Boot Execution Environment (PXE) server.</span></span> <span data-ttu-id="67b29-110">WDS 伺服器元件包含 PXE 伺服器和簡單檔案傳輸通訊協定 (TFTP) server，以便網路將電腦開機以載入和安裝作業系統。</span><span class="sxs-lookup"><span data-stu-id="67b29-110">WDS server components include a PXE server and Trivial File Transfer Protocol (TFTP) server for network booting a computer to load and install an operating system.</span></span>
-   <span data-ttu-id="67b29-111">[Windows 部署服務用戶端](windows-deployment-services-client-functions.md)函式可讓您以程式設計方式存取 WDS 用戶端。</span><span class="sxs-lookup"><span data-stu-id="67b29-111">The [Windows Deployment Services Client Functions](windows-deployment-services-client-functions.md) provide programmatic access to the WDS client.</span></span> <span data-ttu-id="67b29-112">WDS 用戶端元件包括在 Windows 預先安裝環境內執行的圖形化使用者介面 (Windows PE) 並與伺服器元件通訊，以選取並安裝作業系統映射。</span><span class="sxs-lookup"><span data-stu-id="67b29-112">The WDS client components include a graphical user interface that runs within the Windows Pre-Installation Environment (Windows PE) and communicates with the server components to select and install an operating system image.</span></span>
-   <span data-ttu-id="67b29-113">WDS 管理元件沒有 API。</span><span class="sxs-lookup"><span data-stu-id="67b29-113">There is no API for the WDS management components.</span></span> <span data-ttu-id="67b29-114">這些元件是您用來管理伺服器、作業系統映像以及用戶端電腦帳戶的一組工具。</span><span class="sxs-lookup"><span data-stu-id="67b29-114">These components are a set of tools that you use to manage the server, operating system images, and client computer accounts.</span></span> <span data-ttu-id="67b29-115">如需 WDS 管理元件的詳細資訊，請參閱 [Windows 部署服務更新逐步指南](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="67b29-115">For more information about the WDS management components, see [The Windows Deployment Services Update Step-by-Step Guide](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)).</span></span>

<span data-ttu-id="67b29-116">WDS PXE 伺服器是由 PXE 伺服器和 PXE 提供者所組成。</span><span class="sxs-lookup"><span data-stu-id="67b29-116">The WDS PXE Server consists of a PXE server and a PXE provider.</span></span> <span data-ttu-id="67b29-117">PXE 伺服器包含核心網路功能。</span><span class="sxs-lookup"><span data-stu-id="67b29-117">The PXE server contains the core networking capability.</span></span> <span data-ttu-id="67b29-118">PXE 伺服器支援外掛程式介面，也就是所謂的 PXE 提供者。</span><span class="sxs-lookup"><span data-stu-id="67b29-118">The PXE server supports plug-in interfaces which are known as PXE providers.</span></span> <span data-ttu-id="67b29-119">此提供者模型可讓您開發自訂 PXE 解決方案，同時繼續使用核心 PXE 伺服器網路程式碼基底。</span><span class="sxs-lookup"><span data-stu-id="67b29-119">This provider model enables development of custom PXE solutions while continuing to use the core PXE server networking code base.</span></span>

-   <span data-ttu-id="67b29-120">開發人員可以使用 [Windows 部署服務 Server](windows-deployment-services-server-functions.md) 函式來撰寫自訂提供者的 DLL，以便在 WDS 伺服器上與標準開機資訊協商層（ (BINL) ）一起取代或執行。</span><span class="sxs-lookup"><span data-stu-id="67b29-120">Developers can use the [Windows Deployment Services Server Functions](windows-deployment-services-server-functions.md) to write a DLL for a custom provider to replace or run in conjunction with the standard Boot Information Negotiation Layer (BINL), on a WDS server.</span></span> <span data-ttu-id="67b29-121">例如，自訂提供者可以使用文字檔做為其資料存放區，而不是 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="67b29-121">For example, the custom provider may use a text file as its data store instead of Active Directory.</span></span>
-   <span data-ttu-id="67b29-122">開發人員可以使用 [Windows 部署服務伺服器](windows-deployment-services-server-functions.md) 函式，在已註冊之提供者的已排序清單中，撰寫在 BINL 或任何其他 PXE 提供者之前排序的篩選器提供者。</span><span class="sxs-lookup"><span data-stu-id="67b29-122">Developers can use the [Windows Deployment Services Server Functions](windows-deployment-services-server-functions.md) to write a filter provider that is sequenced before BINL, or any other PXE provider, in the ordered list of registered providers.</span></span> <span data-ttu-id="67b29-123">第二個提供者只會服務選取的 PXE 要求，而第一個提供者會處理其他要求。</span><span class="sxs-lookup"><span data-stu-id="67b29-123">The second provider then only services selected PXE requests, while the first provider handles other requests.</span></span> <span data-ttu-id="67b29-124">例如，這可以讓已排序清單中的第二個已註冊提供者提供新功能，而不會中斷第一個提供者所執行的現有 WDS 解決方案。</span><span class="sxs-lookup"><span data-stu-id="67b29-124">For example, this can enable the second registered provider in the ordered list to offer new functionality without disrupting the existing WDS solution implemented in the first provider.</span></span>

<span data-ttu-id="67b29-125">WDS 用戶端包含在 Windows 預先安裝環境內執行的圖形化使用者介面 (Windows PE) 並與伺服器元件通訊，以選取並安裝作業系統映射。</span><span class="sxs-lookup"><span data-stu-id="67b29-125">The WDS client includes a graphical user interface that runs within the Windows Pre-Installation Environment (Windows PE) and communicates with the server components to select and install an operating system image.</span></span> <span data-ttu-id="67b29-126">WDS 用戶端程式庫支援開發可使用 WDS 伺服器的自訂用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="67b29-126">The WDS client library supports the development of custom client applications that can use a WDS server.</span></span>

-   <span data-ttu-id="67b29-127">開發人員可以使用 [Windows 部署服務用戶端功能](windows-deployment-services-client-functions.md) 來撰寫自己的自訂用戶端應用程式，以取代 WDS 用戶端。</span><span class="sxs-lookup"><span data-stu-id="67b29-127">Developers can use the [Windows Deployment Services Client Functions](windows-deployment-services-client-functions.md) to write their own custom client application that replaces the WDS client.</span></span> <span data-ttu-id="67b29-128">例如，自訂應用程式可以列舉儲存在 WDS 伺服器上的映射，並將安裝進度訊息傳送至 PXE 伺服器事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="67b29-128">For example, the custom application can enumerate the images that are stored on a WDS server and send installation progress messages to the PXE server event log.</span></span>

## <a name="windows-deployment-services-samples"></a><span data-ttu-id="67b29-129">Windows 部署服務範例</span><span class="sxs-lookup"><span data-stu-id="67b29-129">Windows Deployment Services Samples</span></span>

<span data-ttu-id="67b29-130">Microsoft Windows 軟體開發套件 (SDK) 提供範例自訂 PXE 提供者、篩選提供者和 WDS 用戶端應用程式，請參閱 [microsoft Windows 軟體開發套件 (sdk) ](https://developer.microsoft.com/windows/downloads/windows-10-sdk/)。</span><span class="sxs-lookup"><span data-stu-id="67b29-130">A sample custom PXE provider, filter provider, and WDS client application is available in the Microsoft Windows Software Development Kit (SDK), see [Microsoft Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/windows-10-sdk/).</span></span>

<span data-ttu-id="67b29-131">您可以在 [桌面程式碼庫](https://github.com/microsoft/Windows-classic-samples)中，線上下載下列 WDS 範例。</span><span class="sxs-lookup"><span data-stu-id="67b29-131">You can download the following WDS samples online in the [desktop code gallery](https://github.com/microsoft/Windows-classic-samples).</span></span>

<dl>

[<span data-ttu-id="67b29-132">Windows 部署服務篩選提供者範例</span><span class="sxs-lookup"><span data-stu-id="67b29-132">Windows Deployment Services filter provider sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/FilterProvider)  
[<span data-ttu-id="67b29-133">Windows 部署服務映射列舉範例</span><span class="sxs-lookup"><span data-stu-id="67b29-133">Windows Deployment Services image enumeration sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/ImageEnumeration)  
[<span data-ttu-id="67b29-134">Windows 部署服務多播取用者範例</span><span class="sxs-lookup"><span data-stu-id="67b29-134">Windows Deployment Services multicast consumer sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Multicast/WdsProvider)  
[<span data-ttu-id="67b29-135">Windows 部署服務多播提供者範例</span><span class="sxs-lookup"><span data-stu-id="67b29-135">Windows Deployment Services multicast provider sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Multicast/WdsProvider)  
[<span data-ttu-id="67b29-136">Windows 部署服務提供者範例</span><span class="sxs-lookup"><span data-stu-id="67b29-136">Windows Deployment Services provider sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/FilterProvider)  
[<span data-ttu-id="67b29-137">Windows 部署服務傳輸管理員範例</span><span class="sxs-lookup"><span data-stu-id="67b29-137">Windows Deployment Services transport manager sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Management/WDSTransportManager)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="67b29-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="67b29-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67b29-139">使用 Windows 部署服務伺服器 API</span><span class="sxs-lookup"><span data-stu-id="67b29-139">Using the Windows Deployment Services Server API</span></span>](using-the-windows-deployment-services-server-api.md)
</dt> <dt>

[<span data-ttu-id="67b29-140">使用 Windows 部署服務用戶端 API</span><span class="sxs-lookup"><span data-stu-id="67b29-140">Using the Windows Deployment Services Client API</span></span>](using-the-windows-deployment-services-client-api.md)
</dt> </dl>

 

 