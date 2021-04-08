---
title: BITS 上傳的 IIS 需求
description: 針對上傳，BITS 需要 Windows Server 2003 上的 IIS 6.0，以及 Windows Server 2008 上的 IIS 7.0;BITS 不支援 Windows XP 上的 IIS 5.1。
ms.assetid: 8ab07af5-3b59-4c98-8e57-f614deb8b594
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8fc1eb9bae86e7bb2635b3a250e8a9efe1bc630
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671612"
---
# <a name="iis-requirements-for-bits-uploads"></a><span data-ttu-id="807a5-103">BITS 上傳的 IIS 需求</span><span class="sxs-lookup"><span data-stu-id="807a5-103">IIS Requirements for BITS Uploads</span></span>

<span data-ttu-id="807a5-104">針對上傳，BITS 需要 Windows Server 2003 上的 IIS 6.0，以及 Windows Server 2008 上的 IIS 7.0;BITS 不支援 Windows XP 上的 IIS 5.1。</span><span class="sxs-lookup"><span data-stu-id="807a5-104">For uploads, BITS requires IIS 6.0 on Windows Server 2003, and IIS 7.0 on Windows Server 2008; BITS does not support IIS 5.1 on Windows XP.</span></span> <span data-ttu-id="807a5-105">您必須啟用 IIS 虛擬目錄的上傳功能，並設定 IIS 延伸模組的 BITS。</span><span class="sxs-lookup"><span data-stu-id="807a5-105">The IIS virtual directory must be enabled for uploads and have the BITS IIS extensions configured.</span></span>

<span data-ttu-id="807a5-106">**Windows Server 的核心安裝：** 不支援 BITS IIS 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="807a5-106">**Core installations of Windows Server:** BITS IIS extensions are not supported.</span></span>

<span data-ttu-id="807a5-107">在 Windows Server 2008 上，使用 **伺服器管理員** 安裝 BITS 伺服器擴充功能。</span><span class="sxs-lookup"><span data-stu-id="807a5-107">On Windows Server 2008, use the **Server Manager** to install the BITS Server Extensions feature.</span></span> <span data-ttu-id="807a5-108">在 **伺服器管理員** 中，按一下左窗格中的 [ **功能** ]。</span><span class="sxs-lookup"><span data-stu-id="807a5-108">From **Server Manager**, click **Features** in the left pane.</span></span> <span data-ttu-id="807a5-109">在 [ **新增功能] 嚮導** 中，檢查 [BITS 伺服器擴充功能]。</span><span class="sxs-lookup"><span data-stu-id="807a5-109">In the **Add Features Wizard**, check BITS Server Extensions.</span></span> <span data-ttu-id="807a5-110">請注意，必須安裝 IIS 6 管理相容性角色。</span><span class="sxs-lookup"><span data-stu-id="807a5-110">Note that the IIS 6 Management Compatibility roles must be installed.</span></span>

<span data-ttu-id="807a5-111">在 Windows Server 2003 上，使用 [ **Windows 元件] 嚮導** 來安裝 BITS 伺服器擴充功能。</span><span class="sxs-lookup"><span data-stu-id="807a5-111">On Windows Server 2003, use the **Windows Components Wizard** to install the BITS server extension.</span></span> <span data-ttu-id="807a5-112">從 **主控台** 中，選取 [ **新增或移除程式**]。</span><span class="sxs-lookup"><span data-stu-id="807a5-112">From **Control Panel**, select **Add or Remove Programs**.</span></span> <span data-ttu-id="807a5-113">然後，選取 [ **新增/移除 Windows 元件** ] 以顯示 [ **Windows 元件] Wizard**。</span><span class="sxs-lookup"><span data-stu-id="807a5-113">Then, select **Add/Remove Windows Components** to display the **Windows Components Wizard**.</span></span> <span data-ttu-id="807a5-114">BITS 伺服器延伸是 Internet Information Services (IIS) 的子元件，這是 Web 應用程式伺服器的子元件。</span><span class="sxs-lookup"><span data-stu-id="807a5-114">The BITS server extension is a subcomponent of Internet Information Services (IIS) which is a sub-component of Web Application Server.</span></span>

> [!Note]  
> <span data-ttu-id="807a5-115">如果重新開機 IISAdmin 服務，則必須先回收 IIS 背景工作進程，BITS 服務才能繼續上傳。</span><span class="sxs-lookup"><span data-stu-id="807a5-115">If the IISAdmin service is restarted, the IIS worker process must be recycled before the BITS service can resume uploads.</span></span> <span data-ttu-id="807a5-116">您可以使用 **IISReset.exe** 命令列公用程式，以手動方式回收 IIS 工作者進程。</span><span class="sxs-lookup"><span data-stu-id="807a5-116">The IIS worker process can be manually recycled by using the **IISReset.exe** command line utility.</span></span>

 

<span data-ttu-id="807a5-117">如需有關為上傳設定 IIS 的詳細資訊，請參閱 [設定伺服器以進行上傳](setting-up-the-server-for-uploads.md)。</span><span class="sxs-lookup"><span data-stu-id="807a5-117">For information on configuring IIS for uploads, see [Setting Up the Server for Uploads](setting-up-the-server-for-uploads.md).</span></span>

<span data-ttu-id="807a5-118">如需 BITS 新增至 IIS 之屬性的詳細資訊，請參閱 [上傳工作的 Bits 伺服器設定](bits-server-settings-for-upload-jobs.md)。</span><span class="sxs-lookup"><span data-stu-id="807a5-118">For details on the properties that BITS adds to IIS, see [BITS Server Settings for Upload Jobs](bits-server-settings-for-upload-jobs.md).</span></span>

 

 




