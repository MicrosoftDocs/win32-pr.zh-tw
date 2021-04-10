---
title: Windows 遠端管理架構
description: Windows 遠端管理的架構是由用戶端和伺服器電腦上的元件所組成。
ms.assetid: 82e67851-fe46-4bb0-8278-9718b5e0c7ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0f5576913c5e4a1f2a105fb77e2282dc682c6659
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682829"
---
# <a name="windows-remote-management-architecture"></a><span data-ttu-id="92302-103">Windows 遠端管理架構</span><span class="sxs-lookup"><span data-stu-id="92302-103">Windows Remote Management Architecture</span></span>

<span data-ttu-id="92302-104">Windows 遠端管理的架構是由用戶端和伺服器電腦上的元件所組成。</span><span class="sxs-lookup"><span data-stu-id="92302-104">The Windows Remote Management architecture consists of components on the client and server computers.</span></span> <span data-ttu-id="92302-105">下圖顯示兩部電腦上的元件、元件與其他元件的互動方式，以及用來在電腦之間通訊的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="92302-105">The following illustration shows the components on both computers, how the components interact with other components, and the protocol that is used to communicate between the computers.</span></span>

![winrm 架構](images/winrm-architecture.png)

## <a name="requesting-client"></a><span data-ttu-id="92302-107">要求用戶端</span><span class="sxs-lookup"><span data-stu-id="92302-107">Requesting Client</span></span>

<span data-ttu-id="92302-108">下列 WinRM 元件位於執行要求資料之腳本的電腦上。</span><span class="sxs-lookup"><span data-stu-id="92302-108">The following WinRM components reside on the computer that is running the script that requests data.</span></span>

-   <span data-ttu-id="92302-109">WinRM 應用程式</span><span class="sxs-lookup"><span data-stu-id="92302-109">WinRM application</span></span>

    <span data-ttu-id="92302-110">這是腳本或 **winrm** 命令列工具，使用 WINRM 腳本 API 對要求資料進行呼叫，或執行方法。</span><span class="sxs-lookup"><span data-stu-id="92302-110">This is the script or **Winrm** command-line tool that uses the WinRM scripting API to make calls to request data or to execute methods.</span></span> <span data-ttu-id="92302-111">如需詳細資訊，請參閱 [WinRM 腳本 API](winrm-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="92302-111">For more information, see the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

-   <span data-ttu-id="92302-112">WSMAuto.dll</span><span class="sxs-lookup"><span data-stu-id="92302-112">WSMAuto.dll</span></span>

    <span data-ttu-id="92302-113">提供腳本支援的自動化層。</span><span class="sxs-lookup"><span data-stu-id="92302-113">The Automation layer that provides scripting support.</span></span>

-   <span data-ttu-id="92302-114">WsmCL.dll</span><span class="sxs-lookup"><span data-stu-id="92302-114">WsmCL.dll</span></span>

    <span data-ttu-id="92302-115">作業系統內的 C API 層。</span><span class="sxs-lookup"><span data-stu-id="92302-115">C API layer within the operating system.</span></span>

-   <span data-ttu-id="92302-116">HTTP API</span><span class="sxs-lookup"><span data-stu-id="92302-116">HTTP API</span></span>

    <span data-ttu-id="92302-117">WinRM 需要 HTTP 和 HTTPS 傳輸的支援。</span><span class="sxs-lookup"><span data-stu-id="92302-117">WinRM requires support for HTTP and HTTPS transport.</span></span>

## <a name="responding-server"></a><span data-ttu-id="92302-118">回應伺服器</span><span class="sxs-lookup"><span data-stu-id="92302-118">Responding Server</span></span>

<span data-ttu-id="92302-119">下列 WinRM 元件位於回應的電腦上。</span><span class="sxs-lookup"><span data-stu-id="92302-119">The following WinRM components reside on the responding computer.</span></span>

-   <span data-ttu-id="92302-120">HTTP API</span><span class="sxs-lookup"><span data-stu-id="92302-120">HTTP API</span></span>

    <span data-ttu-id="92302-121">WinRM 需要 HTTP 和 HTTPS 傳輸的支援。</span><span class="sxs-lookup"><span data-stu-id="92302-121">WinRM requires support for HTTP and HTTPS transport.</span></span>

-   <span data-ttu-id="92302-122">WSMAuto.dll</span><span class="sxs-lookup"><span data-stu-id="92302-122">WSMAuto.dll</span></span>

    <span data-ttu-id="92302-123">提供腳本支援的自動化層。</span><span class="sxs-lookup"><span data-stu-id="92302-123">The Automation layer that provides scripting support.</span></span>

-   <span data-ttu-id="92302-124">WsmCL.dll</span><span class="sxs-lookup"><span data-stu-id="92302-124">WsmCL.dll</span></span>

    <span data-ttu-id="92302-125">作業系統內的 C API 層。</span><span class="sxs-lookup"><span data-stu-id="92302-125">C API layer within the operating system.</span></span>

-   <span data-ttu-id="92302-126">WsmSvc.dll</span><span class="sxs-lookup"><span data-stu-id="92302-126">WsmSvc.dll</span></span>

    <span data-ttu-id="92302-127">WinRM [*接聽*](windows-remote-management-glossary.md) 程式服務。</span><span class="sxs-lookup"><span data-stu-id="92302-127">WinRM [*listener*](windows-remote-management-glossary.md) service.</span></span>

-   <span data-ttu-id="92302-128">WsmProv.dll</span><span class="sxs-lookup"><span data-stu-id="92302-128">WsmProv.dll</span></span>

    <span data-ttu-id="92302-129">提供者子系統。</span><span class="sxs-lookup"><span data-stu-id="92302-129">Provider subsystem.</span></span>

-   <span data-ttu-id="92302-130">WsmRes.dll</span><span class="sxs-lookup"><span data-stu-id="92302-130">WsmRes.dll</span></span>

    <span data-ttu-id="92302-131">資源檔。</span><span class="sxs-lookup"><span data-stu-id="92302-131">Resource file.</span></span>

-   <span data-ttu-id="92302-132">WsmWmiPl.dll</span><span class="sxs-lookup"><span data-stu-id="92302-132">WsmWmiPl.dll</span></span>

    <span data-ttu-id="92302-133">[*WMI 外掛程式*](windows-remote-management-glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="92302-133">[*WMI plug-in*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="92302-134">這可讓您透過 WinRM 取得 WMI 資料。</span><span class="sxs-lookup"><span data-stu-id="92302-134">This allows you to obtain WMI data through WinRM.</span></span>

-   <span data-ttu-id="92302-135">智慧型平臺管理介面 (IPMI) 驅動程式和 WMI IPMI 提供者</span><span class="sxs-lookup"><span data-stu-id="92302-135">Intelligent Platform Management Interface (IPMI) driver and WMI IPMI provider</span></span>

    <span data-ttu-id="92302-136">這些元件提供使用 IPMI 類別要求的任何硬體資料。</span><span class="sxs-lookup"><span data-stu-id="92302-136">These components supply any hardware data that is requested using the IPMI classes.</span></span> <span data-ttu-id="92302-137">如需詳細資訊，請參閱 [IPMI 提供者](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)。</span><span class="sxs-lookup"><span data-stu-id="92302-137">For more information, see [IPMI Provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span> <span data-ttu-id="92302-138">您必須透過載入驅動程式，以手動方式在 SMBIOS 或裝置上偵測到 BMC 硬體。</span><span class="sxs-lookup"><span data-stu-id="92302-138">BMC hardware must have been detected by the SMBIOS or the device created manually by loading the driver.</span></span> <span data-ttu-id="92302-139">如需詳細資訊，請參閱 [Windows 遠端管理的安裝和](installation-and-configuration-for-windows-remote-management.md)設定。</span><span class="sxs-lookup"><span data-stu-id="92302-139">For more information, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="92302-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="92302-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92302-141">關於 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="92302-141">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> </dl>

 

 