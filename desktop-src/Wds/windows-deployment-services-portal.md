---
title: Windows Deployment Services
description: 部署 Windows 作業系統。 使用以網路為基礎的安裝來設定新的用戶端，而不需要系統管理員造訪每部電腦或直接從 CD 或 DVD 媒體安裝。
ms.assetid: 790abc27-03cc-4f93-bf04-a4eb37e614bb
keywords:
- Windows 部署服務 Windows 部署服務
- Windows 部署服務 Windows 部署服務，首頁
- 部署服務 Windows 部署服務
- WDS Windows 部署服務查看 Windows 部署服務
- 遠端安裝服務 Windows 部署服務查看 Windows 部署服務
- RIS Windows 部署服務查看 Windows 部署服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b35bebb000b383552f12d259ca17552165e9247f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967286"
---
# <a name="windows-deployment-services"></a><span data-ttu-id="34044-110">Windows Deployment Services</span><span class="sxs-lookup"><span data-stu-id="34044-110">Windows Deployment Services</span></span>

## <a name="purpose"></a><span data-ttu-id="34044-111">目的</span><span class="sxs-lookup"><span data-stu-id="34044-111">Purpose</span></span>

<span data-ttu-id="34044-112">Windows 部署服務 (WDS) 是 (RIS) 之遠端安裝服務的修訂版本。</span><span class="sxs-lookup"><span data-stu-id="34044-112">Windows Deployment Services (WDS) is the revised version of Remote Installation Services (RIS).</span></span> <span data-ttu-id="34044-113">WDS 可讓您部署 Windows 作業系統。</span><span class="sxs-lookup"><span data-stu-id="34044-113">WDS enables the deployment of Windows operating systems.</span></span> <span data-ttu-id="34044-114">您可以使用 WDS 以網路為基礎的安裝來設定新的用戶端，而不需要系統管理員造訪每部電腦或直接從 CD 或 DVD 媒體安裝。</span><span class="sxs-lookup"><span data-stu-id="34044-114">You can use WDS to set up new clients with a network-based installation without requiring that administrators visit each computer or install directly from CD or DVD media.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="34044-115">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="34044-115">Developer audience</span></span>

<span data-ttu-id="34044-116">WDS API 的主要開發人員物件是針對為 IT 和其他電腦管理群組開發自訂工具和進程的群組。</span><span class="sxs-lookup"><span data-stu-id="34044-116">The primary developer audience of the WDS API is for groups that develop custom tools and processes for IT and other computer administration groups.</span></span> <span data-ttu-id="34044-117">在無法使用標準 Windows 部署服務 (WDS) 解決方案的環境中，WDS API 可讓您以程式設計方式存取某些 WDS 元件。</span><span class="sxs-lookup"><span data-stu-id="34044-117">In environments where the standard Windows Deployment Services (WDS) solution cannot be used, the WDS API enables programmatic access to some WDS components.</span></span>

<span data-ttu-id="34044-118">原始設備製造商 (Oem) 、系統建造商和企業 IT 專業人員，想要瞭解如何將 Windows 部署到新電腦上的詳細資訊，請參閱 [) 更新逐步指南](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) 和 [Windows 自動化安裝套件 Windows 部署服務 WAIK (](https://www.microsoft.com/download/details.aspx?id=10333)中有關標準 Windows 部署服務 (WDS) 解決方案的資訊。</span><span class="sxs-lookup"><span data-stu-id="34044-118">Original Equipment Manufacturers (OEMs), system builders, and corporate IT professionals looking for information on how to deploy Windows onto new computers, should see the information about the standard Windows Deployment Services (WDS) solution in the [Windows Deployment Services Update Step-by-Step Guide](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) and the [Windows Automated Installation Kit (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="34044-119">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="34044-119">Run-time requirements</span></span>

<span data-ttu-id="34044-120">WDS 是以 Windows Server 2003 Service Pack 1 (SP1) 的附加元件的形式提供，並包含在作業系統中，從 Windows Server 2003 Service Pack 2 (SP2) 和 Windows Server 2008 開始。</span><span class="sxs-lookup"><span data-stu-id="34044-120">WDS is available as an add-on for Windows Server 2003 with Service Pack 1 (SP1) and is included in the operating system starting with Windows Server 2003 with Service Pack 2 (SP2) and Windows Server 2008.</span></span> <span data-ttu-id="34044-121">WDS PXE 伺服器 API 需要伺服器上的 WDS 伺服器角色，才能執行自訂 PXE 提供者。</span><span class="sxs-lookup"><span data-stu-id="34044-121">The WDS PXE Server API requires the WDS server role on the server to implement custom PXE providers.</span></span> <span data-ttu-id="34044-122">WDS 用戶端 API 需要 Microsoft Windows 預先安裝環境 (Windows PE 2.0) 安裝程式處理階段。</span><span class="sxs-lookup"><span data-stu-id="34044-122">The WDS Client API requires the Microsoft Windows Preinstallation Environment (Windows PE 2.0) phase of setup processing.</span></span> <span data-ttu-id="34044-123">中 Windows PE 2.0 的 RAMDISK 可開機映射。必須在網路開機程式中下載 WIM 格式，才能執行自訂 WDS 用戶端。</span><span class="sxs-lookup"><span data-stu-id="34044-123">A RAMDISK bootable image of Windows PE 2.0 in the .WIM format must be downloaded as part of the network boot process to implement custom WDS clients.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="34044-124">本節內容</span><span class="sxs-lookup"><span data-stu-id="34044-124">In this section</span></span>



| <span data-ttu-id="34044-125">主題</span><span class="sxs-lookup"><span data-stu-id="34044-125">Topic</span></span>                                                                                                 | <span data-ttu-id="34044-126">描述</span><span class="sxs-lookup"><span data-stu-id="34044-126">Description</span></span>                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="34044-127">關於 Windows 部署服務 API</span><span class="sxs-lookup"><span data-stu-id="34044-127">About the Windows Deployment Services API</span></span>](about-the-windows-deployment-services-api.md)<br/> | <span data-ttu-id="34044-128">WDS 伺服器 API 和 WDS 用戶端 API 的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="34044-128">General information about the WDS Server API and WDS Client API.</span></span><br/>    |
| [<span data-ttu-id="34044-129">Windows 部署服務參考</span><span class="sxs-lookup"><span data-stu-id="34044-129">Windows Deployment Services Reference</span></span>](windows-deployment-services-reference.md)<br/>         | <span data-ttu-id="34044-130">描述 Windows 部署服務函數和結構。</span><span class="sxs-lookup"><span data-stu-id="34044-130">Describes the Windows Deployment Services functions and structures.</span></span><br/> |



 

 

