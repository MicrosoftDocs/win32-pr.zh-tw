---
description: COM + 應用程式的類型
ms.assetid: 4b731f22-6837-4c03-9c8c-a76451369cf1
title: COM + 應用程式的類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fb365863ee2b2fbe41997facdf21d84866af1f6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973391"
---
# <a name="types-of-com-applications"></a><span data-ttu-id="03e46-103">COM + 應用程式的類型</span><span class="sxs-lookup"><span data-stu-id="03e46-103">Types of COM+ Applications</span></span>

<span data-ttu-id="03e46-104">以下是四種基本的 COM + 應用程式類型：</span><span class="sxs-lookup"><span data-stu-id="03e46-104">Following are the four basic types of COM+ applications:</span></span>

-   <span data-ttu-id="03e46-105">**伺服器應用程式。**</span><span class="sxs-lookup"><span data-stu-id="03e46-105">**Server applications.**</span></span> <span data-ttu-id="03e46-106">COM + *伺服器應用程式* 會在自己的進程中執行。</span><span class="sxs-lookup"><span data-stu-id="03e46-106">A COM+ *server application* runs in its own process.</span></span> <span data-ttu-id="03e46-107">伺服器應用程式可支援所有 COM + 服務。</span><span class="sxs-lookup"><span data-stu-id="03e46-107">Server applications can support all COM+ services.</span></span>
-   <span data-ttu-id="03e46-108">**程式庫應用程式。**</span><span class="sxs-lookup"><span data-stu-id="03e46-108">**Library applications.**</span></span> <span data-ttu-id="03e46-109">COM + 連結 *庫應用程式* 是在建立它的用戶端的進程中執行。</span><span class="sxs-lookup"><span data-stu-id="03e46-109">A COM+ *library application* runs in the process of the client that creates it.</span></span> <span data-ttu-id="03e46-110">更具體來說，程式庫應用程式中的元件一律會載入至建立者的進程。</span><span class="sxs-lookup"><span data-stu-id="03e46-110">More specifically, the components in a library application are always loaded into the process of the creator.</span></span> <span data-ttu-id="03e46-111">程式庫應用程式未與伺服器進程明確相關聯。</span><span class="sxs-lookup"><span data-stu-id="03e46-111">Library applications are not explicitly associated with a server process.</span></span> <span data-ttu-id="03e46-112">他們可以使用以角色為基礎的安全性，但不支援遠端存取或已排入佇列的元件。</span><span class="sxs-lookup"><span data-stu-id="03e46-112">They can use role-based security but do not support remote access or queued components.</span></span>
-   <span data-ttu-id="03e46-113">**應用程式 proxy。**</span><span class="sxs-lookup"><span data-stu-id="03e46-113">**Application proxies.**</span></span> <span data-ttu-id="03e46-114">*應用程式 proxy* 是一組檔案，其中包含可讓用戶端從遠端存取服務器應用程式的註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="03e46-114">An *application proxy* is a set of files containing registration information that allows a client to remotely access a server application.</span></span> <span data-ttu-id="03e46-115">在用戶端電腦上執行時，應用程式 proxy 檔案會將 COM + 伺服器應用程式的相關資訊（包括 Clsid、Progid、RemoteServerName 和封送處理資訊）寫入用戶端電腦。</span><span class="sxs-lookup"><span data-stu-id="03e46-115">When run on a client computer, an application proxy file writes information about the COM+ server application, including CLSIDs, ProgIDs, RemoteServerName, and marshaling information, to the client computer.</span></span> <span data-ttu-id="03e46-116">然後可以從用戶端電腦遠端存取服務器應用程式。</span><span class="sxs-lookup"><span data-stu-id="03e46-116">The server application can then be accessed remotely from the client computer.</span></span>
-   <span data-ttu-id="03e46-117">**Com + 預先安裝的應用程式**。</span><span class="sxs-lookup"><span data-stu-id="03e46-117">**COM+ preinstalled applications**.</span></span> <span data-ttu-id="03e46-118">COM + 包含一組預先安裝的應用程式，可處理內建函式。</span><span class="sxs-lookup"><span data-stu-id="03e46-118">COM+ includes a set of preinstalled applications that handle internal functions.</span></span> <span data-ttu-id="03e46-119">預先安裝的應用程式會列在 [元件服務] 系統管理工具的 [COM + 應用程式] 資料夾中，但無法修改或刪除這些應用程式。</span><span class="sxs-lookup"><span data-stu-id="03e46-119">The preinstalled applications are listed in the COM+ Applications folder in the Component Services administrative tool, but they cannot be modified or deleted.</span></span> <span data-ttu-id="03e46-120">這些應用程式包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="03e46-120">These applications include the following:</span></span>
    -   <span data-ttu-id="03e46-121">.NET 公用程式</span><span class="sxs-lookup"><span data-stu-id="03e46-121">.NET Utilities</span></span>
    -   <span data-ttu-id="03e46-122">分析器控制項發行者應用程式</span><span class="sxs-lookup"><span data-stu-id="03e46-122">Analyzer Control Publisher Application</span></span>
    -   <span data-ttu-id="03e46-123">COM + Explorer</span><span class="sxs-lookup"><span data-stu-id="03e46-123">COM+ Explorer</span></span>
    -   <span data-ttu-id="03e46-124">COM + QC 無效信件佇列接聽程式</span><span class="sxs-lookup"><span data-stu-id="03e46-124">COM+ QC Dead Letter Queue Listener</span></span>
    -   <span data-ttu-id="03e46-125">COM + 公用程式</span><span class="sxs-lookup"><span data-stu-id="03e46-125">COM+ Utilities</span></span>
    -   <span data-ttu-id="03e46-126">IIS In-Process 應用程式</span><span class="sxs-lookup"><span data-stu-id="03e46-126">IIS In-Process Applications</span></span>
    -   <span data-ttu-id="03e46-127">IIS 跨進程集區應用程式</span><span class="sxs-lookup"><span data-stu-id="03e46-127">IIS Out-Of-Process Pooled Applications</span></span>
    -   <span data-ttu-id="03e46-128">系統應用程式</span><span class="sxs-lookup"><span data-stu-id="03e46-128">System Application</span></span>

## <a name="notes"></a><span data-ttu-id="03e46-129">備註</span><span class="sxs-lookup"><span data-stu-id="03e46-129">Notes</span></span>

<span data-ttu-id="03e46-130">從 Windows Server 2003，即使已停用系統應用程式，也可以執行 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="03e46-130">As of Windows Server 2003, it is possible to run COM+ applications even if the System Application is disabled.</span></span> <span data-ttu-id="03e46-131">COM + 應用程式將會執行，但不會有系統應用程式通常提供的服務。</span><span class="sxs-lookup"><span data-stu-id="03e46-131">The COM+ applications will run, though without the services usually provided by the System Application.</span></span> <span data-ttu-id="03e46-132">這些服務包括使用元件服務系統管理工具和系統事件追蹤。</span><span class="sxs-lookup"><span data-stu-id="03e46-132">These services include use of the Component Services administrative tool and system event tracking.</span></span>

<span data-ttu-id="03e46-133">此外，從 Windows Server 2003，COM + 系統應用程式的驗證功能包含 EOAC \_ DISABLE AAA 的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="03e46-133">Also as of Windows Server 2003, the authentication capability for the COM+ System Application includes the value EOAC\_DISABLE\_AAA.</span></span> <span data-ttu-id="03e46-134">此值會在啟動系統應用程式時，將 CoInitializeSecurity 函式與[](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)函式搭配使用，以停用啟動為啟動 (AAA) 啟用。</span><span class="sxs-lookup"><span data-stu-id="03e46-134">This value, which disables activate-as-activator (AAA) activations, is used with the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) function when launching the System Application.</span></span> <span data-ttu-id="03e46-135">將驗證功能設定為 EOAC \_ DISABLE \_ AAA，可讓在特殊許可權帳戶下執行的應用程式 (例如 LocalSystem) ，以協助防止其身分識別用來啟動未受信任的元件。</span><span class="sxs-lookup"><span data-stu-id="03e46-135">Setting the authentication capability to EOAC\_DISABLE\_AAA allows an application that runs under a privileged account (such as LocalSystem) to help prevent its identity from being used to launch untrusted components.</span></span>

 

 
