---
title: 遠端 Shell 的配額管理
description: 配額管理可讓使用者更有效率地管理系統資源。
ms.assetid: 6651a500-a95a-45a1-b46a-27b2e9b36a1c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f8cfa177d6f09552238471ff29d81d0ac0b7351
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883217"
---
# <a name="quota-management-for-remote-shells"></a>遠端 Shell 的配額管理

配額管理可讓使用者更有效率地管理系統資源。 Windows遠端系統管理 (WinRM) 已新增一組特定的配額，以提供更好的服務品質、協助防止阻絕服務問題，以及將伺服器資源配置給並行使用者。 WinRM 配額的設定是以針對 Internet Information Services (IIS) 服務所執行的配額基礎結構為基礎。

藉由執行下列動作，執行配額有助於防止效能降低和拒絕服務問題：

-   限制使用者可以建立的 shell 和 shell 進程數目
-   限制並行使用者數目上限
-   管理配置給 shell 的記憶體數量
-   為非使用中的 shell 設定超時時間

## <a name="quota-settings"></a>配額設定

下列配額需要針對遠端 shell 管理強制執行。 您可以透過 winrm 公用程式或群組原則設定來設定這些配額。 由群組原則設定的設定會取代 winrm 公用程式所設定的配額。 如需設定 WinRM 群組原則的詳細資訊，請參閱[Windows 遠端管理的安裝和](installation-and-configuration-for-windows-remote-management.md)設定。

<dl> <dt>

<span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout
</dt> <dd>

刪除非作用中遠端 shell 之前的最長時間（以毫秒為單位）。 預設值為180000毫秒。 最短時間是1000毫秒。

</dd> <dt>

<span id="MaxProcessesPerShell"></span><span id="maxprocessespershell"></span><span id="MAXPROCESSESPERSHELL"></span>MaxProcessesPerShell
</dt> <dd>

每個 shell 允許的進程數目上限，包括 shell 的子進程。 預設值為 25。

</dd> <dt>

<span id="MaxMemoryPerShellMB"></span><span id="maxmemorypershellmb"></span><span id="MAXMEMORYPERSHELLMB"></span>MaxMemoryPerShellMB
</dt> <dd>

每個 shell 配置的記憶體數量上限，包括 shell 的子進程。 預設值為 1024 MB。

> [!Note]  
> 如果將 MaxMemoryPerShellMB 設定為小於預設值，則不支援此行為。

 

</dd> <dt>

<span id="MaxShellsPerUser"></span><span id="maxshellsperuser"></span><span id="MAXSHELLSPERUSER"></span>MaxShellsPerUser
</dt> <dd>

每位使用者的最大 shell 數目。 預設值是 30。

</dd> <dt>

<span id="MaxConcurrentUsers"></span><span id="maxconcurrentusers"></span><span id="MAXCONCURRENTUSERS"></span>MaxConcurrentUsers
</dt> <dd>

可以開啟 shell 的並行使用者數目上限。 預設值為 10。

</dd> </dl>

## <a name="deprecated-quotas"></a>已淘汰配額

WinRM 2.0 將 MaxShellRunTime 配額設定為唯讀。 變更此配額的值將不會影響遠端 shell。

## <a name="retrieving-quota-configuration-information"></a>正在抓取配額設定資訊

若要檢查配額設定，請輸入 **winrm get winrm/config**。

下列程式碼片段是以文字為基礎的 WinRM 設定範例，具有預設配額設定。

``` syntax
Config

          ...         

          Winrs

                   AllowRemoteShellAccess = true

                   IdleTimeout = 7200000

                   MaxConcurrentUsers = 10

                   MaxProcessesPerShell = 25

                   MaxMemoryPerShellMB = 1024

                   MaxShellsPerUser = 30
```

## <a name="configuring-shell-quotas"></a>設定 Shell 配額

您可以透過群組原則設定或手動設定配額。 如需特定設定的詳細資訊，請參閱[Windows 遠端管理的安裝和](installation-and-configuration-for-windows-remote-management.md)設定。

**使用群組原則設定配額**

1.  以系統管理員身分開啟 [命令提示字元] 視窗。
2.  在命令提示字元中，輸入 **gpedit.msc**。 **群組原則物件編輯器**] 視窗隨即開啟。
3.  在 [電腦設定] **\\) \\ 系統管理範本元件** 下，尋找 **Windows 遠端管理**，並 **Windows 遠端 Shell** 群組原則物件 (GPO Windows。
4.  在 [ **擴充** ] 索引標籤上，選取設定以查看描述。 按兩下設定以進行編輯。

**手動設定配額**

1.  以系統管理員身分開啟 [命令提示字元] 視窗。
2.  在命令提示字元中，輸入 **winrm set winrm/config/winrs ' @ {** _&lt; &gt; Quota_*_= "_* _&lt; Value &gt;_ *_"} '_*

例如，若要將每位使用者的最大 shell 數目從5增加到7，請輸入 **winrm set winrm/config/winrs ' @ {MaxShellsPerUser = "7"} '**。

 

 




