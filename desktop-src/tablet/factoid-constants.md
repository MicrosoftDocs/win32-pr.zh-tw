---
description: 定義常數位符串值，藉由提供內容相關資訊給辨識器，來增加辨識的精確度。
ms.assetid: 247a1f7d-8205-4e4d-9cfc-daad9bd2191f
title: " (Msinkaut 的) 的模擬模擬常數"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa748c84f8bd39f18f83e1ec72474bcfbe3017f2
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883677"
---
# <a name="factoid-constants"></a>模擬常數

定義常數位符串值，藉由提供內容相關資訊給辨識器，來增加辨識的精確度。




| Name | 說明 | 
|------|-------------|
| <span id="FACTOID_NONE"></span><span id="factoid_none"></span><dl><dt><strong>FACTOID_NONE</strong></dt></dl> | 停用所有其他 factoids 和字典。<br /> | 
| <span id="___________FACTOID_DEFAULT_________"></span><span id="___________factoid_default_________"></span><dl><dt><strong>FACTOID_DEFAULT</strong></dt></dl> | 西方語言的 factoids 預設設定包括系統字典、使用者字典、各種標點符號，以及 Web 和數位的模擬。 東亞語言的 factoids 預設設定包含辨識器支援的所有字元。 <br /> | 
| <span id="___________FACTOID_SYSTEMDICTIONARY_________"></span><span id="___________factoid_systemdictionary_________"></span><dl><dt><strong>FACTOID_SYSTEMDICTIONARY</strong></dt></dl> | 指出辨識器僅使用系統字典。<br /> | 
| <span id="___________FACTOID_WORDLIST_________"></span><span id="___________factoid_wordlist_________"></span><dl><dt><strong>FACTOID_WORDLIST</strong></dt></dl> | 指示辨識器使用以程式設計方式定義的單字清單。 單字清單是由<a href="inkrecognizercontext-class.md"><strong>InkRecognizerCoNtext</strong></a>物件的 [<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist"><strong>單詞表</strong></a>] 屬性所定義。 <br /><blockquote>[!Note]<br />如果將字串加入至字組清單，也會隱含地加入其大寫版本。 例如，加入 "hello" 會隱含地加入 "Hello" 和 "HELLO"。</blockquote><br /> | 
| <span id="___________FACTOID_EMAIL_________"></span><span id="___________factoid_email_________"></span><dl><dt><strong>FACTOID_EMAIL</strong></dt></dl> | 指示辨識器尋找電子郵件地址。<br /><blockquote>[!Note]<br />此模擬程式必須使用完整的電子郵件地址，例如 " someone@example.com "。 無法辨識獨立的別名，例如「某人」。</blockquote><br /><pre class="syntax" data-space="preserve"><code>someone@example.com</code></pre> | 
| <span id="FACTOID_WEB"></span><span id="factoid_web"></span><dl><dt><strong>FACTOID_WEB</strong></dt></dl> | 指示辨識器尋找網址。<br /><pre class="syntax" data-space="preserve"><code>`https://www.adatum.com`</code></pre> | 
| <span id="___________FACTOID_ONECHAR_________"></span><span id="___________factoid_onechar_________"></span><dl><dt><strong>FACTOID_ONECHAR</strong></dt></dl> | 指示辨識器尋找單一字元。<br /><blockquote>[!Note]<br />此模擬程式會尋找任何隔離的 ANSI 字元。</blockquote><br /> | 
| <span id="___________FACTOID_NUMBER_________"></span><span id="___________factoid_number_________"></span><dl><dt><strong>FACTOID_NUMBER</strong></dt></dl> | 指示辨識器尋找數位。<br /><blockquote>[!Note]<br />數值包含分隔符號、小數、序數和其他常用的數位記號。</blockquote><br /> | 
| <span id="___________FACTOID_DIGIT_________"></span><span id="___________factoid_digit_________"></span><dl><dt><strong>FACTOID_DIGIT</strong></dt></dl> | 指出辨識器要尋找單一位數（0到9）。<br /><pre class="syntax" data-space="preserve"><code>0, 1, 2, 3, 4, 5, 6, 7, 8, 9</code></pre> | 
| <span id="___________FACTOID_NUMBERSIMPLE_________"></span><span id="___________factoid_numbersimple_________"></span><dl><dt><strong>FACTOID_NUMBERSIMPLE</strong></dt></dl> | 提供簡單的數值內容給辨識器。<br /><blockquote>[!Note]<br />此版本的 Tablet PC SDK 不支援此模擬。</blockquote><br /> | 
| <span id="___________FACTOID_CURRENCY_________"></span><span id="___________factoid_currency_________"></span><dl><dt><strong>FACTOID_CURRENCY</strong></dt></dl> | 指示辨識器尋找表示貨幣值的字元。<br /><pre class="syntax" data-space="preserve"><code>$45.95,  60,  50.25,  3000</code></pre> | 
| <span id="___________FACTOID_POSTALCODE_________"></span><span id="___________factoid_postalcode_________"></span><dl><dt><strong>FACTOID_POSTALCODE</strong></dt></dl> | 指示辨識器尋找郵遞區號。<br /><pre class="syntax" data-space="preserve"><code>98112</code></pre> | 
| <span id="___________FACTOID_PERCENT_________"></span><span id="___________factoid_percent_________"></span><dl><dt><strong>FACTOID_PERCENT</strong></dt></dl> | 指示辨識器尋找百分比。<br /><pre class="syntax" data-space="preserve"><code>87%</code></pre> | 
| <span id="___________FACTOID_DATE_________"></span><span id="___________factoid_date_________"></span><dl><dt><strong>FACTOID_DATE</strong></dt></dl> | 指示辨識器尋找表示日期的字元。<br /><pre class="syntax" data-space="preserve"><code>10/30/2001, '01, 31/12, 12/99, 1999-2000</code></pre> | 
| <span id="___________FACTOID_TIME_________"></span><span id="___________factoid_time_________"></span><dl><dt><strong>FACTOID_TIME</strong></dt></dl> | 指示辨識器尋找表示時間的字元。<br /><pre class="syntax" data-space="preserve"><code>12:23:00 PM, 12:30, 24:30, 12:23:01, 1:12 A.M.</code></pre> | 
| <span id="___________FACTOID_TELEPHONE_________"></span><span id="___________factoid_telephone_________"></span><dl><dt><strong>FACTOID_TELEPHONE</strong></dt></dl> | 指出辨識器尋找代表電話號碼的字元。<br /><pre class="syntax" data-space="preserve"><code>123 555 0190, 0-123-206 555 0190, (206)555-0190</code></pre> | 
| <span id="___________FACTOID_FILENAME_________"></span><span id="___________factoid_filename_________"></span><dl><dt><strong>FACTOID_FILENAME</strong></dt></dl> | 指示辨識器尋找表示檔案名的字元。<br /><pre class="syntax" data-space="preserve"><code>mydocument.doc, c:\myfolder\file.c</code></pre> | 
| <span id="___________FACTOID_UPPERCHAR_________"></span><span id="___________factoid_upperchar_________"></span><dl><dt><strong>FACTOID_UPPERCHAR</strong></dt></dl> | 指出辨識器要尋找單一大寫字元： A 到 Z。<br /> | 
| <span id="___________FACTOID_LOWERCHAR_________"></span><span id="___________factoid_lowerchar_________"></span><dl><dt><strong>FACTOID_LOWERCHAR</strong></dt></dl> | 指出辨識器要尋找單一小寫字元： A 到 Z。<br /><blockquote>[!Note]<br />此版本的 Tablet PC SDK 不支援此模擬。</blockquote><br /> | 
| <span id="___________FACTOID_PUNCCHAR_________"></span><span id="___________factoid_puncchar_________"></span><dl><dt><strong>FACTOID_PUNCCHAR</strong></dt></dl> | 指示辨識器尋找標點符號字元。<br /><blockquote>[!Note]<br />此版本的 Tablet PC SDK 不支援此模擬。</blockquote><br /> | 
| <span id="FACTOID_JAPANESECOMMON"></span><span id="factoid_japanesecommon"></span><dl><dt><strong>FACTOID_JAPANESECOMMON</strong></dt></dl> | 指示辨識器尋找常用的日文漢字、片假名和平假名字元。<br /> | 
| <span id="FACTOID_CHINESESIMPLECOMMON"></span><span id="factoid_chinesesimplecommon"></span><dl><dt><strong>FACTOID_CHINESESIMPLECOMMON</strong></dt></dl> | 指出辨識器尋找常用的簡體中文字元。<br /> | 
| <span id="FACTOID_CHINESETRADITIONALCOMMON"></span><span id="factoid_chinesetraditionalcommon"></span><dl><dt><strong>FACTOID_CHINESETRADITIONALCOMMON</strong></dt></dl> | 指出辨識器會尋找常用的繁體中文字元。<br /> | 
| <span id="FACTOID_KOREANCOMMON"></span><span id="factoid_koreancommon"></span><dl><dt><strong>FACTOID_KOREANCOMMON</strong></dt></dl> | 指示辨識器尋找常用的韓文字元。<br /> | 
| <span id="FACTOID_HIRAGANA"></span><span id="factoid_hiragana"></span><dl><dt><strong>FACTOID_HIRAGANA</strong></dt></dl> | 指出辨識器只尋找平假名字元。<br /> | 
| <span id="FACTOID_KATAKANA"></span><span id="factoid_katakana"></span><dl><dt><strong>FACTOID_KATAKANA</strong></dt></dl> | 指出辨識器只尋找片假名字元。<br /> | 
| <span id="FACTOID_KANJICOMMON"></span><span id="factoid_kanjicommon"></span><dl><dt><strong>FACTOID_KANJICOMMON</strong></dt></dl> | 指示辨識器尋找常用的中文字元。<br /> | 
| <span id="FACTOID_KANJIRARE"></span><span id="factoid_kanjirare"></span><dl><dt><strong>FACTOID_KANJIRARE</strong></dt></dl> | 指出辨識器尋找很少使用的中文字元。<br /><blockquote>[!Note]<br />此版本的 Tablet PC SDK 不支援此模擬。</blockquote><br /> | 
| <span id="FACTOID_BOPOMOFO"></span><span id="factoid_bopomofo"></span><dl><dt><strong>FACTOID_BOPOMOFO</strong></dt></dl> | 指示辨識器尋找注音字元。<br /> | 
| <span id="FACTOID_JAMO"></span><span id="factoid_jamo"></span><dl><dt><strong>FACTOID_JAMO</strong></dt></dl> | 指示辨識器尋找韓文相容性拼音字母字元。<br /> | 
| <span id="FACTOID_HANGULCOMMON"></span><span id="factoid_hangulcommon"></span><dl><dt><strong>FACTOID_HANGULCOMMON</strong></dt></dl> | 指示辨識器尋找常用的韓文字元。<br /> | 
| <span id="FACTOID_HANGULRARE"></span><span id="factoid_hangulrare"></span><dl><dt><strong>FACTOID_HANGULRARE</strong></dt></dl> | 指出辨識器尋找很少使用的韓文字元。<br /><blockquote>[!Note]<br />此版本的 Tablet PC SDK 不支援此模擬。</blockquote><br /> | 




## <a name="remarks"></a>備註

在 c + + 中，您可以在 Msinkaut .h 標頭檔中存取這些常數， &lt; &gt; \\ 如果您將 SDK 安裝在預設位置，該檔案位於 Systemdrive： Program FILES \\ MICROSOFT Tablet PC Platform SDK \\ Include 目錄。

> [!Note]  
> 這些常數都是 WCHARs，而不是 Bstr。 必須先將它們轉換成 Bstr，才能做為物件方法的參數使用。 如需 BSTR 資料類型的詳細資訊，請參閱 [使用 COM 程式庫](using-the-com-library.md)。

 

> [!Note]  
> 若為拉丁腳本的辨識器，則會針對回溯相容性提供此類別中定義的 factoids。 針對新的開發，建議您使用 [SetInputScope](/windows/desktop/api/inputscope/nf-inputscope-setinputscope) 函數中定義的值。 如需詳細資訊，請參閱 [使用內容改善精確度](using-context-to-improve-accuracy.md)。

 

您可以使用這些識別碼來指定辨識期間應使用的模擬。

下列 factoids 組合僅支援西方語言。 這些都沒有不同的定義，但可以接受使用 factoids 之物件的「 [**模擬**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) 」屬性的字串常值輸入。 這些模擬型字串常數允許輸入符合運算式中的任何 factoids。



| 合併               | 定義                                                |
|---------------------------|-----------------------------------------------------------|
| "WEB \| 單詞表"           | Web 模擬或字組清單。                         |
| "EMAIL \| 單詞表"         | 電子郵件的智慧標籤或字組清單。                       |
| "FILENAME \| WEB \| 單詞表" | 檔案名模擬或 Web 模擬或字組清單。 |



 

如果您使用 [InkEdit](inkedit-control-reference.md) 控制項，則可以將模擬程式設定為控制項的屬性。

如果您使用 Tablet PC 平臺 Api，您可以在 [**InkRecognizerCoNtext**](inkrecognizercontext-class.md)物件上設定 [**模擬**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)程式屬性。

或者，您可以使用實際的「模擬」字串常數來設定這個屬性。

> [!Note]  
> 模擬型字串常數會區分大小寫。 如需 factoids 及其使用方式的詳細資訊，請參閱使用內容 [改善精確度](using-context-to-improve-accuracy.md)。 若要判斷是否有特定語言的模擬程式，請參閱 [第1版所支援的 Factoids](supported-factoids-from-version-1.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**模擬屬性 \[ InkRecognizeCoNtext 類別\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)
</dt> <dt>

[**模擬屬性 \[ PenInputPanel 類別\]**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)
</dt> <dt>

[**模擬的屬性 \[ InkEdit 控制項\]**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)
</dt> <dt>

[使用內容改善精確度](using-context-to-improve-accuracy.md)
</dt> <dt>

[從版本1支援的 Factoids](supported-factoids-from-version-1.md)
</dt> </dl>

 

