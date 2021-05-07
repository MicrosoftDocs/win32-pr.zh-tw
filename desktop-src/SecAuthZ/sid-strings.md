---
description: 說明 SDDLs 所使用的字串。
ms.assetid: a531532f-afba-46a1-8576-90d4ff881b94
title: SID 字串
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a949a4aec81b24f431b656a9b3a3d4be5666874
ms.sourcegitcommit: 07ba02719c9779e082b108ae74f9699fb0236c34
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/06/2021
ms.locfileid: "108644210"
---
# <a name="sid-strings"></a>SID 字串

在 [安全描述項定義語言](security-descriptor-definition-language.md) (SDDL) 中， [安全描述項字串](security-descriptor-string-format.md) 會針對 [*安全描述項*](/windows/desktop/SecGloss/s-gly)的下列元件使用 SID 字串：

-   擁有者
-   主要群組
-   ACE 中的[信任者](trustees.md)

安全描述項字串中的 sid 字串可以使用 sid 的標準字串表示 (s-*R* - *I* - *s* -  ) 或在 Sddl 中定義的其中一個字串常數。 如需標準 SID 字串標記法的詳細資訊，請參閱 [SID 元件](sid-components.md)。

下列適用于已知 Sid 的 SID 字串常數是在 Sddl 中定義。 如需對應的 [*相對識別碼*](/windows/desktop/SecGloss/r-gly) (rid) 的相關資訊，請參閱 [知名的 sid](well-known-sids.md)。



| SDDL SID 字串 | Sddl 中的常數                               | 帳號別名和對應的 RID                                                                                                                                                                                                                        |
|-----------------|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AA      | SDDL \_ 訪問 \_ 控制 \_ 協助 \_ OPS     | 存取控制協助操作員。 對應的 RID 是網域 \_ 別名 \_ RID \_ 訪問 \_ 控制 \_ 協助 \_ OPS。 **Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista 和 Windows Server 2003：** 無法使用。                |
| AC      | SDDL \_ 所有 \_ 應用程式 \_ 套件                   | 應用程式封裝內容中執行的所有應用程式。 對應的 RID 是安全性內 \_ 建 \_ 封裝 \_ 任何 \_ 套件。 **Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista 和 Windows Server 2003：** 無法使用。             |
| 以<br/> | SDDL \_ 匿名<br/>                       | 匿名登入。 對應的 RID 是安全性 \_ 匿名 \_ 登入 \_ RID。<br/>                                                                                                                                                                      |
| AO<br/> | SDDL \_ 帳戶 \_ 操作員<br/>              | 帳戶操作員。 對應的 RID 是網域 \_ 別名 \_ RID \_ 帳戶 \_ OPS。<br/>                                                                                                                                                                   |
| AP      | SDDL \_ 受保護的 \_ 使用者                     | [受保護的使用者](/windows-server/security/credentials-protection-and-management/protected-users-security-group)。 對應的 RID 是網域 \_ 群組 \_ RID \_ 受保護的 \_ 使用者。 **Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista 和 Windows server 2003：** 無法使用。 |
| 澳大利亞<br/> | SDDL \_ 驗證的 \_ 使用者<br/>            | 已驗證的使用者。 對應的 RID 是安全 \_ 驗證的 \_ 使用者 \_ RID。<br/>                                                                                                                                                               |
| BA<br/> | SDDL 內 \_ 建系統 \_ 管理員<br/>         | 內建系統管理員。 對應的 RID 是網域 \_ 別名 \_ RID \_ ADMINS。<br/>                                                                                                                                                                   |
| BG<br/> | SDDL 內 \_ 建 \_ 來賓<br/>                 | 內建來賓。 對應的 RID 是網域 \_ 別名 \_ RID \_ 來賓。<br/>                                                                                                                                                                           |
| BO<br/> | SDDL \_ 備份 \_ 操作員<br/>               | 備份操作員。 對應的 RID 是網域 \_ 別名 \_ RID \_ 備份 \_ OPS。<br/>                                                                                                                                                                     |
| 備份<br/> | SDDL 內 \_ 建 \_ 使用者<br/>                  | 內建使用者。 對應的 RID 是網域 \_ 別名 \_ RID \_ 使用者。<br/>                                                                                                                                                                             |
| CA<br/> | SDDL \_ CERT \_ SERV 系統 \_ 管理員<br/>      | 憑證發行者。 對應的 RID 是網域 \_ 群組 \_ RID \_ CERT \_ ADMINS。<br/>                                                                                                                                                              |
| LCD<br/> | SDDL \_ CERTSVC \_ DCOM \_ 存取<br/>           | 可使用分散式元件物件模型連接到憑證授權單位單位 (DCOM) 的使用者。 對應的 RID 是網域 \_ 別名 \_ RID \_ CERTSVC \_ DCOM \_ 存取 \_ 群組。 **Windows server 2008、Windows Vista 和 Windows server 2003：** 無法使用。 |
| CG<br/> | SDDL 建立 \_ 者 \_ 群組<br/>                  | Creator 群組。 對應的 RID 是安全 \_ CREATOR \_ 群組 \_ rid。<br/>                                                                                                                                                                          |
| CN      | SDDL \_ CLONEABLE \_ 控制器               | Cloneable 網域控制站。 對應的 RID 是網域 \_ 群組 \_ RID \_ CLONEABLE \_ 控制器。 **Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista 和 Windows Server 2003：** 無法使用。                                 |
| 座標<br/> | SDDL 建立 \_ 者 \_ 擁有者<br/>                  | Creator 擁有者。 對應的 RID 是安全 \_ CREATOR \_ 擁有者 \_ rid。<br/>                                                                                                                                                                          |
| CY      | SDDL \_ 加密 \_ 運算子                    | 加密運算子。 對應的 RID 是網域 \_ 別名 \_ RID \_ 加密 \_ 操作員。  無法使用 *Windows Server 2003：**。                                                                                                                            |
| DA<br/> | SDDL \_ 網域系統 \_ 管理員<br/>          | 網域系統管理員。 對應的 RID 是網域 \_ 群組 \_ RID \_ 管理員。<br/>                                                                                                                                                                     |
| 電源<br/> | SDDL \_ 網域 \_ 電腦<br/>               | 網域電腦。 對應的 RID 是網域 \_ 群組 \_ RID \_ 電腦。<br/>                                                                                                                                                                       |
| 網上<br/> | SDDL \_ 網域 \_ 域 \_ 控制器<br/>     | 網域控制站。 對應的 RID 是網域 \_ 群組 \_ RID \_ 控制器。<br/>                                                                                                                                                                   |
| DG<br/> | SDDL \_ 網域 \_ 來賓<br/>                  | 網域來賓。 對應的 RID 是網域 \_ 群組 \_ RID \_ 來賓。<br/>                                                                                                                                                                             |
| DU<br/> | SDDL \_ 網域 \_ 使用者<br/>                   | 網域使用者。 對應的 RID 是網域 \_ 群組 \_ RID \_ 使用者。<br/>                                                                                                                                                                               |
| EA<br/> | SDDL \_ 企業系統 \_ 管理員<br/>              | 企業系統管理員。 對應的 RID 是網域 \_ 群組 \_ RID \_ ENTERPRISE \_ ADMINS。<br/>                                                                                                                                                     |
| 教育<br/> | SDDL \_ 企業 \_ 域 \_ 控制器<br/> | 企業網域控制站。 對應的 RID 是 SECURITY \_ SERVER \_ LOGON \_ rid。<br/>                                                                                                                                                           |
| EK      | SDDL \_ ENTERPRISE \_ KEY \_ ADMINS              | 企業金鑰系統管理員。 對應的 RID 是網域 \_ 群組 \_ RID \_ ENTERPRISE \_ KEY \_ ADMINS。 **Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、Windows 7、Windows server 2008、Windows Vista 和 Windows server 2003：** 無法使用。 |
| 緊急      | SDDL \_ 事件 \_ 記錄 \_ 讀取器                  | 事件記錄檔讀取器。 對應的 RID 是 DOMAIN \_ ALIAS \_ rid \_ EVENT \_ LOG \_ READERS \_ 群組。 **Windows server 2008、Windows Vista 和 Windows server 2003：** 無法使用。                                                                           |
| 終止      | SDDL \_ RDS \_ 端點 \_ 伺服器               | 端點伺服器。 對應的 RID 是網域 \_ 別名 \_ RID \_ RDS \_ 端點 \_ 伺服器。 **Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista 和 Windows Server 2003：** 無法使用。                                             |
| 可用性      | SDDL \_ HYPER-V \_ 系統 \_ 管理員                     | Hyper-v 系統管理員。 對應的 RID 是網域 \_ 別名 \_ RID \_ hyper-v \_ 系統 \_ 管理員。 **Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista 和 Windows Server 2003：** 無法使用。                                             |
| 你好<br/> | SDDL \_ ML \_ HIGH<br/>                        | 高完整性層級。 對應的 RID 是安全性 \_ 強制性 \_ 高 \_ RID。 **Windows Server 2003：** 無法使用。                                                                                                                               |
| 後      | SDDL \_ IIS \_ 使用者                           | 匿名的網際網路使用者。 對應的 RID 是網域 \_ 別名 \_ RID \_ IUSERS。 **Windows Server 2003：** 無法使用。                                                                                                                               |
| IU<br/> | SDDL \_ 互動式<br/>                     | 以互動方式登入的使用者。 這是在進程以互動方式登入時，新增至進程權杖的群組識別碼。 對應的登入類型為 LOGON32 \_ logon \_ INTERACTIVE。 對應的 RID 是安全性 \_ 互動式 \_ RID。<br/> |
| KA      | SDDL \_ 金鑰 \_ 管理員                          | 網域金鑰系統管理員。 對應的 RID 是網域 \_ 群組 \_ RID \_ 金鑰 \_ 管理員。 **Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、Windows 7、Windows server 2008、Windows Vista 和 Windows server 2003：** 無法使用。 |
| LA<br/> | SDDL \_ 本機系統 \_ 管理員<br/>                    | 本機系統管理員。 對應的 RID 是 DOMAIN \_ USER \_ RID \_ ADMIN。<br/>                                                                                                                                                                         |
| LG<br/> | SDDL \_ 本機 \_ 來賓<br/>                    | 本機來賓。 對應的 RID 是 DOMAIN \_ USER \_ RID \_ GUEST。<br/>                                                                                                                                                                                 |
| 3<br/> | SDDL \_ 本地 \_ 服務<br/>                  | 本地服務帳戶。 對應的 RID 是安全 \_ 本地 \_ 服務 \_ rid。<br/>                                                                                                                                                                  |
| 封      | SDDL \_ PERFLOG \_ 使用者                       | 效能記錄使用者。 對應的 RID 是網域 \_ 別名 \_ RID \_ 記錄 \_ 使用者。                                                                                                                                                                  |
| "LW"<br/> | SDDL \_ ML \_ 低<br/>                         | 低完整性層級。 對應的 RID 是安全的 \_ 強制 \_ 低 \_ rid。 **Windows Server 2003：** 無法使用。                                                                                                                                 |
| 諮詢<br/> | SDDL \_ ML \_ MEDIUM<br/>                      | 中度完整性層級。 對應的 RID 是安全的 \_ 強制 \_ 媒體 \_ rid。 **Windows Server 2003：** 無法使用。                                                                                                                           |
| 多功能      | SDDL \_ ML \_ MEDIUM \_ PLUS                     | 中加上整合層級。 對應的 RID 是安全性 \_ 強制 \_ 媒體 \_ PLUS \_ rid。 **Windows server 2008、Windows Vista 和 Windows server 2003：** 無法使用。                                                                         |
| "MU"<br/> | SDDL \_ PERFMON \_ 使用者<br/>                  | 效能監視器的使用者。 對應的 RID 是網域 \_ 別名 \_ RID \_ 監視 \_ 使用者。<br/>                                                                                                                                                      |
| 存在<br/> | SDDL \_ 網路 \_ 設定 \_ OPS<br/>     | 網路設定操作員。 對應的 RID 是 DOMAIN \_ ALIAS \_ rid \_ NETWORK \_ CONFIGURATION \_ OPS。<br/>                                                                                                                                      |
| 紅外線<br/> | SDDL \_ 網路 \_ 服務<br/>                | Network service 帳戶。 對應的 RID 是安全性 \_ 網路 \_ 服務 \_ RID。<br/>                                                                                                                                                              |
| NU<br/> | SDDL \_ 網路<br/>                         | 網路登入使用者。 這是在整個網路上登入進程的權杖時新增的群組識別碼。 對應的登入類型為 LOGON32 \_ logon \_ NETWORK。 對應的 RID 是安全 \_ 網路 \_ RID。<br/>                |
| 允許      | SDDL \_ 擁有者 \_ 許可權                        | 擁有者許可權 SID。 對應的 RID 是安全 \_ CREATOR \_ 擁有者 \_ 許可權 \_ RID。 無法使用 *Windows Server 2003：**。                                                                                                                             |
| 賓夕法尼亞<br/> | SDDL \_ 組 \_ 策略 \_ 管理員<br/>           | 群組原則系統管理員。 對應的 RID 是網域 \_ 群組 \_ RID \_ 原則系統 \_ 管理員。<br/>                                                                                                                                                       |
| 信箱<br/> | SDDL \_ 印表機 \_ 操作員<br/>              | 印表機操作員。 對應的 RID 是網域 \_ 別名 \_ RID \_ PRINT \_ OPS。<br/>                                                                                                                                                                     |
| 電源<br/> | SDDL \_ 個人 \_ 自助<br/>                  | Principal 本身。 對應的 RID 是安全性 \_ 主體的 \_ 自我 \_ rid。<br/>                                                                                                                                                                        |
| PU<br/> | SDDL \_ POWER \_ 使用者<br/>                    | Power 使用者。 對應的 RID 是網域 \_ 別名 \_ RID \_ POWER \_ USERS。<br/>                                                                                                                                                                         |
| RA      | SDDL \_ RDS \_ 遠端 \_ 訪問 \_ 伺服器         | RDS 遠端存取服務器。 對應的 RID 是網域 \_ 別名 \_ RID \_ RDS \_ 遠端 \_ 訪問 \_ 伺服器。 **Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista 和 Windows Server 2003：** 無法使用。                              |
| RC<br/> | SDDL \_ 限制的程式 \_ 代碼<br/>                | 限制的程式碼。 這是使用 [**CreateRestrictedToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) 函式建立的受限制權杖。 對應的 RID 是安全 \_ 限制的程式 \_ 代碼 \_ RID。<br/>                                                        |
| 資金<br/> | SDDL \_ 遠端 \_ 桌面<br/>                 | 終端機伺服器使用者。 對應的 RID 是 DOMAIN \_ ALIAS \_ rid \_ REMOTE \_ DESKTOP \_ USERS。<br/>                                                                                                                                                     |
| 再次<br/> | SDDL \_ 複寫器<br/>                      | 複製。 對應的 RID 是網域 \_ 別名 \_ RID \_ 複製器。<br/>                                                                                                                                                                            |
| WS-RM      | SDDL \_ RMS_ \_ 服務 \_ 操作員             | RMS 服務。 **僅適用于 Windows Vista**。                                                                                                                                                                                                    |
| RO<br/> | SDDL \_ ENTERPRISE \_ RO \_ dc<br/>             | 企業唯讀網域控制站。 對應的 RID 是網域 \_ 群組 \_ RID \_ ENTERPRISE \_ READONLY \_ 域 \_ 控制器。 **Windows server 2008、Windows Vista 和 Windows server 2003：** 無法使用。                                      |
| 車載<br/> | SDDL \_ RAS \_ 伺服器<br/>                    | RAS 伺服器群組。 對應的 RID 是網域 \_ 別名 \_ RID \_ RAS \_ 伺服器。<br/>                                                                                                                                                                   |
| 陰<br/> | SDDL \_ 別名 \_ PREW2KCOMPACC<br/>            | 授與許可權給使用與 Windows 2000 之前的作業系統相容之應用程式的帳戶的別名。 對應的 RID 是網域 \_ 別名 \_ RID \_ PREW2KCOMPACCESS。<br/>                                                         |
| SA<br/> | SDDL \_ 架構系統 \_ 管理員<br/>          | 架構系統管理員。 對應的 RID 是 DOMAIN \_ GROUP \_ RID \_ SCHEMA \_ ADMINS。<br/>                                                                                                                                                             |
| SI<br/> | SDDL \_ ML \_ 系統<br/>                      | 系統完整性層級。 對應的 RID 是安全的 \_ 強制 \_ 系統 \_ RID。 **Windows Server 2003：** 無法使用。                                                                                                                           |
| 有<br/> | SDDL \_ 伺服器 \_ 運算子<br/>               | 伺服器運算子。 對應的 RID 是網域 \_ 別名 \_ RID \_ 系統 \_ OPS。<br/>                                                                                                                                                                     |
| 匯總      | SDDL \_ 服務判斷提示 \_                    | 驗證服務已判斷提示。 對應的 RID 是安全性 \_ 驗證服務的判斷提示 \_ \_ \_ rid。 **Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista 和 Windows Server 2003：** 無法使用。                        |
| SU<br/> | SDDL \_ 服務<br/>                         | 服務登入使用者。 這是在處理常式記錄為服務時，新增至進程權杖的群組識別碼。 對應的登入類型為 LOGON32 \_ logon \_ SERVICE。 對應的 RID 是安全性 \_ 服務 \_ rid。<br/>                       |
| SY<br/> | SDDL \_ 本機 \_ 系統<br/>                   | 本機系統。 對應的 RID 是安全 \_ 本機 \_ 系統 \_ RID。<br/>                                                                                                                                                                            |
| UD      | SDDL \_ 使用者 \_ 模式 \_ 驅動程式                  | 使用者模式驅動程式。 對應的 RID 是安全性 \_ USERMODEDRIVERHOST \_ 識別碼 \_ 基底 \_ RID。 **Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista 和 Windows Server 2003：** 無法使用。                                            |
| WD<br/> | SDDL \_ 所有人<br/>                        | Everyone。 對應的 RID 是安全 \_ 世界 \_ rid。<br/>                                                                                                                                                                                        |
| "WR"      | SDDL \_ 寫入 \_ 限制的程式 \_ 代碼              | 寫入受限制的程式碼。 對應的 RID 是安全 \_ 寫入 \_ 限制的程式 \_ 代碼 \_ RID。 無法使用 *Windows Server 2003：**。                                                                                                                       |


 

[**ConvertSidToStringSid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida)和 [**ConvertStringSidToSid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida)函式一律會使用標準 SID 字串標記法，且不支援 SDDL SID 字串常數。

如需知名 Sid 的詳細資訊，請參閱 [已知的 sid](well-known-sids.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[\[DTYP \] ：安全描述項描述語言](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>

