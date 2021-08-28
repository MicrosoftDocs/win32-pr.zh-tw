---
description: 本節說明如何建立手寫辨識的自訂字典。
ms.assetid: 83abf534-740c-44a3-bbd4-babb54f2930e
title: 在 Windows 7 和 Windows Server 2008 R2 中建立手寫辨識的自訂字典
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fe391125b21bfe35a9e1a69be6258e1643b424e
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883890"
---
# <a name="creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2"></a>在 Windows 7 和 Windows Server 2008 R2 中建立手寫辨識的自訂字典

本節說明如何建立手寫辨識的自訂字典。

在 Windows 7 作業系統和 Windows Server 2008 R2 作業系統中，手寫辨識的精確度可透過使用自訂字典大幅改進。 這些字典會補充或取代用於手寫的系統字典。 手寫辨識支援是透過筆跡和手寫服務功能提供，必須透過伺服器管理員啟用。

> [!Note]  
> 只有在已安裝該語言的手寫辨識器時，才能針對語言安裝自訂字典。

 

有兩個基本步驟可以設定自訂字典以進行手寫：

-   編譯字組清單。 編譯會建立編譯的自訂字典 ( hwrdict) 檔。
-   安裝已編譯的自訂字典。

## <a name="compiling-a-word-list"></a>編譯單字清單

要編譯的單字清單必須是純文字格式，而且應該使用 Unicode 編碼儲存。 其他編碼將無法運作。 文字檔中的每一行都會以單一專案的形式在字典中取得。 允許包含一或多個空格的 Multiword 單位專案。 會忽略行開頭或結尾的空格。

自訂字典是從命令列編譯的。 若要編譯字典，請開啟命令視窗，流覽至包含單字清單的資料夾，然後使用您想要使用的命令列選項來執行 HwrComp.exe。

下列範例顯示命令列選項的使用語法。

``` syntax
Usage: hwrcomp       [-lang <localename>] [-type <type>]
    [-comment <comment>]
    [-o <dictfile.hwrdict>]
    <inputfile>
     
```

### <a name="explanation-of-options"></a>選項的說明



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>參數</th>
<th>說明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-lang &lt; >localename&gt;</td>
<td>指派給已編譯自訂字典檔案的指定地區設定名稱。 引數 &lt; >localename &gt; 具有 language 區域格式。 其中一個範例是 en-us，表示美國地區的英文語言。 如需此表單的範例，請參閱 [語言識別項常數和字串](/windows/desktop/Intl/language-identifier-constants-and-strings)。 這項功能支援下列語言的 Windows 7 和 Windows Server 2008 R2： en-us、en-us、en-us、en-us、de、de、de、fr、es、es-MX、es-AR，以及。它（it）、nl nl、nl-a、pt-BR、pt、da-深色、sv-SE、nb-no、nn-no、fi、pl-pl、cs CZ、ru-ru、ro-Latn-cs、CA es 和 hr-hr。<br/></td>
</tr>
<tr class="even">
<td>-類型 &lt; 類型&gt;</td>
<td>選項引數 &lt; 類型 &gt; 是將資源作為主要單字清單的單一字串串連， (主要) 或作為主要單字清單的補充 (次要) 後面接著套用資源的實際單字清單名稱 (例如字典或姓氏) 。 以下是可能的值：
<ul>
<li>主要-CITYNAME-清單</li>
<li>主要-COUNTRYNAME-清單</li>
<li>主要-COUNTRYSHORTNAME-清單</li>
<li>主要字典</li>
<li>主要-GIVENNAME-清單</li>
<li>主要-STATEORPROVINCE-清單</li>
<li>主要-STREETNAME-清單</li>
<li>主要-姓氏-清單</li>
<li>次要-CITYNAME-清單</li>
<li>次要-COUNTRYNAME-清單</li>
<li>次要-COUNTRYSHORTNAME-清單</li>
<li>次要字典</li>
<li>次要-EMAILSMTP-清單</li>
<li>次要-EMAILUSERNAME-清單</li>
<li>次要-GIVENNAME-清單</li>
<li>次要-STATEORPROVINCE-清單</li>
<li>次要-STREETNAME-清單</li>
<li>次要-姓氏-清單</li>
<li>次要 URL-清單</li>
</ul>
如果類型值的開頭是前置詞主要，編譯的字典在安裝之後，將會取代該語言的系統字典。 值的主要字典代表語言的主要系統字典。
<blockquote>
[!Note]<br />
取代系統字典不會對原始的系統字典內容執行任何動作，因為取代只有在移除自訂字典後才會生效。
</blockquote>
<br/> 如果類型值的開頭是前置詞次要，編譯的字典將會補充系統字典，而不會取代它。</td>
</tr>
<tr class="odd">
<td>-批註 <comment></td>
<td>指定的批註會編譯到字典檔案中。 批註必須是單一字串，且不能超過64個字元。</td>
</tr>
<tr class="even">
<td>-o <dictfile.hwrdict></td>
<td>輸出會寫入指定的檔案名 <dictfile.hwrdict> 。<br/> 如果遺漏這個選項，輸出檔名稱就會衍生自原始輸入檔名稱，而輸入副檔名為 hwrdict。<br/></td>
</tr>
</tbody>
</table>



 

### <a name="defaults"></a>Defaults

如果未指定任何參數，預設選項值為

-lang <current input language> -類型次要字典

### <a name="examples"></a>範例

以下會編譯輸入檔 mylist1.txt、套用預設選項值，並建立輸出檔 mylist1. hwrdict。

``` syntax
hwrcomp mylist1.txt
```

相反地，下列會將 mylist1.txt 編譯為 myrsrc1. hwrdict，但會將 "英文 (US) " (en-us) 指派為語言和次要字典做為類型。

``` syntax
hwrcomp -lang en-US -type SECONDARY-DICTIONARY -o myrsrc1 mylist1.txt 
```

## <a name="installing-a-compiled-custom-dictionary"></a>安裝已編譯的自訂字典

HwrComp.exe 會建立 hwrdict 檔案，這是可供手寫辨識器使用的二進位格式。 此檔案可以安裝在任何執行 Windows 7 或 Windows Server 2008 R2 且支援手寫辨識的電腦上。 只針對目前的使用者或電腦上的所有使用者安裝字典。

您可以使用工具 HwrReg.exe，從命令列安裝已編譯的自訂字典檔。 如果您想要覆寫一些編譯成檔案或預設值的設定值，這項工具就很有用。 有兩種方式可以執行 HwrReg.exe：在檢查/安裝模式下，以及在清單/移除模式中。

### <a name="running-hwrregexe-in-checkinstall-mode"></a>正在檢查/安裝模式中執行 HwrReg.exe

此模式適用于尚未安裝的自訂字典檔案。 以下顯示命令列選項的使用語法。

``` syntax
Usage: hwrreg        [-check]
    [-lang <localename>] 
    [-scope {all|me}]
    [-noprompt] 
    <dictfile.hwrdict>
```

### <a name="explanation-of-options"></a>選項的說明



| 參數                | 說明                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -檢查                   | 字典檔會在未安裝的情況下進行驗證。 檢查選項會顯示檔案的批註，以及用來安裝檔案的註冊資訊。 此選項適用于在執行安裝之前確認註冊資訊。 <br/> 如果遺漏此選項，HwrReg.exe 會安裝自訂字典。<br/>  |
|  lang &lt; >localename&gt; | 字典檔會在未安裝的情況下進行驗證。 檢查選項會顯示檔案的批註，以及用來安裝檔案的註冊資訊。 此選項適用于在執行安裝之前確認註冊資訊。 <br/> 如果遺漏此選項，HwrReg.exe 會安裝自訂字典。 <br/> |
|  範圍 {所有 \| me}         | 針對所有使用者安裝自訂字典 ( 範圍所有) 或僅限目前使用者 ( 範圍我) 。 使用範圍安裝都需要在提高許可權的命令提示字元中執行命令。否則，將會傳回錯誤碼。 <br/> 如果缺少這個選項，則安裝的範圍僅限於目前的使用者。<br/>                          |
|  noprompt                | HwrReg.exe 不會提示您進行確認。 從腳本執行 hwrReg.exe 時，這會很有用。 <br/>                                                                                                                                                                                                                                                                 |



 

下列範例會安裝適用于 language "丹麥文 (丹麥) " (da 深色) 的自訂字典 myrsrc1，其預設範圍僅限於目前的使用者。

``` syntax
hwrreg -lang da-DK myrsrc1.hwrdict 
```

### <a name="running-hwrregexe-in-listremove-mode"></a>在清單/移除模式中執行 HwrReg.exe

這種模式會列出或移除已安裝的自訂字典。 以下顯示命令列選項的使用語法。

``` syntax
Usage: hwrreg        [-lang <localename>] 
    [-scope {all|me}] 
    [-type <type>]
    -list | -remove
```

### <a name="explanation-of-options"></a>選項的說明



| 參數                | 說明                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  lang &lt; >localename&gt; | 只會列出或移除為此地區設定名稱註冊的字典。 引數 &lt; >localename &gt; 具有表單語言區域。 如需此表單的範例，請參閱 [語言識別項常數和字串](/windows/desktop/Intl/language-identifier-constants-and-strings)。 <br/> 如果遺漏這個選項，則會列出或移除所有語言的字典。<br/> |
|  範圍 {所有 \| me}         | 針對所有使用者安裝自訂字典 ( 範圍所有) 或僅限目前使用者 ( 範圍我) 。 使用範圍安裝都需要在提高許可權的命令提示字元中執行命令。否則，將會傳回錯誤碼。 <br/> 如果缺少這個選項，則安裝的範圍僅限於目前的使用者。<br/>                      |
|  類型 &lt; 類型&gt;       | 只列出或移除以指定類型註冊的字典。<br/> 如果遺漏這個選項，則會列出或移除所有的字典類型。 安裝或移除另一種類型的自訂字典 (例如主要 COUNTRYNAME 清單) 可能會影響其他內容中的手寫辨識。 <br/>                                              |
|  list                    | 列出所有符合其他選項的已安裝字典。<br/> 如果遺漏這個選項，則必須指定 [移除] 選項。<br/>                                                                                                                                                                                                                          |
|  remove                  | 提示移除任何符合其他選項的字典。<br/> 如果遺漏這個選項，則必須指定選項清單。<br/>                                                                                                                                                                                                                     |



 

### <a name="examples"></a>範例

以下列出的字典具有 language "英文 (US) " (en-us) 和輸入主要字典，而且只會針對目前的使用者進行安裝。

``` syntax
hwrreg -list -lang en-US -type PRIMARY-DICTIONARY
                  
```

同樣地，下列程式會移除符合相同準則的字典。

``` syntax
hwrreg -remove -lang en-US -type PRIMARY-DICTIONARY
                  
```

## <a name="general-notes-on-custom-dictionaries"></a>自訂字典的一般注意事項

-   如果您安裝兩個具有相同類型、語言和範圍的自訂字典，則第二個安裝將會覆寫第一個。
-   如果您安裝兩個具有相同類型和語言的自訂字典，但各有不同的範圍 (一個適用于所有使用者，另一個用於目前的使用者) ，則為目前使用者安裝的字典優先，而且會忽略針對所有使用者安裝的字典。

 

