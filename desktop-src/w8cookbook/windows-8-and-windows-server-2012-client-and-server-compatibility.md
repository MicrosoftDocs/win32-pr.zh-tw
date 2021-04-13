---
title: 用戶端與伺服器相容性-Windows 8
description: Windows 8 和 Windows Server 2012 用戶端和伺服器相容性
ms.assetid: 5067219A-EBA2-4FAF-8C17-7AB22C5EADD0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca5b685ae10b97a7b8197737944ea7231d226514
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2019
ms.locfileid: "104313970"
---
# <a name="windows-8-and-windows-server-2012-client-and-server-compatibility"></a><span data-ttu-id="2c69a-103">Windows 8 和 Windows Server 2012 用戶端和伺服器相容性</span><span class="sxs-lookup"><span data-stu-id="2c69a-103">Windows 8 and Windows Server 2012 client and server compatibility</span></span>

<span data-ttu-id="2c69a-104">本節描述作業系統中的變更，您應該特別注意，因為現有的應用程式可能會受到影響，以及如何在用戶端、伺服器或用戶端和伺服器上設計新的應用程式。</span><span class="sxs-lookup"><span data-stu-id="2c69a-104">This section describes changes in the operating system that you should pay special attention to due to the potential impacts on existing apps and how new apps should be designed on clients, on servers, or on both clients and servers.</span></span> <span data-ttu-id="2c69a-105">以下是本節所涵蓋的主題清單（依功能區域分組）：</span><span class="sxs-lookup"><span data-stu-id="2c69a-105">Following is the list of topics covered in this section, grouped by feature area:</span></span>

<span data-ttu-id="2c69a-106">**AppCompat**</span><span class="sxs-lookup"><span data-stu-id="2c69a-106">**AppCompat**</span></span>

-   <span data-ttu-id="2c69a-107">安全性應用程式偵測規則更新</span><span class="sxs-lookup"><span data-stu-id="2c69a-107">Security app detection rules update</span></span>
-   <span data-ttu-id="2c69a-108">判斷填充碼狀態</span><span class="sxs-lookup"><span data-stu-id="2c69a-108">Determining shim status</span></span>
-   <span data-ttu-id="2c69a-109">伺服器應用程式必須能夠在沒有伺服器圖形化 Shell 的情況下執行</span><span class="sxs-lookup"><span data-stu-id="2c69a-109">Server apps must be able to run without the Server Graphical Shell</span></span>
-   <span data-ttu-id="2c69a-110">RDS 伺服器元件會從 Windows 8 中移除</span><span class="sxs-lookup"><span data-stu-id="2c69a-110">RDS server components are removed from Windows 8</span></span>
-   <span data-ttu-id="2c69a-111">檔案類型和通訊協定關聯模型</span><span class="sxs-lookup"><span data-stu-id="2c69a-111">File type and protocol associations model</span></span>
-   <span data-ttu-id="2c69a-112">桌面活動仲裁者</span><span class="sxs-lookup"><span data-stu-id="2c69a-112">Desktop Activity Moderator</span></span>
-   <span data-ttu-id="2c69a-113">.NET Framework 4.5 是預設值，.NET Framework 3.5 是選擇性的</span><span class="sxs-lookup"><span data-stu-id="2c69a-113">.NET Framework 4.5 is default and .NET Framework 3.5 is optional</span></span>
-   <span data-ttu-id="2c69a-114">啟動預設的網頁瀏覽器之後，可能看不到桌面應用程式</span><span class="sxs-lookup"><span data-stu-id="2c69a-114">Desktop apps may not be visible after launching the default web browser</span></span>
-   <span data-ttu-id="2c69a-115">高對比模式</span><span class="sxs-lookup"><span data-stu-id="2c69a-115">High-contrast mode</span></span>
-   <span data-ttu-id="2c69a-116">應用程式 (可執行檔) 資訊清單</span><span class="sxs-lookup"><span data-stu-id="2c69a-116">App (executable) manifest</span></span>
-   <span data-ttu-id="2c69a-117">已取代佇列的目前模型</span><span class="sxs-lookup"><span data-stu-id="2c69a-117">Queued present model is being deprecated</span></span>
-   <span data-ttu-id="2c69a-118">Windows 8 的程式相容性助理案例</span><span class="sxs-lookup"><span data-stu-id="2c69a-118">Program Compatibility Assistant scenarios for Windows 8</span></span>
-   <span data-ttu-id="2c69a-119">已移除桌面小工具</span><span class="sxs-lookup"><span data-stu-id="2c69a-119">Desktop gadgets removed</span></span>

<span data-ttu-id="2c69a-120">**儲存體和檔案系統**</span><span class="sxs-lookup"><span data-stu-id="2c69a-120">**Storage and File System**</span></span>

-   <span data-ttu-id="2c69a-121">Advanced format (4K) 磁片相容性更新</span><span class="sxs-lookup"><span data-stu-id="2c69a-121">Advanced format (4K) disk compatibility update</span></span>
-   <span data-ttu-id="2c69a-122">精簡布建邏輯單元</span><span class="sxs-lookup"><span data-stu-id="2c69a-122">Thin provisioning of logical units</span></span>
-   <span data-ttu-id="2c69a-123">針對 Windows 預先安裝環境 (WinPE) 和伺服器 SKU，現在可選擇增強的儲存體</span><span class="sxs-lookup"><span data-stu-id="2c69a-123">Enhanced storage is now optional for Windows Preinstallation Environment (WinPE) and server SKU</span></span>
-   <span data-ttu-id="2c69a-124">虛擬磁碟服務正在轉換至 Windows Management Instrumentation (WMI) 型 Windows 儲存體管理 API</span><span class="sxs-lookup"><span data-stu-id="2c69a-124">Virtual Disk Service is transitioning to the Windows Management Instrumentation (WMI)-based Windows Storage Management API</span></span>
-   <span data-ttu-id="2c69a-125">已移除本機磁片區的舊版 UI</span><span class="sxs-lookup"><span data-stu-id="2c69a-125">Previous versions UI removed for local volumes</span></span>
-   <span data-ttu-id="2c69a-126">StorAHCI 取代 MSAHCI</span><span class="sxs-lookup"><span data-stu-id="2c69a-126">StorAHCI replaces MSAHCI</span></span>
-   <span data-ttu-id="2c69a-127">Windows 7 備份及還原已淘汰</span><span class="sxs-lookup"><span data-stu-id="2c69a-127">Windows 7 backup and restore deprecated</span></span>
-   <span data-ttu-id="2c69a-128">卸載資料傳輸</span><span class="sxs-lookup"><span data-stu-id="2c69a-128">Offloaded data transfers</span></span>

<span data-ttu-id="2c69a-129">**其他**</span><span class="sxs-lookup"><span data-stu-id="2c69a-129">**Other**</span></span>

-   <span data-ttu-id="2c69a-130">桌面視窗管理員一律開啟</span><span class="sxs-lookup"><span data-stu-id="2c69a-130">Desktop Window Manager is always on</span></span>
-   <span data-ttu-id="2c69a-131">Direct2D 不支援在 Internet Explorer 9 中轉譯為 "rich" 中繼檔</span><span class="sxs-lookup"><span data-stu-id="2c69a-131">Direct2D does not support rendering to "rich" metafiles in Internet Explorer 9</span></span>
-   <span data-ttu-id="2c69a-132">DX9 舊版硬體支援的變更</span><span class="sxs-lookup"><span data-stu-id="2c69a-132">Changes in DX9 legacy hardware support</span></span>
-   <span data-ttu-id="2c69a-133">MSAA 無法供 Windows Store 應用程式使用</span><span class="sxs-lookup"><span data-stu-id="2c69a-133">MSAA is not available to Windows Store apps</span></span>
-   <span data-ttu-id="2c69a-134">NDIS 6.30 驅動程式的埠3已淘汰</span><span class="sxs-lookup"><span data-stu-id="2c69a-134">Port 3 is deprecated for NDIS 6.30 drivers</span></span>

 

 
