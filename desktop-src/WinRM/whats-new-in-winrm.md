---
title: WinRM 2.0 的新功能
description: Windows 遠端管理2.0 版提供新功能。  (WinRM 2.0) 。
ms.assetid: 402c179a-6dd7-4d75-9318-bb8194b5527d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54f4a4829bffdb816854de2a3ebe98106a5a65af
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104374634"
---
# <a name="whats-new-in-winrm-20"></a><span data-ttu-id="3e2fb-104">WinRM 2.0 的新功能</span><span class="sxs-lookup"><span data-stu-id="3e2fb-104">What's New in WinRM 2.0</span></span>

<span data-ttu-id="3e2fb-105">Windows 遠端管理2.0 版提供新功能。</span><span class="sxs-lookup"><span data-stu-id="3e2fb-105">New features are available in Windows Remote Management version 2.0.</span></span> <span data-ttu-id="3e2fb-106"> (WinRM 2.0) </span><span class="sxs-lookup"><span data-stu-id="3e2fb-106">(WinRM 2.0)</span></span>

<span data-ttu-id="3e2fb-107">WinRM 2.0 包含在 Windows Server 2008 R2 和 Windows 7 中。</span><span class="sxs-lookup"><span data-stu-id="3e2fb-107">WinRM 2.0 is included in Windows Server 2008 R2 and Windows 7.</span></span>

<span data-ttu-id="3e2fb-108">您也可以下載適用于 Windows Server 2008 Service Pack 2 (SP2) 和 Windows Vista （含 Service Pack 2） (SP2) 的 WinRM 2.0。</span><span class="sxs-lookup"><span data-stu-id="3e2fb-108">You can also download WinRM 2.0 for Windows Server 2008 with Service Pack 2 (SP2) and Windows Vista with Service Pack 2 (SP2).</span></span> <span data-ttu-id="3e2fb-109">如需下載 WinRM 2.0 的詳細資訊，請參閱 [KB968929](https://support.microsoft.com/kb/968929)。</span><span class="sxs-lookup"><span data-stu-id="3e2fb-109">For information about downloading WinRM 2.0, see [KB968929](https://support.microsoft.com/kb/968929).</span></span>

<span data-ttu-id="3e2fb-110">下表列出 WinRM 2.0 的檔。</span><span class="sxs-lookup"><span data-stu-id="3e2fb-110">The following table lists the documentation for WinRM 2.0.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3e2fb-111">主題</span><span class="sxs-lookup"><span data-stu-id="3e2fb-111">Topic</span></span></th>
<th><span data-ttu-id="3e2fb-112">描述</span><span class="sxs-lookup"><span data-stu-id="3e2fb-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3e2fb-113"><a href="client-shell-api.md">WinRM 用戶端 Shell API</a></span><span class="sxs-lookup"><span data-stu-id="3e2fb-113"><a href="client-shell-api.md">WinRM Client Shell API</a></span></span><br/></td>
<td><span data-ttu-id="3e2fb-114">WinRM 用戶端 Shell 應用程式開發介面 (API) 提供在遠端電腦上建立和管理 shell 和 shell 作業、命令和資料流程的功能。</span><span class="sxs-lookup"><span data-stu-id="3e2fb-114">The WinRM Client Shell application programming interface (API) provides functionality to create and manage shells and shell operations, commands, and data streams on remote computers.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3e2fb-115"><a href="winrm-plugin-api.md">WinRM 外掛程式 API</a></span><span class="sxs-lookup"><span data-stu-id="3e2fb-115"><a href="winrm-plugin-api.md">WinRM Plugin API</a></span></span><br/></td>
<td><span data-ttu-id="3e2fb-116">WinRM 外掛程式 API 提供的功能，可讓使用者藉由針對支援的 <a href="windows-remote-management-glossary.md"><em>資源 uri</em></a> 和作業來執行某些 api 來寫入外掛程式。</span><span class="sxs-lookup"><span data-stu-id="3e2fb-116">The WinRM Plug-in API provides functionality that enables a user to write plug-ins by implementing certain APIs for supported <a href="windows-remote-management-glossary.md"><em>resource URIs</em></a> and operations.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3e2fb-117"><a href="winrm-application-hosting.md">管理託管服務的基礎結構</a></span><span class="sxs-lookup"><span data-stu-id="3e2fb-117"><a href="winrm-application-hosting.md">Infrastructure for Managing Hosted Services</a></span></span><br/></td>
<td><span data-ttu-id="3e2fb-118">WinRM 2.0 引進了裝載架構。</span><span class="sxs-lookup"><span data-stu-id="3e2fb-118">WinRM 2.0 introduces a hosting framework.</span></span> <span data-ttu-id="3e2fb-119">支援兩種裝載模型。</span><span class="sxs-lookup"><span data-stu-id="3e2fb-119">Two hosting models are supported.</span></span> <span data-ttu-id="3e2fb-120">其中一個是網際網路資訊服務 (IIS) 型，另一個則是 WinRM –以服務為基礎。</span><span class="sxs-lookup"><span data-stu-id="3e2fb-120">One is Internet Information Service (IIS)–based and the other is WinRM–service based.</span></span> <br/> <span data-ttu-id="3e2fb-121">如需主機配置的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="3e2fb-121">For more information about the host configuration, see the following topics:</span></span><br/>
<ul>
<li><span data-ttu-id="3e2fb-122"><a href="iis-host-plug-in-configuration.md">IIS 主機外掛程式設定</a></span><span class="sxs-lookup"><span data-stu-id="3e2fb-122"><a href="iis-host-plug-in-configuration.md">IIS Host Plug-in Configuration</a></span></span></li>
<li><span data-ttu-id="3e2fb-123"><a href="wsman-service-plug-in-configuration.md">WinRM 服務外掛程式設定</a></span><span class="sxs-lookup"><span data-stu-id="3e2fb-123"><a href="wsman-service-plug-in-configuration.md">WinRM Service Plug-in Configuration</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3e2fb-124"><a href="dmtf-association-traversal.md">透過關聯遍歷進行的 DMTF 設定檔探索</a></span><span class="sxs-lookup"><span data-stu-id="3e2fb-124"><a href="dmtf-association-traversal.md">DMTF Profile Discovery through Association Traversal</a></span></span><br/></td>
<td><span data-ttu-id="3e2fb-125">關聯分析可讓使用者使用標準篩選機制來抓取關聯類別的實例。</span><span class="sxs-lookup"><span data-stu-id="3e2fb-125">Association traversal enables a user to retrieve instances of Association classes by using a standard filtering mechanism.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3e2fb-126"><a href="remote-shell-infrastructure-improvements.md">遠端 Shell 基礎結構改進</a></span><span class="sxs-lookup"><span data-stu-id="3e2fb-126"><a href="remote-shell-infrastructure-improvements.md">Remote Shell infrastructure improvements</a></span></span><br/></td>
<td><span data-ttu-id="3e2fb-127">本主題包含 WinRM 的遠端基礎結構增強功能的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3e2fb-127">This topic includes information about the remote infrastructure improvements for WinRM.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3e2fb-128"><a href="multi-hop-support.md">多重躍點支援</a></span><span class="sxs-lookup"><span data-stu-id="3e2fb-128"><a href="multi-hop-support.md">Multi-hop Support</a></span></span><br/></td>
<td><span data-ttu-id="3e2fb-129">已將功能新增至 WinRM 2.0，以支援跨多部遠端電腦委派使用者認證。</span><span class="sxs-lookup"><span data-stu-id="3e2fb-129">Functionality was added to WinRM 2.0 that supports delegating user credentials across multiple remote computers.</span></span> <br/> <span data-ttu-id="3e2fb-130"><a href="authentication-constants.md"><strong>驗證常數</strong></a>主題已更新為新增下列常數： <strong>WSManFlagUseCredSsp</strong>。</span><span class="sxs-lookup"><span data-stu-id="3e2fb-130">The <a href="authentication-constants.md"><strong>Authentication Constants</strong></a> topic was updated to add the following constant: <strong>WSManFlagUseCredSsp</strong>.</span></span><br/> <span data-ttu-id="3e2fb-131">已新增下列 c + + API 以提供多重躍點支援： <a href="/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex3"><strong>IWSManEx3</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="3e2fb-131">The following C++ API was added to provide multi-hop support: <a href="/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex3"><strong>IWSManEx3</strong></a>.</span></span><br/> <span data-ttu-id="3e2fb-132">已新增下列腳本 API，以提供多重躍點支援： <a href="wsman-sessionflagusecredssp.md"><strong>WSMan. SessionFlagUseCredSsp</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="3e2fb-132">The following scripting API was added to provide multi-hop support: <a href="wsman-sessionflagusecredssp.md"><strong>WSMan.SessionFlagUseCredSsp</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3e2fb-133"><a href="quotas.md">遠端 Shell 的配額管理</a></span><span class="sxs-lookup"><span data-stu-id="3e2fb-133"><a href="quotas.md">Quota Management for Remote Shells</a></span></span><br/></td>
<td><span data-ttu-id="3e2fb-134">本主題包含遠端 shell 管理配額設定的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3e2fb-134">This topic includes information about quota configuration for remote shell management.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3e2fb-135"><a href="winrm-powershell-commandlets.md">WS-Management PowerShell 命令的受控參考</a></span><span class="sxs-lookup"><span data-stu-id="3e2fb-135"><a href="winrm-powershell-commandlets.md">Managed Reference for WS-Management PowerShell Commands</a></span></span><br/></td>
<td><span data-ttu-id="3e2fb-136">WinRM 2.0 的使用者可以使用 Windows PowerShell Cmdlet 進行系統管理。</span><span class="sxs-lookup"><span data-stu-id="3e2fb-136">Users of WinRM 2.0 can use Windows PowerShell cmdlets for system management.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 





