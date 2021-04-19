---
description: 複寫的內容
ms.assetid: d1f0bc92-37bc-4de2-876a-e6b8b09da58d
title: 複寫的內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2739cb0ff615ddc38f30a7aa9b0a572be5e28a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971319"
---
# <a name="what-gets-replicated"></a><span data-ttu-id="de763-103">複寫的內容</span><span class="sxs-lookup"><span data-stu-id="de763-103">What Gets Replicated</span></span>

## <a name="applications"></a><span data-ttu-id="de763-104">應用程式</span><span class="sxs-lookup"><span data-stu-id="de763-104">Applications</span></span>

<span data-ttu-id="de763-105">在來源電腦上安裝的所有應用程式都會進行複寫，但下列情況除外：</span><span class="sxs-lookup"><span data-stu-id="de763-105">All applications installed on the source computer are replicated except for the following:</span></span>

<dl> <dt>

<span data-ttu-id="de763-106"><span id="Non-COM__application_elements_and_dependencies"></span><span id="non-com__application_elements_and_dependencies"></span><span id="NON-COM__APPLICATION_ELEMENTS_AND_DEPENDENCIES"></span>非 COM + 應用程式元素和相依性</span><span class="sxs-lookup"><span data-stu-id="de763-106"><span id="Non-COM__application_elements_and_dependencies"></span><span id="non-com__application_elements_and_dependencies"></span><span id="NON-COM__APPLICATION_ELEMENTS_AND_DEPENDENCIES"></span>Non-COM+ application elements and dependencies</span></span>
</dt> <dd>

<span data-ttu-id="de763-107">系統管理員必須負責複寫 COM + 應用程式相依的任何資訊，但這不是應用程式本身的一部分，例如資料檔案和 Dll。</span><span class="sxs-lookup"><span data-stu-id="de763-107">The administrator is responsible for replicating anything that a COM+ application depends on but which is not properly part of the application itself, such as data files and DLLs.</span></span> <span data-ttu-id="de763-108">COMREPL 不會在 COM + 應用程式元素之外複寫任何專案。</span><span class="sxs-lookup"><span data-stu-id="de763-108">COMREPL will not replicate anything outside of COM+ application elements.</span></span>

</dd> <dt>

<span data-ttu-id="de763-109"><span id="COM__preinstalled_applications"></span><span id="com__preinstalled_applications"></span><span id="COM__PREINSTALLED_APPLICATIONS"></span>COM + 預先安裝的應用程式</span><span class="sxs-lookup"><span data-stu-id="de763-109"><span id="COM__preinstalled_applications"></span><span id="com__preinstalled_applications"></span><span id="COM__PREINSTALLED_APPLICATIONS"></span>COM+ preinstalled applications</span></span>
</dt> <dd>

<span data-ttu-id="de763-110">COM + 所使用並透過 COM + 安裝程式安裝的應用程式，則不會進行複寫。</span><span class="sxs-lookup"><span data-stu-id="de763-110">Applications that are used internally by COM+ and are installed via the COM+ setup program are not replicated.</span></span> <span data-ttu-id="de763-111">這些選項包括：</span><span class="sxs-lookup"><span data-stu-id="de763-111">These include the following:</span></span>

-   <span data-ttu-id="de763-112">系統應用程式</span><span class="sxs-lookup"><span data-stu-id="de763-112">System application</span></span>
-   <span data-ttu-id="de763-113">COM + 公用程式</span><span class="sxs-lookup"><span data-stu-id="de763-113">COM+ utilities</span></span>
-   <span data-ttu-id="de763-114">COM + QC 無效信件佇列接聽程式</span><span class="sxs-lookup"><span data-stu-id="de763-114">COM+ QC Dead Letter Queue Listener</span></span>

</dd> <dt>

<span data-ttu-id="de763-115"><span id="Applications_created_by_IIS"></span><span id="applications_created_by_iis"></span><span id="APPLICATIONS_CREATED_BY_IIS"></span>IIS 所建立的應用程式</span><span class="sxs-lookup"><span data-stu-id="de763-115"><span id="Applications_created_by_IIS"></span><span id="applications_created_by_iis"></span><span id="APPLICATIONS_CREATED_BY_IIS"></span>Applications created by IIS</span></span>
</dt> <dd>

<span data-ttu-id="de763-116">這些應用程式不會複寫，並包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="de763-116">These applications are not replicated and include the following:</span></span>

-   <span data-ttu-id="de763-117">IIS 同進程應用程式</span><span class="sxs-lookup"><span data-stu-id="de763-117">IIS in-process applications</span></span>
-   <span data-ttu-id="de763-118">IIS 公用程式</span><span class="sxs-lookup"><span data-stu-id="de763-118">IIS utilities</span></span>
-   <span data-ttu-id="de763-119">針對隔離或集區虛擬根目錄建立的所有應用程式</span><span class="sxs-lookup"><span data-stu-id="de763-119">All applications created for isolated or pooled virtual roots</span></span>

</dd> </dl>

## <a name="computer-list"></a><span data-ttu-id="de763-120">電腦清單</span><span class="sxs-lookup"><span data-stu-id="de763-120">Computer List</span></span>

<span data-ttu-id="de763-121">在 [元件服務] 系統管理工具的 [ **電腦** ] 資料夾中指定的遠端電腦，將不會從來源複寫到目的電腦。</span><span class="sxs-lookup"><span data-stu-id="de763-121">The remote computers named in the **Computers** folder in the Component Services administration tool will not be replicated from source to target computer.</span></span>

## <a name="properties"></a><span data-ttu-id="de763-122">屬性</span><span class="sxs-lookup"><span data-stu-id="de763-122">Properties</span></span>

<span data-ttu-id="de763-123">以下是複寫的 **LocalComputer** 集合屬性：</span><span class="sxs-lookup"><span data-stu-id="de763-123">The following **LocalComputer** collection properties are replicated:</span></span>

-   <span data-ttu-id="de763-124">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="de763-124">TransactionTimeout</span></span>
-   <span data-ttu-id="de763-125">ResourcePoolingEnabled</span><span class="sxs-lookup"><span data-stu-id="de763-125">ResourcePoolingEnabled</span></span>
-   <span data-ttu-id="de763-126">DCOMEnabled</span><span class="sxs-lookup"><span data-stu-id="de763-126">DCOMEnabled</span></span>
-   <span data-ttu-id="de763-127">DefaultAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="de763-127">DefaultAuthenticationLevel</span></span>
-   <span data-ttu-id="de763-128">DefaultImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="de763-128">DefaultImpersonationLevel</span></span>
-   <span data-ttu-id="de763-129">SecurityTrackingEnabled</span><span class="sxs-lookup"><span data-stu-id="de763-129">SecurityTrackingEnabled</span></span>
-   <span data-ttu-id="de763-130">CISEnabled</span><span class="sxs-lookup"><span data-stu-id="de763-130">CISEnabled</span></span>
-   <span data-ttu-id="de763-131">SecureReferencesEnabled</span><span class="sxs-lookup"><span data-stu-id="de763-131">SecureReferencesEnabled</span></span>
-   <span data-ttu-id="de763-132">InternetPortsListed</span><span class="sxs-lookup"><span data-stu-id="de763-132">InternetPortsListed</span></span>
-   <span data-ttu-id="de763-133">DeafultToInternetPorts</span><span class="sxs-lookup"><span data-stu-id="de763-133">DeafultToInternetPorts</span></span>
-   <span data-ttu-id="de763-134">連接埠</span><span class="sxs-lookup"><span data-stu-id="de763-134">Ports</span></span>
-   <span data-ttu-id="de763-135">RpcProxyEnabled</span><span class="sxs-lookup"><span data-stu-id="de763-135">RpcProxyEnabled</span></span>

<span data-ttu-id="de763-136">下列 **LocalComputer** 集合屬性不會複寫：</span><span class="sxs-lookup"><span data-stu-id="de763-136">The following **LocalComputer** collection properties are not replicated:</span></span>

-   <span data-ttu-id="de763-137">Description</span><span class="sxs-lookup"><span data-stu-id="de763-137">Description</span></span>
-   <span data-ttu-id="de763-138">ApplicationProxyRSN</span><span class="sxs-lookup"><span data-stu-id="de763-138">ApplicationProxyRSN</span></span>
-   <span data-ttu-id="de763-139">IsRouter</span><span class="sxs-lookup"><span data-stu-id="de763-139">IsRouter</span></span>

<span data-ttu-id="de763-140">如需 **LocalComputer** 集合屬性的說明，請參閱 [**LocalComputer**](localcomputer.md)。</span><span class="sxs-lookup"><span data-stu-id="de763-140">For descriptions of the **LocalComputer** collection properties, see [**LocalComputer**](localcomputer.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="de763-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="de763-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de763-142">檔案管理</span><span class="sxs-lookup"><span data-stu-id="de763-142">File Management</span></span>](file-management.md)
</dt> <dt>

[<span data-ttu-id="de763-143">記錄和錯誤報表</span><span class="sxs-lookup"><span data-stu-id="de763-143">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)
</dt> <dt>

[<span data-ttu-id="de763-144">複寫階段</span><span class="sxs-lookup"><span data-stu-id="de763-144">Replication Phases</span></span>](replication-phases.md)
</dt> <dt>

[<span data-ttu-id="de763-145">使用 COMREPL</span><span class="sxs-lookup"><span data-stu-id="de763-145">Using COMREPL</span></span>](using-comrepl.md)
</dt> </dl>

 

 



