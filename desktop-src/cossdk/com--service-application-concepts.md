---
description: COM + 服務應用程式概念
ms.assetid: d6b1cf4a-ca39-4d50-a33d-aa639937ef9e
title: COM + 服務應用程式概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b24db7a031ed0520f30891d98688af67e853ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468120"
---
# <a name="com-service-application-concepts"></a><span data-ttu-id="cfb7d-103">COM + 服務應用程式概念</span><span class="sxs-lookup"><span data-stu-id="cfb7d-103">COM+ Service Application Concepts</span></span>

<span data-ttu-id="cfb7d-104">您可以使用 [元件服務] 系統管理工具，將 COM + 伺服器應用程式設定為服務應用程式。</span><span class="sxs-lookup"><span data-stu-id="cfb7d-104">You can use the Component Services administrative tool to configure a COM+ server application as a service application.</span></span> <span data-ttu-id="cfb7d-105">以服務方式執行 COM + 伺服器應用程式可提供下列優點：</span><span class="sxs-lookup"><span data-stu-id="cfb7d-105">Running a COM+ server application as a service offers the following advantages:</span></span>

-   <span data-ttu-id="cfb7d-106">如果您的應用程式一律需要執行，則元件服務可以選擇性地自動啟動伺服器，也可以在伺服器超時時重新開機伺服器。例如，如果執行已排入佇列之元件接聽程式元件的電腦重新開機，則已排入佇列的元件接聽程式如果設定為服務，就可以自動啟動。</span><span class="sxs-lookup"><span data-stu-id="cfb7d-106">If your application always needs to be running, Component Services can optionally have the server started automatically and can also restart the server if it times out. For example, if a computer running Queued Components listener components is rebooted, the Queued Components listeners can be started automatically if they are configured as a service.</span></span>
-   <span data-ttu-id="cfb7d-107">如果您的應用程式需要執行特殊許可權的作業，應用程式可以執行為本機系統帳戶。</span><span class="sxs-lookup"><span data-stu-id="cfb7d-107">If your application needs to perform privileged operations, the application can run as the local system account.</span></span> <span data-ttu-id="cfb7d-108">只有 NT 服務可使用此層級的安全性來執行。</span><span class="sxs-lookup"><span data-stu-id="cfb7d-108">Only NT services are allowed to run with this level of security.</span></span> <span data-ttu-id="cfb7d-109">應用程式將與 Windows 叢集服務相容，這會在系統容錯移轉期間管理服務。</span><span class="sxs-lookup"><span data-stu-id="cfb7d-109">The application will be compatible with the Windows Cluster service, which manages services during system failover.</span></span>
-   <span data-ttu-id="cfb7d-110">如果其他服務需要標記為相依的，則元件服務會提供該選項。</span><span class="sxs-lookup"><span data-stu-id="cfb7d-110">If other services need to be marked as dependent, Component Services provides that option.</span></span> <span data-ttu-id="cfb7d-111">例如，如果您的應用程式使用其他服務所提供的功能，則會在應用程式啟動之前啟動標示為相依的服務。</span><span class="sxs-lookup"><span data-stu-id="cfb7d-111">For example, if your application makes use of functionality provided by another service, the service marked as dependent will be started before your application starts.</span></span>

## <a name="starting-an-application-automatically"></a><span data-ttu-id="cfb7d-112">自動啟動應用程式</span><span class="sxs-lookup"><span data-stu-id="cfb7d-112">Starting an Application Automatically</span></span>

<span data-ttu-id="cfb7d-113">當 COM + 伺服器應用程式自動啟動時，它的作用就像是服務，需要開發人員使用「服務」系統管理工具來管理伺服器。</span><span class="sxs-lookup"><span data-stu-id="cfb7d-113">When the COM+ server application is started automatically, it acts like a service, requiring the developer to manage the server using the Services administrative tool.</span></span>

> [!Note]  
> <span data-ttu-id="cfb7d-114">您可以啟動 [元件服務] 系統管理工具，然後按一下 [ **服務] (本機)** 來存取服務系統管理工具。</span><span class="sxs-lookup"><span data-stu-id="cfb7d-114">The Services administrative tool can be accessed by launching the Component Services administrative tool and then clicking **Services (Local)**.</span></span>

 

## <a name="starting-an-application-manually"></a><span data-ttu-id="cfb7d-115">手動啟動應用程式</span><span class="sxs-lookup"><span data-stu-id="cfb7d-115">Starting an Application Manually</span></span>

<span data-ttu-id="cfb7d-116">當 COM + 伺服器應用程式以手動方式啟動時，它的作用就像是具有服務安全性設定的 DLL 主機。</span><span class="sxs-lookup"><span data-stu-id="cfb7d-116">When the COM+ server application is started manually, it acts like a DLL host with the security settings of a service.</span></span> <span data-ttu-id="cfb7d-117">服務會在啟動時以手動方式啟動，並在發生時自動關閉。</span><span class="sxs-lookup"><span data-stu-id="cfb7d-117">The service will be started up manually when activated and shut down automatically when it times out.</span></span>

## <a name="service-configurations"></a><span data-ttu-id="cfb7d-118">服務組態</span><span class="sxs-lookup"><span data-stu-id="cfb7d-118">Service Configurations</span></span>

<span data-ttu-id="cfb7d-119">無論啟動類型為何，您都可以將應用程式設定為以本機系統帳戶執行，或指派給使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="cfb7d-119">Regardless of the startup type, the application can be configured to run as a local system account or assigned to a user account.</span></span> <span data-ttu-id="cfb7d-120">您可以在建立服務時設定本機系統和使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="cfb7d-120">The local system and user account can be configured at the time of creating the service.</span></span> <span data-ttu-id="cfb7d-121">若要設定安全性設定，必須使用「服務」系統管理工具。</span><span class="sxs-lookup"><span data-stu-id="cfb7d-121">To configure the security settings, the Services administrative tool will have to be used.</span></span> <span data-ttu-id="cfb7d-122">也可以針對服務設定相依性。</span><span class="sxs-lookup"><span data-stu-id="cfb7d-122">Dependencies can also be set for the service.</span></span>

<span data-ttu-id="cfb7d-123">您也可以從其他系統服務清單中選取 [相依性]，以任何特定順序啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="cfb7d-123">The application can also be started in any particular order by selecting dependencies from a list of other system services.</span></span> <span data-ttu-id="cfb7d-124">例如，系統服務可以標示為相依，而且在系統服務已依照指定的順序啟動之前，將不會啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="cfb7d-124">For example, the system services can be marked as dependent and will not start the application until the system services have been started in the specified order.</span></span> <span data-ttu-id="cfb7d-125">這會在使用服務應用程式之前，先將它初始化。</span><span class="sxs-lookup"><span data-stu-id="cfb7d-125">This will properly initialize the service application before it is used.</span></span>

<span data-ttu-id="cfb7d-126">如需如何將 COM + 應用程式設定為以服務方式執行的逐步指示，請參閱將 [COM + 伺服器應用程式設定為服務應用程式](configuring-a-com--server-application-as-a-service-application.md)。</span><span class="sxs-lookup"><span data-stu-id="cfb7d-126">For a step-by-step instruction on how to configure a COM+ application to run as a service, see [Configuring a COM+ Server Application as a Service Application](configuring-a-com--server-application-as-a-service-application.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cfb7d-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="cfb7d-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfb7d-128">COM + 服務應用程式工作</span><span class="sxs-lookup"><span data-stu-id="cfb7d-128">COM+ Service Application Tasks</span></span>](com--service-application-tasks.md)
</dt> </dl>

 

 



