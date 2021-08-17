---
title: Windows篩選平臺可擴充 Helper 類別
description: Windows 篩選平台 (WFP) 包含網路診斷架構 (NDF) helper 類別，稱為篩選平臺協助程式類別 (FPHC) 。
ms.assetid: 006ea30c-8682-4a3d-803a-73dba5162696
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff972beffebb44b33eb68a0439193307639522738ac1f8766845404c03d3cd9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065208"
---
# <a name="windows-filtering-platform-extensible-helper-class"></a>Windows篩選平臺可擴充 Helper 類別

[Windows 篩選平台 (WFP) ](/windows/desktop/FWP/windows-filtering-platform-start-page)包含網路診斷架構 (NDF) helper 類別，稱為篩選平臺協助程式類別 (FPHC) 。 FPHC 可協助識別 WFP 造成連線問題的根本原因。 協力廠商防火牆開發人員可以執行自己的 NDF helper 類別。 FPHC 擴充性可讓您在診斷期間叫用這些協力廠商 helper 類別。

本主題假設您已熟悉 [WFP API](/windows/desktop/FWP/windows-filtering-platform-start-page)。

## <a name="why-extend-the-fphc"></a>為什麼要延伸 FPHC？

撰寫呼叫 WFP API 之應用程式的所有開發人員都應該撰寫可延伸 FPHC 的 NDF 協助程式類別。

FPHC 可將 WFP 識別為連接問題的原因。 如果有的話，FPHC 也可以識別建立封鎖網路流量之篩選準則的提供者。 FPHC 會將這項資訊傳遞給 NDF，接著可以通知使用者，WFP 造成連線問題，並提供封鎖流量的提供者名稱。

不過，FPHC 無法對使用者提出矯正措施，也不能提供篩選器封鎖使用者流量的原因。 只有 FPHC 延伸模組可以執行這些工作。

請考慮使用協力廠商防火牆應用程式呼叫 WFP API。 如果協力廠商防火牆會執行 FPHC 延伸模組，則可以執行自訂動作來處理 NDF 所識別的連線問題。 當 NDF 診斷出應用程式已被協力廠商防火牆封鎖時，FPHC 擴充功能可以處理封鎖事件。 FPHC 延伸模組可以處理事件的其中一種方式，就是向使用者顯示使用防火牆解除封鎖程式的提示，然後在使用者確認時解除封鎖程式。 或者，FPHC 擴充功能可以藉由通知使用者應用程式被封鎖的原因來處理事件，例如應用程式因為防火牆被視為惡意程式碼而遭到封鎖。

## <a name="about-wfp-diagnostics"></a>關於 WFP 診斷

當叫用 NDF 以診斷網路問題時，會聯繫協助程式類別，以判斷問題的原因。 如果較高層級的協助程式類別判斷有可能是由 WFP 所造成的網路失敗，則會根據可用資訊產生 FPHC 的假設。 NDF 將此假設（以數個事件屬性的形式）傳遞給 FPHC。 以下是這些屬性的詳細說明，請參閱下面的 [FPHC 事件屬性](#windows-filtering-platform-extensible-helper-class) 一節。

網路問題可以描述為影響特定連接嘗試的連線問題。 例如，使用者可能不小心按一下 [ **不允許**] 來封鎖應用程式。 防火牆接著會封鎖應用程式系結至任何埠。 使用者不知道應用程式被封鎖的原因，可能會嘗試透過應用程式提供的進入點來診斷問題。 FPHC 會查看記錄檔，如果找到相符的記錄檔，就會抓取篩選識別碼和該特定篩選的提供者識別碼。 此時，FPHC 知道該篩選的擁有者是誰，然後將診斷程式交給適當的協助程式類別，以供進一步診斷。

系統會選取最新的 WFP 事件記錄檔中要符合屬性的事件，以與網路問題相關。 如果找不到相符的事件，而且該事件發生的時間已涵蓋于 WFP 記錄中，FPHC 會向 NDF 指出它是否狀況良好。 如果找不到相符的事件，而且 WFP 記錄未包含事件發生的時間，FPHC 會將未定狀態傳回給 NDF。

如果找到相符的事件，FPHC 會使用篩選準則的提供者識別碼，該篩選器會造成事件識別封鎖連線之安全性規則的提供者。 然後，FPHC 會檢查該提供者是否有 helper 類別延伸。 如果找到一個，FPHC 會產生該提供者的假設，然後 NDF 叫用擴充功能。 延伸模組應該會傳回有用的診斷和修復資訊給使用者。

## <a name="helper-class-registration"></a>Helper 類別註冊

必須註冊 FPHC 延伸模組，如 [註冊 NDF 協助程式類別延伸](registering-ndf-helper-class-extensions.md)所述。 執行協助程式類別的開發人員必須註冊其延伸模組，以確保在適當時由 NDF 呼叫此擴充功能。 以下所述的 *相符屬性* 必須儲存在登錄中的 **HKLM \\ System \\ CurrentControlSet \\ Control \\ NetDiagFx** \\ *VendorName* \\ **HostDLLs** \\ *Helper class DLL* \\ **HelperClasses** \\ *helper class Name* \\ **MatchAttributes** 下。

下表顯示用來識別要在 WFP 事件記錄檔中的診斷中使用之假設的相符屬性。 

| 名稱       | 類型    | 描述                                                                                                                                                                                                                                                                                                 |
|------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ProviderID | REG \_ SZ | FPHC 延伸模組的 GUID。 此值必須與 WFP 提供者 GUID 相同。 <br/> 這個字串會區分大小寫。 它應該以大寫字母儲存在登錄中，並以封入括弧和連字號括住。 例如，{C200E360-38C5-11CE-AE62-08002B2B79EF} 是有效的 ProviderID。<br/> |



 

當封鎖篩選的 ProviderID 符合已註冊之 helper 類別的 ProviderID 時，FPHC 會通知 NDF 叫用該 helper 類別，進而擴充 FPHC 的診斷功能。

## <a name="fphc-event-attributes"></a>FPHC 事件屬性

下表列出與每個相符事件相關聯的事件屬性。 每個事件屬性都會儲存在 [**HELPER \_ 屬性**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) 結構中。 當找到相符的事件時，NDF 會將這些屬性傳遞至 FPHC。 這些可以接著傳遞至 FPHC 延伸模組。



| 屬性     | [**屬性 \_類型**](/windows/win32/api/ndattrib/ne-ndattrib-attribute_type) 值 | 描述                                                                                                                               |
|---------------|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 提供者 GUID | 位於 \_ GUID                                        | 與篩選準則相關聯之提供者的 GUID。                                                                                      |
| 時間戳記     | 在 \_ 八位 \_ 字串                               | 指定事件發生時間的 FILETIME 型別緩衝區。 這個時間戳記可以用來唯一識別事件。 |
| ipProtocol    | AT \_ UINT32                                      | 採用 UINT8 格式的傳輸層通訊協定。                                                                                            |
| LocalAddr     | 在 \_ SOCKADDR                                    | 儲存在 [**診斷 \_ SOCKADDR**](/windows/win32/api/ndattrib/ns-ndattrib-diag_sockaddr) 結構中的本機 IP 位址和埠。                                             |
| RemoteAddr    | 在 \_ SOCKADDR                                    | 遠端 IP 位址和埠，儲存在 [**診斷 \_ SOCKADDR**](/windows/win32/api/ndattrib/ns-ndattrib-diag_sockaddr) 結構中。                                            |
| userId        | 在 \_ 八位 \_ 字串                               | 代表 userid 的類型 SID 的緩衝區。 如果 userId 的長度為0，則無法使用 SID。                                        |
| appId         | 在 \_ 字串                                      | 儲存抓取的應用程式識別碼的緩衝區。 如果 appId 的值為 L ""，則無法使用應用程式識別碼。        |



 

## <a name="handling-fphc-events"></a>處理 FPHC 事件

建議將診斷和修復資訊提供給使用者之前，FPHC 延伸模組應收集比 FPHC 通知所提供更多的資料。 您可以從 [WFP 事件管理函數](/windows/desktop/FWP/fwp-mgmt-functions)取得此資料。 這些函式會在 [顯示 Net Events](/windows/desktop/FWP/displaying-net-events) 範例中示範。

SDK 中包含更詳細的事件管理範例。 您可以在 SDK 安裝位置的 C： \\ Program Files \\ Microsoft sdk \\ Windows \\ <version number> \\ 範例 \\ NetDs \\ WFP \\ DiagEvents 中找到範例的原始程式碼。 您可以從[下載中心](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)取得 Windows Vista SDK。

## <a name="built-in-fphc-diagnostics"></a>內建 FPHC 診斷

如果沒有 FPHC 延伸模組，FPHC 可以診斷以下所列的案例。 因為防火牆會封鎖流量，所以 FPHC 診斷的大部分連線失敗。 IPsec 案例較不常見。

下表顯示的某些案例會造成 FPHC 診斷的連線失敗，以及傳遞給 NDF 的描述和修復資訊。



| 狀況                   | 低健康情況描述                                                                                                               | 修復資訊                   |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| 防火牆捨棄              | 這部電腦上的防火牆設定封鎖了連接。                                                                  | 確認您的防火牆設定。       |
| 主要模式失敗          | 因為 IPsec 安全性原則不相符，所以無法連接。                                                                     | 請洽詢 IPsec 原則擁有者。      |
| 快速模式失敗         | 因為 IPsec 安全性原則不相符，所以無法連接。                                                                     | 請洽詢 IPsec 原則擁有者。      |
| 使用者模式失敗          | 因為 IPsec 安全性原則不相符，所以無法連接。                                                                     | 請洽詢 IPsec 原則擁有者。      |
| 認證失敗         | 因為這部電腦上 (CA) 的根憑證授權單位不符合遠端電腦上的根 CA，所以無法連線。 | 更新受信任的根憑證。 |
| 過期的憑證        | 用於 IPsec 驗證的憑證已過期。                                                                           | 要求憑證。               |
| 其他憑證失敗 | 找不到 IPsec 驗證的有效憑證。                                                                          | 要求憑證。               |
| Kerberos 失敗           | 電腦不是此網域的一部分。                                                                                             | 將此電腦加入網域。      |
| 預先共用金鑰              | 重設預先共用的金鑰。                                                                                                            | 重設預先共用的金鑰。            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 篩選平台](/windows/desktop/FWP/windows-filtering-platform-start-page)
</dt> <dt>

[設計 NDF Helper 類別延伸模組](designing-ndf-helper-class-extensions.md)
</dt> <dt>

[註冊 NDF Helper 類別延伸模組](registering-ndf-helper-class-extensions.md)
</dt> <dt>

[NDF Helper 類別範例](ndf-helper-class-examples.md)
</dt> </dl>

 

