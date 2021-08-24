---
description: 存取應用程式或腳本中的 WMI 本機或遠端資料時，您可能會遇到錯誤，範圍從遺失的類別到拒絕存取。 提供者也有可用的偵錯工具選項和疑難排解類別。
ms.assetid: b0aecdf6-ec30-49be-af4e-7eac5d124057
ms.tgt_platform: multiple
title: WMI 疑難排解
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40645c33da838658d66f608d672d979b38012fa855f26637f5896c4ec14c54ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794288"
---
# <a name="wmi-troubleshooting"></a>WMI 疑難排解

存取應用程式或腳本中的 WMI 本機或遠端資料時，您可能會遇到錯誤，範圍從遺失的類別到拒絕存取。 提供者也有可用的偵錯工具選項和疑難排解類別。

> [!Note]  
> 下列檔的目標是開發人員和 IT 系統管理員。 如果您是遇到關於 WMI 的錯誤訊息的使用者，您應該移至 [Microsoft 支援服務](https://support.microsoft.com/) 並搜尋錯誤訊息上所看到的錯誤碼。 如需有關疑難排解 WMI 腳本和 WMI 服務問題的詳細資訊，請參閱 [Wmi 無法運作！](/previous-versions/tn-archive/ff406382(v=msdn.10))

 

## <a name="wmi-diagnosis-utility"></a>WMI Diagnosis Utility

從 Windows 8 和 Windows Server 2012 開始，不再支援 WMI 診斷公用程式 (WMIDiag.exe) 。

* * Windows 7、Windows Server 2008 R2、Windows Vista 和 Windows Server 2008： * *

如果 WMI 傳回錯誤訊息，請注意，它們可能不會指出 WMI 服務或 WMI 提供者中的問題。 失敗可能源自于作業系統的其他部分，並透過 WMI 出現錯誤。 在任何情況下，請勿將 WMI 儲存機制刪除為第一個動作，因為刪除存放庫可能會導致系統損毀或已安裝的應用程式。

若要取得問題來源的詳細資訊，您可以下載並執行[WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en)診斷命令列工具。 這項工具會產生一份報告，通常可以找出問題的來源，並提供如何修正問題的指示。 報表也會協助 Microsoft 支援服務協助您。 您可以[下載下載中心的 WMI Diagnosis Utility。](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d)

除非您要撰寫低 [*耦合提供者*](gloss-d.md)，否則提供者寫入器可能也會發生偵錯工具的問題。 如需詳細資訊，請參閱 [偵錯工具提供者](debugging-providers.md)。

## <a name="logging-and-tracing"></a>記錄和追蹤

WMI 記錄檔不再存在;它們已由[Windows (ETW) 的事件追蹤](/windows/desktop/ETW/event-tracing-portal)取代。 如需詳細資訊，請參閱 [追蹤 Wmi 活動](tracing-wmi-activity.md)、 [記錄 Wmi 活動](logging-wmi-activity.md)和 [wmi 記錄](wmi-log-files.md)檔。

## <a name="troubleshooting-in-scripts-and-applications"></a>腳本和應用程式中的疑難排解

WMI 包含一組類別，可針對使用 WMI 提供者的用戶端應用程式 [進行疑難排解](wmi-troubleshooting-classes.md) 。 如需詳細資訊，請參閱 [疑難排解 WMI 用戶端應用程式](troubleshooting-wmi-client-applications.md)。

## <a name="how-provider-writers-can-prevent-wmi-problems"></a>提供者寫入器如何防止 WMI 問題

提供者寫入器可透過執行下列動作，防止許多會透過 WMI 出現在錯誤訊息中的問題：

-   正確註冊您的提供者。 如需詳細資訊，請參閱 [註冊提供者](registering-a-provider.md)。
-   將 [**\# pragma 自動**](pragma-autorecover.md)回復語句新增至定義您的提供者類別受控物件格式 (MOF) 檔。

如需詳細資訊，請參閱 [偵錯工具提供者](debugging-providers.md)、 [將資料提供給 WMI](providing-data-to-wmi.md)，以及 [提供者設定和疑難排解類別](provider-configuration-and-troubleshooting-classes.md)。

## <a name="access-denied"></a>拒絕存取

存取 WMI 命名空間和資料的腳本和應用程式所報告的拒絕存取錯誤通常會分成三個類別。 下表列出三個錯誤類別以及可能導致錯誤和可能解決方案的問題。



| 錯誤                                                                                                                        | 可能的問題                                                                                                                                                                                                                                                                                                                                                                     | 解決方案                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x800706BA `HRESULT_FROM_WIN32(RPC_S_SERVER_UNAVAILABLE)`<br/> 防火牆問題或伺服器無法使用。<br/>      | 電腦真的不存在，或者 Windows 防火牆封鎖連線<br/>                                                                                                                                                                                                                                                                                        | 連接到 Vista： **netsh advfirewall firewall set rule group = "windows management instrumentation (wmi) " new enable = yes** 連接到下層：允許 Windows 防火牆中的「遠端系統管理」規則。<br/>                                                                                                                                                                                                                                                                                                            |
| 0x80070005 **E \_ \_ 拒絕存取**<br/> DCOM 安全性拒絕存取。<br/>                                       | 使用者無法透過 DCOM 遠端存取電腦。 通常，當連接到具有不同作業系統版本的遠端電腦時，就會發生 DCOM 錯誤。<br/>                                                                                                                                                                                          | 在 dcomcnfg 中提供使用者遠端啟動和遠端啟用許可權。 以滑鼠右鍵按一下 [我的電腦 > 屬性。 在 [COM 安全性] 底下，按一下兩個區段的 [編輯限制]。 將您想要遠端存取、遠端啟動和遠端啟用的使用者提供給使用者。 然後移至 DCOM 設定，尋找「Windows Management Instrumentation」，並提供您想要遠端啟動和遠端啟用的使用者。 如需詳細資訊，請參閱 [在不同的作業系統間連接](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)<br/> |
| 0x80041003 **WBEM \_ E \_ \_ 拒絕存取**<br/> 存取者拒絕存取[ ](gloss-p.md)<br/> | 使用者沒有在 WMI 中執行操作的許可權。 當您將某些類別查詢為低許可權的使用者時，通常會發生這種情況，但當您嘗試叫用方法或將 WMI 實例變更為低許可權使用者時，通常會發生這種情況。 您要連接的命名空間已加密，而且使用者嘗試使用未加密的連接進行連線<br/> | 授與使用者使用 WMI 控制的存取權 (確定他們 \_ 使用支援加密的用戶端，將遠端存取設定為 true) 連線。<br/>                                                                                                                                                                                                                                                                                                                                                                                  |



 

-   通常，當連接到具有不同作業系統版本的遠端電腦時，就會發生 DCOM 錯誤。

-   提供者也可能會拒絕存取特定命名空間中的資料，或可能需要特定層級的連線安全性。 如需詳細資訊，請參閱 [設定用戶端應用程式進程安全性](setting-client-application-process-security.md) 和 [提供者裝載和安全性](provider-hosting-and-security.md)。

-   從網際網路連線防火牆 (ICF) 變更時發生拒絕存取錯誤。

    如需詳細資訊，請參閱[透過 Windows 防火牆連接](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista)。

-   當低完整性用戶端嘗試存取 WMI 時，DCOM 安全性會傳回拒絕存取錯誤。 例如，在 Internet Explorer 中執行的 ActiveX 控制項（其安全性層級設定為 [低]）沒有執行本機 WMI 作業的存取權。

    **Windows 7：** 低完整性使用者具有本機 WMI 作業的唯讀許可權。

## <a name="information-on-errors"></a>錯誤的資訊

當您收到來自 WMI 的錯誤訊息時，您可以在 [**Wmi 錯誤常數**](wmi-error-constants.md) 中找出訊息，或是在腳本、 [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)中找出訊息。 不過，錯誤本身所提供的資訊通常不足以判斷發生什麼事。 WMI 存放庫損毀可能會偽裝為類別或實例「找不到」。

如需 WMI 錯誤的詳細資訊：

-   WMI 記錄會追蹤 WMI 核心和來自提供者內的事件。 如需詳細資訊，請參閱 [記錄 WMI 活動](logging-wmi-activity.md)。
-   使用 [Wmi 疑難排解類別](wmi-troubleshooting-classes.md) 來檢查 wmi 內部狀態，或接收提供者或 WMI 服務事件的通知。 如需詳細資訊，請參閱 [提供者設定和疑難排解類別](provider-configuration-and-troubleshooting-classes.md) 和 [疑難排解 WMI 用戶端應用程式](troubleshooting-wmi-client-applications.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 疑難排解](wmi-troubleshooting.md) \(英文\)
</dt> <dt>

[追蹤 WMI 活動](tracing-wmi-activity.md)
</dt> <dt>

[記錄 WMI 活動](logging-wmi-activity.md)
</dt> </dl>

 

