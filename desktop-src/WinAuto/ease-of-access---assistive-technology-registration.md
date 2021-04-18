---
title: 輕鬆存取輔助技術註冊
description: 本文說明如何使用輕鬆存取中心註冊協助工具應用程式。 它也會說明如何量身打造您的協助工具應用程式，使其可與安全桌面順利搭配運作。
ms.assetid: 6F1F2AAE-B2E4-4F26-8BDF-A3DE8F5C5460
ms.topic: article
ms.date: 04/02/2019
ms.openlocfilehash: 66901cd899fc578b032f86e3752fcdcac0788ba1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965247"
---
# <a name="ease-of-access---assistive-technology-registration"></a>輕鬆存取輔助技術註冊

本文說明如何使用輕鬆存取中心註冊協助工具應用程式。 它也會說明如何量身打造您的協助工具應用程式，使其可與安全桌面順利搭配運作。

輕鬆存取中心是適用于 Microsoft Windows 的主控台應用程式，結合了協助工具和易用性的功能。 藉由使用輕鬆存取中心，使用者可以設定其電腦以符合其實體和認知需求。

輕鬆存取中心的其中一個功能是協助使用者啟動協助工具應用程式，包括 [朗讀程式]、[螢幕小鍵盤] 和 [放大鏡]。 註冊的協力廠商應用程式也會出現在輕鬆存取中心中，並且可以直接從該處啟動。

協助工具應用程式需要與安全桌面順利搭配運作。 安全桌面是使用者介面，當 (電腦在登入時，或當使用者已鎖定桌面) ，而且系統提示使用者允許可能不安全的動作時，就會出現該介面。 基於安全考慮，Windows 會限制在安全桌面上執行的協力廠商軟體。 如果您想要讓協助工具應用程式在安全桌面電腦上執行，您需要向輕鬆存取中心註冊應用程式。

## <a name="registering-with-the-ease-of-access-center"></a>向輕鬆存取中心註冊

協助工具應用程式會在安裝應用程式時，藉由建立一或多個登錄機碼來向輕鬆存取中心註冊。 下表列出登錄機碼中包含的資訊。



| Name                        | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 強制/選用 | 語言      |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|---------------|
| 應用程式名稱            | 資源檔中的應用程式名稱。 此登錄值包含指定格式的字串。 如果應用程式是以英文以外的語言當地語系化，則這可能是應用程式名稱的當地語系化版本。 名稱會出現在輕鬆存取中心中。<br/>                                                                                                                                                                                                                                                                                       | 強制性          | 當地語系化     |
| ATExe                       | 應用程式可執行檔或映射的名稱。 Windows 會使用這個值來判斷協助工具應用程式是否正在執行。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            | 強制性          | 未當地語系化 |
| CopySettingsToLockedDesktop | **DWORD** 值，指出是否要將協助工具應用程式的設定複製到鎖定的桌面。<br/> 如果這個值是1，則應用程式可以將設定寫入使用者登錄中的位置，而 Windows 會將設定複製到使用者登錄中鎖定桌面的相同位置。 這可讓應用程式將其狀態從「標準」桌面保存到鎖定的桌面。<br/>                                                                                                                                                             | 選擇性           | 未當地語系化 |
| Description                 | 應用程式的簡短描述，從資源檔。 此登錄值包含指定格式的字串。 如果應用程式是以英文以外的語言當地語系化，則這可能是描述的當地語系化版本。 這個字串的長度必須小於512個字元。<br/> 此描述會出現在輕鬆存取中心中，以提供協助工具應用程式給使用者的其他相關資訊。<br/> 此值也可以用來通知使用者，應用程式不會在安全桌面上使用。<br/>      | 強制性          | 當地語系化     |
| 設定檔                     | 指定應用程式所提供之住宿的簡短 XML 片段。 它可確保應用程式會出現在輕鬆存取中心的正確類別下。<br/>                                                                                                                                                                                                                                                                                                                                                                                                  | 強制性          | 未當地語系化 |
| PassiveAutoStartBehavior    | <p>**DWORD** 值，指出是否已啟用舊版自動啟動行為。</p><p>預設值為0，表示需要舊版自動啟動行為。 這會導致 [在登入後開始登入] 設定，以簽入現成體驗 (OOBE) 和主控台 (查看主控台 > 輕鬆存取 > 輕鬆存取中心 >) **變更登入設定** ，並在 UAC 和鎖定畫面之後自動啟動。</p><p>值為1時，表示應該使用新的自動啟動行為，其中的 [在登入後啟動] 設定不會簽入 (OOBE) 和主控台，而且只有在核取 [登入後啟動] 設定時，才會在登入) 針對每個使用者 (會話自動啟動一次。</p>                                                                                                                                                                                                                                                                                                                                                                                                  | 選擇性          | 未當地語系化 |
| SecureDesktopAccommodation  | 替代協助工具應用程式的名稱，此應用程式會在安全桌面電腦上執行，以取代此應用程式。 替代項可以是不同的應用程式、相同應用程式的不同版本、Windows 所含的協助工具應用程式之一，如果您不想要在安全桌面上執行任何協助工具應用程式，則可以使用「無」。 <br/>                                                                                                                                                                                                               | 選擇性           | 未當地語系化 |
| 簡單設定檔              | 值，描述如何在一個或兩個字組中分類應用程式：螢幕閱讀程式、放大鏡或螢幕小鍵盤（例如）。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  | 強制性          | 未當地語系化 |
| StartExe                    | 可執行檔的完整路徑。 此值可用來啟動協助工具應用程式。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | 強制性          | 未當地語系化 |
| StartParams                 | 命令列引數。 這些值會與 StartExe 搭配使用，以啟動應用程式。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | 選擇性           | 未當地語系化 |
| TerminateOnDesktopSwitch    | **DWORD** 值，指定協助工具應用程式如何回應安全桌面的轉換。<br/> 如果此值不存在或為1，則 Windows 會在每次與安全桌面的轉換之間終止並重新啟動應用程式。 這是預設行為。<br/> 如果此值為0，則 Windows 不會在桌面轉換時終止協助工具應用程式。 應用程式會繼續在先前的桌面上執行，而且如果實例尚未執行，則 Windows 會在新的桌面上啟動新的實例。<br/> | 選擇性           | 未當地語系化 |


 

### <a name="localization"></a>當地語系化

應用程式名稱和描述的登錄值必須可以當地語系化，以支援多語系消費者介面 (MUI) 。

這些字串採用下列格式，其中角括弧表示必要的元素，而方括弧表示選擇性元素。

*@ <ResDllPath \\ ResDLLFilename>，- <resID> \[ ;<comment>\]*

*<ResDllPath \\ResDLLFilename>* 是資源 DLL 的路徑。 路徑可以包含環境變數。

*<resID>* 這是字串的資源識別碼。

*\[ 批註 \]* 包含任何選擇性批註。

請看以下範例：


```
@%SystemRoot%\system32\anyAT.dll,-5020
```



如需 MUI 的詳細資訊，請參閱 [WINDOWS Mui 知識中心](../intl/about-multilingual-user-interface.md)。

### <a name="hci-profile"></a>HCI 設定檔

電腦 (HCI) 設定檔的互動方式，是根據使用者的需求來決定要提供哪些住宿。 協助工具應用程式應該註冊應用程式有助於容納的殘障類型相關資訊。

設定檔登錄值包含 XML，可描述協助工具應用程式的目標殘障類型。 此 XML 的格式如下：


```XML
<HCIModel>
<Accommodation type="disability"/>
</HCIModel>
```



[ **便利設施類型** ] 屬性的有效值如下所示：

-   輕度視覺
-   嚴重願景
-   輕度認知
-   嚴重認知
-   輕度的靈活性
-   嚴重的靈活性
-   輕度聽力
-   嚴重聽力
-   輕度語音
-   嚴重語音

> [!Note]  
> 這些值區分大小寫。

 

如果協助工具應用程式支援多個住宿，設定檔登錄值應該包含每個住宿的 **便利型** 別屬性。

### <a name="ease-of-access-registry-details"></a>輕鬆存取登錄詳細資料

若要註冊您的協助工具應用程式，您必須在下列登錄位置為您的應用程式建立金鑰，並以名稱/值組填入。

**HKLM \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ 協助工具 \\ ATs\\**

使用下列格式來命名您應用程式的登錄機碼：

*"公司版 \_ ProductName \_ v \# "*

例如「Contoso \_ 放大鏡2.0」 \_ 。

若要新增登錄值，您的安裝程式必須以較高的許可權執行。

### <a name="secure-desktop-accommodation"></a>安全桌面的住宿

**SecureDesktopAccommodation** 登錄機碼可讓您指定協助工具應用程式對安全桌面的回應方式。 根據預設，輕鬆存取中心會在安全桌面電腦上啟動您的應用程式（如果它已在一般桌上型電腦上執行），或已設定為在登入桌面上執行。 藉由使用 **SecureDesktopAccommodation** 機碼，您可以：

-   指定要在安全桌面上使用的應用程式替代版本。 例如，您可能會有停用不安全功能的替代版本，或已優化為使用較少的記憶體，且更快啟動。

    若要指定替代版本，請將 **SecureDesktopAccommodation** 索引鍵設定為替代版本的名稱。 例如，如果您在 Contoso 螢幕讀取器 v1.0 金鑰註冊您的應用程式 \_ \_ ，您可以在 Contoso screen ReaderSecure v1.0 註冊替代版本 \_ \_ 。 然後，將 Contoso  \_ 螢幕讀取器1.0 版的 SecureDesktopAccommodation 機碼設定 \_ 為 "contoso \_ screen ReaderSecure v1.0 \_ "。

-   指定要在安全桌面上使用的 Microsoft 協助工具應用程式來取代您的應用程式。 針對此選項，請將 **SecureDesktopAccommodation** 設定為特定 Microsoft 協助工具應用程式的名稱： "osk"、"magnifierpane" 或 "朗讀程式"。
-   指定您的應用程式不應該在安全桌面電腦上執行，也不應該在任何替代的應用程式上執行。 針對此選項，請將 **SecureDesktopAccommodation** 設定為 "none" (建議) 或不存在的應用程式名稱。

如果協助工具應用程式的 **SecureDesktopAccommodation** 登錄機碼指定要在安全桌面上執行的 Microsoft 協助工具應用程式來取代您的應用程式，則 Windows 會在轉換至安全桌面時通知使用者。 為了通知使用者，Windows 會顯示您應用程式的描述登錄機碼中指定的字串。 例如，如果 ScreenReader Deluxe 1.0 應用程式在安全桌面上使用 Microsoft 朗讀程式，則會包含描述字串，例如：「Microsoft 朗讀程式將用於鎖定、登入及其他安全的桌面，以取代 ScreenReader Deluxe 1.0」。

如果您應用程式的 **SecureDesktopAccommodation** 機碼設定為「無」，請使用 **Description** 金鑰告訴使用者您的應用程式無法在安全桌面上使用，也沒有提供任何替代方法。

Windows 會顯示輕鬆存取中心中相關位置的描述文字。

### <a name="running-at-installation-and-on-the-logon-desktop"></a>在安裝和登入桌面上執行

如果您在下列登錄位置將協助工具應用程式的已註冊金鑰名稱附加至字串，Windows 會在安裝後立即啟動您的應用程式。 此外，每當登入桌面為使用中時，Windows 就會自動執行您的應用程式。

**HKCU \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ 協助工具 \\ 設定**

設定金鑰是以逗號分隔的字串。 若要新增應用程式，請將與您應用程式登錄機碼相同的字串附加到 HKLM \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ 協助工具 \\ ATs \\ 。

### <a name="running-in-a-job"></a>在作業中執行

如果 **TerminateOnDesktopSwitch** 登錄機碼不存在或設定為非零，則 Windows 會在作業的內容中執行應用程式，並在每個桌面轉換時終止並重新啟動應用程式。 在作業中執行可確保只有應用程式的單一實例會在特定時間執行，並讓應用程式不需要監視桌面狀態。 在作業中執行的缺點包括：

-   應用程式會在每一部桌上型電腦轉換時產生啟動成本。
-   只能透過輕鬆存取中心啟動應用程式。
-   應用程式必須持續儲存其設定，因為桌面轉換可以隨時終止。

如果 **TerminateOnDesktopSwitch** 索引鍵存在且設為0，則 Windows 不會在作業中執行協助工具應用程式。 這有下列優點：

-   沒有任何啟動成本與桌面轉換相關聯。
-   您可以在輕鬆存取中心之外啟動應用程式。

未在作業中執行的缺點包括：

-   因為應用程式不會在桌面轉換時重新開機，所以它必須偵測目前的桌面何時處於非使用中狀態，並適當地回應。 例如，應用程式必須放棄硬體的控制權，如此一來，應用程式的安全桌面版本才能使用它，而且應用程式應該進入睡眠模式，以避免使用處理器資源。
-   如果可以透過 [開始] 功能表、Windows 檔案總管或命令列來啟動應用程式，則必須通知輕鬆存取中心。 如需詳細資訊，請參閱 **Windows 標誌鍵 + U**。
-   由於應用程式的多個複本可以同時在不同的桌上型電腦上執行，因此必須撰寫應用程式，以支援多個執行中的複本。

### <a name="windows-logo-key--u"></a>Windows 標誌鍵 + U

如果您的協助工具應用程式設定為在作業中執行，則應用程式的啟動程式碼應該包含對 [**IsProcessInJob**](/windows/desktop/api/jobapi/nf-jobapi-isprocessinjob) 函式的呼叫，以判斷應用程式是否正在作業中啟動。 如果是，應用程式應該啟動輕鬆存取中心然後結束。 下列範例顯示如何呼叫 **IsProcessInJob**。


```C++
BOOL fAlreadyInJob;
BOOL fSuccess = IsProcessInJob(GetCurrentProcess(), NULL, &fAlreadyInJob); 
```



如果協助工具應用程式設定為在作業之外執行，則應該通知輕鬆存取中心應用程式正在啟動，並正常繼續。

無論應用程式的設定方式為何，如果它提供從應用程式中結束的方法（例如 [關閉] 按鈕），則應用程式必須通知輕鬆存取中心正在結束。

應用程式會藉由設定暫存登錄機碼，然後將 Windows 標誌鍵 + U 按鍵組合插入輸入資料流程，來通知輕鬆存取中心。

應用程式應該在下列位置建立暫存金鑰。

**HKCU \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ AccessibilityTemp**

暫存索引鍵的名稱應該與註冊的應用程式名稱相同，例如 "Contoso \_ Screen Reader v1.0 \_ "。 索引鍵的值是在啟動時設定為0x0003 的 **DWORD** ，或在應用程式結束時0x0002 的值。


```C++
INPUT input[4] = {0};

input[0].type = INPUT_KEYBOARD;
input[0].ki.wVk = VK_LWIN;
input[0].ki.dwFlags = 0;

input[1].type = INPUT_KEYBOARD;
input[1].ki.wVk = 0x55; // U key
input[1].ki.dwFlags = 0;

input[2].type = INPUT_KEYBOARD;
input[2].ki.wVk = 0x55; // U key
input[2].ki.dwFlags = KEYEVENTF_KEYUP;

input[3].type = INPUT_KEYBOARD;
input[3].ki.wVk = VK_LWIN;
input[3].ki.dwFlags = KEYEVENTF_KEYUP;

SendInput(ARRAYSIZE(input), input, sizeof(input[0]));
```



### <a name="windows-logo-key--volume-up"></a>Windows 標誌鍵 + 向上音量

當使用者按下 Windows 標誌鍵 + 音量按鍵組合 (（例如 tablet 裝置) ）來啟動協助工具應用程式時，輕鬆存取中心會將下列命令列引數傳遞至應用程式：

**/hardwarebuttonlaunch**

您的應用程式可以使用這個引數來判斷是要正常啟動，還是要據以調整行為。

### <a name="transferring-secure-desktop-settings"></a>傳送安全桌面設定

如果您的協助工具應用程式支援安全桌面，您可以在應用程式轉換至安全桌面時，使用登錄來複製設定。 複製設定有助於讓使用者更順暢地轉換至安全桌面。

若要複製設定，請將應用程式的 CopySettingsToLockedDesktop 登錄機碼設定為1，並將設定儲存在下列登錄位置中。

**HKCU \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ 協助工具 \\ ATConfig\\<AT Key Name>**

當應用程式正在執行時，輕鬆存取中心會監視此登錄位置。 當轉換到安全桌面時，輕鬆存取中心會將設定複製到安全桌面 HKCU hive 中的相同位置。 然後，應用程式可以讀取設定並繼續其狀態。

您的協助工具應用程式應該定期寫入其設定，或每當值變更時。 在應用程式結束時寫入設定將無法運作。 如果應用程式是在作業中執行，則會在結束程式碼有機會執行之前，從安全桌面的轉換結束。 如果應用程式不是在作業中執行，則應用程式不會在離開安全桌面的轉換時終止。

### <a name="caution"></a>警告

因為此處所述的登錄機碼是以使用者模式撰寫，所以並不安全。 如果您的協助工具應用程式會讀取這些機碼的內容，則應謹慎檢查資料並謹慎使用。 具體來說，您的應用程式應該對 **DWORD** 值進行界限檢查、謹慎使用字串長度、不應讀取外掛程式 DLL 名稱，而且不應該執行字串中找到的任何命令。

## <a name="registry-examples"></a>登錄範例

下列範例顯示名為 Contoso ScreenReader 2.0 版之虛構產品的可能登錄值，其當地語系化名稱會儲存為資源。

資料表中的值位於下列索引鍵底下：

**HKLM \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ 協助工具 \\ ATs \\ Contoso \_ Screen Reader \_ 2.0 版**



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>名稱</th>
<th>類型</th>
<th>資料</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ApplicationName</td>
<td>REG_SZ</td>
<td>@% SystemRoot% \system32\ContosoRes.dll，-5020</td>
</tr>
<tr class="even">
<td>Description</td>
<td>REG_SZ</td>
<td>@% SystemRoot% \system32\ContosoRes.dll，-5040</td>
</tr>
<tr class="odd">
<td>設定檔</td>
<td>REG_SZ</td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>XML</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;low vision&quot; />
   <Accommodation type=&quot;severe vision&quot; />
   <Accommodation type=&quot;mild cognitive&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>SimpleProfile</td>
<td>REG_SZ</td>
<td>ScreenReader</td>
</tr>
<tr class="odd">
<td>StartExe</td>
<td>REG_SZ</td>
<td>C:\ContosoTools\Bin\ContosoSR.exe</td>
</tr>
<tr class="even">
<td>StartParams</td>
<td>REG_SZ</td>

</tr>
<tr class="odd">
<td>SecureDesktopAccommodation</td>
<td>REG_SZ</td>
<td>Narrator</td>
</tr>
</tbody>
</table>



 

如果應用程式同時在單一可執行檔中提供螢幕閱讀程式和螢幕放大鏡，螢幕讀取器元件的值可能如下所示：



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>名稱</th>
<th>類型</th>
<th>資料</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ApplicationName</td>
<td>REG_SZ</td>
<td>@C:\Program Files\Contoso\Contosores.dll，-30</td>
</tr>
<tr class="even">
<td>Description</td>
<td>REG_SZ</td>
<td>@C:\Program Files\Contoso\Contosores.dll、-32</td>
</tr>
<tr class="odd">
<td>設定檔</td>
<td>REG_SZ</td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>XML</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;low vision&quot; />
   <Accommodation type=&quot;severe vision&quot; />
   <Accommodation type=&quot;mild cognitive&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>SimpleProfile</td>
<td>REG_SZ</td>
<td>ScreenReader</td>
</tr>
<tr class="odd">
<td>StartExe</td>
<td>REG_SZ</td>
<td>C:\Program Files\Contoso\Bin\ContosoSR.exe</td>
</tr>
<tr class="even">
<td>StartParams</td>
<td>REG_SZ</td>
<td>/r</td>
</tr>
</tbody>
</table>



 

放大鏡元件的值會在下列機碼中：

**HKLM \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Contosoibility \\ ATs \\ Contoso \_ 放大鏡 \_ 2.0 版**



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>名稱</th>
<th>類型</th>
<th>資料</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ApplicationName</td>
<td>REG_SZ</td>
<td>@c:\Program Files\Contoso\Contosores.dll，-31</td>
</tr>
<tr class="even">
<td>Description</td>
<td>REG_SZ</td>
<td>@c:\Program Files\Contoso\Contosores.dll、-42</td>
</tr>
<tr class="odd">
<td>設定檔</td>
<td>REG_SZ</td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>XML</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;mild vision&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>SimpleProfile</td>
<td>REG_SZ</td>
<td>放大</td>
</tr>
<tr class="odd">
<td>StartExe</td>
<td>REG_SZ</td>
<td>c:\Program Files\Contoso\Bin\ContosoSR.exe</td>
</tr>
<tr class="even">
<td>StartParams</td>
<td>REG_SZ</td>
<td>/m</td>
</tr>
</tbody>
</table>



 

 

