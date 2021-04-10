---
description: WMI 以服務的形式執行，其顯示名稱為 &\# 0034;Windows Management Instrumentation&\# 0034; 以及服務名稱 &\# 0034; winmgmt&\# 0034;。
ms.assetid: 8dff43bf-71d0-4d5a-91bc-6f474186d4ba
ms.tgt_platform: multiple
title: 啟動和停止 WMI 服務
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54b820283aac089ad6191ee587e6beadea6dc030
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192069"
---
# <a name="starting-and-stopping-the-wmi-service"></a><span data-ttu-id="57f97-103">啟動和停止 WMI 服務</span><span class="sxs-lookup"><span data-stu-id="57f97-103">Starting and Stopping the WMI Service</span></span>

<span data-ttu-id="57f97-104">WMI 會以服務的形式執行，其顯示名稱為 "Windows Management Instrumentation"，服務名稱為 "winmgmt"。</span><span class="sxs-lookup"><span data-stu-id="57f97-104">WMI runs as a service with the display name "Windows Management Instrumentation" and the service name "winmgmt".</span></span> <span data-ttu-id="57f97-105">在系統啟動時，會自動在 LocalSystem 帳戶下執行 WMI。</span><span class="sxs-lookup"><span data-stu-id="57f97-105">WMI runs automatically at system startup under the LocalSystem account.</span></span> <span data-ttu-id="57f97-106">如果 WMI 未執行，它會在第一個管理應用程式或腳本要求與 WMI 命名空間的連接時自動啟動。</span><span class="sxs-lookup"><span data-stu-id="57f97-106">If WMI is not running, it automatically starts when the first management application or script requests connection to a WMI namespace.</span></span>

<span data-ttu-id="57f97-107">根據系統執行的作業系統版本而定，有數個其他服務相依于 WMI 服務。</span><span class="sxs-lookup"><span data-stu-id="57f97-107">Several other services are dependent upon the WMI service, depending on the operating system version that the system is running.</span></span>

## <a name="starting-winmgmt-service"></a><span data-ttu-id="57f97-108">正在啟動 Winmgmt 服務</span><span class="sxs-lookup"><span data-stu-id="57f97-108">Starting Winmgmt Service</span></span>

<span data-ttu-id="57f97-109">下列程式說明如何啟動 WMI 服務。</span><span class="sxs-lookup"><span data-stu-id="57f97-109">The following procedure describes how to start the WMI service.</span></span>

<span data-ttu-id="57f97-110">**啟動 Winmgmt 服務**</span><span class="sxs-lookup"><span data-stu-id="57f97-110">**To start Winmgmt Service**</span></span>

1.  <span data-ttu-id="57f97-111">在命令提示字元中，輸入 **net** **start** **winmgmt** \[ */<switch>* \] 。</span><span class="sxs-lookup"><span data-stu-id="57f97-111">At a command prompt, enter **net** **start** **winmgmt** \[*/<switch>*\].</span></span>

    <span data-ttu-id="57f97-112">如需可用參數的詳細資訊，請參閱 [winmgmt](winmgmt.md)。</span><span class="sxs-lookup"><span data-stu-id="57f97-112">For more information about the switches that are available, see [winmgmt](winmgmt.md).</span></span> <span data-ttu-id="57f97-113">您可以使用內建的系統管理員帳戶，或以較高的許可權執行的 Administrators 群組中的帳戶，以啟動 WMI 服務。</span><span class="sxs-lookup"><span data-stu-id="57f97-113">You use the built-in Administrator account or an account in the Administrators group running with elevated rights to start the WMI service.</span></span> <span data-ttu-id="57f97-114">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](user-account-control-and-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="57f97-114">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

2.  <span data-ttu-id="57f97-115">其他相依于 WMI 服務的服務，例如 SMS Agent Host 或 Windows 防火牆，將不會自動重新開機。</span><span class="sxs-lookup"><span data-stu-id="57f97-115">Other services that are dependent on the WMI service, such as SMS Agent Host or Windows Firewall, will not automatically be restarted.</span></span>

## <a name="stopping-winmgmt-service"></a><span data-ttu-id="57f97-116">停止 Winmgmt 服務</span><span class="sxs-lookup"><span data-stu-id="57f97-116">Stopping Winmgmt Service</span></span>

<span data-ttu-id="57f97-117">下列程式說明如何停止 WMI 服務。</span><span class="sxs-lookup"><span data-stu-id="57f97-117">The following procedure describes how to stop the WMI Service.</span></span>

<span data-ttu-id="57f97-118">**停止 Winmgmt 服務**</span><span class="sxs-lookup"><span data-stu-id="57f97-118">**To stop Winmgmt Service**</span></span>

1.  <span data-ttu-id="57f97-119">在命令提示字元中，輸入 **net stop winmgmt**。</span><span class="sxs-lookup"><span data-stu-id="57f97-119">At a command prompt, enter **net stop winmgmt**.</span></span>

2.  <span data-ttu-id="57f97-120">其他相依于 WMI 服務的服務也會停止，例如 SMS Agent Host 或 Windows 防火牆。</span><span class="sxs-lookup"><span data-stu-id="57f97-120">Other services that are dependent on the WMI service also halt, such as SMS Agent Host or Windows Firewall.</span></span>

## <a name="examples"></a><span data-ttu-id="57f97-121">範例</span><span class="sxs-lookup"><span data-stu-id="57f97-121">Examples</span></span>

<span data-ttu-id="57f97-122">TechNet 資源庫包含 [WMI service 看門狗腳本](https://Gallery.TechNet.Microsoft.Com/WMI-service-watchdog-script-4fab1282)，說明如何使用 PowerShell 以程式設計方式關閉和重新開機 winmgmt 服務。</span><span class="sxs-lookup"><span data-stu-id="57f97-122">The TechNet Gallery contains the [WMI service watchdog script](https://Gallery.TechNet.Microsoft.Com/WMI-service-watchdog-script-4fab1282), which describes how to programmatically shut down and restart the winmgmt service with PowerShell.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57f97-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="57f97-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57f97-124">使用 WMI Command-Line 工具</span><span class="sxs-lookup"><span data-stu-id="57f97-124">Using the WMI Command-Line Tools</span></span>](using-the-wmi-command-line-tools.md)
</dt> </dl>

 

 



