---
title: 適用於 Windows 的遊戲測試案例：Windows XP、Windows Vista、Windows 7 和 Windows 8 上遊戲的最佳作法
description: 本文提供適用于 Windows 遊戲的測試案例。
ms.assetid: bbe84d3f-e7ff-f14f-ec25-ae1c980749fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b13a4934c539579e49c9b00c60f3603bd64c711
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120273"
---
# <a name="games-for-windows-test-cases-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a>Windows 測試案例的遊戲： Windows XP、Windows Vista、Windows 7 和 Windows 8 遊戲的最佳作法

本文提供適用于 Windows 遊戲的測試案例。

## <a name="how-to-use-this-article"></a>如何使用本文

本文有三個主要區段：

<dl> <dt>

<span id="Test_Requirements"></span><span id="test_requirements"></span><span id="TEST_REQUIREMENTS"></span>**測試需求**
</dt> <dd>

這份檔中的每項測試需求都有四個主要區段：標題和資料表，其中有三個值得注意的區段 (左欄、右上角) 。

<dl> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>標題
</dt> <dd>

測試案例的名稱。

</dd> <dt>

<span id="Box__far_left_column"></span><span id="box__far_left_column"></span><span id="BOX__FAR_LEFT_COLUMN"></span>Box、最左邊的資料行
</dt> <dd>

測試案例所套用的作業系統名稱。

</dd> <dt>

<span id="Box__right_top"></span><span id="box__right_top"></span><span id="BOX__RIGHT_TOP"></span>Box、右上角
</dt> <dd>

測試案例的簡短摘要。

</dd> <dt>

<span id="Box__right_bottom"></span><span id="box__right_bottom"></span><span id="BOX__RIGHT_BOTTOM"></span>Box、右下角
</dt> <dd>

實際測試案例的詳細資料。

</dd> </dl> </dd> <dt>

<span id="Sample_Test_Script"></span><span id="sample_test_script"></span><span id="SAMPLE_TEST_SCRIPT"></span>**範例測試腳本**
</dt> <dd>

如果使用測試需求做為指南，此區段是一般測試階段將遵循的順序範例。

</dd> <dt>

<span id="Test_Tool_Notes"></span><span id="test_tool_notes"></span><span id="TEST_TOOL_NOTES"></span>**測試控管注意事項**
</dt> <dd>

本章節包含每個測試控管的詳細資訊，這些工具可用來確認測試需求中的通過或失敗狀況。

</dd> </dl>

## <a name="test-requirements"></a>測試需求

### <a name="1-game-requirements"></a>1. 遊戲需求

### <a name="11-windows-games-explorer"></a>1.1 Windows 遊戲瀏覽器



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>遊戲必須在 Windows Vista 和 Windows 7 上的遊戲瀏覽器中顯示。 選取時，遊戲也必須顯示正確的中繼資料。 安裝不能建立快捷方式來啟動桌面、[開始] 功能表或任何其他位置中的遊戲。 不得建立移除的工作和快捷方式。</td>
</tr>
<tr class="even">

<td><ol>
<li>安裝遊戲之後，請開啟 [遊戲瀏覽器]。</li>
<li>確認 [遊戲瀏覽器] 中顯示遊戲圖示。</li>
<li>以滑鼠右鍵按一下圖示，並測試每個應用程式定義的 play & 支援工作。</li>
<li>按一下圖示，並確認底部的 [發行者]、[開發人員]、[內容類型]、[發行日期]、[版本])  (的中繼資料都是正確的。</li>
<li>確認遊戲圖示 Windows 體驗指數 (WEI) 資訊顯示在 [遊戲] Explorer 中。</li>
<li>確認在 [遊戲瀏覽器] 中，中繼資料的遊戲超連結可正常運作。  (如果未顯示超連結，則這是未簽署 exe 的可能正負號;請參閱 <a href="#23-sign-files">2.3 章節</a>的 ) 。</li>
<li>確認遊戲在 [遊戲瀏覽器] 中顯示正確的 [家長監護] 控制項評等。  (如果指出未分級，請確認這是未分級的遊戲;否則，這是未簽署 exe 的指標;請參閱 <a href="#23-sign-files">2.3 章節</a>的 ) 。</li>
<li>確認遊戲未在使用者桌面上放置啟動快捷方式。</li>
<li>按一下 [開始]-> [所有程式]。</li>
<li>確認遊戲未在 [開始] 功能表中放置啟動快捷方式。</li>
<li>確認該遊戲不會在主控台以外的 [開始] 功能表中放置卸載快捷方式。</li>
<li>如果遊戲是以數位方式散佈，請確認服務提供者出現在 Windows 遊戲瀏覽器中。</li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="12-windows-family-safety--parental-controls"></a>1.2 Windows 系列安全性/家長監護控制項



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>遊戲必須在標準使用者的內容中執行 &quot; &quot; 。 家長監護必須能夠封鎖遊戲。 確認 GDF 具有 EXE 名稱。</td>
</tr>
<tr class="even">

<td><ol>
<li>在 Windows Vista 或 Windows 7 中建立名為 Toby 的標準使用者帳戶。 啟動-> 主控台-> 新增或移除使用者帳戶-> 建立新帳戶</li>
<li>和 Jane 一樣，從系統管理員帳戶設定遊戲的家長監護。 開始 > 主控台-> 為任何使用者 > 設定家長監護 Toby
<ol>
<li>確認已從 [遊戲瀏覽器] 圖示啟動遊戲。</li>
<li>確認該遊戲在 [家長監護] 主控台中的 [遊戲] 標題下方，顯示正確的 [家長監護] 評等。</li>
<li>套用家長監護之前，請確認遊戲不會在啟動時提示輸入系統管理員認證。</li>
<li>將家長監護設定為 &quot; On &quot; 。</li>
<li>在 [Windows 設定] 區段中，按一下 [遊戲]。</li>
<li>按一下 [確定] (設定現在應該是 &quot; AO/所有遊戲 &quot;) 。</li>
<li>確認遊戲以使用者 Jane 的方式執行這些設定。</li>
<li>以 Jane 的形式登出，並以 Toby 登入。</li>
<li>確認遊戲以這些設定做為使用者 Toby 來執行。</li>
<li>以 Toby 的形式登出，並以 Jane 的身份登入。</li>
<li>返回至上一個畫面，然後選取 [ &quot; 設定遊戲分級] &quot; 。</li>
<li><p>選取低於遊戲 ESRB 評等的評等。</p>
<blockquote>
[!Note]<br />
如果遊戲未分級，請略過此步驟，並移至此測試的下一個部分。 視所測試 SKU 的語言地區設定而定，可能需要選擇不同的評等系統來尋找遊戲評等。
</blockquote>
<p><br/></p></li>
<li>以 Jane 的形式登出，並以 Toby 登入。</li>
<li>確認使用者 Jane 封鎖 ESRB 時，不會啟動使用者 Toby 的遊戲。</li>
<li>以 Toby 的形式登出，並以 Jane 的身份登入。</li>
<li>如果之前有變更，請還原 ESRB 設定。</li>
<li>如果沒有任何 ESRB 設定，請選取 &quot; [封鎖] 或 [允許特定遊戲]， &quot; 然後依名稱選取遊戲。</li>
<li>以 Jane 的形式登出，並以 Toby 登入。</li>
<li>確認使用者 Jane 封鎖 EXE/名稱時，不會啟動使用者 Toby 的遊戲。</li>
<li>以 Jane 的形式登出 Toby，然後再登入。</li>
<li>就像 Jane 一樣，開啟使用者控制項-> 的應用程式限制。</li>
<li>按一下 [ &quot; Toby 只能使用我允許的程式 &quot; ]，然後按一下 [確定] (也就是不允許 exe) 。</li>
<li>移至使用者控制項 |遊戲使用 ESRB 評等來控制及允許特定遊戲。</li>
<li>以 Jane 的形式登出，並以 Toby 登入，然後嘗試播放遊戲。</li>
<li>確認遊戲未遭到封鎖，且 Toby 可以在 [ &quot; 允許無 exe] 設定時播放 &quot; 。</li>
</ol></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="13-windows-vista-rich-saved-games"></a>1.3 Windows Vista 豐富儲存的遊戲

這項需求已淘汰。

### <a name="14-xbox-360-common-controller-for-windows-conditional-requirement"></a>1.4 Xbox 360 Windows 條件式需求的通用控制器 \[\]



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>支援遊戲台控制器的遊戲必須支援使用 XInput API 的適用于 Windows 的 Xbox 360 控制器。 所有對通用控制器觸發程式和按鈕的參考都必須使用 Xbox 360 名稱。</td>
</tr>
<tr class="even">

<td><ol>
<li>啟動遊戲。</li>
<li>移至控制器選項。 **</li>
<li>確認遊戲可將 Windows Xbox 360 控制器辨識為輸入裝置。</li>
<li>玩遊戲並確認遊戲和功能表系統可控制適用于 Windows 的 Xbox 360 控制器。</li>
<li>確認適用于 Windows 的 Xbox 360 控制器根據接受的標準行為。  (B 代表上一頁、A for accept、Start for 遊戲功能表/暫停或接受等 ) </li>
<li>確認遊戲是使用 Xbox 360 名稱來參考控制器按鈕和觸發程式。</li>
</ol>
<br/>
<blockquote>
[!Note]<br />
如果遊戲不支援遊戲控制器及/或僅支援鍵盤/滑鼠，則略過此測試案例。
</blockquote>
<br/> * * 控制器的設定可能位於遊戲之外。 <br/></td>
</tr>
</tbody>
</table>



 

### <a name="15-multiple-aspect-ratios-and-resolutions"></a>1.5 多重外觀比例和解析度



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>遊戲必須至少支援下列外觀比例和相關聯的螢幕解析度： <br/>
<ul>
<li>4:3 &quot; 標準 &quot; (800 600 或 1024 768) </li>
<li>16:9 &quot; 寬銀幕 &quot; (1280 720) </li>
<li>16:10 &quot; 寬銀幕 &quot; (1152 720、1680 1050 或 800 480) </li>
</ul></td>
</tr>
<tr class="even">

<td>找出遊戲的影片選項 (這可能是) 的遊戲中。<br/>
<blockquote>
[!Note]<br />
下列測試必須在寬螢幕監視器上完成。
</blockquote>
<br/>
<ol>
<li>在 [影片解析度] 區段中，選取 [800 600] 或 [1024 768]。</li>
<li>確認遊戲以4:3 的外觀比例解析度執行。</li>
<li>在 [影片解析度] 區段中，選取 [1280 720]。</li>
<li>確認遊戲以16:9 的外觀比例解析度執行。</li>
<li>在 [影片解析度] 區段中，選取 [1680 1050]、[800 480] 或 [1152 720]。</li>
<li>確認遊戲以16:10 的外觀比例解析度執行。</li>
<li>確認遊戲不會延展圖片，而是會顯示更廣泛的觀點。</li>
<li>確認當解決問題發生變更時，遊戲會提示使用者。</li>
<li>如果使用者未在15秒內接受，請確認顯示器會還原為先前的設定。</li>
<li>確認遊戲未在遊戲播放區域的左側和右側新增黑色橫條。  (在這種情況下，您會在畫面中間看到遊戲區域仍處於4:3 的比例。 ) </li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="16-windows-media-center"></a>1.6 Windows Media Center

這項需求已淘汰。

### <a name="17-direct3d-conditional-requirement"></a>1.7 Direct3D \[ 條件式需求\]



| OS                                                                    | 需求                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows 7<br/> Windows Vista<br/> Windows XP<br/> | 如果遊戲使用 Direct3D，支援的最低版本必須是 Direct3D 9，而且 Direct3D 必須是任何顯示設定選項的預設值。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|     <dl> <dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>手動</dt> <dd> 啟動遊戲。 在影片選項中，檢查是否有呈現選項、D3D 和/或 OpenGL。 如果有的話，請確認遊戲轉譯選項預設為 Direct3D。 如果您無法確認 D3D9 是所使用的 DirectX 版本，請繼續進行自動化測試。 <br/> </dd> <dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>自動化測試</dt> <dd> 使用工具： Depends.exe <br/> </dd> </dl> |



 

### <a name="18-enable-high-dpi-aware"></a>1.8 啟用高 DPI 感知



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>在啟用 DPI 縮放比例的情況下，遊戲和其安裝程式必須正確執行，而且沒有視覺問題。</td>
</tr>
<tr class="even">

<td><dl> <dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>手動</dt> <dd>
<ol>
<li>將系統設定為 DPI 150%： <br/> Windows Vista：主控台：個人化、調整字型大小 (DPI) 、自訂 DPI。 設定為150%。<br/> Windows 7：主控台：顯示，設定為較大-150%。<br/></li>
<li>執行安裝程式和遊戲，確認裁剪的畫面或對話方塊沒有任何問題。</li>
</ol>
</dd> <dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>自動化測試</dt> <dd> 確認元素 <dpiAware>true</dpiAware> 包含在內嵌資訊清單中。<br/> 使用工具： Mt.exe <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="2-security-and-compatibility"></a>2. 安全性和相容性

### <a name="21-follow-user-account-control-guidelines"></a>2.1 遵循使用者帳戶控制指導方針



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>應用程式所包含的每個可執行檔 (.EXE 擴充) 都必須有定義其執行層級的內嵌資訊清單：
<pre class="syntax" data-space="preserve"><code><requestedExecutionLevel level=&quot;asInvoker|highestAvailable|requireAdministrator&quot; 
              uiAccess=&quot;true|false&quot;/></code></pre>
<br/>
<blockquote>
[!Note]<br />
若為遊戲和遊戲安裝程式，uiAccess 應一律設為 &quot; false &quot; 。
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td><ol>
<li>確認遊戲可執行檔包含資訊清單。</li>
<li>確認遊戲可執行檔資訊清單並無 requestedexecutionlevel 是 &quot; AsInvoker &quot; 。</li>
</ol>
使用工具： Mt.exe <br/></td>
</tr>
</tbody>
</table>



 

### <a name="22-support-x64-versions-of-windows"></a>2.2 支援 x64 版本的 Windows



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>若要維持與 x64 版 Windows 的相容性： <br/>
<ul>
<li>標題和標題安裝程式不得包含任何16位程式碼，或依賴任何16位元件。</li>
<li>如果遊戲相依于操作的核心模式驅動程式，則必須提供這些驅動程式的 x64 版本。 遊戲安裝程式必須偵測並安裝適用于64位版本 Windows 的適當驅動程式和元件。</li>
</ul>
<blockquote>
[!Note]<br />
64位版 Windows XP Professional 的支援是選擇性的。
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td>手動測試<br/>
<ol>
<li>在64位版本的 Windows 上執行遊戲。 確認遊戲安裝程式在 Windows Vista 或 Windows 7 的64位版本上正常執行。</li>
<li>確認遊戲未在64位版本的 Windows Vista 或 Windows 7 上執行16位可執行檔時遇到錯誤。 錯誤會在錯誤視窗中提及16位應用程式。</li>
<li>如果遊戲有原生的64位可執行檔，則也請使用它。</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="23-sign-files"></a>2.3 簽署檔案



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>所有可執行程式碼檔案 (例如，.exe 和 .dll 延伸模組) 必須使用 Authenticode 憑證進行簽署。 <br/> 如果您使用 Windows Installer，則必須簽署安裝程式 (.msi 檔案) 的封裝檔案。 <br/></td>
</tr>
<tr class="even">

<td>手動測試<br/>
<ol>
<li>流覽至遊戲目錄。</li>
<li>找出所有 .exe 和 .dll 檔案。</li>
<li>以滑鼠右鍵按一下每個檔案的 [屬性]。</li>
<li>確認遊戲可執行檔包含數位簽章。</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="24-sign-drivers"></a>2.4 簽署驅動程式



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>遊戲所安裝的任何核心模式驅動程式都必須使用公開有效的 Authenticode 憑證進行簽署。 <br/> 遊戲所安裝的任何核心模式硬體設備磁碟機都必須有透過 Windows 硬體品質實驗室 (WHQL) 或驅動程式可靠性簽章 (DRS) 程式取得的 Microsoft 簽名。 <br/></td>
</tr>
<tr class="even">

<td>手動測試<br/>
<ol>
<li>安裝遊戲。</li>
<li>確認遊戲安裝程式未顯示未簽署的驅動程式對話方塊 (s) 。</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="25-perform-version-checking-properly"></a>2.5 正確執行版本檢查



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>除非使用者授權合約禁止在未來的作業系統上使用，否則遊戲不能在未來的作業系統上執行，如 Windows 版本號碼的變更所述。 如果遊戲應該會失敗，就必須向使用者顯示訊息，以正常方式進行。</td>
</tr>
<tr class="even">

<td><dl> <dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>手動</dt> <dd>
<ol>
<li>在 windows XP、windows Vista 和 Windows 7 的32位版本，以及在64位版本的 Windows Vista 和 Windows 7 上安裝遊戲。</li>
<li>確認遊戲安裝程式未遇到關於 OS 版本的錯誤。</li>
</ol>
</dd> <dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>自動化測試</dt> <dd> 使用工具：應用程式驗證器<br/>
<ol>
<li>啟動應用程式驗證器。</li>
<li>選取 INSTALL.EXE 之後，請啟用 [相容性： HighVersionLie 測試]。</li>
<li>安裝遊戲，並確定不會根據作業系統版本封鎖安裝。</li>
<li>選取 GAME.EXE 之後，請啟用 [相容性： HighVersionLie 測試]。</li>
<li>執行遊戲，並確定它不會根據作業系統版本封鎖執行。</li>
</ol>
</dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="26-support-concurrent-user-sessions"></a>2.6 支援並行使用者會話



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>遊戲必須支援標準 Windows 多工案例。</td>
</tr>
<tr class="even">

<td>在 Windows Vista 或 Windows 7 中建立名為 Toby 的標準使用者帳戶。 啟動-> 主控台-> 新增或移除使用者帳戶-> 建立新帳戶 <br/>
<ol>
<li>以使用者 Jane 的形式啟動遊戲。</li>
<li>ALT + TAB 回到桌面上。</li>
<li>確認遊戲正確地將 ALT + Tab 切換至 Windows 桌面。</li>
<li>按一下 [開始-> [鎖定右邊的箭號]-> 切換使用者]。</li>
<li>以使用者 Toby 登入。</li>
<li>確認該遊戲在以使用者 Jane 的方式執行時，以使用者 Toby 的形式啟動。</li>
<li>確認在使用者切換程式期間，此遊戲不會遇到使用者 Toby 或使用者 Jane 的錯誤。</li>
<li>如果您可以啟動其他遊戲會話，請確認您無法從原始的遊戲會話聽到音訊。</li>
<li>關閉遊戲並切換回原始的使用者和遊戲。</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="27-support-long-names"></a>2.7 支援長名稱



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>如果遊戲支援儲存檔案，它必須能夠儲存具有完整名稱和路徑的檔案。 遊戲必須適當地處理特殊檔案系統字元，例如 \/： *？ &quot; 在用來建立檔案名或路徑的任何使用者輸入欄位中，< 或 >。</td>
</tr>
<tr class="even">

<td><ol>
<li>啟動遊戲。</li>
<li>開始新的遊戲。</li>
<li>儲存遊戲。 在儲存過程中，請使用 [儲存名稱：我的第一個儲存] 遊戲來確認遊戲是否儲存。</li>
<li>退出主功能表。</li>
<li>嘗試載入新儲存的遊戲。</li>
<li>確認在處理不受支援的檔案系統字元（例如 \/： *）時，此遊戲不會發生錯誤。 &quot; < 或 > 如果遊戲允許您，請為已儲存的遊戲命名。</li>
<li>如果允許使用者命名其設定檔及（或）字元或儲存遊戲，請在這裡使用長檔名時，確認遊戲不會發生錯誤。</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="3-installation"></a>3. 安裝

### <a name="31-easy-install"></a>3.1 簡易安裝



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>使用傳統安裝的遊戲必須在其安裝程式使用者介面中提供簡化的路徑。</td>
</tr>
<tr class="even">

<td><ol>
<li>插入遊戲光碟。</li>
<li>確認該遊戲未顯示 End-User 授權合約 (EULA) 。</li>
<li>如果遊戲支援自訂或 advanced 安裝選項，請確認此選項可在安裝過程中存取。</li>
<li>確認 [預設安裝] 選項會略過安裝程式的所有使用者輸入選項， (選取 [安裝資料夾]、[元件選取] 等) 。</li>
<li>確認遊戲安裝程式不會提示 OS 元件安裝 (DirectX 安裝程式、Visual C 執行時間等) 。</li>
<li>確認遊戲安裝程式未提示防火牆互動。</li>
<li>確認遊戲會自動執行，或在安裝程式結束時出現啟動器功能表。</li>
<li>確認遊戲卸載程式會移除所有已安裝、未轉散發的作業系統元件檔案，並清除所有設定。 不需要清除每一使用者的設定和資料 (例如儲存的遊戲) 。</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="32-support-user-account-control-for-installation"></a>3.2 支援安裝的使用者帳戶控制



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>遊戲安裝程式不能假設它是在與使用者相同的內容中執行。 因此，遊戲必須在第一次執行時，與安裝分開執行每個使用者的工作。</td>
</tr>
<tr class="even">

<td><ol>
<li>確認您可以將遊戲安裝為使用者 Jane。  (在安裝/安裝程式期間，這會需要更高的許可權。 ) </li>
<li>確認遊戲安裝程式會提示使用者 Jane 透過系統管理員認證來提升許可權。  (要提升的提示會在使用者嘗試安裝時出現。 ) </li>
<li>選擇在安裝結束時自動執行遊戲（如果尚未這麼做），或從出現的功能表中啟動。</li>
<li>一旦遊戲中，請建立新的設定檔，並玩遊戲並加以儲存。</li>
<li>離開遊戲。</li>
<li>重新開機遊戲，並確認使用者 Jane 帳戶可以存取使用者設定檔和儲存的遊戲。</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="33-install-to-correct-folders"></a>3.3 安裝到正確的資料夾



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>根據預設，遊戲必須安裝至 Program Files 資料夾。 使用者資料必須在第一次執行時寫入，而不是在安裝期間寫入。</td>
</tr>
<tr class="even">

<td><ol>
<li>使用預設的安裝類型來安裝遊戲。</li>
<li>確認已將遊戲安裝至 Program Files。</li>
</ol>
<blockquote>
[!Note]<br />
如果此測試失敗，請確認該遊戲是否適用于所有使用者的安裝。 如果是，就會發生失敗。
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="34-install-windows-resources-properly"></a>3.4 正確安裝 Windows 資源



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>應用程式不能嘗試安裝受 Windows 資源保護 (WRP) 保護的檔案或登錄機碼。</td>
</tr>
<tr class="even">

<td><ul>
<li>確認安裝程式期間沒有出現任何 Windows 資源保護 WRP] 對話方塊。</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="35-avoid-reboots-during-installation"></a>3.5 避免在安裝期間重新開機



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>遊戲安裝程式不應假設重新發佈套件的 Windows 元件安裝需要重新開機，除非重新開機是由傳回結果或 Microsoft 檔所表示。</td>
</tr>
<tr class="even">

<td><ol>
<li>安裝遊戲。</li>
<li>確認遊戲不需要在安裝後重新開機系統。</li>
</ol>
<blockquote>
[!Note]<br />
如果 Microsoft 系統更新可轉散發套件需要重新開機，請執行下列動作：完成遊戲安裝、卸載遊戲，然後再次安裝遊戲。 在第二次安裝時，遊戲安裝程式不需要重新開機。
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="36-use-file-versioning-correctly"></a>3.6 使用正確的檔案版本控制



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>遊戲安裝程式必須正確檢查，以確定已安裝最新的檔案版本。 安裝遊戲絕不能回歸您不會產生的任何檔案，或是由您未產生的應用程式所共用的檔案。</td>
</tr>
<tr class="even">

<td><ol>
<li>在安裝遊戲之前，請先建立 System32 的預先安裝快照集。<br/>
<ol>
<li>建立名為 G4Wtest 的目錄。</li>
<li>啟動命令視窗， (啟動-> 執行-> cmd) 。</li>
<li>流覽至 c:\windows\system32。</li>
<li>輸入 dir/o：-g/o：-d >> c:\G4Wtest\pregame.txt。</li>
</ol></li>
<li>建立 System32 的後置安裝快照集。 <br/>
<ol>
<li>啟動命令視窗， (啟動-> 執行-> cmd) 。</li>
<li>流覽至 c:\windows\system32。</li>
<li>輸入 dir/o：-g/o：-d >> c:\G4Wtest\postgame.txt。</li>
<li>確認遊戲未回歸任何檔案版本的遊戲未產生的檔案 ( .。。在兩份檔中列出的檔案，其方式是比較 pregame.txt 與 postgame.txt) 。</li>
</ol></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="37-support-autorun-conditional-requirement"></a>3.7 支援自動運行 \[ 條件需求\]



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>針對在 CD、DVD 或其他支援自動執行的卸載式媒體上散佈的遊戲，當光碟第一次插入時，應用程式必須自動執行或提示使用者安裝遊戲。 <br/>
<blockquote>
[!Note]<br />
為了在 windows Vista 之前的 Windows 版本上使用而撰寫的自動執行程式，不應該使用 .NET 執行時間，因為這項技術並不包含在 Windows XP 或舊版的 Windows 中。
</blockquote>
<br/> 如需進一步指引，請參閱 <a href="/windows/win32/DxTechArts/games-for-windows-technical-requirements-1-1-0006">Windows 技術需求</a> 3.7 的遊戲，支援自動執行時間。 <br/></td>
</tr>
<tr class="even">

<td><ol>
<li>插入遊戲光碟或媒體。</li>
<li>確認 [安裝/執行] 對話方塊已自動啟動。</li>
<li>Windows Vista 或 Windows 7：確認遊戲自動執行程式本身不會提示使用者 Jane 透過系統管理員認證來提升許可權。</li>
<li>確認自動執行的可執行檔不需要現成可轉散發元件，例如 .NET 3.5、C Run-Time 程式庫等等。</li>
<li>請確認在安裝後重新插入磁片磁碟機中的光碟，不會再次自動開始安裝。</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="4-reliability"></a>4. 可靠性

### <a name="41-eliminate-unnecessary-reboots"></a>4.1 消除不必要的重新開機



| OS                                              | 需求                                                                                                                                                                   |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows 7<br/> Windows Vista<br/> | 所有應用程式安裝程式都必須利用重新開機管理員 Api 來避免系統重新開機 (請參閱 [需求 3.5](#35-avoid-reboots-during-installation)) 。 |



 

### <a name="42-eliminate-application-verifier-failures"></a>4.2 消除應用程式驗證器失敗



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>在下列測試中，遊戲必須不會在 Microsoft 應用程式驗證器 (AppVerifier) 4.0 版或更新版本下產生任何失敗： <br/>
<ul>
<li>基本概念：控制碼、堆積、鎖定、記憶體、TLS</li>
<li>其他： DangerousAPIs、DirtyStacks</li>
</ul></td>
</tr>
<tr class="even">

<td>使用工具： AppVerifier 4.0 (或更新版本) <br/>
<ol>
<li>安裝 AppVerifier。</li>
<li>啟動 AppVerifier，然後選取 [檔案-> 新增應用程式]。</li>
<li>找出遊戲可執行檔，選取它，然後按一下 [ &quot; 開啟] &quot; 按鈕。</li>
<li>在 [ &quot; 應用程式] &quot; 區段中，選取 [遊戲可執行檔]。</li>
<li>在 [ &quot; 測試] &quot; 區段中，選取 [分類基本和其他] 底下列出的測試 (取消核取 [ &quot; ThreadPool] 和 [TimeRollOver] &quot; &quot; &quot;) ，並確定未選取所有其他測試。</li>
<li>啟動遊戲。</li>
<li>確認遊戲在應用程式驗證器下執行時，不會產生失敗。</li>
</ol>
<blockquote>
[!Note]<br />
有些測試需要完整執行偵錯工具。 這可能需要不受保護的遊戲可執行檔版本，因為反盜版/反盜版技術可能會干擾 AppVerifer。
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="43-support-windows-error-reporting"></a>4.3 支援 Windows 錯誤報告



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>遊戲必須只處理已知和預期的例外狀況，Windows 錯誤報告不得停用。 如果將錯誤 (（例如存取違規) ）插入遊戲中，則必須允許 Windows 錯誤報告報告損毀。</td>
</tr>
<tr class="even">

<td>使用工具：執行緒劫匪 <br/>
<ul>
<li>如果應用程式在測試時當機，請確認該遊戲已正確顯示 Windows 錯誤報告，並收集損毀資料。</li>
</ul></td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>所有可執行檔 (例如，.exe 或 .dll 檔案) 必須包含正確的產品名稱、公司名稱和檔案版本。</td>
</tr>
<tr class="even">

<td><dl> <dt><span id="Manual_test_"></span><span id="manual_test_"></span><span id="MANUAL_TEST_"></span>手動測試：</dt> <dd>
<ol>
<li>在安裝媒體上，以滑鼠右鍵按一下遊戲的可執行檔 (s) ，然後安裝在電腦硬碟上。</li>
<li>選取 [屬性]。</li>
<li>Windows XP：按一下 [ <strong>版本</strong> ] 索引標籤。確認已正確填入 [產品名稱]、[公司名稱] 和 [檔案版本] 欄位。</li>
<li>Windows Vista 或 Windows 7：按一下 [ <strong>詳細資料</strong> ] 索引標籤。確認 [產品名稱] 和 [檔案版本] 欄位已正確填入。 在 Windows Vista 或 Windows 7 的 [屬性] 頁面中看不到公司名稱。</li>
</ol>
</dd> <dt><span id="Automated_test_"></span><span id="automated_test_"></span><span id="AUTOMATED_TEST_"></span>自動化測試：</dt> <dd>
<ul>
<li>使用 Microsoft 遊戲進行 Windows 測試控管;請參閱 <a href="#64-microsoft-games-for-windows-test-tool">第6.4 節</a>。</li>
</ul>
</dd> </dl></td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>正常結束遊戲時，不能造成不明的例外狀況錯誤。</td>
</tr>
<tr class="even">

<td><ul>
<li>播放正常遊戲會話的遊戲之後，請確認遊戲未在結束時產生錯誤。</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="5-sample-test-script"></a>5. 範例測試腳本

這是使用上述測試需求作為指南的一般測試階段範例。

### <a name="51-tools"></a>5.1 工具

-   Windows Vista SP1 和（或） Windows 7 在 AMD CPU 上的32位版本
-   Intel CPU 上的 Windows Vista SP1 和（或） Windows 7 的32位版本
-   Windows Vista SP1 和（或） Windows 7 在 AMD CPU 上的64位版本
-   Intel CPU 上的 Windows Vista SP1 和（或） Windows 7 的64位版本
-   AMD CPU 上的32位 edition Windows XP SP2
-   Intel CPU 上的32位版 Windows XP SP2
-   支援 1680 1050 的全螢幕監視器
-   適用于 Windows 的 Xbox 360 控制器

### <a name="52-pre-install"></a>5.2 預先安裝

1.  Windows Vista 和 Windows 7：建立兩位標準使用者： Jane 和 Toby
2.  Windows Vista 和 Windows 7：確定已啟用使用者帳戶控制
3.  建立 System32 的預先安裝快照集

    1.  建立名為 G4Wtest 的目錄
    2.  顯示命令視窗 (啟動-> 執行-> cmd) 
    3.  流覽至 c： \\ windows \\ system32
    4.  輸入 dir/o：-g/o：-d >> c： \\ G4Wtest \\pregame.txt

4.  Windows Vista 和 Windows 7：設定為 150% DPI \[ 1。8\]
5.  繼續 [安裝](#3-installation)

### <a name="53-install"></a>5.3 安裝

1.  以使用者 Jane 登入
2.  將遊戲光碟插入 CD/DVD 光碟機中，確認 [安裝/執行] 對話方塊自動出現 \[ 3。7\]
3.  確認遊戲安裝程式會提示使用者 Jane 提升系統管理員認證 \[ 3。2\]
4.  確認遊戲自動執行程式本身不會提示使用者 Jane 透過系統管理員認證3.7 進行提升 \[\]
5.  確認遊戲未顯示超過一份 End-User 授權合約 (EULA) \[ 3。1\]
6.  確認遊戲顯示預設/簡單和自訂/Advanced 安裝選項 \[ 3。1\]
7.  確認 [預設/簡單安裝] 選項會略過安裝程式的所有使用者輸入選項， (選取 [安裝資料夾]、[元件選取] 等等。 ) \[ 3。1\]
8.  確認遊戲安裝程式不會提示 OS 元件安裝 (DirectX 安裝程式、C Run-Time 程式庫等等。 ) \[ 3。1\]
9.  確認遊戲安裝程式未提示防火牆互動 \[ 3。1\]
10. 確認遊戲安裝程式未遇到關於 OS 版本 \[ 2.5 \] \[ 4.2 的錯誤\]
11. 確認遊戲安裝程式未顯示未簽署的驅動程式對話方塊 (s) \[ 2。4\]
12. 確認未在安裝程式期間出現任何 Windows 資源保護 (WRP) 對話方塊： \[ 3。4\]
13. 確認在安裝後將光碟重新插入磁片磁碟機，不會再次自動開始安裝
14. 確認遊戲不需要在安裝3.5 後重新開機系統 \[\]
15. 確認您可以將遊戲安裝為使用者 Jane \[ 3。2\]
16. 確認遊戲會自動執行，或在安裝程式結束時出現啟動器功能表 \[ 3。1\]
17. 如果遊戲在安裝後自動執行，請跳至[運行](#55-runtime)時間
18. 如果遊戲離開啟動功能表，或無法卸載，請參閱[安裝後](#54-post-install)的章節

### <a name="54-post-install"></a>5.4 安裝後

1.  確認遊戲未在使用者桌面1.1 上放置啟動快捷方式 \[\]
2.  確認遊戲未在 [開始] 功能表1.1 中放置啟動快捷方式 \[\]
3.  確認遊戲圖示顯示在 Windows 遊戲瀏覽器 \[ 1.1 中\]
4.  確認底部的 [發行者]、[開發人員]、[內容類型]、[發行日期]、[版本])  (的中繼資料，以及是否正確 \[ 1。1\]
5.  確認遊戲圖示顯示 Windows 體驗指數 (Windows 遊戲瀏覽器1.1 中) 資訊的 \[\]
6.  確認適用于中繼資料的遊戲超連結在 Windows 遊戲瀏覽器1.1 中正確運作 \[\]
7.  確認該遊戲在 Windows 遊戲瀏覽器1.1 中顯示精確的家長監護控制項分級 \[\]
8.  建立 System32 的後置安裝快照集

    1.  顯示命令視窗 (啟動-> 執行-> cmd) 
    2.  流覽至 c： \\ windows \\ system32
    3.  輸入 dir/o：-g/o：-d >> c： \\ G4Wtest \\postgame.txt
    4.  藉由比較 pregame.txt 與 postgame.txt 3.6，確認遊戲未回歸兩份檔中所列檔案的任何檔案版本 \[\]

9.  繼續進行[運行](#55-runtime)時間

### <a name="55-runtime"></a>5.5 執行時間

1.  執行時間1：如果出現 [啟動] 功能表，請從該處啟動遊戲。 如果在安裝後自動執行遊戲或從遊戲啟動器功能表啟動，請執行下列動作：如果沒有，請跳至執行時間2：

    1.  如果遊戲允許， (建立設定檔) 
    2.  開始新的遊戲
    3.  儲存遊戲
    4.  離開遊戲
    5.  從遊戲瀏覽器啟動遊戲
    6.  確認遊戲從遊戲瀏覽器圖示 \[ 1.2 啟動\]
    7.  確認遊戲不會在啟動1.2 時提示輸入系統管理員認證 \[\]
    8.  確認使用者 Jane 帳戶3.2 可存取使用者設定檔和儲存遊戲 \[\]
    9.  繼續執行執行時間3

2.  執行時間2：如果遊戲未從遊戲啟動器功能表自動執行或顯示啟動，這會是3.1 的失敗 \[ \] ; 不過，測試可以正常地繼續：

    1.  從遊戲瀏覽器啟動遊戲
    2.  確認遊戲從遊戲瀏覽器圖示 \[ 1.2 啟動\]
    3.  確認遊戲不會在啟動1.2 時提示輸入系統管理員認證 \[\]
    4.  繼續執行執行時間3

3.  執行時間3：如果遊戲支援遊戲台，請確認遊戲可將 Windows Xbox 360 控制器辨識為輸入裝置 \[ 1。4\]

    1.  如有需要，請透過 [選項] 功能表啟用控制器
    2.  使用 Xbox 360 名稱確認遊戲參考控制器按鈕和觸發程式
    3.  確認遊戲和功能表系統可控制適用于 Windows 的 Xbox 360 控制器
    4.  確認適用于 Windows 的 Xbox 360 控制器根據接受的標準運作

4.  將影片設定為 \[ 1.5 \] ：

    1.  確認遊戲以4:3 的外觀比例解析度執行 (800 600 或 1024 768) 
    2.  確認遊戲以16:9 的外觀比例解析度執行 (1280 720) 
    3.  確認遊戲以16:10 的外觀比例解析度（ (1680 1050、800 480 或 1152 720）執行) 
    4.  確認當解決問題時，遊戲提示使用者
    5.  如果您未在15秒內接受，請確認顯示器會還原為先前的設定
    6.  確認遊戲不會延展圖片，而是會顯示更廣大的視圖區域
    7.  確認遊戲未在遊戲播放區域的左邊和右邊新增黑色橫條

5.  如果影片設定中有提供，請確認遊戲轉譯選項預設為 Direct3D \[ 1.7 \] ; 否則，請繼續進行 [自動化測試](#58-automated-tests)
6.  如果出現提示或選項可供使用，請建立使用者設定檔。 確認在使用長檔名時，遊戲不會遇到錯誤 \[ 2。7\]
7.  開始新的遊戲、建立遊戲儲存，並確認在處理不支援的檔案系統字元時，遊戲不會遇到錯誤 \[ 2。7\]
8.  確認遊戲正確地將 ALT + Tab 切換至 Windows 桌面 \[ 2。6\]

    1.  按一下 [開始-> 切換使用者]，切換執行遊戲的使用者
    2.  以 Toby 登入
    3.  確認在以使用者 Jane 2.6 的形式執行時，遊戲以使用者 Toby 的形式啟動 \[\]
    4.  確認在使用者切換程式期間，此遊戲不會遇到使用者 Toby 或使用者 Jane 的錯誤 \[ 2。6\]
    5.  確認您無法聽到原始遊戲會話2.6 的音訊 \[\]
    6.  離開遊戲
    7.  登出 Toby
    8.  切換回正在執行遊戲的原始使用者
    9.  ALT + TAB 回到遊戲中

9.  離開遊戲
10. 繼續進行[後置運行](#56-post-runtime)時間

### <a name="56-post-runtime"></a>5.6 後置執行時間

1.  確認遊戲未在結束4.3 時產生錯誤 \[\]
2.  確認已將遊戲安裝至 Program Files \[ 3。3\]
3.  繼續進行[家長](/windows)監護

### <a name="57-parental-controls"></a>5.7 家長監護

1.  在主控台中開啟家長監護
2.  確認該遊戲在家長監護的遊戲標題下方顯示精確的家長監護，主控台 \[ 1。2\]
3.  請參閱測試案例 \[ 1.2 \] 以進行下列測試：

    1.  將家長監護設定為 [開啟] 之後，請確認遊戲以使用者 Jane 1.2 的這些設定執行。 \[\]
    2.  登出並以 Toby 登入
    3.  確認遊戲以這些設定作為使用者 Toby 1.2 來執行 \[\]
    4.  登出並以 Jane 登入
    5.  在 [家長監護] 區段中，封鎖使用者 Toby 從您剛剛安裝的遊戲中，讓使用者看得到一個 ESRB 等級以上的遊戲

        範例：如果遊戲的分級為 E，請設定它，讓 Toby 只能播放評為 C 的遊戲

    6.  確認遊戲以使用者 Jane 1.2 的這些設定執行 \[\]
    7.  登出並以使用者 Toby 登入
    8.  當使用者 Jane 1.2 封鎖 ESRB 時，確認遊戲未在使用者 Toby 上啟動 \[\]
    9.  以使用者 Jane 的形式登出使用者 Toby 及重新登入
    10. 如果之前有變更，請還原 ESRB 設定
    11. 如果沒有任何 ESRB 設定，請選取 [封鎖或允許特定遊戲]，然後依名稱選取遊戲。
    12. 以 Jane 的形式登出，並以 Toby
    13. 確認使用者 Jane 1.2 封鎖了 EXE/名稱時，該遊戲未在使用者 Toby 上啟動 \[\]
    14. 以 Jane 的形式登出 Toby 和上一頁
    15. 像 Jane 一樣，開啟使用者控制項-> 應用程式限制
    16. 按一下 [Toby 只能使用我允許的程式]，然後按一下 [確定] (即 [不允許 exe]) 
    17. 按一下 [全選] 方塊，然後按一下 [確定]。
    18. 前往使用者控制項 \| 遊戲控制，並允許使用 ESRB 分級的特定遊戲
    19. 以 Jane 的身份登入，並以 Toby 登入，然後嘗試播放遊戲
    20. 確認遊戲未被封鎖，而且 Toby 可以在 [允許沒有 exe] 設定為1.2 時播放 \[\]
    21. 以使用者 Jane 的形式登出使用者 Toby 及重新登入
    22. 移至主控台中的 [家長監護]，並移除限制
    23. 確認這兩個使用者現在都可以玩遊戲

4.  繼續進行 [自動化測試](#58-automated-tests)

### <a name="58-automated-tests"></a>5.8 自動化測試

1.  確認在應用程式驗證器下執行時，遊戲未產生失敗-請參閱商標測試控管檔 \[ 4。2\]
2.  確認遊戲可執行檔包含資訊清單-請參閱商標測試控管檔 \[ 2。1\]
3.  確認遊戲可執行檔資訊清單並無 requestedexecutionlevel 為 "AsInvoker"-請參閱商標測試控管檔 \[ 2。1\]
4.  繼續進行 [其他測試](#59-other-tests)

### <a name="59-other-tests"></a>5.9 其他測試

1.  確認遊戲可執行檔包含數位簽章 \[ 2。3\]
2.  確認遊戲安裝程式在 Windows Vista 及/或 Windows 7 2.3 的64位版本上正常執行 \[\]
3.  在 Windows Vista 及/或 Windows 7 2.3 的64位版本上執行16位可執行檔時，請確認該遊戲未遇到錯誤 \[\]
4.  在測試時強制應用程式損毀，並確認遊戲顯示 Windows 錯誤報告正確，並收集損毀資料 \[ 4。3\]
5.  確定正確的檔案摘要 \[ 4。3\]

    1.  按一下 [開始-> 電腦]
    2.  流覽至遊戲目錄
    3.  在 [搜尋] 視窗中，輸入 \*.dll
    4.  針對每個檔案：以滑鼠右鍵按一下檔案，然後按一下 [屬性]

        -   在 Windows XP 中：按一下 [版本] 索引標籤。確認已正確填入 [產品名稱]、[公司名稱] 和 [檔案版本] 欄位。 \[4.3\]
        -   在 Windows Vista 和 Windows 7 中：按一下 [詳細資料] 索引標籤。確認 [產品名稱] 和 [檔案版本] 欄位已正確填入。 在 Windows Vista 或 Windows 7 屬性頁面4.3 中看不到公司名稱 \[\]

    5.  針對 .exe 檔案重複此檢查

6.  啟動遊戲。

    1.  按 CTRL + ALT + DEL
    2.  按一下 [關機選項] 箭號
    3.  按一下 [重新開機]
    4.  驗證遊戲不會封鎖關機 \[ 3。1\]

7.  繼續 [卸載](#510-uninstall)

### <a name="510-uninstall"></a>5.10 卸載

-   確認遊戲卸載程式會移除所有已安裝、未轉散發的作業系統元件檔案，並清除所有設定 \[ 3。1\]

    -   在 Windows Vista 或 Windows 7 中確認主控台是移除程式1.1 的唯一方法 \[\]

## <a name="test-tool-notes"></a>測試控管注意事項

這些是上述測試需求中所列的每個測試控管的附注。

### <a name="61-appverifier-40-or-higher"></a>6.1 Appverifier 4.0 (或更新版本) 

**測試案例：2.5、4。2**

> [!Note]  
> 有些應用程式無法執行，因為禁止複製的 AppVerifier 正在執行中。 您可以使用遊戲可執行檔的未受保護髮行版來執行，以解決此問題。

 

1.  在執行 Windows XP 的電腦上安裝 AppVerifier 4.0 (或更高版本) 
2.  啟動 AppVerifier，然後按一下 [檔案-> 新增應用程式]
3.  找出遊戲可執行檔、選取它，然後按一下 [開啟]。
4.  在 [應用程式] 區段中，選取 [遊戲可執行檔]
5.  在 [基本概念] 區段中，選取下列測試：

    -   處理
    -   堆積
    -   鎖定
    -   記憶體
    -   TLS

6.  在 [其他] 區段中，選取下列測試：

    -   DangerousAPIs
    -   DirtyStacks

7.  確定未選取所有其他測試
8.  啟動遊戲
9.  玩遊戲
10. 關閉遊戲
11. 在 AppVerifier 中選取 View-> 記錄
12. 在 [應用程式] 區段中，選取應用程式 .exe 檔
13. 在 [記錄檔] 區段中，選取記錄檔並觀察錯誤計數。 如果沒有任何錯誤，請結束 AppVerifier 測試。 如果發生錯誤，請按一下 [流覽] 按鈕
14. 搜尋檔 (CTRL + F) 嚴重性 = "錯誤
15. 根據失敗的 LayerName = 部分建立 bug

### <a name="62-manifest-test---mtexe"></a>6.2 資訊清單測試-mt.exe

**測試案例：1.8、2。1**

此工具是從 MT.exe 所在的命令提示字元執行。

範例：

``` syntax
mt.exe -inputresource:"c:\yourdir\YourGame.exe";#1 -out:yourgame.manifest
```

1.  按一下 [開始-> 執行-> 輸入 cmd，然後按一下 [確定] 按鈕
2.  執行 mt.exe 工具，為隨遊戲安裝的每個 .exe 檔案產生資訊清單檔
3.  開啟產生的資訊清單檔案
4.  確定每個 .exe 檔案都包含下列所要求的 (：

    ``` syntax
    <description>Example Game Name</description>
    <trustInfo xmlns="urn:schemas-microsoft-com:asm.v2">
      <security>
        <requestedPrivileges>
          <requestedExecutionLevel level="asInvoker"></requestedExecutionLevel>
        </requestedPrivileges>
      </security>
    </trustInfo>
      <asmv3:windowsSettings xmlns=http://schemas.microsoft.com/SMI/2005/WindowsSettings>
        <dpiAware>true<dpiAware>
      </asmv3:windowsSettings>
    </asmv3:application>
    ```

> [!Note]  
> 每個檔案都應該要有要求的執行層級，而且至少要有遊戲的可執行檔的 DPIAware。

 

### <a name="63-thread-hijacker---threadhijackerexe"></a>6.3 執行緒劫匪-threadhijacker.exe

此工具是從 threadhijacker.exe 所在的命令提示字元執行。

範例：

``` syntax
threadhijacker.exe /process:str
```

其中 str 是program.exe 的 \_ 名稱 \_

1.  顯示工作管理員，按一下 [處理常式] 索引標籤，然後找出遊戲可執行檔的名稱。
2.  以系統管理員模式開啟命令提示字元
3.  流覽至 threadhijacker.exe 所在的目錄
4.  Type： **threadhijacker.exe/process：** str，其中 str 是您想要叫用之可執行檔的名稱

### <a name="64-microsoft-games-for-windows-test-tool"></a>6.4 Windows 測試控管的 Microsoft 遊戲

此工具位於 DirectX SDK 中。 一旦 SDK 安裝在電腦上，就可以將 Windows 測試控管的安裝程式放置在測試電腦上，然後安裝。

在安裝 DirectX SDK 的開發電腦上，找出適用于 Windows Test Tool 安裝程式的 Microsoft 遊戲。 依預設，它位於下列位置：

``` syntax
%SystemDrive%\Program Files (x86)\Microsoft DirectX SDK (Date)\Utilities\bin\x86\Microsoft Games for Windows Test Tools\
```

1.  將安裝程式 (MicrosoftGFWTestTool.msi/setup.exe) 複製到測試電腦。
2.  執行安裝程式。
3.  啟動 Windows 測試控管的 Microsoft 遊戲。
4.  在 [ **專案清單** ] 欄位中，將 [ **建立新專案** ] 取代為您的標題名稱， **然後按一下 [新建]**。

    等候基準完成。

5.  在 [ **遊戲資訊** ] 區段中填寫任何您可能擁有的資訊，然後按一下 [ **更新遊戲資訊**]。
6.  按一下 [ **測試案例** ] 索引標籤。
7.  從頂端開始，繼續進行測試案例，適當地按一下 [ **通過** ] 或 [ **失敗** ]。

    如需有關在報表中包含錯誤的詳細資訊，請參閱本節稍後的「撰寫 Bug」。

8.  核取 [**報表**] 和 [ **Bug 編輯**] 索引標籤，以在查看報表 (之後返回 [**專案**] 索引標籤) 。
9.  按一下 [ **編譯報告**]。

    當報表完成編譯時，就會開啟一個視窗。 您會在這裡找到 .ZIP *的檔案名report.zip 的名稱* \_ 。 此檔案包含在測試階段期間收集的所有記錄和結果。

### <a name="writing-a-bug"></a>撰寫 Bug

有兩種方式可以撰寫 bug 報告：您可以完成測試案例，然後按一下 [當標題無法測試案例時 **失敗** ]，或者按一下 [ **bug 編輯** ] 索引標籤並手動加入 bug 報表。

### <a name="clicking-fail-on-a-test-case"></a>在測試案例上按一下 [失敗]

1.  當您按一下測試案例的 [ **失敗** ] 時，[ **問題類型** ] 下拉式清單會自動設定為測試案例類型。
2.  將簡短描述新增至簡要描述問題的 [ **標題** ] 欄位。
3.  將問題的詳細描述新增至 [觀察到的 **行為** ] 欄位。
4.  視需要新增預期的 (，而不是 [ **預期行為** ] 欄位) 問題的描述。
5.  新增如何重現問題至 **重現步驟** 欄位的詳細描述。
6.  完成時，按一下 [ **儲存** ] 按鈕。

### <a name="manually-adding-a-bug"></a>手動新增 Bug

此程式與按一下 [ **失敗**] 相同，但自動填入的下拉式清單除外。 在此情況下，請選取適當的 TCR 失敗類型，或針對落在 TR 範圍之外但仍應回報的 bug 選取 **\* \* 非 TR 問題 \* \*** 。

## <a name="resources"></a>資源

<dl> <dt>

<span id="Games_for_Windows__Technical_Requirements"></span><span id="games_for_windows__technical_requirements"></span><span id="GAMES_FOR_WINDOWS__TECHNICAL_REQUIREMENTS"></span>適用于 Windows 的遊戲：技術需求
</dt> <dd>

[Windows 技術需求的遊戲： Windows XP、Windows Vista 和 Windows 7 遊戲的最佳作法](./games-for-windows-technical-requirements-1-1-0006.md)

</dd> <dt>

<span id="Windows_SDK"></span><span id="windows_sdk"></span><span id="WINDOWS_SDK"></span>Windows SDK
</dt> <dd>

[Windows Sdk](https://msdn.microsoft.com/bb980924.aspx)

</dd> <dt>

<span id="User_Account_Control_Guidelines"></span><span id="user_account_control_guidelines"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES"></span>使用者帳戶控制指導方針
</dt> <dd>

[使用者帳戶控制相容性的 Windows Vista 應用程式開發需求](/previous-versions/dotnet/articles/bb530410(v=msdn.10))

</dd> <dt>

<span id="Windows_Installer_Information"></span><span id="windows_installer_information"></span><span id="WINDOWS_INSTALLER_INFORMATION"></span>Windows Installer 資訊
</dt> <dd>

[Windows Installer](../msi/windows-installer-portal.md)

</dd> <dt>

<span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>WinQual 開發人員入口網站 
</dt> <dd>

[Windows Quality Online Services (Winqual) ](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)

</dd> <dt>

<span id="DirectX_Developer_Portal"></span><span id="directx_developer_portal"></span><span id="DIRECTX_DEVELOPER_PORTAL"></span>DirectX 開發人員入口網站
</dt> <dd>

[DirectX 開發人員中心](/previous-versions/windows/apps/hh452744(v=win.10))

</dd> <dt>

<span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Windows 和 DirectX SDK Blog 的遊戲
</dt> <dd>

[適用於 Windows 與 DirectX SDK 的遊戲](https://walbourn.github.io/)

</dd> <dt>

<span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>其他 DirectX 文章
</dt> <dd>

[DirectX 技術文章](./dx9-technical-articles.md)

</dd> </dl>

 

