---
description: 本主題定義使用 NLS 功能時的重要詞彙。
ms.assetid: daf929b2-8ff9-4a17-b294-f2c0eaef5848
title: NLS 術語
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a86808d31cb034e7ad29e4580b8f201ad3c9a6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695427"
---
# <a name="nls-terminology"></a>NLS 術語

本主題定義使用 NLS 功能時的重要詞彙。

## <a name="locale-and-language-terms"></a>地區設定和語言詞彙

下表摘要說明地區設定和語言詞彙。 另請參閱 [地區設定和語言](locales-and-languages.md)。



|                          | 語言群組                                                                                                                                                                                                                                                                   | 非 Unicode 程式的語言                                                                                                                                                                                                                | 標準及格式                                                                                                                                                                                                                   |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **目的**              | 提供所有鍵盤配置、輸入法編輯器 (Ime) 、TrueType 字型、字型連結、授權套件檔案 (LPKs) 、點陣圖字型，以及作業系統針對一組語言所需的字碼頁轉譯資料表。 因此會影響這份清單中的所有其他設定。 | 決定作業系統的預設點陣圖字型和 OEM、ANSI 和 Macintosh 字碼頁。 這種語言只會影響非完整 Unicode 的應用程式。 在 Windows XP 之前，這種語言稱為「系統地區設定」。 | 決定將日期、時間、貨幣和數位格式化為每個使用者預設值的設定。 也決定排序文字的排序次序。 在 Windows XP 之前，標準及格式稱為「使用者地區設定」。 |
| **第一個設定**            | 安裝                                                                                                                                                                                                                                                                     | 安裝                                                                                                                                                                                                                                     | 安裝                                                                                                                                                                                                                            |
| **使用者可以如何變更** |  (主控台專案) 的地區選項<br/> **WINDOWS XP：** 地區及語言選項<br/> 僅 (系統管理員) <br/>                                                                                                                                       |  (主控台專案) 的地區選項<br/> **WINDOWS XP：** 地區及語言選項<br/> 僅 (系統管理員) <br/>                                                                                                       |  (主控台專案) 的地區選項<br/> **WINDOWS XP：** 地區及語言選項<br/>                                                                                                                               |
| **預設值**              | 需要西歐和美國及語言群組，才能顯示當地語系化版本的語言。                                                                                                                                                                         | 當地語系化版本的語言。                                                                                                                                                                                                                   | 當地語系化作業系統的語言。                                                                                                                                                                                                 |
| **Function**             | [**EnumSystemLanguageGroups**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlanguagegroupsa)                                                                                                                                                                                                                     | [**GetSystemDefaultLangID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlangid)                                                                                                                                                                                         | [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid)、 [ **GetUserDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename)                                                                                                                          |



 



|                          | 執行緒地區設定                                                                                                                                                 | 輸入語言                                                                                            | 系統預設 UI 語言                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **目的**              | 決定用於為執行緒格式化日期、時間、貨幣和大量數位的設定。 也決定排序文字的排序次序。 | 由語言和輸入的方法所組成。                                                             | 決定功能表和對話方塊、訊息、安裝程式資訊 (INF) 檔和說明檔的預設語言。<br/> **Windows Vista 和更新版本：** 所謂的安裝語言。 扮演較有限的角色，大部分都是由系統慣用的 UI 語言所取代。<br/> 如需詳細資訊，請參閱 [消費者介面語言管理](user-interface-language-management.md)<br/> |
| **第一個設定**            | 預設為標準及格式                                                                                                                              | 安裝                                                                                              | 安裝                                                                                                                                                                                                                                                                                                                                                                                   |
| **使用者可以如何變更** | [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)                                                                                                                    |  (主控台專案) 的地區選項<br/> **WINDOWS XP：** 地區及語言選項<br/> | No                                                                                                                                                                                                                                                                                                                                                                                             |
| **預設值**              | 標準及格式                                                                                                                                         | 具有預設輸入方法之當地語系化版本的語言。                                                  | 當地語系化版本的語言。                                                                                                                                                                                                                                                                                                                                                                 |
| **Function**             | [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale)                                                                                                                    | [**GetKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout)                                                     | [**GetSystemDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultuilanguage)                                                                                                                                                                                                                                                                                                                               |



 



|                          | 系統 UI 語言，系統慣用 UI 語言                                                                                                                                                                  | 使用者 UI 語言，使用者慣用 UI 語言                                                                                                                                               | 執行緒慣用 UI 語言                                                                                                                                                                 |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **目的**              | 判斷作業系統的功能表和對話、訊息、INF 檔案和說明檔的語言。 如需詳細資訊，請參閱 [消費者介面語言管理](user-interface-language-management.md)。 | 判斷使用者的功能表和對話、訊息和說明檔的語言。 如需詳細資訊，請參閱 [消費者介面語言管理](user-interface-language-management.md)。 | **Windows Vista 和更新版本：** 指定應用程式執行緒的慣用語言。 如需詳細資訊，請參閱 [消費者介面語言管理](user-interface-language-management.md)。 |
| **第一個設定**            | 預設值為 Null                                                                                                                                                                                                    | 預設值為 Null                                                                                                                                                                             | 預設值為 Null                                                                                                                                                                               |
| **使用者可以如何變更** | 地區及語言選項<br/> 僅 (系統管理員) <br/>                                                                                                                                          |  (主控台專案) 的地區選項<br/> **WINDOWS XP：** 地區及語言選項<br/>                                                                                   | [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)                                                                                                                        |
| **預設值**              | **Windows Vista 和更新版本：** 當地語系化版本的語言，後面接著任何回退。                                                                                                                             | **在 Windows Vista 之前：** 當地語系化版本的語言。<br/> **Windows Vista 和更新版本：** 當地語系化版本的語言，後面接著任何回退。<br/>                     | Null 清單                                                                                                                                                                                     |
| **Function**             | [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages)                                                                                                                                             | [**GetUserDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultuilanguage)、 [ **GetUserPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages)                                                            | [**GetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getthreadpreferreduilanguages)                                                                                                                        |



 



|                          | 處理慣用 UI 語言                                                                                                                                                                 |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **目的**              | **Windows 7 和更新版本：** 判斷應用程式處理的慣用語言。 如需詳細資訊，請參閱 [消費者介面語言管理](user-interface-language-management.md)。 |
| **第一個設定**            | 預設值為 Null                                                                                                                                                                                |
| **使用者可以如何變更** | 地區及語言選項只 (系統管理員)                                                                                                                                             |
| **預設值**              | **Windows 7 和更新版本：** 當地語系化版本的語言，後面接著任何回退。                                                                                                             |
| **Function**             | [**GetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getprocesspreferreduilanguages)、 [ **SetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages)                                             |



 

## <a name="code-page"></a>字碼頁

256程式碼點字碼頁無法支援在單一文字中混合腳本的原因之一，是 Unicode 增加的主要原因之一。 字碼頁對於撰寫主控台程式碼、維護繼承應用程式或在舊版 Windows 上執行，以及與非 Unicode 啟用的非 Microsoft 軟體進行互動，都是很重要的。

## <a name="input-language"></a>輸入語言

輸入語言是以每一進程的資料 (變數來表示，例如，希臘文) 和輸入方法 (例如鍵盤) 。 您可以安裝多個輸入語言，而且使用者可以在兩者之間切換。

為了設定和取出輸入語言值，應用程式會分別呼叫 [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) 和 [**GetKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout)。 使用者可以透過主控台的 [地區及語言選項] 部分中的 [ **語言** ] 索引標籤，來新增和移除輸入語言。

預設的輸入語言是作業系統的當地語系化語言，它是啟動新的應用程式時所使用的設定， (或針對某些應用程式) 開啟新視窗時的設定。 切換到不同的輸入語言是以每個應用程式為基礎來進行。 換句話說，您可以在兩個不同的應用程式中使用兩種不同的輸入語言。 例如，使用者可以使用國際美國鍵盤配置來輸入德文、使用非 Microsoft) 軟體的語音輸入 (英文），以及在三個不同應用程式中使用輸入法的西班牙文。

## <a name="language-for-non-unicode-programs"></a>非 Unicode 程式的語言

非 Unicode 程式的語言 (先前稱為「系統地區設定」 ) 決定作業系統上預設使用的字碼頁。 非 Unicode 程式的語言設定只會影響非 Unicode 應用程式，也就是 ANSI 應用程式。 設定語言會指示 Windows 模擬以非 Unicode 為基礎的作業系統（當地語系化為此語言）。 變更非 Unicode 程式的語言時，會安裝所需的點陣圖字型檔案，以支援指定語言的非 Unicode 應用程式。 若要允許使用者選取非 Unicode 程式的語言，則必須安裝適當的語言群組。 您的應用程式需要腳本支援，才能選取非 Unicode 程式的語言。 非 Unicode 程式的語言是一種系統設定，而且需要重新開機才能執行。

有時候非 Unicode 程式的兩個語言之間並沒有明顯的差異。 例如，這是德文 (中性) 和德文 (奧地利) 地區設定的情況。 一般情況下，其中一個語言群組的設定非常類似，而且只有 OEM 或 MAC 字碼頁不同。

ANSI 應用程式應該在安裝期間檢查非 Unicode 程式設定的語言。 它會使用 [**GetACP**](/windows/desktop/api/Winnls/nf-winnls-getacp) 或 [**GetOEMCP**](/windows/desktop/api/Winnls/nf-winnls-getoemcp) 來取得值。 不支援任何函式來設定非 Unicode 程式的語言。 不過，使用者可以使用主控台的 [地區及語言選項] 部分中的 [ **Advanced** ] 索引標籤來變更它。 以下是非 Unicode 程式設定的一些語言範例：

1.  如果德文使用者想要執行專為日文 Windows 95 設計的日文應用程式，則必須選取日文作為非 Unicode 程式的語言。 在選取此選項之後，非 Unicode 德文應用程式就會發生問題。 例如，德文的母音 (？) 未正確顯示。
2.  如果德文使用者想要在非 Unicode 德文應用程式中輸入日文文字，則必須選取日文作為非 Unicode 程式的語言。 如同在第一個範例中，這會導致在非 Unicode 應用程式中輸入德文文字的問題。
3.  想要在非 Unicode 阿拉伯文應用程式中輸入阿拉伯文、法文和英文的阿拉伯文使用者應選取阿拉伯文做為非 Unicode 程式的語言，因為阿拉伯文 ANSI 字碼頁包含大部分的法文字元和所有英文字元。

## <a name="language-group"></a>語言群組

語言群組可控制非 Unicode 程式的語言、標準及格式、輸入語言，以及可選取的使用者介面語言。 針對每個當地語系化版本，指定的語言群組是預設值，而且無法移除。 例如，Windows 預設會安裝西歐和美國語言群組。 因此，如果英文版的 Windows 是安裝在非英文說話的國家/地區，則使用者通常會安裝另一個語言群組。

新增語言群組時，Windows 會複製 (但不會啟用) 必要的鍵盤檔、輸入法編輯器 (Ime) 、TrueType 字型檔案、點陣圖字型檔案，以及國家語言支援 ( nls) 檔案。 新增語言群組也會加入字型連結的登錄值，並安裝複雜字集語言的腳本引擎， (阿拉伯文、希伯來文、印度文和泰文) 。

除了西歐和美國語言群組以外，還有其他16個語言群組：



<table>
<tbody>
<tr class="odd">
<td><dl> 阿拉伯文<br />
亞美尼亞文<br />
波羅的語系<br />
中歐<br />
古斯拉夫文<br />
喬治亞文<br />
希臘文<br />
Hebrew<br />
</dl></td>
<td><dl> 印度<br />
日文<br />
韓文<br />
簡體中文<br />
繁體中文<br />
泰文<br />
突厥<br />
越南文<br />
</dl></td>
</tr>
</tbody>
</table>



 

任何語言群組的數目和組合都可以安裝在任何作業系統上。 例如，西班牙文使用者可以安裝斯拉夫語言群組來處理俄文文字。 在此情況下，文字處理應用程式也需要支援斯拉夫語言群組。

> [!Note]  
> 新增適當的語言群組不會自動讓應用程式接受文字。 建議您進行測試。 例如，非 Unicode 應用程式可能需要變更非 Unicode 程式的語言。

 

## <a name="location"></a>Location

**WINDOWS XP：** 位置是地理識別碼。 它是以每個使用者的資料變數表示，以定義使用者所在的國家/地區。

若要設定此值，應用程式會呼叫 [**SetUserGeoID**](/windows/desktop/api/Winnls/nf-winnls-setusergeoid)。 為了取得值，應用程式會呼叫 [**GetUserGeoID**](/windows/desktop/api/Winnls/nf-winnls-getusergeoid)。

## <a name="standards-and-formats"></a>標準及格式

標準及格式 (先前的「使用者地區設定」 ) 是每個使用者的變數，可決定預設排序次序以及格式化日期、時間、貨幣和數位的預設設定。 變數會以語言呈現， (有時會與國家/地區) 組合，但它不是語言本身。 例如，將 [標準] 和 [格式] 變數設定為 [希伯來文]，表示使用者想要使用希伯來文的格式設定慣例，而不一定是希伯來文語言。 此外，[標準] 和 [格式] 變數會決定日期和月份名稱所使用的字串。 例如，如果使用者顯示「1998年11月25日」，則 "11 月" 字串可能會根據標準及格式變數而變更。 變更變數會自動加入輸入地區設定和語言的預設設定。

為了取得標準及格式變數設定，應用程式會呼叫 [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid) 或 [**GetUserDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename)。 沒有任何 NLS 函數可設定變數。 不過，使用者可以透過主控台的 [地區及語言選項] 部分中的 [ **地區選項** ] 索引標籤來變更它。

應用程式通常應該使用「標準」和「格式化」變數設定來顯示資料。 不過，使用固定地區設定來顯示資料的應用程式應該傳遞特定的地區設定識別碼，而不是使用地區設定 \_ 使用者 \_ 預設值。

## <a name="thread-locale"></a>執行緒地區設定

執行緒地區設定是以每個執行緒的地區設定資料變數表示，以決定執行緒的日期、時間、貨幣和大型數位的格式。 它預設為目前為標準及格式選取的地區設定值。 若要設定執行緒地區設定，應用程式會呼叫 [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)。 為了取得執行緒地區設定，應用程式會呼叫 [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale)。

在大多數情況下，不應覆寫執行緒地區設定。 一般來說，它只能用來將伺服器應用程式的執行緒地區設定與用戶端電腦的標準及格式變數進行同步處理。 例如，用於全球銀行的紐約股票交換的財務股票交易應用程式，必須以美國的格式顯示時間、日期和股票價格。 此應用程式會使用 [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) 將執行緒地區設定設為英文 (的美國) 然後使用 NLS 函數來格式化日期、時間和股票價格。

變更執行緒地區設定不會影響所有 API 函式。 因此，它不一定是覆寫標準及格式變數的可靠方法。 相反地，控制標準及格式的應用程式應該使用固定的地區設定來顯示資料，傳遞特定的地區設定識別碼，而不是使用地區設定 \_ 使用者 \_ 預設值。

## <a name="nls-example"></a>NLS 範例

下列範例顯示標準與格式、非 Unicode 程式的語言、位置和使用者 UI 語言之間的相互作用。

身為智利但居住在美國的使用者，有一部執行 Windows XP 英文的電腦。 使用者將位置設定為使用網際網路服務提供者 (ISP) 取得美國天氣。 不過，標準及格式變數會設定為西班牙文 (智利) ，以便根據智利文標準將資訊格式化。 此外，使用者會使用韓文字處理器（這是 ANSI 應用程式），如此一來，非 Unicode 程式的語言就會設定為韓文 (韓國) 。 若要使用應用程式，使用者可以使用英文鍵盤，也會安裝韓文 IME 以支援第二個輸入語言。 使用者的同事（共用電腦，但不熟悉英文）可以將使用者 UI 語言設定為西班牙文 (西班牙) 使用電腦時。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於國家語言支援](about-national-language-support.md)
</dt> <dt>

[地區設定和語言](locales-and-languages.md)
</dt> <dt>

[多語系使用者介面](multilingual-user-interface.md)
</dt> </dl>

 

 
