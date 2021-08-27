---
title: 使用 DsAddSidHistory
description: 本主題說明如何使用 DsAddSidHistory 函數。
ms.assetid: cbf4983c-551d-4771-870e-a192ed898eb7
ms.tgt_platform: multiple
keywords:
- 使用 DsAddSidHistory Active Directory
- 使用 DsAddSidHistory Active Directory Active Directory
- DsAddSidHistory Active Directory，使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e987a55f7fe39a8e4705f6aca9e44189e0f7a2
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881833"
---
# <a name="using-dsaddsidhistory"></a>使用 DsAddSidHistory

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya)函式會從一個網域 (來源網域) 取得安全性主體 (SID) 的主要帳戶安全識別碼，然後將它新增至不同樹系中另一個 (目的地) 網域中安全性主體的 **sIDHistory** 屬性。 當來源網域處於 Windows 2000 原生模式時，此函式也會抓取來源主體的 **sIDHistory** 值，並將其新增至目的地主體的 **sidhistory**。

將 Sid 新增至安全性主體的 **sIDHistory** 是一項安全性敏感的作業，可有效地授與目的地主體存取來源主體可存取的所有資源，但前提是該信任存在於適用的資源網域到目的地網域中。

在原生模式 Windows 2000 網域中，使用者登入會建立存取權杖，其中包含使用者主要帳戶 SID 和群組 sid，以及使用者為其成員之群組的使用者 **sidhistory** 和 **sIDHistory** 。 將這些先前的 Sid (**sIDHistory** 值) 在使用者的權杖中，會授與使用者存取受存取控制清單保護之資源的存取權 (acl) 包含先前的 sid。

這種作業有助於某些 Windows 2000 的部署案例。 尤其是，它支援在 Windows NT 4.0 生產環境中，為已存在於生產環境中的使用者和群組建立新 Windows 2000 樹系中帳戶的案例。 藉由將 Windows NT 4.0 帳戶 SID 放在 Windows 2000 帳戶 **sIDHistory** 中，就會保留使用者登入新的 Windows 2000 帳戶的網路資源存取權。

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya)也 ()  (4.0 Windows NT 支援以原生模式 Windows 2000 網域) Windows 2000 若要進行這項遷移，必須在目的地 Windows 2000 網域中，在其 **sIDHistory** 的網網域本機群組中包含的本機群組 sid，其為在來源網域中 Windows 2000 伺服器) 上 acl 中所參考之本機群組的主要 sid (或網網域本機群組。 藉由建立包含 **sIDHistory** 的目的地本機群組和來源本機群組的所有成員，將會針對所有成員維護由參考來源本機群組之 acl 所保護的已遷移伺服器資源存取權。

> [!Note]  
> 使用 [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) 需要瞭解在這些案例和其他案例中，其管理和安全性方面的影響。 如需詳細資訊，請參閱《 Windows 2000 支援工具》中 Dommig.doc 提供的「規劃從 Windows NT 到 Microsoft Windows 2000」的技術白皮書。 您也可以在產品 CD 的 [支援工具] 下找到此檔集 \\ \\ 。

 

## <a name="authorization-requirements"></a>授權需求

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) 需要來源和目的地網域中的系統管理員許可權。 具體而言，此 API 的呼叫端必須是目的地網域中網域系統管理員群組的成員。 執行此成員資格的硬式編碼檢查。 此外， *SrcDomainCreds* 參數中提供的呼叫端或帳戶（如果不是 **Null**）必須是來源網域中的系統管理員或網域系統管理員群組的成員。

## <a name="domain-and-trust-requirements"></a>網域和信任需求

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya)要求目的地網域必須處於 Windows 2000 原生模式或更新版本中，因為只有此網欄位型別支援 **sIDHistory** 屬性。 來源網域可以是 Windows NT 4.0 或 Windows 2000、混合或原生模式。 來源和目的地網域不得位於相同的樹系中。 Windows NT 4.0 網域的定義不在樹系中。 此樹系內的條件約束可確保不會在相同的樹系中建立重複的 Sid （不論是否顯示為主要 Sid 或 **sIDHistory** 值）。

在下表所列的情況下， [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya)需要來源網域到目的地網域的外部信任。



| 案例                                                                             | 說明                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 來源網域是 Windows 2000。<br/>                                    | 來源 **sIDHistory** 屬性（僅適用于 Windows 2000 來源網域）可能會使用 LDAP 唯讀，這需要此信任以進行完整性保護。<br/>                                                                                             |
| 來源網域是 Windows NT 4.0，而 *SrcDomainCreds* 為 **Null**。<br/> | 使用呼叫端認證支援來源網域作業所需的模擬，取決於此信任。 模擬也需要目的地網域控制站預設在網域控制站上啟用「受信任的委派」。<br/> |



 

但是，如果來源網域是 Windows NT 4.0 且 *SrcDomainCreds* 不是 **Null**，則來源和目的地網域之間不需要信任。

## <a name="source-domain-controller-requirements"></a>來源網域控制站需求

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya)需要選取作為來源網域中作業目標的網域控制站，是 Windows NT 4.0 網域中的 pdc，或 Windows 2000 網域中的 pdc Emulator。 來源網域審核是透過寫入作業產生的，因此，在 Windows NT 4.0 來源網域中需要 pdc，而且僅限 pdc 的限制可確保在單一電腦上產生 **DsAddSidHistory** 的審核。 這可減少審核所有 Dc 之審核記錄的需求，以監視此作業的使用情形。

> [!Note]  
> 在 Windows NT 4.0 來源網域中，來源網域中的作業 PDC (目標) 必須執行 Service Pack 4 (SP4) 和更新版本，以確保適當的審核支援。

 

您必須在來源網域控制站上，將下列登錄值建立為 REG \_ DWORD 值，並在 Windows NT 4.0 和 Windows 2000 來源 dc 設定為1。

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            Lsa
               TcpipClientSupport
```

設定此值會啟用 TCP 傳輸上的 RPC 呼叫。 這是必要的，因為根據預設，SAMRPC 介面只能在具名管道上進行遠端處理。 使用具名管道會導致認證管理系統適用于進行網路呼叫的互動式登入使用者，但對於使用使用者提供的認證進行網路呼叫的系統程式來說，並不具彈性。 RPC over TCP 更適合該用途。 設定這個值並不會降低系統安全性。 如果已建立或變更此值，則必須重新開機來源網域控制站，這項設定才會生效。

&lt; &gt; 為了進行審核，必須在來源網域中建立新的本機群組 "SrcDomainName $ $ $"。

## <a name="auditing"></a>稽核

系統會審核 [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya)作業，以確保來源和目的地網域系統管理員都能夠偵測此函式的執行時間。 來源和目的地網域都必須進行審核。 **DsAddSidHistory** 會確認每個網域中的 Audit 模式都是 on，且「成功/失敗」事件的帳戶管理審核是開啟的。 在目的地網域中，會針對每個成功或失敗的 **DsAddSidHistory** 作業產生唯一的「新增 Sid 歷程記錄」 audit 事件。

在 Windows NT 4.0 系統上無法使用唯一的「新增 Sid 歷程記錄」審核事件。 若要產生明確反映對來源網域使用 [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) 的 audit 事件，它會針對名稱為 audit 記錄檔中唯一識別碼的特殊群組執行作業。 本機群組 " &lt; SrcDomainName &gt; $ $ $" 的名稱是由附加了三個貨幣符號 ($)  (ASCII 碼 = 0X24 和 Unicode = U + 0024) 的來源網域 NetBIOS 名稱所組成，必須在呼叫 **DsAddSidHistory** 之前于來源網域控制站上建立。 這項作業的目標每個來源使用者和全域群組都會加入至此群組的成員資格，然後從這個群組中移除。 這會產生來源網域中的「新增成員」和「刪除」成員審核事件，藉由搜尋參考組名的事件來監視。

> [!Note]  
> 無法審核 Windows NT 4.0 或 Windows 2000 混合模式來源網域中本機群組的 [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya)作業，因為無法將本機群組設為另一個本機群組的成員，因此無法新增至特殊的 " &lt; SrcDomainName &gt; $ $ $" 本機群組。 這項缺少的審核並不會對來源網域提出安全性問題，因為此作業不會影響來源網域資源的存取。 將來源本機群組的 SID 新增至目的地本機群組，並不會將存取權授與任何其他使用者的來源資源（受該本機群組保護）。 將成員新增至目的地本機群組不會授與他們存取來源資源的許可權。 新增的成員只會被授與從來源網域遷移之目的地網域中的伺服器存取權，這可能會有受來源本機群組 SID 保護的資源。

 

## <a name="data-transmission-security"></a>資料傳輸安全性

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) 會強制執行下列安全性措施：

-   從 Windows 2000 工作站進行呼叫時，會使用呼叫端的認證來驗證和隱私權-保護對目的地網域控制站的 RPC 呼叫。 如果 *SrcDomainCreds* 不是 **Null**，則工作站和目的地 DC 都必須支援128位加密，以保護認證的安全。 如果無法使用128位加密且提供 *SrcDomainCreds* ，則必須在目的地 DC 上進行呼叫。
-   目的地網域控制站會使用 *SrcDomainCreds* 或呼叫端的認證與來源網域控制站進行通訊，以相互驗證和完整性-使用 SAM 查閱) 和 **sIDHistory** (（使用 LDAP 讀取) ）來保護來源帳戶 SID 的讀取 (。

## <a name="threat-models"></a>威脅模型

下表列出與 [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) 呼叫相關聯的潛在威脅，並解決與特定威脅相關的安全性措施。




| 潛在威脅 | 安全性措施 | 
|------------------|------------------|
| 攔截式攻擊<br /> 未經授權的使用者會攔截來源物件傳回呼叫的 <em>查閱 SID</em> ，將來源物件 SID 取代為要插入至目標物件 SIDhistory 的任意 SID。<br /> | <em>來源物件的查閱 SID</em>是經過驗證的 RPC，使用呼叫端的系統管理員認證與封包完整性訊息保護。 這可確保無法在沒有偵測的情況下修改傳回呼叫。 目的地網域控制站會建立唯一的「新增 SID 歷程記錄」 audit 事件，以反映新增至目的地帳戶 <strong>sIDHistory</strong>的 sid。<br /> | 
| 特洛伊來源網域<br /> 未經授權的使用者在私人網路上建立「特洛伊木馬程式」來源網域，此網域具有與合法來源網域相同的網域 SID 和部分相同的帳戶 Sid。 未經授權的使用者接著會嘗試在目的地網域中執行 <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a> ，以取得來源帳戶的 SID。 這樣做不需要真正的來源網域系統管理員認證，也不需要離開實際來源網域中的審核記錄。 未經授權的使用者建立特洛伊程式檔來源網域的方法，可能是下列其中一項：<ul><li>取得來源網域 SAM 的複本 (BDC 備份) 。</li><li>建立新的網域，改變磁片上的網域 SID 以符合合法的來源網域 SID，然後建立足夠的使用者以具現化具有所需 SID 的帳戶。</li><li>建立 BDC 複本。 這需要來源網域系統管理員認證。 然後，未經授權的使用者會將複本帶到私人網路以執行攻擊。</li></ul><br /> | 雖然有許多方法可讓未經授權的使用者取得或建立所需的來源物件 SID，但未經授權的使用者無法使用它來更新帳戶的 <strong>sIDHistory</strong> ，而不是目的地網域系統管理員群組的成員。 因為網域系統管理員成員資格的檢查是以硬式編碼的方式在目標 DC 上進行，所以沒有任何方法可進行磁片修改來變更保護此功能的存取控制資料。 在目的地網域中，會審核嘗試複製特洛伊程式的來源帳戶。 只要針對高度信任的個人保留網域系統管理員群組的成員資格，就可以減輕這種攻擊。<br /> | 
| SID 歷程記錄的磁片修改<br /> 具有網域系統管理員認證的複雜未授權使用者，以及對目的地網域中之 DC 的實體存取權，可以修改磁片上的帳戶 <strong>sIDHistory</strong> 值。<br /> | 使用 <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a>不會啟用這項嘗試。 這項攻擊的解決方式是防止實體存取所有高度信任的系統管理員以外的網域控制站。<br /> | 
| 用來移除保護的惡意程式碼<br /> 未經授權的使用者或 rogue 系統管理員若具有目錄服務程式碼的實體存取權，就可以建立以下的惡意程式碼：<ol><li>移除程式碼中 Domain Administrators 群組的成員資格檢查。</li><li>變更來源網域控制站上的呼叫，將 SID 指向未進行審核的 LookupSidFromName。</li><li>移除 audit log 呼叫。</li></ol><br /> | 具有 DS 程式碼實體存取權的人員，以及足以建立 rogue 程式碼的知識，都具有任意修改帳戶 <strong>sIDHistory</strong> 屬性的能力。 <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a> API 不會增加此安全性風險。<br /> | 
| 易受遭竊 Sid 的資源<br /> 如果未經授權的使用者使用這裡所述的其中一種方法來修改帳戶 <strong>sIDHistory</strong>，且感興趣的資源網域信任未經授權的使用者帳戶網域，則未經授權的使用者可能會未經授權存取遭竊的 sid 資源，而不會在 SID 遭竊的帳戶網域中留下審核記錄。<br /> | 資源網域系統管理員只會設定從安全性觀點來合理的信任關係，以保護其資源。 在受信任的目標網域中，使用 <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a> 受限於網域系統管理員群組的成員，這些成員在其職責範圍內已經有廣泛的許可權。<br /> | 
| Rogue 目標網域<br /> 未經授權的使用者會使用其<strong>sIDHistory</strong>包含已從來源網域遭竊之 SID 的帳戶，建立 Windows 2000 網域。 未經授權的使用者會使用此帳戶來取得資源的未經授權存取權。<br /> | 未經授權的使用者需要來源網域的系統管理員認證，才能使用 <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a>，並在來源網域控制站上保留審核記錄。 Rogue 目標網域只會在信任 rogue 網域的其他網域中取得未經授權的存取權，這需要這些資源網域中的系統管理員許可權。<br /> | 




 

## <a name="operational-constraints"></a>操作條件約束

本節描述使用 [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) 函式的操作條件約束。

*SrcPrincipal* 的 SID 不得存在於目的地樹系中，可做為主要帳戶 SID 或帳戶的 **sIDHistory** 。 例外狀況是在嘗試將 SID 新增至包含相同 SID 的 **sIDHistory** 時， [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya)不會產生錯誤。 此行為可讓 **DsAddSidHistory** 以相同的輸入執行多次，進而產生成功和一致的結束狀態，以供工具開發人員方便使用。

> [!Note]  
> 通用類別目錄複寫延遲可能會提供一個視窗，在這段期間可能會建立重複的 Sid。 不過，系統管理員可以輕鬆地刪除重複的 Sid。

 

*SrcPrincipal* 和 *DstPrincipal* 必須是下列其中一種類型：

-   User
-   啟用安全性的群組，包括：

    <dl> 本機群組  
    通用群組  
    網域本機群組 (Windows 2000 原生模式)   
    萬用群組 (Windows 2000 原生模式)   
    </dl>

*SrcPrincipal* 和 *DstPrincipal* 的物件類型必須相符。

-   如果 *SrcPrincipal* 是使用者， *DstPrincipal* 必須是使用者。
-   如果 *SrcPrincipal* 是本機或網域本機群組， *DstPrincipal* 必須是網域本機群組。
-   如果 *SrcPrincipal* 是全域群組或萬用群組， *DstPrincipal* 必須是全域群組或萬用群組。

*SrcPrincipal* 和 *DstPrincipal* 不可以是下列其中一種類型： ([**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) 失敗，並在這些情況下發生錯誤) 

-   電腦 (工作站或網域控制站) 
-   網域間信任
-   暫時重複的帳戶 (幾乎未使用的功能，這是 LANman 的舊版) 
-   具有知名 Sid 的帳戶。 已知的 Sid 在每個網域中都相同;因此，將它們新增至 **sIDHistory** 會違反 Windows 2000 樹系的 SID 唯一性需求。 已知 Sid 的帳戶包含下列本機群組：

    <dl> Account Operators  
    系統管理員  
    Backup Operators  
    Guests  
    列印運算子  
    Replicator  
    Server Operators  
    使用者  
    </dl>

如果 *SrcPrincipal* 有已知的相對識別碼 (RID) 和網域專屬的前置詞，也就是網域系統管理員、網域使用者及網域電腦，則 *DstPrincipal* 必須擁有相同的已知 RID，才能讓 [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) 成功。 具有已知 Rid 的帳戶包含下列使用者和全域群組：

-   系統管理員
-   來賓
-   Domain Administrators
-   網域來賓
-   網域使用者

## <a name="setting-the-registry-value"></a>設定登錄值

下列程式說明如何設定 TcpipClientSupport 登錄值。

**若要設定 TcpipClientSupport 登錄值**

1.  建立下列登錄值作為 \_ 來源網域控制站上的 REG DWORD 值，並將其值設定為1。

    **HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Control \\ Lsa \\ TcpipClientSupport**

2.  然後，重新開機來源網域控制站。 此登錄值會導致 SAM 在 TCP/IP 上接聽。 如果未在來源網域控制站上設定此值， [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya)將會失敗。

## <a name="enabling-auditing-of-usergroup-management-events"></a>啟用使用者/群組管理事件的審核

下列程式說明如何在 Windows 2000 或 Windows Server 2003 來源或目的地網域中啟用使用者/群組管理事件的審核。

**啟用 Windows 2000 或 Windows Server 2003 來源或目的地網域中的使用者/群組管理事件的審核**

1.  在 Active Directory 消費者和電腦 MMC 嵌入式管理單元中，選取 [目的地網域網域控制站] 容器。
2.  以滑鼠右鍵按一下 [ **網域控制站** ]，然後選擇 [ **屬性**]。
3.  按一下 [ **群組原則** ] 索引標籤。
4.  選取 [ **預設網域控制站原則** ]，然後按一下 [ **編輯**]。
5.  在 [電腦設定] **\\ Windows 設定 \\ 安全性設定 \\ 本機原則 \\ 稽核原則**] 下，按兩下 [**審核帳戶管理**]。
6.  在 [ **審核帳戶管理** ] 視窗中，選取 [ **成功** ] 和 [ **失敗** ] 審核。 原則更新會在重新開機之後或重新整理之後生效。
7.  藉由在群組原則 MMC 嵌入式管理單元中查看有效稽核原則來確認是否已啟用審核。

下列程式說明如何在 Windows NT 4.0 網域中啟用使用者/群組管理事件的審核。

**啟用 Windows NT 4.0 網域中的使用者/群組管理事件的審核**

1.  在 [ **網域的使用者管理員**] 中，按一下 [ **原則** ] 功能表，然後選取 [ **Audit**]。
2.  選取 [ **Audit 這些事件**]。
3.  針對 **使用者和群組管理**，請檢查 **成功和失敗**。

下列程式說明如何在 Windows NT 4.0、Windows 2000 或 Windows Server 2003 來源網域中啟用使用者/群組管理事件的審核。

**啟用 Windows NT 4.0、Windows 2000 或 Windows Server 2003 來源網域中的使用者/群組管理事件的審核**

1.  在 [ **網域的使用者管理員**] 中，按一下 [ **使用者** ] 功能表，然後選取 [ **新的本機群組**]。
2.  輸入由來源網域 NetBIOS 名稱所組成的組名，該名稱會附加三個貨幣符號 ($) ，例如 FABRIKAM $ $ $。 [描述] 欄位應該會指出此群組是用來審核 [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) 或複製作業的使用。 確定群組中沒有成員。 按一下 [確定]。

如果未如這裡所述啟用來源和目的地的審核， [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) 作業就會失敗。

## <a name="set-up-trust-if-required"></a>視需要設定信任

如果下列其中一項為 true，就必須從來源網域將信任建立到目的地網域 (這必須發生在不同的樹系) 中：

-   來源網域是 Windows Server 2003。
-   來源網域是 Windows NT 4.0，而 *SrcDomainCreds* 為 **Null**。

 

 





