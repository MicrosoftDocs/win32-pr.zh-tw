---
title: ADSI 中的事件追蹤
description: Windows Server 2008 和 Windows Vista 引進 Active Directory 服務介面 (ADSI) 的事件追蹤。
ms.assetid: 743aeeba-5b48-47c7-aaf5-0e9b48e206db
ms.tgt_platform: multiple
keywords:
- 事件追蹤 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b26aee00404f5cf97d228698f64fec804c28e62
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423708"
---
# <a name="event-tracing-in-adsi"></a>ADSI 中的事件追蹤

Windows Server 2008 和 Windows Vista 引進[Active Directory 服務介面](active-directory-service-interfaces-adsi.md) (ADSI) 的[事件追蹤](/windows/desktop/ETW/event-tracing-portal)。 ADSI LDAP 提供者的某些區域具有複雜的基礎執行，或牽涉到的一連串步驟，讓您難以診斷問題。 為了協助應用程式開發人員進行疑難排解，事件追蹤已新增至下欄區域：

## <a name="schema-parsing-and-downloading"></a>架構剖析和下載

ADSI 中的 IADs 介面需要在用戶端上快取 LDAP 架構，如此一來，就可以正確地封送處理屬性 (，如 [ADSI 架構模型](adsi-schema-model.md)) 中所述。 為了達成此目的，ADSI 會將每個處理常式的架構載入 (，並將每個 LDAP 伺服器/網域) 至記憶體中，從儲存在本機磁片上的架構 ( .sch) 檔案，或從 LDAP 伺服器下載。 相同用戶端電腦上的不同進程會使用磁片上的快取架構（如果有的話）。

如果無法從磁片或伺服器取得架構，ADSI 會使用硬式編碼的預設架構。 發生這種情況時，無法封送處理不屬於這個預設架構的屬性，而且 ADSI 在抓取這些屬性時會傳回錯誤。 有許多因素可能會導致這種情況發生，包括剖析架構時發生問題，以及沒有足夠的許可權可下載架構。 通常很難判斷為何會使用特定的預設架構。 在此區域使用事件追蹤將有助於更快速地診斷問題並加以修正。

## <a name="changing-and-setting-the-password"></a>變更和設定密碼

[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) 和 [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) 採用多個機制，根據可用的設定 (來執行要求的作業，如 [設定和變更使用者密碼與 LDAP 提供者](setting-user-passwords-for-ldap-providers.md)) 中所述。 當 **ChangePassword** 和 **SetPassword** 失敗時，很難判斷確切的原因，而事件追蹤將有助於疑難排解這些方法的問題。

## <a name="adsi-bind-cache"></a>ADSI 系結快取

ADSI 會在內部嘗試重複使用 LDAP 連線， (查看 [連接](connection-caching.md) 快取) 。 進行疑難排解時，追蹤是否已開啟新連接來與伺服器通訊，或是否使用現有的連接，是很有用的。 這也有助於追蹤連線快取的生命週期 (有時也稱為系結快取) 和它的建立或關閉，以及是否發生連接的參考。 在 [無伺服器](/windows/desktop/AD/serverless-binding-and-rootdse)系結的情況下，ADSI 會呼叫 DC 定位器來選取使用者內容網域的伺服器。 然後，ADSI 會維持網域伺服器對應的快取，以便進行後續連接。 事件追蹤有助於追蹤選取的 DC，因此有助於疑難排解連接相關的問題。

## <a name="enabling-tracing-and-starting-a-tracing-session"></a>啟用追蹤和啟動追蹤會話

若要開啟 ADSI 追蹤，請建立下列登錄機碼：

**HKEY \_LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **追蹤** \\ **_ProcessName_**

*ProcessName* 是您要追蹤之進程的完整名稱，包括其延伸 (例如「Svchost.exe」 ) 。 此外，您可以在此機碼中放入名為的 **DWORD** 類型的選擇性值。 強烈建議您設定此值，因此只會追蹤特定的進程。 否則，將會追蹤 *ProcessName* 所指定之應用程式的所有實例。

然後執行下列命令：

**tracelog.exe-開始***會話* 名稱 **- \# guid**_提供者 \_ guid_ **-f** *檔案名* **-旗** 標 *追蹤旗標***層級** *traceLevel*

*sessionname* 只是用來標示追蹤會話的任意識別碼 (您稍後在停止追蹤會話) 時，必須參考此會話名稱。 ADSI 追蹤提供者的 GUID 是「7288c9f8-d63c-4932-a345-89d6b060174d」。 *filename* 會指定要寫入事件的記錄檔。 *追蹤旗標* 必須是下列其中一個值：



|         旗標                        |         值              |
|---------------------------------|-----------------------|
| **DEBUG \_ 架構**<br/>    | 0x00000001<br/> |
| **DEBUG \_ CHANGEPWD**<br/> | 0x00000002<br/> |
| **DEBUG \_ SETPWD**<br/>    | 0x00000004<br/> |
| **DEBUG \_ BINDCACHE**<br/> | 0x00000008<br/> |



 

這些旗標會根據下表來決定要追蹤的 [ADSI](active-directory-service-interfaces-adsi.md) 方法：



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>DEBUG_SCHEMA</strong><br/></td>
<td><ul>
<li>LdapGetSchema</li>
<li>GetSchemaInfoTime</li>
<li>LdapReadSchemaInfoFromServer</li>
<li>ProcessSchemaInfo</li>
<li>HelperReadLdapSchemaInfo</li>
<li>ProcessClassInfoArray</li>
<li>ReadSchemaInfoFromRegistry</li>
<li>StoreSchemaInfoFromRegistry</li>
<li>AttributeTypeDescription</li>
<li>ObjectClassDescription</li>
<li>DITContentRuleDescription</li>
<li>DirectoryString</li>
<li>DirectoryStrings</li>
<li>DITContentRuleDescription</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><strong>DEBUG_CHANGEPWD</strong><br/></td>
<td><ul>
<li>CADsUser：： ChangePassword</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><strong>DEBUG_SETPWD</strong><br/></td>
<td><ul>
<li>CADsUser：： SetPassword</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><strong>DEBUG_BINDCACHE</strong><br/></td>
<td><ul>
<li>GetServerBasedObject</li>
<li>GetServerLessBasedObject</li>
<li>GetGCDomainName</li>
<li>GetDefaultDomainName</li>
<li>GetUserDomainFlatName</li>
<li>BindCacheLookup</li>
<li>EquivalentPortNumbers</li>
<li>CanCredentialsBeReused</li>
<li>BindCacheAdd</li>
<li>BindCacheAddRef</li>
<li>AddReferralLink</li>
<li>CommonRemoveEntry</li>
<li>BindCacheDerefHelper</li>
<li>NotifyNewConnection</li>
<li>QueryForConnection</li>
<li>LdapOpenBindWithCredentials</li>
<li>LdapOpenBindWithDefaultCredentials</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

您可以藉由在 *追蹤旗標* 引數中結合適當的位來合併旗標。 例如，若要指定 **debug \_ SCHEMA** 和 **debug \_ BINDCACHE** 旗標，則會0x00000009 適當的 *追蹤旗標* 值。

最後， *traceLevel* 旗標應為下列其中一個值：



|      旗標                                    |       值                |
|------------------------------------------|-----------------------|
| **追蹤 \_ 層級 \_ 錯誤**<br/>       | 0x00000002<br/> |
| **追蹤 \_ 層級 \_ 資訊**<br/> | 0x00000004<br/> |



 

**追蹤 \_層級 \_ 資訊** 會導致追蹤處理常式記錄所有事件，而 **追蹤 \_ 層級的 \_ 錯誤** 會導致追蹤進程只記錄錯誤事件。

若要終止追蹤，請執行下列命令：

**tracelog.exe-停止** *sessionname*

在上述範例中， *sessionname* 與啟動追蹤區段的命令所提供的名稱相同。

## <a name="remarks"></a>備註

藉由指定特定的 PID，而不是追蹤電腦上的所有處理常式，更有效地追蹤特定的進程。 如果您需要追蹤相同電腦上的多個應用程式，可能會對效能造成影響。程式碼的效能導向區段中有大量的偵錯工具輸出。 此外，在追蹤多個進程時，系統管理員必須小心地設定記錄檔的許可權;否則，任何使用者都可以讀取追蹤記錄，而其他使用者可以追蹤包含安全資訊的處理常式。

例如，假設系統管理員設定應用程式 "Test.exe" 的追蹤，而且未在登錄中指定 PID 來追蹤處理常式的多個實例。 現在另一位使用者想要追蹤應用程式「Secure.exe」。 如果追蹤記錄檔未受到適當限制，則該使用者必須做的就是將 "Secure.exe" 重新命名為 "Test.exe"，並且將會進行追蹤。 一般而言，最好只在進行疑難排解時追蹤特定的進程，並在進行疑難排解時立即移除追蹤登錄機碼。

由於啟用事件追蹤將會產生額外的記錄檔，因此系統管理員應謹慎地監視記錄檔大小;本機電腦上的磁碟空間不足可能會造成拒絕服務。

## <a name="example-scenarios"></a>範例案例

案例1：系統管理員在應用程式中看到未預期的錯誤，此應用程式會設定使用者帳戶的密碼，因此它們會採取下列步驟來使用事件追蹤來修正問題。

1.  撰寫可重現問題的腳本，並建立登錄機碼

    **HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **服務** \\ **adsi** \\ **追蹤** \\ **cscript.exe**

2.  使用下列命令，啟動追蹤會話、將 *追蹤旗標* 設定為 0X2 (**DEBUG \_ CHANGEPASSWD**) 和 *traceLevel* to 0x4 (**追蹤 \_ 層級 \_ 資訊**) ：

    **tracelog.exe-start scripttrace-guid \# 7288c9f8-d63c-4932-a345-89d6b060174d-f。 \\adsi-旗標 0x2-層級0x4**

3.  使用測試腳本執行 cscript.exe，以重現問題，然後終止追蹤會話：

    **tracelog.exe-停止 scripttrace**

4.  刪除登錄機碼

    **HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **服務** \\ **adsi** \\ **追蹤** \\ **cscript.exe**

5.  執行 ETW 工具 Tracerpt.exe，以剖析記錄檔中的追蹤資訊：

    **tracelog.exe-start scripttrace-guid \# 7288c9f8-d63c-4932-a345-89d6b060174d-f。 \\adsi-旗標 0x2-層級0x4**

案例2：系統管理員想要在名為 w3wp.exe 且已在執行中的 [ASP](https://msdn.microsoft.com/asp.net/default.aspx) 應用程式中，追蹤架構剖析和下載作業。 若要這樣做，系統管理員會採取下列步驟：

1.  建立登錄機碼

    **HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **服務** \\ **adsi** \\ **追蹤** \\ **w3wp.exe**

    在該索引鍵中，建立名為 PID 的類型值，並將它設定為目前在本機電腦上執行之 w3wp.exe 實例的處理序識別碼。

2.  然後，他們會建立追蹤會話、將 *追蹤旗標* 設定為 0X1 (**DEBUG \_ SCHEMA**) 和 *traceLevel* to 0x4 (**追蹤 \_ 層級 \_ 資訊**) ：

    **tracelog.exe-start w3wptrace-guid \# 7288c9f8-d63c-4932-a345-89d6b060174d-f。 \\w3wp.exe .etl-旗標 0x1-層級0x4**

3.  重現需要疑難排解的操作。
4.  終止追蹤會話：

    **tracelog.exe-停止 w3wptrace**

5.  刪除登錄機碼 **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **追蹤** \\ **w3wp.exe**。
6.  執行 ETW 工具 tracerpt.exe，以剖析記錄檔中的追蹤資訊：

    **tracerpt.exe。 \\w3wp.exe .etl-o-報告**

 

