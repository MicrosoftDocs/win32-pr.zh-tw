---
description: Windows API 的參考內容清單。
ms.assetid: 9CA123F9-92F1-4761-9468-266DA422F70E
title: Windows API 索引
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e61a3f738905e98ad9cd1db85dbaa1746d7c613b1cc5b628805bcc3ddbea74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737635"
---
# <a name="windows-api-index"></a>Windows API 索引

以下是適用于桌面和伺服器應用程式的 Windows 應用程式設計介面 (API) 的參考內容清單。

使用 Windows API，您可以開發可在所有版本的 Windows 上順利執行的應用程式，同時充分利用每個版本特有的特性和功能。  (請注意，這先前稱為 WIN32 API。 Windows API 的名稱會更精確地反映其在16位 Windows 的根目錄，以及其在64位 Windows 上的支援。 ) 

## <a name="user-interface"></a>使用者介面

Windows UI API 會建立和使用 Windows 來顯示輸出、提示輸入使用者輸入，以及執行其他支援與使用者互動的工作。 大部分的應用程式會建立至少一個視窗。

-   [協助工具](../winauto/windows-accessibility-features-reference.md)
-   [桌面視窗管理員 (DWM) ](../dwm/reference.md)
-   [全球化服務](../intl/globalization-services.md)
-   [高 DPI](../hidpi/high-dpi-reference.md)
-   [多語系消費者介面 (MUI) ](../intl/multilingual-user-interface-reference.md)
-   [ (NLS 的國家語言支援) ](../intl/national-language-support-reference.md)
-   [消費者介面元素](../devnotes/user-interface.md)：

    -   [按鈕](../controls/bumper-button-button-control-reference.md)
    -   [游標](../menurc/caret-functions.md)
    -   [下拉式方塊](../controls/bumper-combobox-combobox-control-reference.md)
    -   [通用對話方塊](../dlgbox/common-dialog-box-reference.md)
    -   [通用控制項](../controls/individual-control-info.md)
    -   [資料指標](../menurc/cursor-reference.md)
    -   [對話方塊](../dlgbox/dialog-box-reference.md)
    -   [編輯控制項](../controls/bumper-edit-control-edit-control-reference.md)
    -   [標題控制項](../controls/bumper-header-control-header-control-reference.md)
    -   [圖示](../menurc/icon-reference.md)
    -   [鍵盤加速器](../menurc/keyboard-accelerator-reference.md)
    -   [清單方塊](../controls/bumper-list-box-list-box-control-reference.md)
    -   [清單視圖控制項](../controls/bumper-list-view-list-view-control-reference.md)
    -   [功能表](../menurc/menu-reference.md)
    -   [進度列](../controls/bumper-progress-bar-progress-bar-control-reference.md)
    -   [屬性工作表](../controls/bumper-property-sheet-property-sheets-reference.md)
    -   [Rich Edit 控制項](../controls/bumper-rich-edit-rich-edit-control-reference.md)
    -   [捲軸](../controls/bumper-scroll-bar-scroll-bars-reference.md)
    -   [靜態控制項](../controls/bumper-static-control-static-control-reference.md)
    -   [字串](../menurc/string-reference.md)
    -   [工具列](../controls/bumper-toolbar-toolbar-control-reference.md)
    -   [工具提示](../controls/bumper-tooltip-tooltip-control-reference.md)
    -   [Trackbars](../controls/bumper-trackbar-trackbar-control-reference.md)
    -   [樹狀檢視控制項](../controls/bumper-tree-view-tree-view-control-reference.md)

-   [Windows動畫管理員](../uianimation/windows-animation-reference.md)
-   [Windows功能區架構](../windowsribbon/windowsribbon-reference-entry.md)

## <a name="windows-environment-shell"></a>Windows 環境 (Shell) 

-   [Windows屬性系統](../properties/property-system-reference.md)
-   [Windows殼](/previous-versions/windows/desktop/legacy/ff521731(v=vs.85))
-   [Windows 搜尋](../search/-search-reference-entry-page.md)
-   [主控台](/windows/console/console-reference)

## <a name="user-input-and-messaging"></a>使用者輸入和訊息

-   [使用者互動](../user-interaction.md)
    -   [直接操作](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal)
    -   [筆跡輸入](/previous-versions/windows/desktop/input_ink/input-ink-portal)
    -   [輸入意見設定](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
    -   [互動內容](/previous-versions/windows/desktop/input_intcontext/interaction-context-portal)
    -   [指標裝置輸入堆疊](/previous-versions/windows/desktop/input_pointerdevice/pointer-device-stack-portal)
    -   [指標輸入訊息和通知](/previous-versions/windows/desktop/inputmsg/messages-and-notifications)
    -   [星形控制器輸入](/previous-versions/windows/desktop/input_radial/radialcontroller-portal)
    -   [Text Services Framework (TSF)](../tsf/text-services-framework.md)
    -   [觸控點擊測試](/previous-versions/windows/desktop/input_touchhittest/touch-hit-testing-portal)
    -   [觸控插入](/previous-versions/windows/desktop/input_touchinjection/touch-injection-portal)
-   [舊版使用者互動](../legacy-user-interaction-features.md)
    -   [觸控輸入](../wintouch/windows-touch-portal.md)
    -   [鍵盤輸入](../inputdev/keyboard-input.md)
    -   [滑鼠輸入](../inputdev/mouse-input.md)
    -   [原始輸入](../inputdev/raw-input.md)
-   [Windows 和訊息](../winmsg/windowing.md)：

    -   [訊息和訊息佇列](../winmsg/message-and-message-queue-reference.md)
    -   [Windows](../winmsg/window-reference.md)
    -   [視窗類別](../winmsg/window-class-reference.md)
    -   [視窗程式](../winmsg/window-procedure-reference.md)
    -   [計時器](../winmsg/timer-reference.md)
    -   [視窗屬性](../winmsg/window-property-reference.md)
    -   [勾點](../winmsg/hook-reference.md)

## <a name="data-access-and-storage"></a>資料存取與存放

-   [背景智慧型傳送服務 (BITS)](../bits/bits-reference.md)
-   [資料備份](../backup/backup.md)
    -   [Backup](../backup/backup-reference.md)
    -   [重複資料刪除](/previous-versions/windows/desktop/dedup/data-deduplication-api-reference)
    -   [磁碟區陰影複製](../vss/volume-shadow-copy-reference.md)
    -   [Windows Server Backup](/previous-versions/windows/desktop/wsb/windows-server-backup-api-interfaces)
-   [資料 Exchange](../dataxchg/data-exchange.md)：

    -   [剪貼簿](../dataxchg/clipboard-reference.md)
    -   [動態資料交換 (DDE) ](../dataxchg/dynamic-data-exchange-reference.md)
    -   [動態資料交換管理 (DDEML) ](../dataxchg/dynamic-data-exchange-management-library-reference.md)

-   [目錄管理](../fileio/directory-management-reference.md)
-   [磁碟管理](../fileio/disk-management-reference.md)
-   [分散式檔案系統 (DFS)](/previous-versions/windows/desktop/dfs/distributed-file-system-reference)
-   [分散式檔案系統複寫](/previous-versions/windows/desktop/dfsr/dfsr-wmi-classes)
-   [可擴充的儲存體引擎](../extensible-storage-engine/extensible-storage-engine-reference.md)
-   [檔案和 i/o (本機檔案系統) ](../fileio/file-management-reference.md)
-   [iSCSI 探索程式庫 API](/previous-versions/windows/desktop/iscsidisc/iscsi-discovery-library-reference)
-   [離線檔案](/previous-versions/windows/desktop/offlinefiles/offline-files-reference)
-   [包裝](/previous-versions/windows/desktop/opc/packaging-programming-reference)
-   [遠端差異壓縮](/previous-versions/windows/desktop/rdc/remote-differential-compression-reference)
-   [交易式 NTFS](../fileio/transactional-ntfs-reference.md)
-   [磁碟區管理](../fileio/volume-management-reference.md)
-   [虛擬硬碟 (VHD) ](/previous-versions/windows/desktop/legacy/dd323700(v=vs.85))
-   [Windows 存放裝置管理](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)
-   [Windows Data Access Component](/previous-versions/windows/desktop/legacy/aa968814(v=vs.85))
    -   [Microsoft 開放式資料庫連接 (ODBC)](/sql/odbc/reference/syntax/odbc-reference)
    -   [Microsoft OLE DB](/previous-versions/windows/desktop/ms718050(v=vs.85))
    -   [Microsoft ActiveX Data Objects (ADO)](/sql/ado/reference/ado-programmer-s-reference)

## <a name="diagnostics"></a>診斷

[診斷](/previous-versions//bb648685(v=vs.85))API 可讓您針對應用程式或系統問題進行疑難排解，並監視效能。

-   [應用程式復原和重新啟動](../recovery/application-recovery-and-restart-reference.md)
-   [偵錯](../debug/debugging-reference.md)
-   [錯誤處理](../debug/error-handling-reference.md)
-   [事件記錄](../eventlog/event-logging-reference.md)
-   [事件追蹤](../etw/event-tracing-reference.md)
-   [ (HCP) 的硬體計數器分析 ](/previous-versions/windows/desktop/hcp/hcp-reference)
-   [網路診斷架構 (NDF) ](../ndf/ndf-reference.md)
-   [網路監視器](../netmon2/reference.md)
-   [效能計數器](../perfctrs/performance-counters-reference.md)
-   [效能記錄檔及警示 (PLA) ](/previous-versions/windows/desktop/pla/performance-logs-and-alerts-reference)
-   [進程快照](/previous-versions/windows/desktop/proc_snap/process-snapshotting-reference)
-   [進程狀態 (PSAPI.DLL) ](../psapi/psapi-reference.md)
-   [結構化例外狀況處理](../debug/structured-exception-handling-reference.md)
-   [系統監視器](../sysmon/system-monitor-reference.md)
-   [等候鏈遍歷](../debug/wait-chain-traversal.md)
-   [Windows 錯誤報告 (WER)](../wer/wer-reference.md)
-   [Windows 事件記錄檔](../wes/windows-event-log-reference.md)
-   [Windows疑難排解平臺](/previous-versions/windows/desktop/wintt/windows-troubleshooting-reference)

## <a name="graphics-and-multimedia"></a>圖形與多媒體

[圖形、多媒體、](/previous-versions//aa969176(v=vs.85)) [音訊和影片](../audio-and-video.md)api 可讓應用程式併入格式化的文字、圖形、音訊和影片。

-   [核心音訊](../coreaudio/programming-reference.md)
-   [Direct2D](../direct2d/reference.md)
-   [DirectComposition](../directcomp/reference.md)
-   [DirectShow](../directshow/directshow-reference.md)
-   [DirectWrite](../directwrite/reference.md)
-   [DirectX](../directx-sdk--august-2009-.md)
-   [圖形裝置介面 (GDI) ](../gdi/windows-gdi.md)
-   [GDI+](../gdiplus/-gdiplus-class-gdi-reference.md)
-   [媒體串流](../mediastreaming/media-streaming-api-portal.md)
-   [Microsoft 媒體基礎](../medfound/media-foundation-programming-reference.md)
-   [Microsoft 電視技術](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-application-interface)
-   [Opengl](../opengl/opengl-reference.md)
-   [監視設定](../monitor/monitor-configuration-reference.md)
-   [多顯示器監視](../gdi/multiple-display-monitors-reference.md)
-   [取得圖片](/previous-versions/windows/desktop/acquisition/programming-reference)
-   [Windows色彩系統](../wcs/reference.md)
-   [Windows 影像處理元件 (WIC)](../wic/-wic-codec-reference.md)
-   [Windows媒體音訊和影片編解碼器和 DSP](/previous-versions//dd443208(v=vs.85))
-   [Windows Media Center](/previous-versions/windows/desktop/acquisition/programming-reference)
-   [Windows媒體格式](../wmformat/programming-reference.md)
-   [WindowsMedia Library 共用服務](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal)
-   [Windows Media Player](../wmp/windows-media-player-object-model-reference.md)
-   [Windows Media Services](/previous-versions/windows/desktop/dd893580(v=vs.85))
-   [Windows Movie Maker](/previous-versions/windows/desktop/wmmdvdm/windows-movie-maker-apis)
-   [Windows多媒體](../multimedia/multimedia-reference.md)

## <a name="devices"></a>裝置

-   [AllJoyn](/previous-versions/windows/desktop/alljoyn/alljoyn-api-portal)
-   [通訊資源](../devio/communications-reference.md)
-   [裝置存取](/previous-versions/windows/desktop/deviceaccess/device-access-api-c---programming-reference)
-   [裝置管理](../devio/device-management-reference.md)
-   [增強的存放區](/previous-versions/windows/desktop/enstor/enhanced-storage-reference)
-   [函數探索](/previous-versions/windows/desktop/fundisc/function-discovery-reference)
-   [映射主控](../imapi/imapi-reference.md)
-   [位置](../locationapi/windows-location-programming-reference.md)
-   [PnP X 關聯資料庫](/previous-versions/windows/desktop/fundisc/pnp-x-association-database-reference)
-   [列印](/windows-hardware/drivers/print/introduction-to-printing)
    -   [列印多工緩衝處理器](../printdocs/printing-and-print-spooler-reference.md)
    -   [列印檔案套件](../printdocs/tailored-app-printing-api.md)
    -   [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
    -   [列印票證](../printdocs/print-ticket-api.md)
    -   [XPS 列印](../printdocs/xpsprint-api.md)
-   [感應器](../sensorsapi/sensor-api-programming-reference.md)
-   [系統事件通知服務 (SENS) ](../sens/sens-reference.md)
-   [工具說明](../toolhelp/tool-help-reference.md)
-   [UPnP](../upnp/universal-plug-and-play-start-page.md)
-   [裝置上的 Web 服務](../wsdapi/web-services-for-devices-reference.md)
-   [Windows Image Acquisition (WIA)](../wia/-wia-reference.md)
-   [Windows媒體裝置管理員](../wmdm/programming-reference.md)
-   [Windows 可攜式裝置](../wpd_sdk/programming-reference.md)

## <a name="system-services"></a>系統服務

[系統服務](/previous-versions//aa969179(v=vs.85))api 可讓應用程式存取電腦的資源和基礎作業系統的功能，例如記憶體、檔案系統、裝置、進程和執行緒。

-   [COM](../com/reference.md)
-   [COM+](../cossdk/com--reference.md)
-   [壓縮 API](../cmpapi/-compression-portal.md)
-   [分散式交易協調器 (DTC)](/previous-versions/windows/desktop/ms686108(v=vs.85))
-   [動態連結程式庫 (Dll) ](../dlls/dynamic-link-library-functions.md)
-   [說明 API](/previous-versions/windows/desktop/helpapi/help-api-reference)
-   [處理序間通訊](../ipc/interprocess-communications.md)：
    -   [Mailslots](../ipc/mailslot-functions.md)
    -   [管道](../ipc/pipe-functions.md)
-   [核心交易管理員 (KTM) ](../ktm/ktm-reference.md)
-   [記憶體管理](../memory/memory-management-reference.md)
-   [作業錄製器](/previous-versions/windows/desktop/oprec/-operation-portal)
-   [電源管理](../power/power-management-reference.md)
-   [遠端桌面服務](../termserv/terminal-services-reference.md)
-   [處理序](../procthread/process-and-thread-reference.md)
-   [服務](../services/service-reference.md)
-   [同步處理](../sync/synchronization-reference.md)
-   [執行緒](../procthread/process-and-thread-reference.md)
-   [Windows桌面共用](/previous-versions/windows/desktop/rdp/windows-desktop-sharing-reference)
-   [Windows 系統資訊](../sysinfo/windows-system-information.md)
    -   [控制碼和物件](../sysinfo/handle-and-object-functions.md)
    -   [登錄](../sysinfo/registry-reference.md)
    -   [Time](../sysinfo/time-reference.md)
    -   [時間提供者](../sysinfo/time-provider-reference.md)

## <a name="security-and-identity"></a>安全性與身分識別

[安全性和身分識別](../devnotes/security.md)api 會在登入時啟用密碼驗證，為所有可共用的系統物件、特殊許可權的存取控制、版權管理和安全性審核提供任意的保護。

-   [驗證](../secauthn/authentication-reference.md)
-   [授權](../secauthz/authorization-reference.md)
-   [憑證註冊](../seccertenroll/certificate-enrollment-api-reference.md)
-   [碼編譯](../seccrypto/cryptography-reference.md)
-   [新一代密碼編譯 (CNG) ](../seccng/cng-reference.md)
-   [目錄服務](/previous-versions//ms682458(v=vs.85))
    -   [Active Directory Domain Services](../ad/active-directory-domain-services-reference.md)
    -   [Active Directory 服務介面 (ADSI) ](../adsi/adsi-reference.md)
-   [可延伸的驗證通訊協定 (EAP)](../eap/extensible-authentication-protocol-reference.md)
-   [可延伸的驗證通訊協定主機 (EAPHost) ](../eaphost/about-eap-host.md)
-   [MS-CHAP 密碼管理](/previous-versions/windows/desktop/mschap/ms-chap-password-management-reference)
-   [網路存取保護 (NAP)](../nap/nap-reference.md)
-   [NPS) 的網路原則伺服器擴充功能 (](../nps/ias-internet-authentication-service-reference.md)
-   [家長監護](../parcon/parental-controls-reference.md)
-   [安全性 WMI 提供者](../secprov/security-wmi-providers-reference.md)
-   [TPM 基本服務 (TBS)](../tbs/tbs-reference.md)
-   [Windows 生物特徵辨識架構](../secbiomet/biometric-service-api-reference.md)

## <a name="application-installation-and-servicing"></a>應用程式安裝和維護

-   [遊戲總管](/previous-versions/windows/desktop/legacy/ee415251(v=vs.85))
-   [並存元件](../sbscs/side-by-side-assemblies-reference.md)
-   [封裝、部署和查詢 Api](../appxpkg/api-reference.md
)
-   [開發人員授權](../devlic/developer-license-apis.md)
-   [重新開機管理員](../rstmgr/restart-manager-reference.md)
-   [Windows Installer](../msi/windows-installer-portal.md)

## <a name="system-admin-and-management"></a>系統管理員與管理

[系統管理](../srvnodes/system-administration.md)介面可讓您安裝、設定及服務應用程式或系統。

-   [開機設定資料 WMI 提供者](/previous-versions/windows/desktop/bcd/bcd-reference)
-   [容錯移轉叢集](/previous-versions/windows/desktop/mscs/failover-cluster-apis-portal)
-   [檔案伺服器資源管理員 (FSRM)](/previous-versions/windows/desktop/fsrm/fsrm-reference)
-   [群組原則](/previous-versions/windows/desktop/Policy/group-policy-reference)
-   [Microsoft Management Console (MMC) 2。0](/previous-versions/windows/desktop/mmc/mmc-reference)
-   [NetShell](/previous-versions/windows/desktop/netshell/netshell-reference)
-   [設定管理基礎結構](/previous-versions/windows/desktop/smi/settings-management-infrastructure--smi-)
-   [軟體清查記錄](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)
-   [軟體授權](/previous-versions/windows/desktop/secslapi/software-licensing-api-reference)
-   [重新開機管理員](../rstmgr/restart-manager-portal.md)
-   [設定管理基礎結構](/previous-versions/windows/desktop/smi/settings-management-infrastructure--smi-)
-   [[系統還原]](../sr/system-restore-portal.md)
-   [系統關閉](../shutdown/system-shutdown.md)
-   [工作排程器](../taskschd/task-scheduler-start-page.md)
-   [使用者存取記錄](/previous-versions/windows/desktop/ual/user-access-logging-reference)
-   [Windows Virtual PC](../vpc/virtual-pc-reference.md)
-   [Microsoft Virtual Server](/previous-versions/windows/desktop/msvs/microsoft-virtual-server-reference)
-   [網路負載平衡提供者](/previous-versions/windows/desktop/wlbsprov/network-load-balancing-provider-reference)
-   [Windows DefenderWMI v2](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)
-   [Windows Deployment Services](../wds/windows-deployment-services-portal.md)
-   [Windows Genuine Advantage](/previous-versions/windows/desktop/wingen/windows-genuine-advantage-api-functions)
-   [Windows管理基礎結構](/previous-versions/windows/desktop/wmi_v2/wmi-reference)
-   [Windows Management Instrumentation (WMI)](../wmisdk/wmi-reference.md)
-   [Windows 遠端管理](../winrm/portal.md)
-   [Windows資源保護](../wfp/windows-resource-protection-portal.md)
-   [Windows Server Update Services](/previous-versions/windows/desktop/ms744624(v=vs.85))
-   [Windows系統評定工具](../winsat/winsat-reference.md)
-   [Windows Update 代理程式](../wua_sdk/portal-client.md)

## <a name="networking-and-internet"></a>網路和網際網路

[網路](../devnotes/networking.md)api 可讓應用程式透過網路進行通訊。 您也可以建立和管理共用資源的存取權，例如目錄和網路印表機。

-   [網域名稱系統 (DNS)](../dns/dns-reference.md)
-   [動態主機設定通訊協定 (DHCP)](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
-   [傳真服務](/previous-versions/windows/desktop/fax/-mfax-fax-service-reference)
-   [連線精靈](/previous-versions/windows/desktop/get_connected/get-connected-wizard-api-reference)
-   [HTTP 伺服器](../http/http-server-api-reference.md)
-   [網際網路連線共用和防火牆](/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference)
-   [IP 協助程式](../iphlp/ip-helper-function-reference.md)
-   [IPv6 網際網路連線防火牆](/previous-versions/windows/desktop/ics/ipv6-firewall-configuration-reference)
-   [管理資訊基礎](/previous-versions/windows/desktop/mib/management-information-base-reference)
-   [訊息佇列 (MSMQ)](/previous-versions/windows/desktop/legacy/ms700112(v=vs.85))
-   [多播位址動態用戶端配置通訊協定 (MADCAP) ](/previous-versions/windows/desktop/madcap/madcap-reference)
-   [ (NAT) 的網路位址轉譯 ](/previous-versions/windows/desktop/ics/network-address-translation-traversal-reference)
-   [網路清單管理員 (NLM) ](../nla/network-list-manager-api-reference.md)
-   [網路管理](../netmgmt/network-management-reference.md)
-   [網路共用管理](../netshare/network-share-management-reference.md)
-   [對等](../p2psdk/portal.md)
-   [QOS) 的服務品質 (](/previous-versions/windows/desktop/qos/qos-reference)
-   [遠端程序呼叫](../rpc/reference.md)
-   [路由及遠端存取服務 (RAS) ](../rras/portal.md)
-   [簡易網路管理通訊協定 (SNMP)](../snmp/snmp-reference.md)
-   [SMB 管理](/previous-versions/windows/desktop/smb/smb-management-api-portal)
-   [ (TAPI 的電話語音應用程式設計介面) ](../tapi/telephony-application-programming-interfaces.md)
-   [WebDAV](../webdav/webdav-api-reference.md)
-   [WebSocket 通訊協定元件](../websock/web-socket-protocol-component-api-portal.md)
-   無線網路功能：
    -   [Bluetooth](../bluetooth/bluetooth-reference.md)
    -   [Irda](/previous-versions/windows/desktop/irda/irda-and-windows-sockets-reference)
    -   [行動寬頻](../mbn/mobile-broadband-networks-api-reference.md)
    -   [原生 Wifi](../nativewifi/native-wifi-reference.md)
    -   [Windows Connect Now](../wcn/windows-connect-now-reference.md)
    -   [Windows 連線管理員](../wcm/windows-connection-manager-reference.md)
-   [Windows 篩選平台](../fwp/fwp-reference.md)
-   [具有進階安全性的 Windows 防火牆](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference)
-   [Windows (WinHTTP) 的 HTTP 服務](../winhttp/winhttp-reference.md)
-   [Windows網際網路 (WinINet) ](../wininet/wininet-reference.md)
-   [Windows網路 (WNet) ](../wnet/windows-networking-reference.md)
-   [Windows網路虛擬化](/previous-versions/windows/desktop/wnv/windows-network-virtualization-portal)
-   [WindowsRSS 平臺](/previous-versions/windows/desktop/ms684702(v=vs.85))
-   [Windows (Winsock) 的通訊端](../winsock/winsock-reference.md)
-   [WindowsWeb 服務](../wsw/windows-web-services-reference.md)
-   [XML HTTP 擴充要求](/previous-versions/windows/desktop/ixhr2/ixmlhttprequest2-portal)

## <a name="deprecated-or-legacy-apis"></a>已淘汰或舊版 Api

以下是 Windows 用戶端和伺服器作業系統已過期或已取代或淘汰的技術和 api。

-   [DirectMusic](/previous-versions/ms807133(v=msdn.10))
-   [DirectSound](/previous-versions/windows/desktop/ee416975(v=vs.85))
-   Microsoft [UDDI SDK](/previous-versions/windows/desktop/aa966237(v=bts.10))現在隨附于[microsoft BizTalk Server](/previous-versions/bb905520(v=msdn.10))。
-   [網路動態資料交換 (DDE) ](../ipc/network-dde-reference.md)
-   [遠端安裝服務](/previous-versions/windows/it-pro/windows-server-2003/cc786442(v=ws.10))：改用[Windows 部署服務](../wds/windows-deployment-services-portal.md)。
-   [虛擬磁碟服務 (VDS) ](../vds/vds-reference.md)：請改用[Windows 儲存體管理](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)。
-   終端機服務：使用 [遠端桌面服務](../termserv/terminal-services-reference.md)。
-   [Windows媒體版權管理員](/previous-versions//bb614742(v=vs.85))
-   [Windows 訊息中心 (mapi) ](/previous-versions/windows/desktop/windowsmapi/mapi-stub-library-and-simple-mapi)：請改用[Office MAPI](/previous-versions/office/developer/office-2007/cc765775(v=office.12)) 。
-   [Windows 小工具平台](/previous-versions/windows/desktop/gadgetplatform/windows-gadget-platform-portal)：改為建立 UWP 應用程式。
-   [Windows 提要](/previous-versions/windows/desktop/sidebar/-sidebar-ref-entry)欄位：改為建立 UWP 應用程式。
-   [Windows SideShow](/previous-versions//ms744179(v=vs.85))：沒有取代。
-   [WPF 點陣圖效果](/previous-versions/windows/desktop/wibe/-wibe-about-bitmapeffects)
