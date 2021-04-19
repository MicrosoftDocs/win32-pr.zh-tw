---
title: 對 Windows 應用程式的封裝、部署及查詢進行疑難排解
description: 使用這些建議來針對封裝、部署或查詢應用程式封裝時所遇到的問題進行疑難排解。
ms.assetid: 38E327C6-0345-4FA6-BCDB-5FA2FCD421FB
ms.topic: article
ms.date: 02/20/2020
manager: dcscontentpm
ms.custom:
- CI 111497
- CSSTroubleshooting
- contperf-fy21q2
ms.openlocfilehash: a2ee7c28e7de2d616bd01e9b5cae0de3c325caf4
ms.sourcegitcommit: 80198645ddacc3c12c72f3814b71ade0f415e705
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/25/2021
ms.locfileid: "106993689"
---
# <a name="troubleshooting-packaging-deployment-and-query-of-windows-apps"></a>對 Windows 應用程式的封裝、部署及查詢進行疑難排解

使用這些建議來針對您在封裝、部署或查詢 Windows 應用程式套件時所遇到的問題進行疑難排解 ( msix/.appx) 開發人員。

> [!NOTE]
> 本文適用于開發人員。 如果您不是開發人員，而且您正在尋找 Windows 應用程式安裝錯誤的說明，請參閱 [windows 支援](https://support.microsoft.com/hub/4338813/windows-help?os=windows-10)。

## <a name="get-diagnostic-information"></a>取得診斷資訊

當 API 失敗時，它會傳回描述問題的錯誤碼。 如果錯誤碼未提供足夠的資訊，您可以在詳細的事件記錄檔中找到更多診斷資訊。

若要使用 **事件檢視器** 來存取封裝和部署事件記錄檔，請遵循下列步驟：

1. 請執行下列其中一個步驟：

    * 按一下 [Windows] 功能表上的 [ **開始** ]，輸入 **事件檢視器**，然後 **按 enter**。
    * 執行 **eventvwr.msc services.msc**。

2. 在左側頁面中，展開 [**本機)**  >  **應用程式和服務記錄** 檔] 事件檢視器 ( >  **Microsoft**  >  **Windows**。
3. 檢查下列類別的可用記錄：

    * **AppxPackagingOM**  > **Microsoft-Windows-AppxPackaging/Operational**
    * **Appxdeployment-server-伺服器**  > **Microsoft-Windows-AppXDeploymentServer/Operational**

從查看 **appxdeployment-server-Server** 底下的記錄開始。 如果錯誤是由 **0x80073CF0** 或 **ERROR_INSTALL_OPEN_PACKAGE_FAILED** 所造成，則 **AppxpackagingOM** 記錄中可能會有其他詳細資料。

您也可以使用 PowerShell 中的 [AppxLog](/powershell/module/appx/get-appxlog) 命令取得前幾個記錄的事件。 下列範例會顯示與最近部署作業相關聯的記錄檔。

```PowerShell
Get-Appxlog
```

下列範例會在另一個視窗中，顯示與互動式資料表中最新部署作業相關聯的記錄檔。

```PowerShell
Get-Appxlog | Out-GridView
```

## <a name="common-error-codes"></a>常見的錯誤碼

下表列出一些最常見的錯誤碼。 如果您需要這些錯誤之一的進一步協助，或如果您遇到不在此清單中的錯誤碼，請參閱 [其他說明選項](#get-additional-help)。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>錯誤碼</th>
<th>值</th>
<th>描述與可能的原因</th>
</tr>
</thead>
<tbody>
<tr class="even">
<td><strong>E_FILENOTFOUND</strong></td>
<td>0x80070002</td>
<td>找不到檔案或路徑。 這可能發生在 COM typelib 驗證期間，目錄的路徑實際上必須存在於您的 MSIX 套件中。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_BAD_FORMAT</strong></td>
<td>0x8007000B</td>
<td>封裝的格式不正確，需要重新建立或重新簽署。<br/> 如果簽署憑證主體名稱與 AppxManifest.xml 發行者名稱不相符，您可能會收到此錯誤。<br/> 請參閱 <a href="how-to-sign-a-package-using-signtool.md">如何使用 SignTool 簽署應用程式套件</a>。<br/></td>
</tr>
<tr class="even">
<td><strong>E_INVALIDARG</strong></td>
<td>0x80070057</td>
<td>一或多個引數無效。 如果您檢查 AppXDeployment-Server 事件記錄檔，並看到下列事件：「安裝封裝時，系統無法登錄 repositoryExtension 副檔名，因為發生下列錯誤：參數不正確。」 <br/> 如果資訊清單元素 DisplayName 或 Description 包含 Windows 防火牆不允許的字元，您可能會收到這個錯誤;亦即 | 而且全部都是因為 Windows 無法建立套件的 AppContainer 設定檔。 請從資訊清單移除這些字元，並嘗試安裝套件。 <br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_OPEN_</strong><br/> <strong>PACKAGE_FAILED</strong><br/></td>
<td>0x80073CF0</td>
<td>無法開啟封裝。<br/> 可能的原因：<br/>
<ul>
<li>套件未經簽署。</li>
<li>發行者名稱與簽署憑證主體不符。</li>
<li>遺漏 file://前置詞，或在指定的位置找不到封裝。</li>
</ul>
如需詳細資訊，請檢查 <strong>AppxPackagingOM</strong> 事件記錄檔。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_PACKAGE_</strong><br/> <strong>NOT_FOUND</strong><br/></td>
<td>0x80073CF1</td>
<td>找不到封裝。<br/> 移除目前使用者未安裝的封裝時，您可能會收到此錯誤。<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_INVALID_</strong><br/> <strong>包</strong><br/></td>
<td>0x80073CF2</td>
<td>封裝資料無效。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_RESOLVE_</strong><br/> <strong>DEPENDENCY_FAILED</strong><br/></td>
<td>0x80073CF3</td>
<td>套件無法通過更新、相依性或衝突的驗證。<br/> 可能的原因：<br/>
<ul>
<li>傳入的套件與安裝的套件衝突。</li>
<li>找不到指定的套件相依性。</li>
<li>套件不支援正確的處理器架構。</li>
</ul>
如需詳細資訊，請檢查 <strong>Appxdeployment-server 伺服器</strong> 事件記錄檔。<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_OUT_</strong><br/> <strong>OF_DISK_SPACE</strong><br/></td>
<td>0x80073CF4</td>
<td>您的電腦上沒有足夠的磁碟空間。 請釋放一些空間，然後再試一次。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_NETWORK_</strong><br/> <strong>失敗</strong><br/></td>
<td>0x80073CF5</td>
<td>無法下載套件。<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>REGISTRATION_FAILURE</strong><br/></td>
<td>0x80073CF6</td>
<td>無法註冊封裝。<br/> 如需詳細資訊，請查看 <strong>Appxdeployment-server 伺服器</strong> 事件記錄檔。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>DEREGISTRATION_EFAILURE</strong><br/></td>
<td>0x80073CF7</td>
<td>無法取消註冊封裝。<br/> 移除封裝時，您可能會收到此錯誤。<br/> 如需詳細資訊，請查看 <strong>Appxdeployment-server 伺服器</strong> 事件記錄檔。<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_CANCEL</strong></td>
<td>0x80073CF8</td>
<td>使用者已取消安裝要求。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_FAILED</strong></td>
<td>0x80073CF9</td>
<td>套件安裝失敗。 洽詢軟體廠商。<br/> 如需詳細資訊，請查看 <strong>Appxdeployment-server 伺服器</strong> 事件記錄檔。<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_REMOVE_FAILED</strong></td>
<td>0x80073CFA</td>
<td>封裝移除失敗。<br/> 您可能會收到此錯誤，指出在套件卸載期間發生的失敗。<br/> 如需詳細資訊，請參閱 <a href="/uwp/api/windows.management.deployment.packagemanager.removepackageasync"><strong>RemovePackageAsync</strong></a>。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGE_</strong><br/> <strong>ALREADY_EXISTS</strong><br/></td>
<td>0x80073CFB</td>
<td>已安裝所提供的套件，因此無法重新安裝該套件。 <br/> 如果您安裝的套件與已經安裝的套件不符，您可能會收到這個錯誤。 請注意，數位簽章也是封裝的一部分。 因此，如果已重建或重新簽署套件，它就不再與先前安裝的封裝位相同。 有兩個可修正此錯誤的可能選項： (1) 遞增應用程式的版本號碼，然後重建並重新簽署封裝 (2) 移除系統上每個使用者的舊套件，再安裝新的套件。 <br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_NEEDS_REMEDIATION</strong></td>
<td>0x80073CFC</td>
<td>無法啟動應用程式。 請嘗試重新安裝應用程式。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>PREREQUISITE_FAILED</strong><br/></td>
<td>0x80073CFD</td>
<td>無法滿足指定的安裝先決條件。<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_</strong><br/> <strong>REPOSITORY_CORRUPTED</strong><br/></td>
<td>0x80073CFE</td>
<td>套件存放庫已損毀。<br/> 如果此登錄機碼參考的資料夾不存在或已損毀，您可能會收到此錯誤： <br/> <strong>HKLM\Software\Microsoft\Windows</strong><br/> <strong>CurrentVersion\Appx\PackageRepositoryRoot</strong><br/> 若要從此狀態復原，請重新整理您的電腦。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>POLICY_FAILURE</strong><br/></td>
<td>0x80073CFF</td>
<td>若要安裝此應用程式，您需要開發人員授權或啟用側載功能的系統。 <br/> 如果套件不符合下列其中一項需求，您可能會收到此錯誤：<br/>
<ul>
<li>應用程式會使用 F5 在具有 Windows 開發人員授權的電腦上 Visual Studio 中進行部署。</li>
<li>封裝會使用 Microsoft 簽章簽署，並部署為 Windows 或 Microsoft Store 的一部分。</li>
<li>封裝會以信任的簽章簽署，並安裝在具有開發人員授權的電腦上、已啟用 AllowAllTrustedApps 原則的已加入網域電腦，或是已啟用 AllowAllTrustedApps 原則的 Windows 側載授權電腦上。</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_UPDATING</strong></td>
<td>0x80073D00</td>
<td>因為應用程式目前正在更新，所以無法啟動。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DEPLOYMENT_</strong><br/> <strong>BLOCKED_BY_POLICY</strong><br/></td>
<td>0x80073D01</td>
<td>原則封鎖了封裝部署作業。 請連絡您的系統管理員。<br/> 可能的原因：<br/>
<ul>
<li>應用程式控制原則封鎖了封裝部署。</li>
<li>封裝部署會被 [ &quot; 允許特殊設定檔中的部署作業] &quot; 原則封鎖。</li>
</ul>
其中一個可能的原因是漫遊設定檔的需求。 如需有關在使用者帳戶上設定漫遊使用者設定檔的詳細資訊，請參閱 <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj649079(v=ws.11)">部署漫遊使用者設定檔</a>。 如果您的系統上未設定任何原則，而且您仍然看到此錯誤，可能是您以暫存設定檔登入。 請登出再重新登入，然後再次嘗試操作。<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGES_IN_USE</strong></td>
<td>0x80073D02</td>
<td>無法安裝封裝，因為它修改的資源目前正在使用中。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_RECOVERY_</strong><br/> <strong>FILE_CORRUPT</strong><br/></td>
<td>0x80073D03</td>
<td>無法復原封裝，因為復原所需的資料已損毀。<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INVALID_</strong><br/> <strong>STAGED_SIGNATURE</strong><br/></td>
<td>0x80073D04</td>
<td>簽章無效。 若要在開發人員模式下註冊，Appxsignature.p7x. appxsignature.p7x 和 AppxBlockMap.xml 必須有效或不應該存在。<br/> 如果您是使用 F5 搭配 Visual Studio 的開發人員，請確定您建立的專案目錄不包含舊版封裝的簽章或區塊對應檔案。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DELETING_EXISTING_</strong><br/> <strong>APPLICATIONDATA_STORE_FAILED</strong><br/></td>
<td>0x80073D05</td>
<td>刪除封裝先前現有的應用程式資料時發生錯誤。<br/> 如果 <a href="/previous-versions/hh441475(v=vs.110)">模擬器正在執行</a> ，您可能會收到此錯誤。 關閉模擬器。 如果應用程式資料中有開啟的檔案，您也可以取得此錯誤 (例如，如果您在文字編輯器中開啟記錄檔) 。<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>PACKAGE_DOWNGRADE</strong><br/></td>
<td>0x80073D06</td>
<td>無法安裝封裝，因為已安裝此套件的較高版本。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_SYSTEM_</strong><br/> <strong>NEEDS_REMEDIATION</strong><br/></td>
<td>0x80073D07</td>
<td>偵測到系統二進位檔中有錯誤。 若要修正此問題，請嘗試重新整理電腦。 <br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_APPX_INTEGRITY_</strong><br/> <strong>FAILURE_EXTERNAL</strong><br/></td>
<td>0x80073D08</td>
<td>在系統上偵測到損毀的非 Windows 二進位檔。 <br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_RESILIENCY_</strong><br/> <strong>FILE_CORRUPT</strong><br/></td>
<td>0x80073D09</td>
<td>因為修復所需的資料已損毀，所以無法繼續操作。 <br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_FIREWALL_</strong><br/> <strong>SERVICE_NOT_RUNNING</strong><br/></td>
<td>0x80073D0A</td>
<td>無法安裝封裝，因為 Windows 防火牆服務未執行。 啟用 Windows 防火牆服務，然後再試一次。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGE_MOVE_FAILED</strong></td>
<td>0x80073D0B</td>
<td>套件移動作業失敗。<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_VOLUME_</strong><br/> <strong>NOT_EMPTY</strong><br/></td>
<td>0x80073D0C</td>
<td>部署作業失敗，因為磁片區不是空的。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_VOLUME_</strong><br/> <strong>OFFLINE</strong><br/></td>
<td>0x80073D0D</td>
<td>部署作業失敗，因為磁片區已離線。 針對套件更新，磁片區指的是所有套件版本的已安裝磁片區。<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_VOLUME_</strong><br/> <strong>腐敗</strong><br/></td>
<td>0x80073D0E</td>
<td>部署作業失敗，因為指定的磁片區已損毀。<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_NEEDS_REGISTRATION</strong><br/> <strong></strong><br/></td>
<td>0x80073D0F</td>
<td>部署作業失敗，因為指定的應用程式必須先註冊。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_WRONG_</strong><br/> <strong>PROCESSOR_ARCHITECTURE</strong><br/></td>
<td>0x80073D10</td>
<td>部署作業失敗，因為封裝的目標處理器架構錯誤。<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_DEV_SIDELOAD_</strong><br/> <strong>LIMIT_EXCEEDED</strong><br/></td>
<td>0x80073D11</td>
<td>您已達到此裝置上允許的最大開發人員側載封裝數目。 請卸載側載套件，然後再試一次。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_OPTIONAL_</strong><br/> <strong>PACKAGE_REQUIRES_</strong><br/> <strong>MAIN_PACKAGE</strong><br/></td>
<td>0x80073D12</td>
<td>需要主要應用程式封裝，才能安裝此選用套件。 請先安裝主要套件，然後再試一次。<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_NOT_</strong><br/> <strong>SUPPORTED_ON_FILESYSTEM</strong><br/></td>
<td>0x80073D13</td>
<td>此檔案系統不支援此應用程式套件類型。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGE_MOVE_</strong><br/> <strong>BLOCKED_BY_STREAMING</strong><br/></td>
<td>0x80073D14</td>
<td>在應用程式完成串流處理之前，會封鎖「套件移動」作業。<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_OPTIONAL_</strong><br/> <strong>PACKAGE_APPLICATIONID_</strong><br/> <strong>NOT_UNIQUE</strong><br/></td>
<td>0x80073D15</td>
<td>主要或另一個選用的應用程式套件與此選用套件具有相同的應用程式識別碼。 變更選用封裝的應用程式識別碼，以避免發生衝突。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGE_STAGING_</strong><br/> <strong>舉 SERVICEREQUESTSTATUSENUM.ONHOLD</strong><br/></td>
<td>0x80073D16</td>
<td>已保留此暫存會話，以允許設定另一個預備作業的優先順序。<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_INVALID_</strong><br/> <strong>RELATED_SET_UPDATE</strong><br/></td>
<td>0x80073D17</td>
<td>無法更新相關的集合，因為更新的集合無效。 您必須同時更新相關集合中的所有套件。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_OPTIONAL_</strong><br/> <strong>PACKAGE_REQUIRES_MAIN_</strong><br/> <strong>PACKAGE_FULLTRUST_CAPABILITY</strong><br/></td>
<td>0x80073D18</td>
<td>具有 FullTrust 進入點的選用套件需要主要套件具有 <strong>runFullTrust</strong> 功能。<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br/> <strong>BY_USER_LOG_OFF</strong><br/></td>
<td>0x80073D19</td>
<td>發生錯誤，因為使用者已登出。<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PROVISION_OPTIONAL_</strong><br/> <strong>PACKAGE_REQUIRES_MAIN_</strong><br/> <strong>PACKAGE_PROVISIONED</strong><br/></td>
<td>0x80073D1A</td>
<td>選用套件布建也需要布建相依性主要套件。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGES_REPUTATION_</strong><br/> <strong>CHECK_FAILED</strong><br/></td>
<td>0x80073D1B</td>
<td>這些套件無法進行 <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">SmartScreen 信譽檢查</a>。<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGES_REPUTATION_</strong><br/> <strong>CHECK_TIMEDOUT</strong><br/></td>
<td>0x80073D1C</td>
<td><a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">SmartScreen 信譽檢查</a>作業已超時。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DEPLOYMENT_OPTION_</strong><br/> <strong>NOT_SUPPORTED</strong><br/></td>
<td>0x80073D1D</td>
<td>不支援目前的部署選項。<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_APPINSTALLER_</strong><br/> <strong>ACTI加值稅ION_BLOCKED</strong><br/></td>
<td>0x80073D1E</td>
<td>因為此應用程式的 appinstaller 更新設定，所以已封鎖啟用。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_REGISTRATION_FROM_</strong><br/> <strong>REMOTE_DRIVE_NOT_SUPPORTED</strong><br/></td>
<td>0x80073D1F</td>
<td>不支援遠端磁片磁碟機。 使用<strong> \\ server\share</strong>來註冊遠端封裝。<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_APPX_RAW_</strong><br/> <strong>DATA_WRITE_FAILED</strong><br/></td>
<td>0x80073D20</td>
<td>無法處理並將下載的套件資料寫入磁片。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br/> <strong>BY_VOLUME_POLICY_PACKAGE</strong><br/></td>
<td>0x80073D21</td>
<td>因為每個套件系列的原則限制了非系統磁片區上的部署，所以部署作業已遭到封鎖。 針對每個原則，此應用程式必須安裝到系統磁片磁碟機，但不會設為預設值。 在 [存放裝置設定] 中，讓系統磁片磁碟機成為儲存新內容的預設位置，然後重試安裝。<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br/> <strong>BY_VOLUME_POLICY_MACHINE</strong><br/></td>
<td>0x80073D22</td>
<td>因為電腦範圍內的原則限制了非系統磁片區上的部署，所以部署作業已遭到封鎖。 針對每個原則，此應用程式必須安裝到系統磁片磁碟機，但不會設為預設值。 在 [存放裝置設定] 中，讓系統磁片磁碟機成為儲存新內容的預設位置，然後重試安裝。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br/> <strong>BY_PROFILE_POLICY</strong><br/></td>
<td>0x80073D23</td>
<td>因為不允許特殊設定檔部署，所以已封鎖部署作業 (特殊設定檔是使用者設定檔，在使用者登出) 之後將會捨棄變更。 請嘗試登入不是特殊設定檔的帳戶。 您可以嘗試登出並重新登入目前的帳戶，或嘗試登入其他帳戶。<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_DEPLOYMENT_FAILED_</strong><br/> <strong>CONFLICTING_MUTABLE_PACKAGE_</strong><br/> <strong>目錄</strong><br/></td>
<td>0x80073D24</td>
<td>部署作業失敗，因為有衝突的套件可變動 <a href="/uwp/schemas/appxpackage/uapmanifestschema/element-desktop6-mutablepackagedirectory">套件目錄</a>。 若要安裝此套件，請移除具有衝突可變動套件目錄的現有套件。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_SINGLETON_RESOURCE_</strong><br/> <strong>INSTALLED_IN_ACTIVE_USER</strong><br/></td>
<td>0x80073D25</td>
<td>套件安裝失敗，因為指定了單一資源，且已安裝該套件的另一個使用者登入。 確定已安裝套件的所有作用中使用者都已登出，然後重試安裝。<br/></td>
</tr>
<tr class="even">
<td>ERROR_DIFFERENT_VERSION_<strong></strong><br/> <strong>OF_PACKAGED_SERVICE_INSTALLED</strong><br/></td>
<td>0x80073D26</td>
<td>套件安裝失敗，因為安裝了不同版本的服務。 請嘗試安裝較新版本的套件。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_SERVICE_EXISTS_</strong><br/> <strong>AS_NON_PACKAGED_SERVICE</strong><br/></td>
<td>0x80073D27</td>
<td>套件安裝失敗，因為服務的版本存在於 msix/.appx 套件之外。 請洽詢您的軟體廠商。<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGED_SERVICE_</strong><br/> <strong>REQUIRES_ADMIN_PRIVILEGES</strong><br/></td>
<td>0x80073D28</td>
<td>套件安裝失敗，因為需要系統管理員許可權。 請洽詢系統管理員以安裝此套件。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_REDIRECTION_TO_</strong><br/> <strong>DEFAULT_ACCOUNT_NOT_ALLOWED</strong><br/></td>
<td>0x80073D29</td>
<td>封裝部署失敗，因為當呼叫者未這麼做時，此作業會重新導向至預設帳戶。<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_LACKS_</strong><br/> <strong>CAPABILITY_TO_DEPLOY_ON_HOST</strong><br/></td>
<td>0x80073D2A</td>
<td>封裝部署失敗，因為封裝需要能夠以原生方式將此主機設為目標。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_UNSIGNED_PACKAGE_</strong><br/> <strong>INVALID_CONTENT</strong><br/></td>
<td>0x80073D2B</td>
<td>封裝部署失敗，因為它的內容對未簽署的套件無效。<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_UNSIGNED_PACKAGE_</strong><br/> <strong>INVALID_PUBLISHER_NAMESPACE</strong><br/></td>
<td>0x80073D2C</td>
<td>封裝部署失敗，因為它的發行者不在未簽署的命名空間中。<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_SIGNED_PACKAGE_</strong><br/> <strong>INVALID_PUBLISHER_NAMESPACE</strong><br/></td>
<td>0x80073D2D</td>
<td>封裝部署失敗，因為它的發行者不在已簽署的命名空間中。<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_EXTERNAL_</strong><br/> <strong>LOCATION_NOT_ALLOWED</strong><br/></td>
<td>0x80073D2E</td>
<td>封裝部署失敗，因為它的發行者不在已簽署的命名空間中。<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_FULLTRUST_</strong><br/> <strong>HOSTRUNTIME_REQUIRES_MAIN_</strong><br/> <strong>PACKAGE_FULLTRUST_CAPABILITY</strong><br/></td>
<td>0x80073D2F</td>
<td>解析為具有完全信任內容之套件的主機執行時間相依性，需要主要套件具有 <strong>runFullTrust</strong> 功能。<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_PACKAGING_INTERNAL</strong></td>
<td>0x80080200</td>
<td>封裝 API 遇到內部錯誤。<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INTERLEAVING_</strong><br/> <strong>NOT_ALLOWED</strong><br/></td>
<td>0x80080201</td>
<td>封裝無效，因為它的內容是交錯的。<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_RELATIONSHIPS_</strong><br/> <strong>NOT_ALLOWED</strong><br/></td>
<td>0x80080202</td>
<td>封裝無效，因為它包含 OPC 關聯性。<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_MISSING_</strong><br/> <strong>REQUIRED_FILE</strong><br/></td>
<td>0x80080203</td>
<td>封裝無效，因為它遺漏資訊清單或區塊對應，或存在程式碼完整性檔案，但遺失簽章檔案。<br/> 請確定封裝未遺失其中一個或多個必要的檔案：<br/>
<ul>
<li>\AppxManifest.xml</li>
<li>\AppxBlockMap.xml</li>
</ul>
如果封裝包含 \AppxMetadata\CodeIntegrity.cat，它也必須包含 \AppxSignature.p7x。<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_MANIFEST</strong></td>
<td>0x80080204</td>
<td>封裝的 AppxManifest.xml 檔無效。<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_BLOCKMAP</strong></td>
<td>0x80080205</td>
<td>封裝的 AppxBlockMap.xml 檔無效。<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_CORRUPT_CONTENT</strong></td>
<td>0x80080206</td>
<td>無法讀取套件內容，因為它已損毀。<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_BLOCK_</strong><br/> <strong>HASH_INVALID</strong><br/></td>
<td>0x80080207</td>
<td>區塊的計算雜湊值不符合區塊對應中儲存的值。<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_REQUESTED_</strong><br/> <strong>RANGE_TOO_LARGE</strong><br/></td>
<td>0x80080208</td>
<td>當轉譯成區塊的位元組範圍時，要求的位元組範圍超過 4 GB。<br/></td>
</tr>
<tr class="even">
<td><strong>TRUST_E_NOSIGNATURE</strong></td>
<td>0x800B0100</td>
<td>主體中沒有簽章。<br/> 如果封裝未簽署或簽章無效，您可能會收到此錯誤。 必須簽署套件才能進行部署。<br/></td>
</tr>
<tr class="odd">
<td><strong>CERT_E_UNTRUSTEDROOT</strong></td>
<td>0x800B0109</td>
<td>憑證鏈已處理，但在信任提供者不信任的根憑證中終止。<br/> 請參閱 <a href="/previous-versions/br230260(v=vs.110)">簽署封裝</a>。<br/></td>
</tr>
<tr class="even">
<td><strong>CERT_E_CHAINING</strong></td>
<td>0x800B010A</td>
<td>無法建立信任的根憑證授權單位的憑證鏈。<br/> 請參閱 <a href="/previous-versions/br230260(v=vs.110)">簽署封裝</a>。<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong> <br/> <strong>SIP_CLIENT_DATA</strong> <br/></td>
<td>0x80080209</td>
<td>用來簽署封裝的 <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO</strong></a>結構未包含必要的資料<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_</strong> <br/> <strong>KEY_INFO</strong> <br/></td>
<td>0x8008020A</td>
<td>用來加密或解密封裝的 <a href="/windows/win32/api/appxpackaging/ns-appxpackaging-appx_key_info"><strong>APPX_KEY_INFO</strong></a> 結構包含不正確資料。<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>CONTENTGROUPMAP</strong><br/></td>
<td>0x8008020B</td>
<td>Msix/.appx 套件的內容群組對應無效。<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>APPINSTALLER</strong><br/></td>
<td>0x8008020C</td>
<td>封裝的 <a href="/windows/msix/app-installer/app-installer-root">appinstaller</a> 檔無效。<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_DELTA_BASELINE_</strong><br/> <strong>VERSION_MISMATCH</strong><br/></td>
<td>0x8008020D</td>
<td>差異套件中的基準套件版本與要更新之基準套件中的版本不相符。<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_DELTA_PACKAGE_</strong><br/> <strong>MISSING_FILE</strong><br/></td>
<td>0x8008020E</td>
<td>差異套件遺漏更新套件中的檔案。<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>DELTA_PACKAGE</strong><br/></td>
<td>0x8008020F</td>
<td>差異套件無效。<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_DELTA_APPENDED_</strong><br/> <strong>PACKAGE_NOT_ALLOWED</strong><br/></td>
<td>0x80080210</td>
<td>目前的作業不允許差異附加的封裝。<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>PACKAGING_LAYOUT</strong><br/></td>
<td>0x80080211</td>
<td>封裝設定檔案無效。<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>PACKAGESIGNCONFIG</strong><br/></td>
<td>0x80080212</td>
<td>PackageSignConfig 檔無效。<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_RESOURCESPRI_</strong><br/> <strong>NOT_ALLOWED</strong><br/></td>
<td>0x80080213</td>
<td>當套件資訊清單中沒有任何資源元素時，不允許使用 .resources 檔。<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_FILE_</strong><br/> <strong>COMPRESSION_MISMATCH</strong><br/></td>
<td>0x80080214</td>
<td>基準中的檔案壓縮狀態和更新的封裝不符。<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>PAYLOAD_PACKAGE_EXTENSION</strong><br/></td>
<td>0x80080215</td>
<td>若是以較舊平臺為目標的裝載套件，則不允許使用非 .appx 延伸模組。<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>ENCRYPTION_EXCLUSION_FILE_LIST</strong><br/></td>
<td>0x80080216</td>
<td>EncryptionExclusionFileList 檔無效。<br/></td>
</tr>
</tbody>
</table>

## <a name="applications-dont-start-and-their-names-are-dimmed"></a>應用程式無法啟動，而且其名稱會呈現暗灰色

在以 Windows 10 為基礎的電腦上，您無法啟動某些應用程式，且應用程式名稱會呈現暗灰色。

![某些應用程式名稱在 [開始] 功能表中會顯示為暗灰色](./images/app-names-dimmed.png)

當您選取灰色名稱來嘗試開啟應用程式時，可能會收到下列其中一個錯誤訊息：

> 發生問題 \<*application name*> 。 請洽詢您的系統管理員，瞭解如何修復或重新安裝  
> 錯誤：無法開啟此應用程式

此外，下列事件專案會記錄在 **應用程式和 Services\Microsoft\Windows\Apps** 下的「TWinUI/Operational」記錄檔中：

> 記錄檔名稱： Microsoft-Windows-TWinUI/Operational  
> 來源： Microsoft-Windows-沉浸式 Shell  
> 日期： <*日期*>  
> 事件識別碼：5960  
> 工作分類： (5960)   
> 層級：錯誤  
> 關鍵字：  
> 描述：  
> 應用程式的啟用 Microsoft.BingNews_8wekyb3d8bbwe！適用于 Windows 的 AppexNews。 因為啟動合約的套件處於狀態：已修改，所以已封鎖其錯誤0x80073CFC。  

### <a name="cause"></a>原因

發生此問題的原因是已修改應用程式對應套件狀態值的登錄專案。

### <a name="resolution"></a>解決方案

> [!WARNING]
> 如果您使用登錄編輯程式或使用其他方法不正確地修改登錄，則可能會發生嚴重問題。 您可能必須重新安裝作業系統才能解決問題。 Microsoft 無法保證可以解決這些問題。 您必須自行承擔修改登錄的風險。

若要修正此問題：

1. 啟動登錄編輯程式，然後找出 **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList** 子機碼。
2. 若要備份子機碼資料，請以滑鼠右鍵按一下 **PackageList**，選取 [ **匯出**]，然後將資料儲存為登錄檔。
3. 針對事件識別碼5960記錄專案中列出的每個應用程式，請遵循下列步驟：  
   1. 找出 **PackageStatus** 專案。
   2. 將 **PackageStatus** 的值設定為零 (**0**) 。
   > [!NOTE]  
   > 如果 **PackageList** 下的應用程式沒有任何專案，則問題有一些其他原因。 在本文的範例事件案例中，完整的子機碼是 **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList\Microsoft.BingNews_8wekyb3d8bbwe!AppexNews\PackageStatus**
4. 重新啟動電腦。

## <a name="get-additional-help"></a>取得其他說明

如果您需要進一步協助解決問題，請在封裝、部署或查詢 Windows 應用程式套件 ( msix/.appx) 時遇到問題。如需開發人員，請參閱這些額外的開發人員支援資源。

- [Microsoft 問&a](/answers/topics/uwp.html?filter=all&sort=active) 提供專家和 Microsoft 工程師的相關和及時解答您的技術問題。
- 如需有關開發問題的社區協助，我們有 [論壇](https://social.msdn.microsoft.com/Forums/newthread?category=windowsapps&forum=wpdevelop&prof=required)和 [StackOverflow](https://stackoverflow.com/questions)。
- [Windows 開發人員支援](https://developer.microsoft.com/windows/support)網站說明其他支援選項。

## <a name="related-topics"></a>相關主題

- [如何使用 SignTool 簽署應用程式套件](how-to-sign-a-package-using-signtool.md) \(英文\)
- [如何針對應用程式封裝簽章錯誤進行疑難排解](how-to-troubleshoot-app-package-signature-errors.md)
