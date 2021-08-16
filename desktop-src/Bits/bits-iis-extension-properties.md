---
title: BITS IIS 擴充功能屬性
description: 背景智慧型傳送服務 (位) 使用 ISAPI 擴充 IIS 以支援上傳作業。
ms.assetid: 08a40cc1-ec6d-4b65-971a-15c7b06df148
keywords:
- BITS IIS 擴充功能屬性位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37c81d57114a23a07c5f952a9cb33399644f5cbed8bbf67cccf802a1c996b72b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835167"
---
# <a name="bits-iis-extension-properties"></a>BITS IIS 擴充功能屬性

背景智慧型傳送服務 (位) 使用 ISAPI 擴充 IIS 以支援 [**上傳作業**](/windows/win32/api/bits/ne-bits-bg_job_type)。 下表列出 BITS 新增至虛擬目錄元件之 IIS 元資料庫的屬性。 BITS 會使用這些屬性來判斷如何上傳檔案。 BITS IIS 延伸模組屬性是可繼承的，但 **BITSUploadEnabled** 除外。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>屬性</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>BITSUploadEnabled</strong>資料類型： <strong>布林值</strong><br/></td>
<td>指出是否已在虛擬目錄上啟用 BITS 上傳。 如果設定不存在或為0，則會停用 BITS 上傳。<br/> 這是一個唯讀屬性。 若要設定這個屬性，請呼叫<a href="/windows/win32/api/bitscfg/nn-bitscfg-ibitsextensionsetup"><strong>IBITSExtensionSetup</strong></a>介面的<a href="/windows/win32/api/bitscfg/nf-bitscfg-ibitsextensionsetup-enablebitsuploads"><strong>EnableBITSUploads</strong></a>或<a href="/windows/win32/api/bitscfg/nf-bitscfg-ibitsextensionsetup-disablebitsuploads"><strong>DisableBITSUploads</strong></a>方法。<br/></td>
</tr>
<tr class="even">
<td><strong>BITSSessionTimeout</strong>資料類型： <strong>DWORD</strong><br/></td>
<td>如果上傳檔案未進行任何進度，則維持連接的秒數;進行進度時，會重設計時器。 如果達到超時，則 BITS 會關閉連接，並清除與會話相關聯的資料。<br/> 設定簡短的會話超時可能是上傳-回復作業的問題，因為只有當使用者登入並聯機到網路時，才會下載回復。 在下載回復之前，會話可能會出現一段時間，在這種情況下，會話就會取消，而且會刪除回復檔。<br/> 請注意，如果 <a href="/windows/win32/bits/group-policies">JobInactivityTimeout</a> 群組原則值 (預設值為 90) 天，則 BITS 會取消工作，不論此設定為何。<br/> 預設值為 1209600 (14 天) 。<br/></td>
</tr>
<tr class="odd">
<td><strong>BITSMaximumUploadSize</strong>資料類型： <strong>字串</strong><br/></td>
<td>每個作業可上傳的位元組數目上限。 將最大位元組數目指定為十進位字串;字串值必須小於或等於 &quot; 1844674407370955 &quot; 。 空字串與指定 &quot; 1844674407370955 相同 &quot; 。<br/> 預設值為空字串。<br/>
<blockquote>
[!Note]<br />
在 IIS 7 中，預設上傳限制為30000000個位元組。 <strong>BITSMaximumUploadSize</strong>屬性的值不能超過 IIS 限制。 如需變更 IIS 預設值的詳細資訊和詳細資訊，請參閱 <a href="https://support.microsoft.com//kb/942074">KB942074</a>。
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><strong>BITSServerNotificationType</strong>資料類型： <strong>DWORD</strong><br/></td>
<td>指定如何將上傳檔案傳送至伺服器應用程式。 可能的值為：0、1和2。<br/> 值為0表示不會將檔案傳送至伺服器應用程式。 BITS 會將上傳檔案放在遠端名稱所指定的目錄中， (當您將檔案 <a href="/windows/win32/api/bits/nf-bits-ibackgroundcopyjob-addfile">新增</a> 至作業) 時所指定的遠端名稱，而不會通知伺服器應用程式。 如果檔案目前存在於目的地目錄中，則會取代為上傳檔案。<br/> 1值表示 BITS 會將上傳檔案的位置傳遞至 <strong>BITSServerNotificationURL</strong> 屬性中指定的伺服器應用程式。 伺服器應用程式會處理檔案，並視需要產生回復檔。 根據預設，BITS 會在接收到伺服器應用程式的回應之後，從伺服器移除上傳和回復檔案。 若要讓 BITS 將上傳檔案複製到工作中的遠端檔案名所指定的位置，請在您的回應中包含 <a href="/windows/win32/bits/notification-protocol-for-server-applications">位複製檔案到目的地</a> 的標頭。 如果您未包含標頭，而且想要儲存上傳和回復檔案，則必須先將上傳和回復檔案複製到新的位置，然後再回應。<br/> 值為2表示 BITS 會將要求主體中的上傳檔案傳遞至 <strong>BITSServerNotificationURL</strong> 屬性中指定的伺服器應用程式。 伺服器應用程式會處理檔案，並在回應本文中傳回回複（如有需要）。<br/> 如需要求和回應標頭的詳細資訊，請參閱 <a href="/windows/win32/bits/notification-protocol-for-server-applications">伺服器應用程式的通知通訊協定</a>。<br/> 伺服器應用程式必須在五分鐘內提供回應。 如果伺服器應用程式未在五分鐘內回復，則作業會進入暫時性錯誤狀態。 當 <a href="/windows/win32/api/bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay"><strong>重試延遲</strong></a> 到期時，BITS 伺服器會傳送另一個通知給伺服器應用程式 (應該撰寫伺服器應用程式，以處理重複的通知) 。<strong>BITS 1.5：</strong> 通知超時時間為30秒。<br/> <br/> 預設值為 0。<br/></td>
</tr>
<tr class="odd">
<td><strong>BITSServerNotificationURL</strong>資料類型： <strong>字串</strong><br/></td>
<td>選擇性。 包含 BITS 張貼上傳檔案的伺服器應用程式的 URL。 如果 <strong>BITSServerNotificationType</strong> 屬性的值是1或2，則您必須指定 URL。 URL 的限制為2200個字元，不包括 null 結束字元。 URL 必須是 HTTP URL;BITS 不支援 HTTPS 通知 Url。<br/> 如果在上傳時無法使用 URL，BITS 會重試上傳，直到通知 URL 存在或重試期限到期為止。<br/> 請注意，如果作業中指定的遠端名稱包含查詢字串，則查詢字串會附加至您指定的 URL。 例如，如果遠端名稱包含， https://myserver/myvdir/subdir/file.asp?ACCOUNT=86433 而且您將 <strong>BITSServerNotificationURL</strong> 設定指定為 https://otherserver/myvdir2/bag.asp ，則 BITS 張貼的 URL 就是 https://otherserver/myvdir2/bag.asp?ACCOUNT=86433 。<br/> 如果原始 URL 為， https://myserver/myvdir/file.txt 且通知 url 為 myasp，則 BITS 會使用 HTTP//myserver/myvdir/myasp 作為通知 url。<br/> 如果 URL 的路徑和檔案名部分包含在用戶端和伺服器上的字碼頁不通用的 Unicode 字元，則伺服器上的 URL 轉譯將會失敗，而且 BITS 工作將會處於錯誤狀態。 如果 URL 的伺服器部分包含 Unicode 字元，您必須使用 <a href="/windows/win32/intl/handling-internationalized-domain-names--idns">國際化功能變數名稱</a> (IDN) 來將伺服器部分編碼。<br/></td>
</tr>
<tr class="even">
<td><strong>BITSHostId</strong>資料類型： <strong>字串</strong><br/></td>
<td>如果伺服器安裝是不使用共用存放裝置的 web 伺服陣列，請設定此屬性。<br/> 在上傳程式中斷之後，指定要重新連接之伺服器的伺服器名稱或 IP 位址。 一般來說，您會指定要設定的伺服器名稱。 URL 的限制為300個字元，不包括 null 結束字元。<br/> 如果您未指定此屬性，且上傳程式中斷，BITS 可能會在伺服器陣列中的另一部伺服器上繼續工作。 不過，先前的伺服器仍包含中斷前的部分上傳檔案。 在 <strong>BITSSessionTimeout</strong> 到期後，BITS 會移除部分檔案。<br/>
<blockquote>
[!Note]<br />
如果使用網路負載平衡 (NLB) 或具有多個 IP 位址的 DNS 名稱的 web 伺服陣列中使用 SSL，則請勿使用 <strong>BITSHostId</strong> 屬性，除非您在憑證中包含叢集名稱和個別的伺服器名稱。  (如果 <strong>BITSHostId</strong> 中指定的伺服器名稱與憑證上的一般名稱不相符，作業將會失敗 ) 。請改為針對 NLB 將親和 <a href="/previous-versions/tn-archive/bb687542(v=technet.10)">性</a> 參數設定為 <strong>單一</strong> ，以確保用戶端在未來會與相同的伺服器進行通訊。
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>BITSHostIdFallbackTimeout</strong>資料類型： <strong>DWORD</strong><br/></td>
<td>BITS 用戶端在還原為作業遠端檔案名中指定的主機名稱之前，嘗試重新連線到 <strong>BITSHostId</strong> 伺服器名稱的秒數。 當 BITS 無法連線到 <strong>BITSHostId</strong> 伺服器時，就會開始計時器。 當用戶端成功連接到伺服器時，就會重設計時器。<br/> 請注意，作業 (的 [無進度超時] 值，請參閱 <a href="/windows/win32/api/bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout"><strong>IBackgroundCopyJob：： SetNoProgressTimeout</strong></a>) 應超過這個超時值。 如果不是，則工作會失敗，然後回復超時值過期。<br/> 只有當您設定 <strong>BITSHostId</strong> 屬性時，才設定這個屬性。<br/> 預設值為 86400 (1 天) 。<br/></td>
</tr>
<tr class="even">
<td><strong>BITSAllowOverwrites</strong>資料類型： <strong>整數</strong><br/></td>
<td>指出上傳檔案是否可以覆寫具有相同名稱的現有檔案。 如果 <strong>BITSAllowOverwrites</strong> 是1，則上傳檔案會覆寫現有的檔案。<br/> 預設值為 0。<br/> <strong>IIS 6.0：</strong> 您只能從腳本設定此屬性，您無法在 IIS 使用者介面中使用 [BITS 延伸模組屬性] 頁面來設定這個屬性。<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>BITSCleanupUseDefault</strong>資料類型： <strong>布林值</strong><br/></td>
<td>指出清除工作是否使用預設排程。 預設會每隔12小時執行一次清除工作。<br/> 設定為1則使用預設排程;否則為0以指定排程。<br/> 若要指定排程，請使用 <strong>BITSCleanupCount</strong> 和 <strong>BITSCleanupUnits</strong> 屬性。<br/> 清除工作會藉由刪除未在會話超時期間內修改的作業來清除虛擬目錄 (查看 <strong>BITSSessionTimeout</strong>) 。<br/> 預設值為1，使用預設排程。<br/> <strong>IIS 6.0：</strong> 不支援。<br/></td>
</tr>
<tr class="even">
<td><strong>BITSCleanupCount</strong>資料類型： <strong>整數</strong><br/></td>
<td>指定執行清除工作之間要等候的間隔。 您可以指定的間隔取決於單位。 如需可能的間隔值，請參閱 <strong>BITSCleanupUnits</strong> 屬性。<br/> 如果 <strong>BITSCleanupUseDefault</strong> 為0，則會忽略這個屬性。<br/> <strong>IIS 6.0：</strong> 不支援。<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>BITSCleanupUnits</strong>資料類型： <strong>整數</strong><br/></td>
<td>指定 <strong>BITSCleanupCount</strong> 屬性中所指定之清除間隔的單位。 如果 <strong>BITSCleanupUseDefault</strong> 為0，則會忽略這個屬性。<br/> 可能的值包括：<dl> 0：單位為分鐘。 可能的值為1到60。<br />
1：單位為小時。 此為預設值。 可能的值為1到24。<br />
2：單位是天。 可能的值為1到360。<br />
</dl> <br/> <strong>IIS 6.0：</strong> 不支援。<br/> <br/></td>
</tr>
<tr class="even">
<td><strong>BITSNumberOfSessionsLimit</strong>資料類型： <strong>整數</strong><br/></td>
<td>限制使用者可以同時存在的上傳會話數目。 如果使用者的會話數目超過此限制，當清除工作執行時，將會刪除最近的會話，直到使用者的會話數目低於限制為止。<br/> 預設值是50會話。<br/> <strong>IIS 6.0：</strong> 不支援。<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>BITSSessionLimitEnable</strong>資料類型： <strong>布林值</strong><br/></td>
<td>指出 BITS 是否會限制每個使用者的上傳會話數目。 如果設定不存在或為0，則會停用此限制。<br/> 若要指定限制，請設定 <strong>BITSNumberOfSessionsLimit</strong> 屬性。<br/> 預設值是 1。<br/> <strong>IIS 6.0：</strong> 不支援。<br/> <br/></td>
</tr>
</tbody>
</table>



 

下列範例示範如何使用 Windows 腳本主機來設定 BITS IIS 延伸模組屬性。 如果虛擬目錄指向遠端共用，也請設定 **UNCUserName** 和 **UNCPassword** IIS 屬性。


```JScript
if (WScript.Arguments.length < 2)
{
    WScript.Echo("Usage: bitsvdir virtual_directory local_directory");
    WScript.Quit(1);
}

VirtualDirectoryName = WScript.Arguments(0);
LocalDirectoryName = WScript.Arguments(1);

ServerObj = GetObject("IIS://LocalHost/W3SVC/1/ROOT");
VirtualDir = ServerObj.Create("IIsWebVirtualDir", VirtualDirectoryName );

VirtualDir.Path = LocalDirectoryName;
VirtualDir.AppIsolated = 0;
VirtualDir.AccessScript = true;
VirtualDir.AccessRead = false;
VirtualDir.AccessWrite = false;
VirtualDir.SetInfo();

// Set BITS specific IIS configuration settings
VirtualDir.EnableBITSUploads();
VirtualDir.BITSMaximumUploadSize = "4294967296";
VirtualDir.SetInfo();

WScript.Echo( "Created virtual directory " + VirtualDirectoryName + 
              " with a local directory of " + LocalDirectoryName );
WScript.Quit( 0 );
```



 

