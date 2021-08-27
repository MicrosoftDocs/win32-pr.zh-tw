---
title: 遠端 Shell 基礎結構改進
description: Windows遠端系統管理2.0 版 (WinRM 2.0) 提供許多遠端 shell 基礎結構的增強功能。
ms.assetid: b22693ba-fa43-44bb-9b2d-0c64fad6e3cc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf88a472319b4b4677992f97509a3603cfe4a32f272388caf9db100b6e7457ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121658"
---
# <a name="remote-shell-infrastructure-improvements"></a>遠端 Shell 基礎結構改進

Windows遠端系統管理2.0 版 (WinRM 2.0) 提供許多遠端 shell 基礎結構的增強功能。 下列主題將詳細說明這些改進：

-   [多重躍點支援](multi-hop-support.md)
-   [遠端 Shell 的配額管理](quotas.md)

WinRM 遠端 shell 基礎結構的其中一項改進，是加入更健全的 shell 管理員來維護使用者特定的 shell 資訊。 WinRM 使用者可以在遠端電腦上建立 shell 來執行命令或腳本。 此外，使用者可以在電腦上建立多個 shell。 使用者和系統管理員都需要管理 shell 的能力。 使用者可以列舉、取得和刪除其所建立的 shell。 系統管理員可以列舉所有使用中的 shell，並取得本機或遠端主機上特定 shell 的詳細資料。 系統管理員也可以刪除本機或遠端主機上的任何作用中 shell。

當使用者或系統管理員列舉使用中的 shell 時，WinRM 服務可以傳回下列資訊。

<dl> <dt>

<span id="ShellId"></span><span id="shellid"></span><span id="SHELLID"></span>ShellId
</dt> <dd>

指定 shell 的唯一識別碼。

</dd> <dt>

<span id="Environment_variables"></span><span id="environment_variables"></span><span id="ENVIRONMENT_VARIABLES"></span>環境變數
</dt> <dd>

指定使用者所設定的任何環境變數。

</dd> <dt>

<span id="WorkingDirectory"></span><span id="workingdirectory"></span><span id="WORKINGDIRECTORY"></span>WorkingDirectory
</dt> <dd>

指定 shell 的起始目錄。

</dd> <dt>

<span id="ResourceURI"></span><span id="resourceuri"></span><span id="RESOURCEURI"></span>ResourceURI
</dt> <dd>

指定 shell 作業的資源 URI。 資源 URI 可以用來抓取 shell 實例特定的外掛程式設定。

</dd> <dt>

<span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout
</dt> <dd>

指定在沒有任何要求的情況下，shell 將保持開啟狀態的最大持續時間（以毫秒為單位）。

</dd> <dt>

<span id="InputStreams"></span><span id="inputstreams"></span><span id="INPUTSTREAMS"></span>InputStreams
</dt> <dd>

指定 shell 的輸入資料流程。

</dd> <dt>

<span id="OutputStreams"></span><span id="outputstreams"></span><span id="OUTPUTSTREAMS"></span>OutputStreams
</dt> <dd>

指定 shell 的輸出資料流程。

</dd> <dt>

<span id="Shell_creation_time"></span><span id="shell_creation_time"></span><span id="SHELL_CREATION_TIME"></span>Shell 建立時間
</dt> <dd>

指定 shell 的建立時間戳記。

</dd> <dt>

<span id="IdleTime"></span><span id="idletime"></span><span id="IDLETIME"></span>IdleTime
</dt> <dd>

指定 shell 已閒置的持續時間（以毫秒為單位）。

</dd> <dt>

<span id="UserId"></span><span id="userid"></span><span id="USERID"></span>UserId
</dt> <dd>

指定使用者識別碼。

</dd> <dt>

<span id="Hostname_or_IP_address"></span><span id="hostname_or_ip_address"></span><span id="HOSTNAME_OR_IP_ADDRESS"></span>主機名稱或 IP 位址
</dt> <dd>

指定建立 shell 之電腦的主機名稱或 IP 位址。

</dd> <dt>

<span id="Shell_memory_usage"></span><span id="shell_memory_usage"></span><span id="SHELL_MEMORY_USAGE"></span>Shell 記憶體使用量
</dt> <dd>

指定 shell 已使用的記憶體數量。

</dd> <dt>

<span id="Number_of_processes"></span><span id="number_of_processes"></span><span id="NUMBER_OF_PROCESSES"></span>進程數目
</dt> <dd>

指定 shell 所建立的進程數目。

</dd> </dl>

## <a name="enumerating-a-shell-on-a-local-host"></a>列舉本機主機上的 Shell

下列命令示範如何使用 winrm 公用程式來列舉 WinRM 用戶端上的 shell： **winrm 列舉 shell**。

下列以文字為基礎的範例會顯示 shell 列舉的輸出：

``` syntax
Shell
    ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E
    ResourceUri = http://schemas.microsoft.com/wbem/wsman/1/windows/shell/cmd
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin
    OutputStreams = stdout stderr
    ShellRunTime = P0DT0H0M36S
    ShellInactivity = P0DT0H0M35S

Shell
    ShellId = EE3F11CE-FB3C-4C4E-B113-6F4D643C97D8
    ResourceUri = http://schemas.microsoft.com/powershell/Microsoft.PowerShell
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin pr
    OutputStreams = stdout
    ShellRunTime = P0DT0H1M46S
    ShellInactivity = P0DT0H0M45S
    MemoryUsed = 48MB
    ChildProcesses = 0

Shell
    ShellId = 8FD7F2C4-A434-4D58-A7E8-46F8BF202D0B
    ResourceUri = http://schemas.microsoft.com/powershell/Microsoft.PowerShell
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin pr
    OutputStreams = stdout
    ShellRunTime = P0DT0H1M47S
    ShellInactivity = P0DT0H0M47S
    MemoryUsed = 48MB
    ChildProcesses = 0
```

如需詳細資訊，請參閱下列命令所提供的線上說明： **winrm 列舉-？**。

## <a name="retrieving-information-about-a-specific-shell"></a>正在抓取特定 Shell 的相關資訊

系統管理員或使用者也可以使用 ShellId 識別碼來取得 shell 的相關資訊。 下列命令示範如何使用 winrm 公用程式來取得特定 shell 的相關資訊： **winrm get shell？ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E**。

下列以文字為基礎的範例會顯示 shell 資訊的輸出：

``` syntax
Shell
    ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E
    ResourceUri = http://schemas.microsoft.com/wbem/wsman/1/windows/shell/cmd
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin
    OutputStreams = stdout stderr
    ShellRunTime = P0DT0H0M36S
    ShellInactivity = P0DT0H0M35S
```

如需詳細資訊，請參閱下列命令所提供的線上說明： **winrm get-？**。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[多重躍點支援](multi-hop-support.md)
</dt> <dt>

[遠端 Shell 的配額管理](quotas.md)
</dt> <dt>

[WS-Management PowerShell 命令的受控參考](winrm-powershell-commandlets.md)
</dt> </dl>

 

 




