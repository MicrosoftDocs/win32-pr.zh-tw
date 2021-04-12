---
title: 新功能 (BITS)
description: 下表指出背景智慧型傳送服務 (位) 的每個版本的新功能。
ms.assetid: ef05f2e1-88be-4adb-aca7-a7b1451cfd04
keywords:
- 新功能位
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: b171a1d8cede9e3fd49ac81ab47ffb09f72b6200
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024409"
---
# <a name="whats-new-bits"></a>新功能 (BITS)

因為它的第一個版本是 Windows XP 的一部分，所以背景智慧型傳送服務 (位) 持續改進，為開發人員和系統管理員新增更強大的控制項，以控制及管理下載。 已新增一組豐富的 PowerShell Cmdlet;它可以連接到更多類型的 HTTP 伺服器;比以往更小心的是使用者的網路頻寬和成本。 

下表指出背景智慧型傳送服務 (位) 的每個版本的新功能。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>版本</th>
<th>功能描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>版本10。3</td>
<td>新功能︰<br/>
<ul>
<li>已新增 <a href="/windows/win32/api/bits10_3/nn-bits10_3-ibackgroundcopyjobhttpoptions3"><strong>BackgroundCopyJobHttpOptions3</strong></a> ，以將 HTTP 標頭標示為僅限寫入，以及設定伺服器憑證驗證回呼。</li>
<li>BITS 會在其他系統服務建立時保留其服務識別。</li>
<li>只要裝置已插入，BITS 將繼續在連線的待命上傳輸檔案。</li>
</ul>
BITS 10.3 版包含在 Windows 10 2019 年5月更新 (10.0;組建 18362) 和更新版本。
</td>
</tr>
<tr class="even">
<td>版本10。2</td>
<td>新功能︰<br/>
<ul>
<li>已新增 <a href="/windows/win32/api/bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2"><strong>BackgroundCopyJobHttpOptions2</strong></a> 來變更 HTTP 下載的 HTTP 方法。</li>
<li>BITS 現在會使用預設 proxy 順序，與系統的其餘部分一致。</li>
<li>程式設計人員可以更輕鬆地為企業案例設定 BITS proxy 設定。</li>
<li>BITS 現在比較小心，並支援 [新式待命](/windows-hardware/design/device-experiences/modern-standby)。</li>
<li>除了[群組原則](./group-policies)之外，BITS 現在還支援行動裝置管理員 (MDM) [原則](/windows/client-management/mdm/policy-configuration-service-provider)。</li>
</ul>
BITS 10.2 版包含在 Windows 10 2018 年10月更新 (10.0;組建 17763) 和更新版本。
</td>
</tr>
<tr class="odd">
<td>版本10。1</td>
<td>新功能︰<br/>
<ul>
<li>已新增 <a href="/windows/win32/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6"><strong>BackgroundCopyFile6</strong></a> 和 <a href="/windows/win32/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3"><strong>IBackgroundCopyCallback3</strong></a> ，以啟用 HTTP 下載的隨機存取案例。</li>
<li>新增 <strong>BITS_JOB_PROPERTY_ON_DEMAND_MODE</strong> 並 <strong>BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS</strong> 至 <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id"><strong>BITS_JOB_PROPERTY_ID</strong></a> 列舉，以分別調整下載和通知行為。</li>
</ul>
BITS 10.1 版包含在 Windows 10 Creator 的 Update 和更新版本中。
</td>
</tr>
<tr class="even">
<td>版本 5.0</td>
<td>新功能︰<br/>
<ul>
<li>加入 <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5"><strong>IBackgroundCopyJob5</strong></a> 介面，這個介面會將用來取得和設定 BITS 工作屬性的泛型方法，新增至繼承自 <a href="/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4"><strong>IBackgroundCopyJob4</strong></a> 介面的方法。<br/> 如需使用新 <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5"><strong>IBackgroundCopyJob5</strong></a> 介面的相關資訊，請參閱如何控制是否允許在 bits 下載作業中，透過 <a href="how-to-block-a-bits-job-from-downloading-over-an-expensive-connection.md">昂貴的連接來下載 bits 作業</a> ，以及 <a href="how-to-get-the-last-set-of-http-headers-received-for-each-file-in-a-bits-download-job.md">如何取得每個檔案所收到的最後一組 HTTP 標頭</a>。<br/></li>
<li>加入 <a href="/windows/win32/api/bits5_0/ns-bits5_0-bits_job_property_value"><strong>BITS_JOB_PROPERTY_VALUE</strong></a> 聯集和 <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id"><strong>BITS_JOB_PROPERTY_ID</strong></a>，以及 <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_transfer_policy"><strong>BITS_JOB_TRANSFER_POLICY</strong></a> 列舉。 如需使用範例，請參閱上述的 how to 主題。</li>
<li>加入 <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5"><strong>IBackgroundCopyFile5</strong></a> 介面，這會新增方法，以在 BackgroundCopyFile 物件上取得和設定泛型屬性至繼承自 <a href="/windows/win32/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4"><strong>IBackgroundCopyFile4</strong></a> 介面的方法。 新增泛型屬性可讓您在未來增強 BackgroundCopyFile 功能，而不需要建立新的介面。</li>
<li><a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5"><strong>IBackgroundCopyFile5</strong></a>所公開的第一個泛型屬性是<strong>HttpResponseHeaders</strong>屬性。</li>
<li>加入 <a href="/windows/win32/api/bits5_0/ns-bits5_0-bits_file_property_value"><strong>BITS_FILE_PROPERTY_VALUE</strong></a> 聯集和 <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_file_property_id"><strong>BITS_FILE_PROPERTY_ID</strong></a> 列舉。</li>
</ul>
BITS 5.0 版包含在 Windows Server 2012 和 Windows 8 作業系統中，其中% windir% \System32\QMgr.dll 的版本是 7.7. xxxx &quot; &quot; 。<br/> 下列功能已新增至 Windows 10 中的位<br/>
<ul>
<li>在 Windows 10 1607 版中，您可以使用 BITS COM Api 和 BITS PowerShell Cmdlet， (可在 PowerShell 遠端會話中使用) 。 這在管理沒有本機登入功能的 Windows Server 2016 版本時特別有用。 BITS 工作是透過在工作階段使用者帳戶內容中執行的 PowerShell 遠端工作階段啟動，並只會在至少有一個和該使用者帳戶關聯的作用中本機登入工作階段或 PowerShell 遠端工作階段時，才會呈現進度。 請考慮使用持續性的 PowerShell 遠端會話 (參閱 <a href="/powershell/module/microsoft.powershell.core/new-pssession">新的 PSSession</a>) 以進行長時間執行的傳送。</li>
<li>在 Windows 10 1607 版中，只要協助程式權杖沒有系統管理員功能，BITS 作業擁有者就可以在不是系統管理員的情況下設定 helper 權杖。 這將能透過讓背景下載或更新工具在具有較低權限的 NetworkService 帳戶 (而非具有系統管理員權限的帳戶) 下執行，來降低背景下載或更新工具的弱點數量。</li>
</ul>
BITS 5.0 版也包含在 Windows 10 中，其中% windir% \System32\QMgr.dll 的版本是 7.8. xxxx。 &quot; &quot;<br/></td>
</tr>
<tr class="odd">
<td>4.0 版</td>
<td>新功能︰<br/>
<ul>
<li>對等快取現在使用 Windows BranchCache。 這個新的對等快取模型會取代用於 BITS 3.0 版的模型。 如需詳細資訊，請參閱 <a href="peer-caching.md">對等</a>快取。</li>
<li>新增更有彈性的資源存取模型，讓應用程式能夠將一組安全性權杖與 BITS 傳送工作產生關聯。 如需詳細資訊，請參閱 <a href="helper-tokens-for-bits-transfer-jobs.md">BITS 傳送工作的協助程式權杖</a>。</li>
<li>新增 <a href="bits-compact-server.md">BITS Compact 伺服器</a>，這是一種獨立的 HTTP/HTTPS 檔案伺服器，可讓您在電腦之間以非同步方式傳輸有限數量的大型檔案。</li>
<li>新增更細微的頻寬節流。 如需詳細資訊，請參閱 <a href="group-policies.md">群組原則</a>。</li>
</ul>
BITS 4.0 版包含在 Windows Server 2008 R2 和 Windows 7 作業系統中。<br/> 您也可以下載適用于 Windows Server 2008 Service Pack 2 (SP2) 、Windows Vista （含 Service Pack 1） (SP1) ，以及 Windows Vista （含 Service Pack 2 (SP2) ）的 BITS 4.0。 如需下載 BITS 4.0 的詳細資訊，請參閱 <a href="https://support.microsoft.com/kb/968929">KB968929</a>。<br/> % Windir% \System32\QMgr.dll 的版本為 &quot; 7.5. xxxx &quot; 。<br/></td>
</tr>
<tr class="even">
<td>3.0 版</td>
<td>新功能︰<br/>
<ul>
<li>新增 <a href="peer-caching.md">對等</a> 快取，可讓您從對等下載內容，也可以提供內容給網域網路中的對等。</li>
<li>已新增下載檔案時的 <a href="/windows/win32/api/Bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred">通知</a> 。</li>
<li>在下載進行期間新增對 <a href="/windows/win32/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname">暫存檔案</a> 的存取權。</li>
<li>已新增控制 HTTP 重新 <a href="/windows/win32/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags">導向</a>的能力。</li>
<li>新增更多 <a href="group-policies.md">群組原則</a> 來控制對等快取和限制下載時間。</li>
<li>將診斷和疑難排解事件新增至系統事件記錄檔。</li>
<li>已新增 (UAC) 的「 <a href="user-account-control-and-bits.md">使用者帳戶控制</a> 」支援。</li>
<li>在 Windows Vista 和更新版本上，預設的位啟動類型為延遲自動啟動。</li>
</ul>
<blockquote>
[!Note]<br />
BITS 現在會使用群組原則來限制您可以建立的作業和檔案數目。 這可能會影響目前建立大量作業或將大量檔案新增至作業的應用程式。
</blockquote>
<br/> <br/> BITS 3.0 版包含在 Windows Server 2008 和 Windows Vista 作業系統中。 <br/> % Windir% \System32\QMgr.dll 的版本為 &quot; 7.0. xxxx &quot; 。<br/></td>
</tr>
<tr class="odd">
<td>版本2。5</td>
<td>新增對自訂 HTTP 標頭的支援、安全 HTTP 傳輸的憑證型用戶端驗證，以及 IPv6。 此外，也新增了網際網路閘道裝置的使用 (IGD) 計數器，以更精確地計算可用的 <a href="network-bandwidth.md">頻寬</a>。<br/> Windows Server 2008、Windows Vista 和 Windows XP Service Pack 3 (SP3) 作業系統都有提供 BITS 2.5 功能。 <br/> 您也可以下載適用于 Windows Server 2003 （含 Service Pack 2）的 BITS 2.5 (SP2) 、Windows Server 2003 Service Pack 1 (SP1) 和 Windows XP Service Pack 2 (SP2) 。 若要下載 BITS 2.5，請移至 <a href="https://www.microsoft.com/download/details.aspx?id=4933">Microsoft 下載中心</a> 並安裝 KB923845。<br/> % Windir% \System32\QMgr.dll 的版本為 6.7. xxxx。 &quot; &quot;<br/></td>
</tr>
<tr class="even">
<td>版本2。0</td>
<td>已新增執行並行前景下載的支援、使用伺服器訊息區 (SMB) 遠端名稱的路徑、下載檔案範圍、變更遠端名稱的首碼或完整名稱，以及限制用戶端頻寬的使用。 JobInactivityTimeout 原則現在位於 [電腦設定]、[系統管理範本]、[網路] 背景智慧型傳送服務 (BITS) 下。<br/> BITS 2.0 版包含在 Windows XP SP2 和 Windows Server 2003 SP1 中。 您也可以下載適用于 Windows Server 2003 和 Windows XP 的 BITS 2.0。 若要下載 BITS 2.0，請移至 <a href="https://www.microsoft.com/download/details.aspx?id=19031">Microsoft 下載中心</a> 並安裝 KB842773。<br/> % Windir% \System32\QMgr.dll 的版本為 6.6. xxxx。 &quot; &quot;<br/></td>
</tr>
<tr class="odd">
<td>1.5 版</td>
<td>已新增上傳和上傳-回復功能、事件的命令列執行，以及明確的認證和 proxy 認證。<br/> 從位1.5 開始，具有 <a href="/windows/win32/secauthz/restricted-tokens">受限權杖</a> 的使用者無法建立或修改作業。<br/> BITS 1.5 版包含在 Windows Server 2003 中。 您可以從 <a href="https://www.microsoft.com/download/details.aspx?id=22250">Microsoft 下載中心</a>取得適用于 Windows XP 的可轉散發套件。<br/> % Windir% \System32\QMgr.dll 的版本為 &quot; 6.5. &quot; xxxx。<br/></td>
</tr>
<tr class="even">
<td>版本1。2</td>
<td>與1.0 版相同的功能。 包含內部升級和改進。<br/> BITS 1.2 版包含在 Windows XP Service Pack 1 (SP1) 中。<br/> % Windir% \System32\QMgr.dll 的版本為 &quot; 6.2. &quot; xxxx。<br/></td>
</tr>
<tr class="odd">
<td>版本 1.0</td>
<td>初始版本。 在背景或前景中提供優先順序、節流和非同步下載。 電腦重新開機和網路中斷連線之後，下載會自動繼續。<br/> BITS 1.0 版包含在 Windows XP 中。<br/> % Windir% \System32\QMgr.dll 的版本是 &quot; 6.0. xxxx &quot; 。<br/></td>
</tr>
</tbody>
</table>

若要根據 BITS 功能來照亮程式中的功能，請在 (上使用 QueryInterface，例如) 工作物件，以查看工作物件是否可讓您建立所需的版本。 或者，請參閱 [判斷電腦上的位版本](./determining-the-version-of-bits-on-a-computer.md) ，以將 QMgr.dll 版本號碼轉換成 bits 版本。

## <a name="version-103"></a>版本10。3

此版本已新增下列介面
-   [**IBackgroundCopyJobHttpOptions3**](/windows/win32/api/Bits10_3/nn-bits10_3-ibackgroundcopyjobhttpoptions3) 
    [ **IBackgroundCopyServerCertificateValidationCallback**](/windows/win32/api/Bits10_3/nn-bits10_3-ibackgroundcopyservercertificatevalidationcallback)


## <a name="version-102"></a>版本10。2

此版本已新增下列介面
-   [**IBackgroundCopyJobHttpOptions2**](/windows/win32/api/Bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2)


## <a name="version-101"></a>版本10。1

此版本已新增下列介面
-   [**BackgroundCopyFile6**](/windows/win32/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6)
-   [**IBackgroundCopyCallback3**](/windows/win32/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3)

已加入下列常數以搭配 [BITS_JOB_PROPERTY_ID 列舉](/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id)使用。

-   **依 \_ \_ \_ \_ 需求 \_ 模式的 BITS 作業屬性**
-   **BITS \_ 作業 \_ 屬性 \_ 最小 \_ 通知 \_ 間隔 \_ 毫秒**


## <a name="version-50"></a>版本 5.0

此版本已新增下列介面：

-   [**IBackgroundCopyJob5**](/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5)

## <a name="version-40"></a>4.0 版

此版本已新增下列介面：

-   [**IBitsToken**](/windows/win32/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
-   [**IBackgroundCopyFile4**](/windows/win32/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4)

## <a name="version-30"></a>3.0 版

此版本已新增下列介面：

-   [**IBackgroundCopyCallback2**](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2)
-   [**IBackgroundCopyFile3**](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyfile3)
-   [**IBackgroundCopyJob4**](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4)
-   [**IBitsPeer**](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeer)
-   [**IBitsPeerCacheAdministration**](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration)
-   [**IBitsPeerCacheRecord**](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeercacherecord)
-   [**IEnumBitsPeerCacheRecords**](/windows/win32/api/Bits3_0/nn-bits3_0-ienumbitspeercacherecords)
-   [**IEnumBitsPeers**](/windows/win32/api/Bits3_0/nn-bits3_0-ienumbitspeers)

新增下列常數以搭配 [**IBackgroundCopyJobHttpOptions：： SetSecurityFlags**](/windows/win32/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags) 方法使用：

-   **BG \_ HTTP 重新 \_ 導向 \_ 原則 \_ 允許 \_ 無訊息**
-   **BG \_ HTTP 重新 \_ 導向 \_ 原則 \_ 允許 \_ 報表**
-   **不 \_ 允許 BG HTTP 重新 \_ 導向 \_ 原則 \_**
-   **BG \_ HTTP 重新 \_ 導向 \_ 原則 \_ 遮罩**
-   **BG \_ HTTP 重新 \_ 導向 \_ 原則 \_ 允許 \_ HTTPS \_ 至 \_ HTTP**

## <a name="version-25"></a>版本2。5

針對2.5 版新增了下列介面和列舉：

-   [**IBackgroundCopyJobHttpOptions**](/windows/win32/api/Bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions)
-   [**BG \_ 證書 \_ 存儲 \_ 位置**](/windows/win32/api/Bits2_5/ne-bits2_5-bg_cert_store_location)

## <a name="version-20"></a>版本2。0

針對2.0 版新增了下列介面、結構和主題：

-   [**IBackgroundCopyJob3**](/windows/win32/api/Bits2_0/nn-bits2_0-ibackgroundcopyjob3)
-   [**IBackgroundCopyFile2**](/windows/win32/api/Bits2_0/nn-bits2_0-ibackgroundcopyfile2)
-   [**BG \_ 檔案 \_ 範圍**](/windows/win32/api/Bits2_0/ns-bits2_0-bg_file_range)
-   [群組原則](group-policies.md)

如需並行前景下載的詳細資訊，請參閱「 [**BG \_ 工作 \_ 優先順序**](/windows/win32/api/Bits/ne-bits-bg_job_priority)」的備註一節。

如需使用 SMB 通訊協定的相關資訊，請參閱 [**BG 檔案 \_ \_ 資訊**](/windows/win32/api/Bits/ns-bits-bg_file_info)。

## <a name="version-15"></a>1.5 版

針對1.5 版新增了下列介面和主題：

-   [**IBackgroundCopyJob2**](/windows/win32/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2)
-   [從 Upload-Reply 作業中取出回復](retrieving-the-reply-from-an-upload-reply-job.md)
-   [註冊以執行程式](registering-to-execute-a-program.md)
-   [上傳作業的 BITS 伺服器設定](bits-server-settings-for-upload-jobs.md)
-   [設定伺服器以進行上傳](setting-up-the-server-for-uploads.md)
-   [使用 BITS 通知要求/回應標頭](using-bits-notification-request-response-headers.md)

 
## <a name="updating-bits-versions"></a>更新 BITS 版本
 
您可以下載 Windows Server 2008 （含 Service Pack 2）的 BITS 4.0 (SP2) 、Windows Vista （含 Service Pack 1） (SP1) ，以及 Windows Vista （含 Service Pack 2 (SP2) ）。 如需下載 BITS 4.0 的詳細資訊，請參閱 [KB968929](https://support.microsoft.com/kb/968929)。
