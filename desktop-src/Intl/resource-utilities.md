---
description: 本主題說明用來建立 MUI 應用程式的兩個公用程式。
ms.assetid: 8ba94001-fc46-41e0-a071-0dc500a20753
title: 資源公用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d9bb8a8608c97b700beebb53ce95fdf4b85c4d5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481504"
---
# <a name="resource-utilities"></a>資源公用程式

本主題說明用來建立 MUI 應用程式的兩個公用程式。 雖然 MUIRCT 是一種 mui 專屬的工具，但 mui 也利用標準的 Windows RC 編譯器公用程式。 [當地語系化資源和建立應用程式](localizing-resources-and-building-the-application.md)時，會提供使用這些公用程式的指示。

## <a name="muirct-utility"></a>MUIRCT 公用程式

MUIRCT (Muirct.exe) 是一種命令列公用程式，可將標準可執行檔分割成 LN 檔和特定語言的 (，也就是可當地語系化的) 資源檔。 每個產生的檔案都包含檔案關聯的資源配置資料。 MUIRCT 包含在 Windows Vista 的 Microsoft Windows SDK 中。

> [!Note]  
> 從 Windows Vista 開始，會更新 Win32 資源載入器，以從特定語言的檔案和 LN 檔案載入資源。

 

### <a name="muirct-usages"></a>MUIRCT 使用方式

1.  根據 rc 設定檔將二進位檔分割成主要二進位檔和 mui 檔案 \_ 。

    `Muirct -q rc_config [-c checksum_file [-b LangID]] [-x LangID] [-g LangId]     [-f] [-m] [-v level] source_file [output_LN_file] [output_MUI_file]`

2.  從總和檢查碼檔案中解壓縮總和檢查碼 \_ ，然後將它插入輸出檔中 \_ 。

    `Muirct -c checksum_file [-b LangID] -e output_file`

3.  根據總和檢查碼檔案計算總和檢查碼 \_ ，並將它插入輸出檔中 \_ 。

    `Muirct  -c checksum_file [-b LangID] -q rc_config  -z output_file`

4.  從輸入檔傾印資源設定資料內容 \_ 。

    `Muirct -d input_file`

### <a name="muirct-syntax"></a>MUIRCT 語法

MUIRCT 可以從命令列參數和（或）使用-q 參數指定的資源設定檔中取得方向。


```C++
muirct [-h|-?] [ -c checksum_file] [-b langid]  ]
     [-g langid] [-q resource configuration file<RCF>] [-v level] [-x langid]
     [-e output_file]  [-z output_file] [-f] [-d MUI'ized file] [-m file_version]

source_filename [language_neutral_filename] [mui_filename]
```



**參數和引數**




| | |-h |-？ |顯示說明畫面。 | |-c |指定要從中解壓縮或計算資源總和檢查碼的輸入 checksum_file。 Checksum_file 必須是包含可當地語系化資源的 Win32 二進位檔案。 如果 checksum_file 包含多個語言的資源，則必須使用-b 參數來指定應使用的是哪一個，否則 MUIRCT 會失敗。 <br /> | |-b |指定當以-c 指定的 checksum_file 包含多種語言的資源時，所要使用的語言。 這個參數只能搭配-c 參數使用。 語言識別項可以是十進位或十六進位格式。 如果 checksum_file 包含多種語言的資源，但未指定-b，或在 checksum_file 中找不到-b 參數所指定的語言，則 MUIRCT 會失敗。 <br /> | |-g |在 LN 檔案的資源設定資料區段中，指定要包含為最終回溯語言的語言識別項。 如果資源載入器無法從執行緒慣用 UI 語言載入要求的 mui 檔，它會使用最終的回溯語言做為最後一次嘗試。 LangID 值可以指定為十進位或十六進位格式。 例如，英文 (美國) 可由-g 0x409 或-g 1033 指定。 <br /> | |-q |指定根據 rc_config 檔案配置，將 source_file 分割成 output_LN_file 和 output_MUI_file。 Rc_config 檔案是一種 XML 格式的檔案，可指定要將哪些資源解壓縮至 mui 檔案，而且會保留在 LN 檔案中。 Rc_config 可以指定 output_LN_file 和 output_MUI_file 之間的資源類型和個別命名專案的散發。 Source_file 必須是包含單一語言之資源的 Win32 二進位檔，否則 MUIRCT 會失敗。 如果檔案是中性語言，則 MUIRCT 不會分割該檔案，而是以檔案中的語言識別項值0表示。 Output_LN_file 和 output_mui_file 是要分割 source_file 的中性語言和 mui 檔案的名稱。 這些檔案名是選擇性的。 如果未指定，MUIRCT 會將副檔名 ln 和 mui 附加至 source_file。 通常您應該先移除 "ln" 延伸模組，然後再部署檔案。 MUIRCT 會根據 source_file 名稱和檔案版本來計算總和檢查碼，然後將結果插入每個輸出檔案的資源設定區段，以建立 output_LN_file 和 output_MUI_file 的關聯。 與-c 參數搭配使用時，-q 參數優先。 如果以-q 參數提供的 rc_config 檔案包含總和檢查碼 MUIRCT，則會忽略-c 參數，並將值的總和檢查碼值從 rc_config 檔案插入到 LN 和 mui 檔案。 如果在 rc_config 中找不到總和檢查碼值，MUIRCT 會根據-c 參數的行為來計算資源總和檢查碼。 <br /> | |-v |指定記錄的資訊層級。 指定1以列印所有基本錯誤訊息和作業結果。 指定2，也可以包含包含在 mui 檔和 LN 檔案中的資源資訊 (類型、名稱、語言識別項) 。 預設值為-v 1 <br /> | |-x |指定 MUIRCT 將所有資源類型新增至 mui 檔案的資源區段中的語言識別項。 LangID 值可以指定為十進位或十六進位格式。 例如，英文 (美國) 可由-x 0x409 或-x 1033 指定。 <br /> | |-e |解壓縮隨附于-c 參數的 checksum_file 中的資源總和檢查碼，並將它插入指定的 output_file。 當指定-e 時，MUIRCT 會忽略-c 參數以外的所有參數。 在此情況下，checksum_file 必須是 Win32 二進位檔案，其中包含具有總和檢查碼值的資源設定資料區段。 Output_file 必須是現有的 LN 檔或 mui 檔案。 <br /> | |-z |計算並插入指定輸出檔中的資源總和檢查碼資料。 MUIRCT 會對-c 參數所提供的輸入和選擇性的-b 參數進行基礎總和檢查碼計算。 如果您指定不存在之-z 參數的輸出檔，MUIRCT 會結束併發生失敗。<br /> 範例：根據 Notepad.exe 中的可當地語系化資源來計算總和檢查碼，並將總和檢查碼插入輸出檔 Notepad2.exe。<br /><code>muirct -c notepad.exe -q myprog.rcconfig -z notepad2.exe</code><br /> | |-f |建立具有版本資源的 mui 檔案，此檔案是唯一可當地語系化的資源。 根據預設，MUIRCT 不允許這種情況。<br /> | |-d |在原始檔中尋找並顯示內嵌資源設定資料。 當您指定這個參數時，MUIRCT 會忽略所有其他的命令列選項。<br /> | |-m |指定計算與 output_LN_file 和 output_MUI_file 相關聯的總和檢查碼時，所要使用的版本號碼。 <br /> | |source_filename |當地語系化二進位原始程式檔的名稱;無法使用萬用字元。 這個檔案只能包含一種語言的資源。 如果檔案中有多種語言的資源，除非使用-b 參數，否則 MUIRCT 會失敗。 如果檔案包含的資源具有僅具有0值的語言識別項，則 MUIRCT 不會分割檔案，因為語言識別項為0表示中立的語言。<br /> 若是-d 參數，source_filename 是 LN 檔或特定語言的資源檔，MUIRCT 會顯示資源設定資料。 <br /> | |language_neutral_filename |選。 LN 檔案的名稱。 如果您未指定此檔案的名稱，MUIRCT 會將第二個副檔名 "ln" 附加至來原始檔案名，以做為非語言相關的檔案名。 通常您應該先移除 "ln" 延伸模組，然後再部署檔案。<blockquote>[!Note]<br />LN 檔案不能包含字串或功能表。 您應手動移除它們。</blockquote><br /> | |mui_filename |選。 特定語言的資源檔名稱。 如果您未指定名稱，MUIRCT 會將第二個副檔名 "mui" 附加至來原始檔案名，以作為檔案名。一般來說，MUIRCT 會建立特定語言的資源檔。 但是，如果有下列任何一種情況，則不會建立資源檔：<br /><ul><li>原始二進位檔案中沒有可當地語系化的資源。</li><li>在原始二進位檔案中唯一找到的資來源語言是中立的語言。</li><li>原始的二進位檔案具有多個語言的資源，而不會計算中性語言。 如果二進位檔案包含兩種語言的資源，而其中一個是中性語言，則公用程式會將檔案視為單一語言，並在有可當地語系化的資源時建立特定語言的資源檔。</li></ul> | 




 

### <a name="muirct-language-output"></a>MUIRCT 語言輸出

MUIRCT 會根據下列順序（從最高優先順序到最低），選擇要插入 LN 檔案資源設定資料的 "UltimateFallbackLanguage" 屬性值：

1.  來源資源設定檔中的 "UltimateFallbackLanguage" 屬性（如果其中一個是以輸入形式傳遞）。
2.  使用-g 參數指定的語言。
3.  輸入檔語言。

MUIRCT 會根據下列順序挑選 "language" 屬性值，以在 mui 檔案資源設定資料中插入：

1.  來源資源設定檔中的 "language" 屬性（如果其中一個是以輸入形式傳遞）。
2.  -X 參數所指定的語言 (強制語言) 。
3.  輸入檔語言。

### <a name="muirct-checksum-handling"></a>MUIRCT 總和檢查碼處理

除非您透過資源設定檔指定總和檢查碼，否則作業系統通常會計算檔案中特定語言資源的總和檢查碼。 只要 LN 檔和所有相關聯的語言特定資源檔的總和檢查碼相同，且 LN 和語言相依的資源設定中的 language 屬性相符，資源載入器就可以成功載入資源。

MUIRCT 支援數個在資源設定資料中放置適當總和檢查碼的方法：

1.  為每個語言建立可執行檔，其中包含程式碼和資源。 之後，請使用 MUIRCT 將每個檔案分割成 LN 檔和特定語言的資源檔。 MUIRCT 會多次執行，以產生每個語言的資源檔。 您可以透過下列方式執行組建：
    1.  使用-q 參數來指定資源設定檔中的總和檢查碼值。 MUIRCT 會將此值放在產生的所有 LN 檔和特定語言的資源檔中。 您必須採用策略來選擇此值，如本主題稍後所述。
    2.  使用-c 參數 (，並選擇性地使用-b 參數) 選擇具有 MUIRCT 從中解壓縮總和檢查碼之資源的單一語言。
    3.  使用-z 參數來選擇具有資源的單一語言，MUIRCT 一律從中解壓縮總和檢查碼。 使用其他方法建立檔案之後，請套用此總和檢查碼。
2.  建立可執行檔，其中包含單一語言的程式碼和資源。 之後，請使用 MUIRCT 來分割 LN 檔和特定語言資源檔之間的資源。 最後，使用二進位當地語系化工具來修改每個語言產生的資源檔。

總和檢查碼處理最常見的慣例是以英文 (美國) 資源作為總和檢查碼。 您可以自由採用不同的慣例，只要每個 LN 檔案都是一致的。 例如，軟體發展企業完全可以接受軟體發展企業將其總和檢查碼以法文 (法國) 資源為基礎，而非英文 (美國) 資源，只要所有的應用程式都有法文 (法國) 的資源，就會以總和檢查碼作為基礎。 您也可以使用資源設定檔，將任意十六進位值（最多16個十六進位數位）指派為總和檢查碼。 最後一個策略會防止 MUIRCT 的-z、-c 和-b 參數有效使用。 它需要採用使用 [**GuidGen**](/previous-versions/windows/embedded/ms924300(v=msdn.10)) 或其他工具來產生總和檢查碼值的方法。 此策略也會要求您設定原則，以決定何時要在新增可當地語系化的資源時修改該值。

若要將英文 (美國) 總和檢查碼套用至所有檔案，您可以使用上述任何一種總和檢查碼處理方法。 例如，您可以針對英文 (的美國) 產生 LN 檔案和特定語言的資源檔，然後使用 MUIRCT-d 參數來取得產生的總和檢查碼。 您可以將此總和檢查碼複製到資源設定檔中，並搭配使用-q 參數與 MUIRCT，將總和檢查碼套用至所有其他檔案。

### <a name="use-of-a-resource-configuration-file-with-muirct"></a>使用資源設定檔搭配 MUIRCT

使用 MUIRCT 時，您可以指定資源設定資料。 無論您是否明確提供資源設定檔，每個特定語言的資源檔都有資源設定資料，如同任何含有相關聯資源檔的 LN 檔案一樣。 例如：

-   如果您使用-q 參數來指定資源設定檔，但您的輸入來源檔案中沒有可當地語系化的資源，則不會產生特定語言的資源檔，而產生的 LN 檔案不會包含資源設定資料。 此外，如果輸入來源檔案有多語系資源，則 MUIRCT 不會將檔案分割。

> [!Note]  
> 目前，當資源設定檔的 neutralResources 元素未包含 resourceType 元素，而且 localizedResources 元素包含字串和功能表時，MUIRCT 的行為不一致。 在這種情況下，MUIRCT 會分割資源，如下所示：
>
> -   原始二進位檔 (中的所有資源（包括字串和功能表) ，加上 MUI 資源）都會放置在 LN 檔案中。
> -   字串、功能表和 MUI 資源會放在適當的語言特定資源檔中。

 

### <a name="examples-for-using-muirct"></a>使用 MUIRCT 的範例

**標準使用量範例**


```C++
muirct -q mui.MMF bar.exe barnew.exe barnew.exe.mui

muirct -d myprog.exe.mui
```



**使用-d 參數輸出 LN 檔案的範例**

以下範例是使用-d 參數搭配 MUIRCT，從 LN 檔案 Shell32.dll 的資源設定資料輸出：


```C++
Signature          -    fecdfecd
Length             -    148
RC Config Version  -    10000
FileType           -    11
SystemAttributes   -    100
UltimateFallback location    -  external
Service Checksum   -    14f44a8d86bef14af26d9a885964c935
Checksum           -    f5b3b7ab330439d6fcc07582c3afb613
MainNameTypes      -    AVI FTR ORDERSTREAM TYPELIB UIFILE XML MUI
MainIDTypes        -    1 2 3 12 14 16 24
MuiNameTypes       -    MUI
MuiIDTypes         -    2 3 4 5 6 9 14 16
UltimateFallbackLanguage   -   en-US
```



**使用-d 參數 Language-Specific 資源檔輸出的範例**

以下範例是使用 MUIRCT 的-d 參數，從 mui 檔案（Shell32.dll mui）的資源設定資料輸出：


```C++
Signature          -    fecdfecd
Length             -     c8
RC Config Version  -    10000
FileType           -    12
SystemAttributes   -    100
Service Checksum   -    14f44a8d86bef14af26d9a885964c935
Checksum           -    f5b3b7ab330439d6fcc07582c3afb613
MainNameTypes      -    MUI
MainIDTypes        -    2 3 4 5 6 9 14 16
Language           -    en-US
```



## <a name="rc-compiler-utility"></a>RC 編譯器公用程式

RC 編譯器 (Rc.exe) 是一種命令列公用程式，可將資源定義腳本檔案（ ( .rc) 延伸模組）編譯為 ( 的資源檔) .res 延伸。 RC 編譯器包含在 Windows SDK 中。 本檔僅說明如何搭配使用 RC 編譯器與資源載入器的 MUI 相關功能。 如需編譯器的完整資訊，請參閱 [關於資源檔](../menurc/about-resource-files.md)。

RC 編譯器可讓您從一組來源、LN 檔和個別的特定語言資源檔建立。 針對 MUIRCT，檔案會與資源設定資料相關聯。

### <a name="rc-compiler-syntax-as-used-for-mui-resources"></a>用於 MUI 資源的 RC 編譯器語法

RC 編譯器參數在 [使用 rc](../menurc/using-rc-the-rc-command-line-.md)中有詳細的定義。 本節只會定義用來建立 MUI 資源的參數。 請記住，每個參數都不區分大小寫。 除非另有指示，否則資源類型會假設為非語言相關。


```C++
rc [-h|-?] -fm mui_res_name [-q rc_config_file_name] [-g langid] [-g1 ] [-g2 version]
```



**參數和引數**




| | |-h |-？ |顯示說明畫面。 | |-fm |針對特定語言的資源使用指定的資源檔。 資源編譯器通常會建立特定語言的資源檔。 但是，如果有下列任何一種情況，則不會建立檔案：<br /><ul><li>.Rc 檔中沒有可當地語系化的資源。</li><li>.Rc 檔中唯一找到的資來源語言是中性語言。</li><li>.Rc 檔案有多個語言的資源，不會計算中性語言。 如果 .rc 檔包含兩種語言的資源，其中一個是中性語言，則編譯器會將檔案視為單一語言。 如果有任何可當地語系化的資源，編譯器會建立特定語言的資源檔。</li></ul> | |-q |使用指定的資源設定檔來取得要放在特定語言資源檔和 LN 檔案中的資源類型。 如需詳細資訊，請參閱 <a href="preparing-a-resource-configuration-file.md">準備資源設定檔</a>。 除了此參數之外，您還可以使用-j 和-k 參數，但最好是使用資源設定檔。 <br /> 藉由搭配使用-q 參數與資源設定檔，您可以執行以專案為基礎的分割，並提供最後會在 LN 和語言特定資源檔中使用二進位資源設定的屬性。 使用-j 和-k 參數無法進行分割。<blockquote>[!Note]<br />如果您將資源和版本資訊儲存在不同的資源設定檔中，RC 編譯器分割進程就無法正常運作。 在此情況下，RC 編譯器不會分割版本資訊。 因此，連結特定語言的資源檔時，會發生連結器錯誤，因為該檔案沒有版本資源。</blockquote><br /><br /> | |-g |指定十六進位的最終回溯 <a href="language-identifiers.md">語言</a> 識別碼。<br /> | |-g1 |即使版本資源是唯一可當地語系化的內容，也會建立 MUI 檔案。 根據預設，如果版本是唯一可當地語系化的資源，RC 編譯器就不會產生 .res 檔。<br /> | |-g2 |指定在計算總和檢查碼時要使用的自訂版本號碼。<br /> | |mui_res_name |特定語言資源的資源檔。<br /> | |rc_config_file_name |資源設定檔案。<br /> | |langid |語言識別項。<br /> | |版本 |自訂版本號碼，格式如下： "6.2.0.0"。<br /> | 




 

### <a name="example-for-using-rc-compiler-to-build-mui-resources"></a>使用 RC 編譯器建立 MUI 資源的範例

為了說明使用 MUI 資源的 RC 編譯器操作，讓我們檢查下列命令列，以取得資源檔 Myfile.txt .rc：


```C++
rc -fm myfile_res.res -q myfile.rcconfig myfile.rc
```



此命令列會導致 RC 編譯器執行下列作業：

-   根據 .rc 檔的名稱，建立預設為 Myfile.txt 的語言專屬資源檔 Myfile.txt \_ .res 和非語言相關資源檔。
-   將 2 (專案 5 6 7 8 9 10 11 12) 、4、5、6、9、11、16、23、240、1024我 \_ 的類型資源類型新增至特定語言的 .res 檔案（如果它們位於 .rc 檔中）。
-   將資源類型16（以及資源檔中所述的任何其他資源類型）新增至語言中性 .res 檔和語言特定 .res 檔。 請注意，在此範例中，會在兩個位置加入資源類型16。
-   選擇 "UltimateFallbackLanguage" 屬性值，根據下列準則（從最高優先順序到最低順序）來插入 LN 檔案資源設定資料：
    -   資源設定檔中的 "UltimateFallbackLanguage" 屬性（如果其中一個是以輸入形式傳遞）。
    -   要根據 RC 編譯器語言順序插入資源設定資料的語言屬性值， (非語言相關和特定語言的資源檔語言) 。 考慮事項包括 .rc 檔中的語言、-gl 參數的語言值，以及英文 (美國) 的識別碼0x0409。

## <a name="remarks"></a>備註

如果您在 neutralResources 元素中包含任何圖示 (3) 、對話方塊 (5) 、字串 (6) 或版本 (16) 資源類型，則您必須在資源設定檔的 localizedResources 元素中複製該專案。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[多語系消費者介面參考](multilingual-user-interface-reference.md)
</dt> <dt>

[MUI 資源管理](mui-resource-management.md)
</dt> <dt>

[當地語系化資源和建立應用程式](localizing-resources-and-building-the-application.md)
</dt> </dl>

 

 
