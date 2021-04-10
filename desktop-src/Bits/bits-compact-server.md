---
title: BITS Compact Server
description: 背景智慧型傳送服務 (位) Compact Server 是一種獨立的 HTTP/HTTPS 檔案伺服器，可讓您在電腦之間以非同步方式傳輸有限數量的大型檔案。
ms.assetid: ab4cf901-6d93-433c-b1b2-ffa54d10725c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b40e2840c24e15379fac11a5a12ed76c225e7be5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842524"
---
# <a name="bits-compact-server"></a><span data-ttu-id="c599d-103">BITS Compact Server</span><span class="sxs-lookup"><span data-stu-id="c599d-103">BITS Compact Server</span></span>

<span data-ttu-id="c599d-104">背景智慧型傳送服務 (位) Compact Server 是一種獨立的 HTTP/HTTPS 檔案伺服器，可讓您在電腦之間以非同步方式傳輸有限數量的大型檔案。</span><span class="sxs-lookup"><span data-stu-id="c599d-104">The Background Intelligent Transfer Service (BITS) Compact Server is a stand-alone HTTP/HTTPS file server that provides the ability to transfer a limited number of large files asynchronously between computers.</span></span> <span data-ttu-id="c599d-105">Compact Server 是以 NT 服務的形式建立，並且使用 HTTP.SYS。</span><span class="sxs-lookup"><span data-stu-id="c599d-105">The Compact Server is built as an NT Service and uses HTTP.SYS.</span></span>

<span data-ttu-id="c599d-106">在下列情況下，企業和小型企業客戶會使用 BITS Compact 伺服器：</span><span class="sxs-lookup"><span data-stu-id="c599d-106">The BITS Compact Server is intended for use by enterprise and small business customers under the following conditions:</span></span>

-   <span data-ttu-id="c599d-107">預期的使用量最多可有25個 URL 群組，且每個 URL 群組都支援3個同時進行的檔案傳輸。</span><span class="sxs-lookup"><span data-stu-id="c599d-107">The anticipated usage is a maximum of 25 URL groups, and each URL group supports 3 simultaneous file transfers.</span></span>
-   <span data-ttu-id="c599d-108">在相同網域或互相信任網域中的電腦之間進行檔案傳輸。</span><span class="sxs-lookup"><span data-stu-id="c599d-108">File transfers occur between computers in the same domain or mutually trusted domains.</span></span>
-   <span data-ttu-id="c599d-109">檔案傳輸並非適用于網際網路面向的用戶端。</span><span class="sxs-lookup"><span data-stu-id="c599d-109">File transfers are not intended for Internet-facing clients.</span></span>

## <a name="installing-the-bits-compact-server"></a><span data-ttu-id="c599d-110">安裝 BITS Compact Server</span><span class="sxs-lookup"><span data-stu-id="c599d-110">Installing the BITS Compact Server</span></span>

<span data-ttu-id="c599d-111">BITS Compact Server 是選擇性的伺服器元件。</span><span class="sxs-lookup"><span data-stu-id="c599d-111">The BITS Compact Server is an optional server component.</span></span> <span data-ttu-id="c599d-112">您可以使用下列其中一個選項來安裝 BITS Compact 伺服器：</span><span class="sxs-lookup"><span data-stu-id="c599d-112">You can use one of the following options to install the BITS Compact Server:</span></span>

-   <span data-ttu-id="c599d-113">伺服器管理員</span><span class="sxs-lookup"><span data-stu-id="c599d-113">Server Manager</span></span>

-   <span data-ttu-id="c599d-114">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c599d-114">Windows PowerShell</span></span>

-   <span data-ttu-id="c599d-115">套件管理員</span><span class="sxs-lookup"><span data-stu-id="c599d-115">Package Manager</span></span>

<span data-ttu-id="c599d-116">**使用伺服器管理員安裝 BITS Compact Server**</span><span class="sxs-lookup"><span data-stu-id="c599d-116">**To install the BITS Compact Server by using Server Manager**</span></span>

1.  <span data-ttu-id="c599d-117">在 **伺服器管理員** 的 [**功能摘要**] 區段中，按一下 [**新增功能**]。</span><span class="sxs-lookup"><span data-stu-id="c599d-117">In the **Features Summary** section of the **Server Manager**, click **Add Features**.</span></span>
2.  <span data-ttu-id="c599d-118">在 [新增功能] 嚮導中，選取 **背景智慧型傳送服務 (位)** 和 **Compact Server**。</span><span class="sxs-lookup"><span data-stu-id="c599d-118">In the Add Features Wizard, select **Background Intelligent Transfer Service (BITS)** and **Compact Server**.</span></span>
3.  <span data-ttu-id="c599d-119">遵循 wizard 的指示，包括安裝必要的軟體（如有指定）。</span><span class="sxs-lookup"><span data-stu-id="c599d-119">Follow the wizard instructions, including installing the required software if indicated.</span></span>

<span data-ttu-id="c599d-120">如需詳細資訊，請參閱 **伺服器管理員** 線上說明。</span><span class="sxs-lookup"><span data-stu-id="c599d-120">For more information, see the **Server Manager** online help.</span></span>

<span data-ttu-id="c599d-121">**使用 Windows PowerShell 安裝 BITS Compact Server**</span><span class="sxs-lookup"><span data-stu-id="c599d-121">**To install the BITS Compact Server by using Windows PowerShell**</span></span>

1.  <span data-ttu-id="c599d-122">在 Windows PowerShell 命令提示字元中，輸入下列命令： **Import-module ServerManager**。</span><span class="sxs-lookup"><span data-stu-id="c599d-122">In a Windows PowerShell command prompt, type the following command: **Import-Module ServerManager**.</span></span> <span data-ttu-id="c599d-123">然後按 Enter。</span><span class="sxs-lookup"><span data-stu-id="c599d-123">Then press Enter.</span></span>
2.  <span data-ttu-id="c599d-124">輸入下列命令： **ADD-WINDOWSFEATURE BITS-Compact-Server**。</span><span class="sxs-lookup"><span data-stu-id="c599d-124">Type the following command: **Add-WindowsFeature BITS-Compact-Server**.</span></span> <span data-ttu-id="c599d-125">然後按 Enter。</span><span class="sxs-lookup"><span data-stu-id="c599d-125">Then press Enter.</span></span>

<span data-ttu-id="c599d-126">下列以文字為基礎的範例示範如何使用 Windows PowerShell Cmdlet 來安裝 BITS Compact Server。</span><span class="sxs-lookup"><span data-stu-id="c599d-126">The following text-based example demonstrates installing the BITS Compact Server using Windows PowerShell cmdlets.</span></span>

``` syntax
PS C:\> Import-Module ServerManager
PS C:\> Add-WindowsFeature BITS-Compact-Server

Success Restart Needed Exit Code Feature Result
------- -------------- --------- --------------
True    No             Success   {Compact Server}


PS C:\>
```

<span data-ttu-id="c599d-127">如需使用 Cmdlet 的詳細資訊，請參閱 [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) 檔。</span><span class="sxs-lookup"><span data-stu-id="c599d-127">For information about using cmdlets, see the [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) documentation.</span></span>

<span data-ttu-id="c599d-128">如需 Import-Module Cmdlet 的詳細資訊，請參閱 Microsoft TechNet Library 中的 [import-module](/previous-versions//dd347701(v=technet.10)) 。</span><span class="sxs-lookup"><span data-stu-id="c599d-128">For more information about the Import-Module cmdlet, see [Import-Module](/previous-versions//dd347701(v=technet.10)) in the Microsoft TechNet Library.</span></span> <span data-ttu-id="c599d-129">如需命令列的說明，請輸入 **get-help import-module**。</span><span class="sxs-lookup"><span data-stu-id="c599d-129">For help at the command line, type **get-help import-module**.</span></span>

<span data-ttu-id="c599d-130">如需 Add-WindowsFeature Cmdlet 的詳細資訊，請參閱 Microsoft TechNet Library 中的 [add-windowsfeature](/previous-versions//dd347701(v=technet.10)) 。</span><span class="sxs-lookup"><span data-stu-id="c599d-130">For more information about the Add-WindowsFeature cmdlet, see [Add-WindowsFeature](/previous-versions//dd347701(v=technet.10)) in the Microsoft TechNet Library.</span></span> <span data-ttu-id="c599d-131">如需命令列的說明，請輸入 **Get-help 附加程式**。</span><span class="sxs-lookup"><span data-stu-id="c599d-131">For help at the command line, type **get-help Add-WindowsFeature**.</span></span>

<span data-ttu-id="c599d-132">**使用封裝管理員安裝 BITS Compact Server**</span><span class="sxs-lookup"><span data-stu-id="c599d-132">**To install the BITS Compact Server by using Package Manager**</span></span>

-   <span data-ttu-id="c599d-133">輸入下列命令： **PkgMgr.exe/iu： LightweightServer**。</span><span class="sxs-lookup"><span data-stu-id="c599d-133">Enter the following command: **PkgMgr.exe /iu:LightweightServer**.</span></span>

> [!Note]  
> <span data-ttu-id="c599d-134">如果 Compact Server 服務已重新開機或電腦重新開機，則設定會遺失。</span><span class="sxs-lookup"><span data-stu-id="c599d-134">The settings are lost if the Compact Server service is restarted or if the computer is rebooted.</span></span>

 

## <a name="bits-compact-server-remote-management"></a><span data-ttu-id="c599d-135">BITS Compact Server 遠端系統管理</span><span class="sxs-lookup"><span data-stu-id="c599d-135">BITS Compact Server Remote Management</span></span>

<span data-ttu-id="c599d-136">BITS Compact Server 搭配 BITS 遠端系統管理，可提供更安全的遠端檔案傳輸。</span><span class="sxs-lookup"><span data-stu-id="c599d-136">The BITS Compact Server with BITS Remote Management enables more secure remote file transfers.</span></span> <span data-ttu-id="c599d-137">BITS 遠端系統管理使用 Windows Management Instrumentation (WMI) 提供者，讓系統管理員或控制器應用程式在用戶端上遠端建立 BITS 傳送工作，以及發佈要在 BITS Compact 伺服器上裝載的檔案。</span><span class="sxs-lookup"><span data-stu-id="c599d-137">BITS Remote Management uses a Windows Management Instrumentation (WMI) provider to let a system administrator or a controller application remotely create BITS transfer jobs on the clients and to publish files for hosting on the BITS Compact Server.</span></span> <span data-ttu-id="c599d-138">BITS 提供者也可用來讓應用程式能夠從遠端使用 BITS 用戶端搭配 BITS Compact 伺服器，以將檔案從一部遠端電腦傳送到另一部遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="c599d-138">The BITS provider can also be used to enable an application to remotely use the BITS client in conjunction with the BITS Compact Server to transfer files from one remote computer to another remote computer.</span></span>

<span data-ttu-id="c599d-139">如需詳細資訊，請參閱 [位提供者](/previous-versions/windows/desktop/bitsprov/bits-provider) 檔。</span><span class="sxs-lookup"><span data-stu-id="c599d-139">For more information, see the [BITS provider](/previous-versions/windows/desktop/bitsprov/bits-provider) documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c599d-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="c599d-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c599d-141">位提供者</span><span class="sxs-lookup"><span data-stu-id="c599d-141">BITS provider</span></span>](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> </dl>

 

 