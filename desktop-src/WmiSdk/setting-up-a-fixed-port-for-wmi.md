---
description: WMI 是以共用服務主機的一部分執行，預設會透過 DCOM 指派埠。 不過，您可以將 WMI 服務設定為在個別主機中執行為唯一的進程，並指定固定的埠。
ms.assetid: 62908445-2a43-4a20-a998-e497c6ecf48e
ms.tgt_platform: multiple
title: 設定適用于 WMI 的固定埠
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49c6d6b0bf42951766cfd813ccb4b5eed041600a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978397"
---
# <a name="setting-up-a-fixed-port-for-wmi"></a><span data-ttu-id="03ccf-104">設定適用于 WMI 的固定埠</span><span class="sxs-lookup"><span data-stu-id="03ccf-104">Setting Up a Fixed Port for WMI</span></span>

<span data-ttu-id="03ccf-105">WMI 是以共用服務主機的一部分執行，預設會透過 DCOM 指派埠。</span><span class="sxs-lookup"><span data-stu-id="03ccf-105">WMI runs as part of a shared service host with ports assigned through DCOM by default.</span></span> <span data-ttu-id="03ccf-106">不過，您可以將 WMI 服務設定為在個別主機中執行為唯一的進程，並指定固定的埠。</span><span class="sxs-lookup"><span data-stu-id="03ccf-106">However, you can set up the WMI service to run as the only process in a separate host and specify a fixed port.</span></span>

<span data-ttu-id="03ccf-107">下列程式是自動化的設定，可讓 WMI 具有固定的埠。</span><span class="sxs-lookup"><span data-stu-id="03ccf-107">The following procedure is an automated setup to allow WMI to have a fixed port.</span></span> <span data-ttu-id="03ccf-108">此程式使用 [**winmgmt**](winmgmt.md) 命令列工具。</span><span class="sxs-lookup"><span data-stu-id="03ccf-108">The procedure uses the [**winmgmt**](winmgmt.md) command-line tool.</span></span>

<span data-ttu-id="03ccf-109">**設定適用于 WMI 的固定埠**</span><span class="sxs-lookup"><span data-stu-id="03ccf-109">**To set up a fixed port for WMI**</span></span>

1.  <span data-ttu-id="03ccf-110">在命令提示字元中，輸入 **winmgmt-standalonehost**</span><span class="sxs-lookup"><span data-stu-id="03ccf-110">At the command prompt, type **winmgmt -standalonehost**</span></span>
2.  <span data-ttu-id="03ccf-111">輸入命令 **net stop "Windows Management Instrumentation"**，或使用 **net stop winmgmt** 的簡短名稱，以停止 WMI 服務</span><span class="sxs-lookup"><span data-stu-id="03ccf-111">Stop the WMI service by typing the command **net stop "Windows Management Instrumentation"**, or use the short name of **net stop winmgmt**</span></span>
3.  <span data-ttu-id="03ccf-112">輸入 **net start "Windows Management Instrumentation"** 或 **net start winmgmt** ，以重新開機新服務主機中的 WMI 服務</span><span class="sxs-lookup"><span data-stu-id="03ccf-112">Restart the WMI service again in a new service host by typing **net start "Windows Management Instrumentation"** or **net start winmgmt**</span></span>
4.  <span data-ttu-id="03ccf-113">輸入 **netsh firewall add PORTOPENING TCP 24158 WMIFixedPort** ，為 WMI 服務建立新的埠號碼</span><span class="sxs-lookup"><span data-stu-id="03ccf-113">Establish a new port number for the WMI service by typing **netsh firewall add portopening TCP 24158 WMIFixedPort**</span></span>

<span data-ttu-id="03ccf-114">若要復原您對 WMI 所做的任何變更，請輸入 **winmgmt/sharedhost**，然後再次停止並啟動 winmgmt 服務。</span><span class="sxs-lookup"><span data-stu-id="03ccf-114">To undo any changes you make to WMI, type **winmgmt /sharedhost**, then stop and start the winmgmt service again.</span></span>

## <a name="examples"></a><span data-ttu-id="03ccf-115">範例</span><span class="sxs-lookup"><span data-stu-id="03ccf-115">Examples</span></span>

<span data-ttu-id="03ccf-116">如需針對 WMI 設定固定埠的腳本，請參閱下列腳本庫程式 [代碼範例](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389 )。</span><span class="sxs-lookup"><span data-stu-id="03ccf-116">For a script that sets up a fixed port for WMI, see the following Scripting Gallery [code sample](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389 ).</span></span>

<span data-ttu-id="03ccf-117">或是啟用或停用 WMI 埠設定的 PowerShell 程式碼範例，請參閱 TechNet 資源庫上的 [WmiSinglePort](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389) 範例。</span><span class="sxs-lookup"><span data-stu-id="03ccf-117">or a PowerShell code example that enables or disables the WMI port settings, see the [Set-WmiSinglePort](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389) example on TechNet Gallery.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03ccf-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="03ccf-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03ccf-119">連接至遠端電腦上的 WMI</span><span class="sxs-lookup"><span data-stu-id="03ccf-119">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="03ccf-120">疑難排解遠端 WMI 連接</span><span class="sxs-lookup"><span data-stu-id="03ccf-120">Troubleshooting a Remote WMI Connections</span></span>](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> <dt>

[<span data-ttu-id="03ccf-121">提供者裝載和安全性</span><span class="sxs-lookup"><span data-stu-id="03ccf-121">Provider Hosting and Security</span></span>](provider-hosting-and-security.md)
</dt> </dl>

 

 



