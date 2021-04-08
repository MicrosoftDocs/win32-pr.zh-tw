---
title: 遠端硬體管理
description: 遠端硬體管理
ms.assetid: 0ea6d075-6154-4ab9-adcb-e599e5aee614
ms.tgt_platform: multiple
keywords:
- 遠端硬體管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68bbb470d513b49d2158865c4c42051cc16856ed
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682381"
---
# <a name="remote-hardware-management"></a><span data-ttu-id="7cf87-104">遠端硬體管理</span><span class="sxs-lookup"><span data-stu-id="7cf87-104">Remote Hardware Management</span></span>

<span data-ttu-id="7cf87-105">Windows 遠端管理硬體管理的目的是要藉由提供遠端硬體元件的監視和控制，特別是在系統啟動之前，以及在作業系統失敗之後，以降低整體 IT 管理成本。</span><span class="sxs-lookup"><span data-stu-id="7cf87-105">Windows Remote Management hardware management is intended to reduce overall IT administration costs by providing monitoring and control of remote hardware components, especially before the system is started and after an operating system failure.</span></span>

<span data-ttu-id="7cf87-106"> (Oem 的原始設備製造商) 開發了一個可解決硬體管理需求的通用架構。</span><span class="sxs-lookup"><span data-stu-id="7cf87-106">Original Equipment Manufacturers (OEMs) have developed a common architecture to address the need for hardware management.</span></span> <span data-ttu-id="7cf87-107">此架構的重要部分是基礎板 [*管理控制器*](windows-remote-management-glossary.md) (BMC) 。</span><span class="sxs-lookup"><span data-stu-id="7cf87-107">An important piece of this architecture is the [*baseboard management controller*](windows-remote-management-glossary.md) (BMC).</span></span> <span data-ttu-id="7cf87-108">BMC 是專門用來監視伺服器電腦狀態的裝置。</span><span class="sxs-lookup"><span data-stu-id="7cf87-108">A BMC is a specialized device that monitors the state of the server computer.</span></span> <span data-ttu-id="7cf87-109">BMC 可提供伺服器硬體的遠端控制、捕獲狀態資料，以及接收有關重大錯誤和其他硬體狀態變更的通知。</span><span class="sxs-lookup"><span data-stu-id="7cf87-109">The BMC provides remote control of server hardware, retrieves status data, and receives notifications about critical errors and other hardware status changes.</span></span> <span data-ttu-id="7cf87-110">監視遠端伺服器的腳本或應用程式可以直接從 BMC 取得來自伺服器的資料（透過遠端作業系統或 [*頻外的*](windows-remote-management-glossary.md)[*方式*](windows-remote-management-glossary.md)）。</span><span class="sxs-lookup"><span data-stu-id="7cf87-110">A script or application that is monitoring a remote server can obtain data from the server either [*in-band*](windows-remote-management-glossary.md), through the remote operating system, or [*out-of-band*](windows-remote-management-glossary.md), directly from the BMC.</span></span>

<span data-ttu-id="7cf87-111">BMC 具有可偵測的感應器，例如，當伺服器電腦過熱或電壓超出可接受範圍時。</span><span class="sxs-lookup"><span data-stu-id="7cf87-111">A BMC has sensors that can detect, for example, when the server computer is overheating or when voltage is out of the acceptable range.</span></span> <span data-ttu-id="7cf87-112">有幾個標準可用來定義 BMC 的架構。</span><span class="sxs-lookup"><span data-stu-id="7cf87-112">Several standards exist to define the architecture of BMC.</span></span> <span data-ttu-id="7cf87-113">[*智慧型平臺管理介面 (IPMI)*](windows-remote-management-glossary.md)是經常使用的一種標準。</span><span class="sxs-lookup"><span data-stu-id="7cf87-113">The [*Intelligent Platform Management Interface (IPMI)*](windows-remote-management-glossary.md) is one such standard that is used frequently.</span></span> <span data-ttu-id="7cf87-114">不過，儘管是 IPMI 標準，但是伺服器硬體的管理存取權是專屬的，而且需要使用 Oem 所提供的管理工具。</span><span class="sxs-lookup"><span data-stu-id="7cf87-114">However, despite the IPMI standard, management access to server hardware is proprietary and requires use of management tools supplied by OEMs.</span></span> <span data-ttu-id="7cf87-115">此外，也會使用特製化的有線通訊協定、遠端系統管理控制通訊協定 (RMCP) （具有非標準的安全性機制來驗證存取）來提供 BMC 的遠端存取。</span><span class="sxs-lookup"><span data-stu-id="7cf87-115">Also, remote access to a BMC is provided using a specialized wire protocol, Remote Management Control Protocol (RMCP), which has nonstandard security mechanisms for authentication of access.</span></span>

<span data-ttu-id="7cf87-116">Microsoft [IPMI 提供者](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) 與 IPMI 驅動程式可讓您透過具有 wmi [類別](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)的標準 wmi 提供者，從遠端伺服器電腦取得 BMC 資料。</span><span class="sxs-lookup"><span data-stu-id="7cf87-116">The Microsoft [IPMI provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) and IPMI driver, allow you to obtain BMC data from remote server computers through a standard WMI provider with WMI [classes](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span> <span data-ttu-id="7cf87-117">雖然您可以撰寫透過 DCOM 取得遠端資料的一般 WMI 腳本，但在許多情況下，取得 IPMI 資料的慣用方法是透過 **winrm** 命令列公用程式或 [winrm 腳本 Api](winrm-scripting-api.md) 或 [winrm c + + API](winrm-c---api.md)。</span><span class="sxs-lookup"><span data-stu-id="7cf87-117">While you can write a normal WMI script that obtains remote data through DCOM, in many cases the preferred method of obtaining IPMI data is through the **Winrm** command-line utility or the [WinRM Scripting API](winrm-scripting-api.md) or [WinRM C++ API](winrm-c---api.md).</span></span> <span data-ttu-id="7cf87-118">Winrm 公用程式和 WinRM 服務 Api 依賴 WS-Management 的通訊協定，並且可以從本機或遠端電腦取得 IPMI 資料，而不需要使用 DCOM。</span><span class="sxs-lookup"><span data-stu-id="7cf87-118">The Winrm utility and the WinRM service APIs rely on the WS-Management protocol and can obtain IPMI data either from local or remote computer without using DCOM.</span></span>

<span data-ttu-id="7cf87-119">BMC 也有一個稱為「系統事件記錄檔 (」的事件資料庫，) 會記錄受監視電腦中的事件。</span><span class="sxs-lookup"><span data-stu-id="7cf87-119">The BMC also has an event database called the System Event Log (SEL) which records events in the monitored computer.</span></span> <span data-ttu-id="7cf87-120">您無法訂閱將這些事件傳遞至腳本，就像您可以使用 WMI 事件類別一樣。</span><span class="sxs-lookup"><span data-stu-id="7cf87-120">You cannot subscribe to have these events delivered to a script as you can with WMI event classes.</span></span> <span data-ttu-id="7cf87-121">不過，您可以使用 Wecutil.exe 命令列工具來訂閱它們。</span><span class="sxs-lookup"><span data-stu-id="7cf87-121">However, you can use the Wecutil.exe command-line tool to subscribe to them.</span></span> <span data-ttu-id="7cf87-122">如需如何使用此工具的詳細資訊，請在命令提示字元中輸入 **>wecutil/？**。</span><span class="sxs-lookup"><span data-stu-id="7cf87-122">For more information about how to use this tool, at a command prompt type **wecutil /?**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7cf87-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="7cf87-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cf87-124">WS-Management 通訊協定</span><span class="sxs-lookup"><span data-stu-id="7cf87-124">WS-Management Protocol</span></span>](ws-management-protocol.md)
</dt> <dt>

[<span data-ttu-id="7cf87-125">關於 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="7cf87-125">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> </dl>

 

 