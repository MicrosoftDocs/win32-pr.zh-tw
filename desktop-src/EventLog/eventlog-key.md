---
description: 事件記錄檔包含下列標準記錄和自訂記錄：
ms.assetid: 87d860e3-2495-4e15-bb42-341e92935e55
title: Eventlog 索引鍵
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eed1e64d3084d6b952693957c65766b257cb552a861c9989ea0550111e9b224
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119383768"
---
# <a name="eventlog-key"></a>Eventlog 索引鍵

事件記錄檔包含下列標準記錄和自訂記錄：



| 記錄檔             | 描述                                                                                                                                                                                                                                  |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **應用程式** | 包含應用程式所記錄的事件。 例如，資料庫應用程式可能會記錄檔案錯誤。 應用程式開發人員會決定要記錄哪些事件。                                                                             |
| **安全性**    | 包含事件，例如有效和不正確登入嘗試，以及與資源使用相關的事件，例如建立、開啟或刪除檔案或其他物件。 系統管理員可以開始進行審核，以將事件記錄在安全性記錄檔中。 |
| **系統**      | 包含系統元件所記錄的事件，例如，驅動程式失敗或其他系統元件在啟動時載入。                                                                                                               |
| *>customlog*     | 包含建立自訂記錄檔的應用程式所記錄的事件。 使用自訂記錄檔可讓應用程式控制記錄檔的大小或附加 Acl，以利安全起見，而不會影響其他應用程式。                         |



 

事件記錄服務會使用儲存在 **Eventlog** 登錄機碼中的資訊。 **Eventlog** 索引鍵包含數個子機碼，稱為「*記錄*」。 每個記錄檔都包含事件記錄服務在應用程式寫入事件記錄檔和讀取時，用來尋找資源的資訊。

**Eventlog** 索引鍵的結構如下所示：

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            Eventlog
               Application
               Security
               System
               CustomLog
```

請注意，網域控制站會在 **目錄服務** 和檔案複寫 **服務** 記錄檔中記錄事件，並且在 **dns 伺服器** 中記錄事件。

每個記錄檔都可以包含下列登錄值。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>登錄值</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CustomSD</strong></td>
<td>限制對事件記錄檔的存取。 此值的類型為 REG_SZ。 使用的格式為 <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">安全描述項定義語言</a> (SDDL) 。 建立授與下列一或多個許可權的 ACL：<dl> 清除 (0x0004) <br />
閱讀 (0x0001) <br />
撰寫 (0x0002) <br />
</dl> 若要成為語法有效的 SDDL，CustomSD 值必須指定擁有者和群組擁有者 (例如 O:BAG： SY) ，但不會使用擁有者和群組擁有者。 如果 CustomSD 設定為錯誤的值，當事件記錄檔服務啟動時，系統事件記錄檔中就會引發事件，而事件記錄檔會取得與應用程式記錄檔原始 CustomSD 值相同的預設安全描述項。 不支援 Sacl。<br/> 如需詳細資訊，請參閱 <a href="event-logging-security.md">事件記錄安全性</a>。<br/> <strong>Windows Server 2003：</strong>支援 Sacl。<br/> <strong>Windows XP/2000：</strong>不支援這個值。<br/> <br/></td>
</tr>
<tr class="even">
<td><strong>DisplayNameFile</strong></td>
<td>不使用這個值。 <strong>Windows Server 2003 和 Windows XP/2000：</strong>儲存事件記錄檔之當地語系化名稱的檔案名。 儲存在此檔案中的名稱會顯示為事件檢視器中的記錄檔名稱。 如果事件記錄檔的登錄中未出現此專案，事件檢視器會將登錄子機碼的名稱顯示為記錄檔名稱。 此值的類型為 REG_EXPAND_SZ。 預設值為% SystemRoot% \system32\els.dll。<br/></td>
</tr>
<tr class="odd">
<td><strong>DisplayNameID</strong></td>
<td>不使用這個值。 <strong>Windows Server 2003 和 Windows XP/2000：</strong>記錄檔名稱字串的訊息識別碼。 此數位表示顯示當地語系化顯示名稱的訊息。 訊息會儲存在 <strong>DisplayNameFile</strong> 值所指定的檔案中。 此值的類型為 REG_DWORD。<br/></td>
</tr>
<tr class="even">
<td><strong>檔案</strong></td>
<td>儲存每個事件記錄檔之檔案的完整路徑。 這可讓事件檢視器和其他應用程式尋找記錄檔。 此值的類型為 REG_SZ 或 REG_EXPAND_SZ。 這是選擇性的值。 如果未指定值，則預設為%SystemRoot%\system32\winevt\logs\，後面接著以事件記錄檔登錄機碼名稱為基礎的檔案名。特定事件記錄檔路徑應該使用命令列公用程式來設定 wevtutil.exe 或使用 <a href="/windows/desktop/api/winevt/nf-winevt-evtsetchannelconfigproperty"><strong>EvtSetChannelConfigProperty</strong></a> 函式搭配傳遞至 <em>PropertyId</em> 參數的 EvtChannelLoggingConfigLogFilePath。<br/> 如果已設定特定檔案，請確定事件記錄檔服務具有該檔案的完整許可權。<br/> 此值必須是位於本機目錄的檔案的有效檔案名， (不是遠端電腦，而不是 DOS 裝置、非磁片磁碟機，而不是管道) 。 如果檔案設定錯誤，當事件記錄檔服務啟動時，系統事件記錄檔中就會引發事件。<br/> 請勿在檔案路徑中使用環境變數，該檔案在事件記錄檔服務的內容中無法展開。<br/> <strong>Windows Server 2003 和 Windows XP/2000：</strong>此值預設為%SystemRoot%\system32\config\，後面接著以事件記錄檔登錄機碼名稱為基礎的檔案名。 如果檔案設定設為不正確值，記錄檔將不會正確地初始化，或所有要求都會以無訊息模式移至預設記錄 (應用程式) 。<br/></td>
</tr>
<tr class="odd">
<td><strong>MaxSize</strong></td>
<td>記錄檔的大小上限（以位元組為單位）。 此值的類型為 REG_DWORD。 系統、應用程式或安全性記錄檔的值必須設定為64K 的倍數。 預設值為1MB。<strong>Windows Server 2003 和 Windows XP/2000：</strong>此值限制為0xFFFFFFFF，預設值為512K。<br/></td>
</tr>
<tr class="even">
<td><strong>PrimaryModule</strong></td>
<td>未使用此值。<strong>Windows Server 2003 和 Windows XP/2000：</strong>此值是子機碼的名稱，其中包含事件來源之子機碼中專案的預設值。 此值的類型為 REG_SZ。<br/></td>
</tr>
<tr class="odd">
<td><strong>保留</strong></td>
<td>此值的類型為 REG_DWORD。 預設值為 0。 如果這個值為0，則一律會覆寫事件的記錄。 如果這個值是0xFFFFFFFF 或任何非零值，則永遠不會覆寫記錄。 當記錄檔達到大小上限時，您必須手動清除記錄檔;否則會捨棄新的事件。 您也必須先清除記錄檔，才能變更其大小。<strong>Windows Server 2003 和 Windows XP/2000：</strong>此值是受保護的事件記錄不受覆寫的時間間隔（以秒為單位）。 當事件的存留期達到或超過此值時，就可以覆寫它。<br/></td>
</tr>
<tr class="even">
<td><strong>來源</strong></td>
<td>不使用這個值。 <strong>Windows Server 2003 和 Windows XP/2000：</strong>將事件寫入此記錄檔的應用程式、服務或應用程式群組的名稱。 此值應僅供讀取，且不會改變。 事件記錄服務會根據記錄檔下子機碼中列出的每個程式來維護清單。 此值的類型為 REG_MULTI_SZ。<br/></td>
</tr>
<tr class="odd">
<td><strong>AutoBackupLogFiles</strong></td>
<td>此值的類型為 REG_DWORD，且事件記錄檔服務會使用此值來判斷是否應該自動儲存事件記錄檔。 預設值為0，這會停用自動備份。 只有當保留值為-1 (0xFFFFFFFF) 時，服務才會備份記錄檔。 其他值將會被忽略。<strong>Windows Server 2003：</strong>保留可以設定為-1 (0xFFFFFFFF) 或 1 (0x00000001) 讓 AutoBackupLogFiles 運作。 其他值將會被忽略。<br/></td>
</tr>
<tr class="even">
<td><strong>RestrictGuestAccess</strong></td>
<td>不使用這個值。 <strong>Windows XP/2000：</strong>此值的類型為 REG_DWORD，預設值為1。 當值設定為1時，會限制來賓和匿名帳戶對事件記錄檔的存取，當這個值為0時，它會允許 Guest 帳戶存取事件記錄檔。<br/></td>
</tr>
<tr class="odd">
<td><strong>隔離</strong></td>
<td>定義記錄檔的預設存取權限。 此值的類型為 REG_SZ。 您可以指定下列其中一個值：
<ul>
<li><strong>應用程式</strong></li>
<li><strong>系統</strong></li>
<li><strong>Custom</strong></li>
</ul>
預設隔離為 [ <strong>應用程式</strong>]。 <strong>應用程式</strong>的預設許可權 (使用 SDDL) 來顯示： <br/>
<pre class="syntax" data-space="preserve"><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system               (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins            (read, write, clear)
            L&quot;(A;;0x7;;;SO)&quot;                    // server operators           (read, write, clear)
            L&quot;(A;;0x3;;;IU)&quot;                    // INTERACTIVE LOGON          (read, write)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON             (read, write)
            L&quot;(A;;0x3;;;S-1-5-3)&quot;               // BATCH LOGON                (read, write)
            L&quot;(A;;0x3;;;S-1-5-33)&quot;              // write restricted service   (read, write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers          (read) </code></pre>
<strong>系統</strong>的預設許可權 (使用 SDDL) 來顯示： <br/>
<pre class="syntax" data-space="preserve"><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system             (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins          (read, write, clear)
            L&quot;(A;;0x3;;;BO)&quot;                    // backup operators         (read, write)
            L&quot;(A;;0x5;;;SO)&quot;                    // server operators         (read, clear) 
            L&quot;(A;;0x1;;;IU)&quot;                    // INTERACTIVE LOGON        (read)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON           (read, write)
            L&quot;(A;;0x1;;;S-1-5-3)&quot;               // BATCH LOGON              (read)
            L&quot;(A;;0x2;;;S-1-5-33)&quot;              // write restricted service (write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers        (read)</code></pre>
<strong>自訂</strong>隔離的預設許可權與應用程式相同。<br/> <strong>Windows Server 2003 和 Windows XP/2000：</strong>此值無法使用。<br/></td>
</tr>
</tbody>
</table>



 

每個記錄檔也都包含事件來源。 如需詳細資訊，請參閱 [事件來源](event-sources.md)。

