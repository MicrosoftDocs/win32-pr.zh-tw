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
# <a name="whats-new-in-winrm-20"></a>WinRM 2.0 的新功能

Windows 遠端管理2.0 版提供新功能。  (WinRM 2.0) 

WinRM 2.0 包含在 Windows Server 2008 R2 和 Windows 7 中。

您也可以下載適用于 Windows Server 2008 Service Pack 2 (SP2) 和 Windows Vista （含 Service Pack 2） (SP2) 的 WinRM 2.0。 如需下載 WinRM 2.0 的詳細資訊，請參閱 [KB968929](https://support.microsoft.com/kb/968929)。

下表列出 WinRM 2.0 的檔。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>主題</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="client-shell-api.md">WinRM 用戶端 Shell API</a><br/></td>
<td>WinRM 用戶端 Shell 應用程式開發介面 (API) 提供在遠端電腦上建立和管理 shell 和 shell 作業、命令和資料流程的功能。 <br/></td>
</tr>
<tr class="even">
<td><a href="winrm-plugin-api.md">WinRM 外掛程式 API</a><br/></td>
<td>WinRM 外掛程式 API 提供的功能，可讓使用者藉由針對支援的 <a href="windows-remote-management-glossary.md"><em>資源 uri</em></a> 和作業來執行某些 api 來寫入外掛程式。<br/></td>
</tr>
<tr class="odd">
<td><a href="winrm-application-hosting.md">管理託管服務的基礎結構</a><br/></td>
<td>WinRM 2.0 引進了裝載架構。 支援兩種裝載模型。 其中一個是網際網路資訊服務 (IIS) 型，另一個則是 WinRM –以服務為基礎。 <br/> 如需主機配置的詳細資訊，請參閱下列主題：<br/>
<ul>
<li><a href="iis-host-plug-in-configuration.md">IIS 主機外掛程式設定</a></li>
<li><a href="wsman-service-plug-in-configuration.md">WinRM 服務外掛程式設定</a></li>
</ul></td>
</tr>
<tr class="even">
<td><a href="dmtf-association-traversal.md">透過關聯遍歷進行的 DMTF 設定檔探索</a><br/></td>
<td>關聯分析可讓使用者使用標準篩選機制來抓取關聯類別的實例。<br/></td>
</tr>
<tr class="odd">
<td><a href="remote-shell-infrastructure-improvements.md">遠端 Shell 基礎結構改進</a><br/></td>
<td>本主題包含 WinRM 的遠端基礎結構增強功能的相關資訊。 <br/></td>
</tr>
<tr class="even">
<td><a href="multi-hop-support.md">多重躍點支援</a><br/></td>
<td>已將功能新增至 WinRM 2.0，以支援跨多部遠端電腦委派使用者認證。 <br/> <a href="authentication-constants.md"><strong>驗證常數</strong></a>主題已更新為新增下列常數： <strong>WSManFlagUseCredSsp</strong>。<br/> 已新增下列 c + + API 以提供多重躍點支援： <a href="/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex3"><strong>IWSManEx3</strong></a>。<br/> 已新增下列腳本 API，以提供多重躍點支援： <a href="wsman-sessionflagusecredssp.md"><strong>WSMan. SessionFlagUseCredSsp</strong></a>。<br/></td>
</tr>
<tr class="odd">
<td><a href="quotas.md">遠端 Shell 的配額管理</a><br/></td>
<td>本主題包含遠端 shell 管理配額設定的相關資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="winrm-powershell-commandlets.md">WS-Management PowerShell 命令的受控參考</a><br/></td>
<td>WinRM 2.0 的使用者可以使用 Windows PowerShell Cmdlet 進行系統管理。<br/></td>
</tr>
</tbody>
</table>



 

 

 





