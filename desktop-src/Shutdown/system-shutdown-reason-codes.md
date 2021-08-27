---
description: ExitWindowsEx 和 InitiateSystemShutdownEx 函式會在 dwReason 參數中使用關機原因代碼。 系統會處理最大數目原因的原因 \_ \_ 代碼。 最大 \_ 數目 \_ 的原因是由 reason. h 所定義。
ms.assetid: db1ecee0-40eb-4761-b5d8-9cc3c1c98cdf
title: '系統關機原因代碼 (原因 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef40cf53afd3abaf261e15f2caba735dea7963ee5b5f19cebc78c63a373962fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073198"
---
# <a name="system-shutdown-reason-codes"></a>系統關機原因代碼

[**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)和 [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa)函式會在 *dwReason* 參數中使用關機原因代碼。

系統會處理最大數目原因的原因 \_ \_ 代碼。 最大 \_ 數目 \_ 的原因是由 reason. h 所定義。

以下是主要原因旗標。 它們表示一般問題類型。



| 常數/值                                                                                                                                                                                                                                                                                 | 描述                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SHTDN_REASON_MAJOR_APPLICATION"></span><span id="shtdn_reason_major_application"></span><dl> <dt>**SHTDN \_\_主要 \_ 應用程式**</dt> <dt>0x00040000</dt>的原因 </dl>             | 應用程式問題。<br/>                                                                                                                                      |
| <span id="SHTDN_REASON_MAJOR_HARDWARE"></span><span id="shtdn_reason_major_hardware"></span><dl> <dt>**SHTDN \_\_主要 \_ 硬體**</dt> <dt>0x00010000</dt>的原因 </dl>                      | 硬體問題。<br/>                                                                                                                                         |
| <span id="SHTDN_REASON_MAJOR_LEGACY_API"></span><span id="shtdn_reason_major_legacy_api"></span><dl> <dt>**SHTDN \_\_主要 \_ 舊版 \_ API**</dt> <dt>0x00070000</dt>的原因 </dl>               | 已使用 [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna) 函式，而不是 [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa)。<br/> |
| <span id="SHTDN_REASON_MAJOR_OPERATINGSYSTEM"></span><span id="shtdn_reason_major_operatingsystem"></span><dl> <dt>**SHTDN \_\_主要 \_ 作業系統**</dt> <dt>0x00020000</dt>的原因 </dl> | 作業系統問題。<br/>                                                                                                                                 |
| <span id="SHTDN_REASON_MAJOR_OTHER"></span><span id="shtdn_reason_major_other"></span><dl> <dt>**SHTDN \_原因 \_ 嚴重的 \_ 其他**</dt> <dt>0x00000000</dt> </dl>                               | 其他問題。<br/>                                                                                                                                            |
| <span id="SHTDN_REASON_MAJOR_POWER"></span><span id="shtdn_reason_major_power"></span><dl> <dt>**SHTDN \_原因 \_ 主要 \_ POWER**</dt> <dt>0x00060000</dt> </dl>                               | 電源失敗。<br/>                                                                                                                                          |
| <span id="SHTDN_REASON_MAJOR_SOFTWARE"></span><span id="shtdn_reason_major_software"></span><dl> <dt>**SHTDN \_原因 \_ 主要 \_ 軟體**</dt> <dt>0x00030000</dt> </dl>                      | 軟體問題。<br/>                                                                                                                                         |
| <span id="SHTDN_REASON_MAJOR_SYSTEM"></span><span id="shtdn_reason_major_system"></span><dl> <dt>**SHTDN \_原因 \_ 主要 \_ 系統**</dt> <dt>0x00050000</dt> </dl>                            | 系統失敗。<br/>                                                                                                                                         |



以下是次要原因旗標。 他們會修改指定的主要原因旗標。 您可以將任何次要原因與任何主要原因搭配使用，但有些組合並沒有意義。



| 常數/值                                                                                                                                                                                                                                                                                                    | 描述                               |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------|
| <span id="SHTDN_REASON_MINOR_BLUESCREEN"></span><span id="shtdn_reason_minor_bluescreen"></span><dl> <dt>**SHTDN \_\_次要 \_ 藍屏**</dt> <dt>0x0000000F</dt>的原因 </dl>                                   | 藍色螢幕損毀事件。<br/>       |
| <span id="SHTDN_REASON_MINOR_CORDUNPLUGGED"></span><span id="shtdn_reason_minor_cordunplugged"></span><dl> <dt>**SHTDN \_原因 \_ 次要 \_ CORDUNPLUGGED**</dt> <dt>0x0000000b</dt> </dl>                          | 拔出。<br/>                     |
| <span id="SHTDN_REASON_MINOR_DISK"></span><span id="shtdn_reason_minor_disk"></span><dl> <dt>**SHTDN \_\_次要 \_ 磁片**</dt> <dt>0x00000007</dt>原因 </dl>                                                     | 磁碟]。<br/>                          |
| <span id="SHTDN_REASON_MINOR_ENVIRONMENT"></span><span id="shtdn_reason_minor_environment"></span><dl> <dt>**SHTDN \_原因 \_ 次要 \_ 環境**</dt> <dt>0x0000000c</dt> </dl>                                | 環境。<br/>                   |
| <span id="SHTDN_REASON_MINOR_HARDWARE_DRIVER"></span><span id="shtdn_reason_minor_hardware_driver"></span><dl> <dt>**SHTDN \_\_次要 \_ 硬體 \_ 驅動程式**</dt> <dt>0x0000000d</dt>的原因 </dl>                   | 司機。<br/>                        |
| <span id="SHTDN_REASON_MINOR_HOTFIX"></span><span id="shtdn_reason_minor_hotfix"></span><dl> <dt>**SHTDN \_\_次要修正 \_ 程式**</dt> <dt>0x00000011</dt>的原因 </dl>                                               | 熱修正。<br/>                       |
| <span id="SHTDN_REASON_MINOR_HOTFIX_UNINSTALL"></span><span id="shtdn_reason_minor_hotfix_uninstall"></span><dl> <dt>**SHTDN \_\_次要修正 \_ 程式 \_ 卸載**</dt> <dt>0x00000017</dt>的原因 </dl>                | 熱修正卸載。<br/>        |
| <span id="SHTDN_REASON_MINOR_HUNG"></span><span id="shtdn_reason_minor_hung"></span><dl> <dt>**SHTDN \_\_次要無 \_ 反應**</dt> <dt>0x00000005</dt>原因 </dl>                                                     | 反應 遲鈍。<br/>                  |
| <span id="SHTDN_REASON_MINOR_INSTALLATION"></span><span id="shtdn_reason_minor_installation"></span><dl> <dt>**SHTDN \_\_次要 \_ 安裝的原因**</dt> <dt>0x00000002</dt> </dl>                             | 安裝。<br/>                  |
| <span id="SHTDN_REASON_MINOR_MAINTENANCE"></span><span id="shtdn_reason_minor_maintenance"></span><dl> <dt>**SHTDN \_\_次要 \_ 維護**</dt> <dt>0x00000001</dt>的原因 </dl>                                | 維護。<br/>                   |
| <span id="SHTDN_REASON_MINOR_MMC"></span><span id="shtdn_reason_minor_mmc"></span><dl> <dt>**SHTDN \_\_次要 \_ MMC**</dt> <dt>0x00000019</dt>的原因 </dl>                                                        | MMC 問題。<br/>                     |
| <span id="SHTDN_REASON_MINOR_NETWORK_CONNECTIVITY"></span><span id="shtdn_reason_minor_network_connectivity"></span><dl> <dt>**SHTDN \_\_次要 \_ 網路 \_ 連接**</dt> <dt>0x00000014</dt>的原因 </dl>    | 網路連線能力。<br/>          |
| <span id="SHTDN_REASON_MINOR_NETWORKCARD"></span><span id="shtdn_reason_minor_networkcard"></span><dl> <dt>**SHTDN \_原因 \_ 次要 \_ NETWORKCARD**</dt> <dt>0x00000009</dt> </dl>                                | 網路卡。<br/>                  |
| <span id="SHTDN_REASON_MINOR_OTHER"></span><span id="shtdn_reason_minor_other"></span><dl> <dt>**SHTDN \_\_次要 \_ 其他**</dt> <dt>0x00000000</dt>的原因 </dl>                                                  | 其他問題。<br/>                   |
| <span id="SHTDN_REASON_MINOR_OTHERDRIVER"></span><span id="shtdn_reason_minor_otherdriver"></span><dl> <dt>**SHTDN \_原因 \_ 次要 \_ OTHERDRIVER**</dt> <dt>0x0000000e</dt> </dl>                                | 其他驅動程式事件。<br/>            |
| <span id="SHTDN_REASON_MINOR_POWER_SUPPLY"></span><span id="shtdn_reason_minor_power_supply"></span><dl> <dt>**SHTDN \_\_次要 \_ 電源 \_ 供應**</dt> <dt>0x0000000a</dt>的原因 </dl>                            | 電源。<br/>                  |
| <span id="SHTDN_REASON_MINOR_PROCESSOR"></span><span id="shtdn_reason_minor_processor"></span><dl> <dt>**SHTDN \_\_次要 \_ 處理器**</dt> <dt>0x00000008</dt>的原因 </dl>                                      | 處理器。<br/>                     |
| <span id="SHTDN_REASON_MINOR_RECONFIG"></span><span id="shtdn_reason_minor_reconfig"></span><dl> <dt>**SHTDN \_原因 \_ 次要 \_ 重新設定**</dt> <dt>0x00000004</dt> </dl>                                         | 配置。<br/>                   |
| <span id="SHTDN_REASON_MINOR_SECURITY"></span><span id="shtdn_reason_minor_security"></span><dl> <dt>**SHTDN \_\_次要 \_ 安全性**</dt> <dt>0x00000013</dt>的原因 </dl>                                         | 安全性問題。<br/>                |
| <span id="SHTDN_REASON_MINOR_SECURITYFIX"></span><span id="shtdn_reason_minor_securityfix"></span><dl> <dt>**SHTDN \_原因 \_ 次要 \_ SECURITYFIX**</dt> <dt>0x00000012</dt> </dl>                                | 安全性修補程式。<br/>                |
| <span id="SHTDN_REASON_MINOR_SECURITYFIX_UNINSTALL"></span><span id="shtdn_reason_minor_securityfix_uninstall"></span><dl> <dt>**SHTDN \_\_次要 \_ SECURITYFIX \_ 卸載**</dt> <dt>0x00000018</dt>的原因 </dl> | 安全性修補程式卸載。<br/> |
| <span id="SHTDN_REASON_MINOR_SERVICEPACK"></span><span id="shtdn_reason_minor_servicepack"></span><dl> <dt>**SHTDN \_原因 \_ 次要 \_ SERVICEPACK**</dt> <dt>0x00000010</dt> </dl>                                | Service pack。<br/>                  |
| <span id="SHTDN_REASON_MINOR_SERVICEPACK_UNINSTALL"></span><span id="shtdn_reason_minor_servicepack_uninstall"></span><dl> <dt>**SHTDN \_\_次要 \_ SERVICEPACK \_ 卸載**</dt> <dt>0x00000016</dt>的原因 </dl> | 卸載 Service pack。<br/>   |
| <span id="SHTDN_REASON_MINOR_TERMSRV"></span><span id="shtdn_reason_minor_termsrv"></span><dl> <dt>**SHTDN \_原因 \_ 次要 \_ TERMSRV**</dt> <dt>0x00000020</dt> </dl>                                            | 終端機服務。<br/>             |
| <span id="SHTDN_REASON_MINOR_UNSTABLE"></span><span id="shtdn_reason_minor_unstable"></span><dl> <dt>**SHTDN \_\_次要不 \_ 穩定的原因**</dt> <dt>0x00000006</dt> </dl>                                         | 穩定。<br/>                      |
| <span id="SHTDN_REASON_MINOR_UPGRADE"></span><span id="shtdn_reason_minor_upgrade"></span><dl> <dt>**SHTDN \_\_次要 \_ 升級原因**</dt> <dt>0x00000003</dt> </dl>                                            | 升級。<br/>                       |
| <span id="SHTDN_REASON_MINOR_WMI"></span><span id="shtdn_reason_minor_wmi"></span><dl> <dt>**SHTDN \_\_次要 \_ WMI**</dt> <dt>0x00000015</dt>的原因 </dl>                                                        | WMI 問題。<br/>                     |



下列選擇性旗標會提供事件的其他相關資訊。



| 常數/值                                                                                                                                                                                                                                                                      | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SHTDN_REASON_FLAG_USER_DEFINED"></span><span id="shtdn_reason_flag_user_defined"></span><dl> <dt>**SHTDN \_原因 \_ 旗標 \_ 使用者 \_ 定義**</dt> <dt>0x40000000</dt> </dl> | 原因代碼是由使用者定義。 如需詳細資訊，請參閱定義自訂原因代碼。 <br/> 如果不存在此旗標，則會由系統定義原因代碼。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SHTDN_REASON_FLAG_PLANNED"></span><span id="shtdn_reason_flag_planned"></span><dl> <dt>**SHTDN \_原因 \_ 旗 \_**</dt>標已規劃的 <dt>0x80000000</dt> </dl>                 | 已規劃關機。 系統會 (SSD) 檔產生系統狀態資料。 此檔案包含系統狀態資訊，例如處理常式、執行緒、記憶體使用量和設定。 <br/> 如果不存在此旗標，則表示關機未計畫。 通知和報告選項是由一組原則所控制。 例如，登入之後，系統會顯示一個對話方塊，報告已啟用原則的未計畫關機。 只有在系統上啟用 SSD 原則時，才會建立 SSD 檔案。 系統管理員可以使用[Windows 錯誤報告](../wer/windows-error-reporting.md)將 SSD 資料傳送到中央位置或 Microsoft。<br/> |



## <a name="remarks"></a>備註

系統會辨識下列組合。 下表指出在關機事件追蹤器中顯示的字串，並提供更詳細的描述。 預設字串是「找不到此原因的標題」。



| 合併                                                                                                | 描述                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SHTDN \_ 原因 \_ 主要 \_ 應用程式 \| SHTDN \_ 原因次要無 \_ \_ 反應                                            | 「應用程式：沒有回應」未規劃的重新開機或關機，無法針對沒有回應的應用程式進行疑難排解。<br/>                                                                                                                             |
| SHTDN \_ 原因 \_ 主要 \_ 應用程式 \| SHTDN \_ 原因 \_ 次要 \_ 安裝 \| SHTDN \_ 原因旗 \_ \_ 標已規劃    | 「應用程式：安裝 (計畫的) 」計畫的重新開機或關機，以執行應用程式安裝。<br/>                                                                                                                              |
| SHTDN \_ 原因 \_ 主要 \_ 應用程式 \| SHTDN \_ 原因 \_ 次要 \_ 維護                                     | 「應用程式：維護 (未規劃的) 」未規劃的重新開機或關機，以服務應用程式。<br/>                                                                                                                                    |
| SHTDN \_ 原因 \_ 主要 \_ 應用程式 \| SHTDN \_ 原因 \_ 次要 \_ 維護 \| SHTDN \_ 原因旗 \_ \_ 標已規劃     | 「Application：維護 (計畫的) 」計畫的重新開機或關機，以在應用程式上執行規劃的維護。<br/>                                                                                                                  |
| SHTDN \_ 原因 \_ 主要 \_ 應用程式 \| SHTDN \_ 原因不 \_ \_ 穩定                                        | 「應用程式：不穩定」未規劃的重新開機或關機，無法對不穩定的應用程式進行疑難排解。<br/>                                                                                                                                     |
| SHTDN \_ 原因 \_ 主要 \_ 硬體 \| SHTDN \_ 原因 \_ 次要 \_ 安裝                                       | 「硬體：安裝 (未規劃的) 」未規劃的重新開機或關機，無法開始或完成硬體安裝。<br/>                                                                                                                     |
| SHTDN \_ 原因 \_ 主要 \_ 硬體 \| SHTDN \_ 原因 \_ 次要 \_ 安裝 \| SHTDN \_ 原因 \_ 旗 \_ 標已規劃       | 「硬體：安裝 (計畫的) 」計畫的重新開機或關機，以開始或完成硬體安裝。<br/>                                                                                                                          |
| SHTDN \_ 原因 \_ 主要 \_ 硬體 \| SHTDN \_ 原因 \_ 次要 \_ 維護                                        | 「硬體：維護 (未規劃的) 」未規劃的重新開機或關閉系統上的硬體服務。<br/>                                                                                                                               |
| SHTDN \_ 原因 \_ 主要 \_ 硬體 \| SHTDN \_ 原因 \_ 次要 \_ 維護 \| SHTDN \_ 原因 \_ 旗 \_ 標已規劃        | 「硬體：維修 (計畫的) 」計畫的重新開機或關機，以在系統上服務硬體。<br/>                                                                                                                                    |
| \_ \_ 主要 \_ 舊版 \_ API 的 SHTDN 原因                                                                          | 「舊版 API 關閉」此關閉是由舊版 [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna) 函式所起始。 應用程式應該使用 [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) 函式。<br/> |
| SHTDN \_ 原因 \_ 主要 \_ 作業系統 \| SHTDN \_ 原因 \_ 次要修正 \_ 程式                                      | 「作業系統：熱修正 (未規劃的) 」未規劃的重新開機或關機，以安裝熱修正。<br/>                                                                                                                                        |
| SHTDN \_ 原因 \_ 主要 \_ 作業系統 \| SHTDN \_ 原因 \_ 次要修正 \_ 程式 \| SHTDN \_ 原因 \_ 旗 \_ 標已規劃      | 「作業系統：已規劃的熱修正 (計畫的) 」計畫的重新開機或關機，以安裝熱修正。<br/>                                                                                                                                             |
| SHTDN \_ 原因 \_ 主要 \_ 作業系統 \| SHTDN \_ 原因 \_ 次要 \_ 重新設定                                    | 「作業系統：重新設定 (未規劃的) 」未計畫的重新開機或關機，以變更作業系統設定。<br/>                                                                                                        |
| SHTDN \_ 原因 \_ 主要 \_ 作業系統 \| SHTDN \_ 原因 \_ 次要 \_ 重新設定 \| SHTDN \_ 原因 \_ 旗 \_ 標已規劃    | 「作業系統：重新設定 (計畫的) 」規劃的重新開機或關機，以變更作業系統設定。<br/>                                                                                                             |
| SHTDN \_ 原因 \_ 主要 \_ 作業系統 \| SHTDN \_ 原因 \_ 次要 \_ SECURITYFIX                                 | 「作業系統：安全性修正 (未規劃的) 」未計畫的重新開機或關機，以安裝安全性修補程式。<br/>                                                                                                                            |
| SHTDN \_ 原因 \_ 主要 \_ 作業系統 \| SHTDN \_ 原因 \_ 次要 \_ SECURITYFIX \| SHTDN \_ 原因 \_ 旗 \_ 標已規劃 | 「作業系統：安全性修正 (計畫的) 」計畫的重新開機或關機，以安裝安全性修補程式。<br/>                                                                                                                                 |
| SHTDN \_ 原因 \_ 主要 \_ 作業系統 \| SHTDN \_ 原因 \_ 次要 \_ SERVICEPACK \| SHTDN \_ 原因 \_ 旗 \_ 標已規劃 | 「作業系統： Service pack (計畫的) 」計畫的重新開機或關機，以安裝 Service pack。<br/>                                                                                                                                   |
| SHTDN \_ 原因 \_ 主要 \_ 作業系統 \| SHTDN \_ 原因 \_ 次要 \_ 升級 \| SHTDN \_ 原因 \_ 旗 \_ 標已規劃     | 「作業系統：升級 (計畫的) 」規劃的重新開機或關機，以升級作業系統設定。<br/>                                                                                                                    |
| SHTDN \_ 原因 \_ 的 \_ 其他 \| 主要 \_ SHTDN \_ 原因 \_                                                 | 「其他 (未規劃的) 」未計畫的關機或重新開機。<br/>                                                                                                                                                                                 |
| SHTDN \_ 原因 \_ 主要 \_ 其他 \| SHTDN \_ 原因 \_ 已 \_ 規劃次要其他 \| SHTDN \_ 原因 \_ 旗 \_ 標                 | 「已規劃的其他 () 」規劃的關機或重新開機。<br/>                                                                                                                                                                                      |
| SHTDN \_ 原因 \_ 主要的 \_ 其他 \| SHTDN \_ 原因次要無 \_ \_ 反應                                                  | 「其他失敗：系統沒有回應」系統變得沒有回應。<br/>                                                                                                                                                                  |
| SHTDN \_ 原因 \_ 主要 \_ 電源 \| SHTDN \_ 原因 \_ 次要 \_ CORDUNPLUGGED                                         | 「電源故障：插線線」電腦已中斷。<br/>                                                                                                                                                                           |
| SHTDN \_ 原因 \_ 主要 \_ POWER \| SHTDN \_ 原因 \_ 次要 \_ 環境                                           | 「電源故障：環境」發生電源中斷。<br/>                                                                                                                                                                                |
| SHTDN \_ 原因 \_ 主要 \_ 系統 \| SHTDN \_ 原因 \_ 次要 \_ 藍屏                                           | 「系統失敗：停止錯誤」電腦顯示藍色螢幕損毀事件。<br/>                                                                                                                                                        |
| SHTDN \_ 原因 \_ 主要 \_ 系統 \| SHTDN \_ 原因 \_ 次要 \_ 網路連線 \_ 能力                                | 「網路連線中斷 (未規劃的) 」電腦必須因為網路連線問題而關閉。<br/>                                                                                                                    |
| SHTDN \_ 原因 \_ 主要 \_ 系統 \| SHTDN \_ 原因 \_ 次要 \_ 安全性                                             | 「安全性問題」電腦因安全性問題而需要關機。<br/>                                                                                                                                                          |



 

您也可以定義自己的關機原因，並將其新增至登錄。 每個原因代碼都應該以登錄值的形式儲存在下列機碼中：**HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows \\ CurrentVersion \\ 可靠性 \\ \\<預設 \_ 系統 \_ 語言 \_ 識別碼>**

此索引鍵包含下列格式的值名稱： *xxxxx*;*nnn*;*nnnnn*。 分號會分隔值名稱的元件。

<dl> <dt>

<span id="xxxxx"></span><span id="XXXXX"></span>*Xxxxx*
</dt> <dd>

下列其中一到五個控制項旗標 (不能使用任何其他字元) 。



| 旗標 | 描述                                                                                       |
|------|---------------------------------------------------------------------------------------------------|
| P    | 規劃的關機;否則，會發生未計畫的關機。                                               |
| C    | 需要批註。 此旗標必須與 S 一起使用。<br/>                                  |
| B    | 需要識別碼。 此旗標必須搭配 D 使用。<br/>                                      |
| S    | 顯示 [預期的關機] 對話方塊。 必須使用 S、D 或兩者都是。<br/>   |
| D    | 顯示 [未預期的關機] 對話方塊。 必須使用 S、D 或兩者都是。<br/> |



 

使用旗標的順序並不重要。 例如，CSP 表示已規劃的關機，其中會顯示預期的關機對話方塊，並需要批註。

</dd> <dt>

<span id="nnn"></span><span id="NNN"></span>*nnn*
</dt> <dd>

主要原因。 此元件必須是範圍64-255 中的數位。 範圍0-63 是保留供系統使用。

</dd> <dt>

<span id="nnnnn"></span><span id="NNNNN"></span>*nnnnn*
</dt> <dd>

次要原因。 此元件必須在0-65535 範圍內。

</dd> </dl>

自訂原因會依主要原因號碼在使用者介面中排序，然後依次要原因號碼排序。 沒有兩個自訂原因可能會使用相同的主要和次要原因，除非有一個已規劃的原因，另一個則未計畫。 否則，系統將會使用第一個實例，並忽略其他實例。

每個登錄值的資料都是兩個字串（以 \\ n r 分隔） \\ 。 第一個字串是要在 [關機] 對話方塊中顯示的標題字串，並寫入事件記錄檔。 大小上限為64個字元。 標題字串必須是唯一的。 自訂標題不能符合系統所定義的標準標題，或其他自訂標題。 第二個字串是要在關機對話方塊中顯示的描述字串;這是選擇性的。 大小上限為256個字元。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsXP \[ desktop apps \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | WindowsServer 2003 \[ desktop app \| UWP 應用程式\]<br/>                         |
| 標頭<br/>                   | <dl> <dt>原因。h</dt> </dl> |



 

 
