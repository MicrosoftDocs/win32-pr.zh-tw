---
description: 本主題說明 Windows Search 如何支援多種語言。
ms.assetid: a800d2ac-3aee-4e74-a29a-a70355138ebc
title: Windows Search 支援的語言
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 350a8861a5817a8ac5710214ccd35c780f2c9dd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689895"
---
# <a name="languages-supported-by-windows-search"></a>Windows Search 支援的語言

本主題說明 Windows Search 如何支援多種語言。

## <a name="tokenization-wordbreakers-and-language-resources"></a>Token 化、文字分隔和語言資源

Windows Search 與語言無關，但是跨語言搜尋的精確度可能因文字分隔 token 化文字的方式而有所不同。 文字分隔會針對語言執行各種 token 化規則，並將文字分成個別的權杖或單字，以進行編制索引或搜尋。

索引文字和查詢字串的語言都會分成標記。 由於 token 化規則會因語言而異，因此每個語言或語言系列都有個別的文字分隔。 如果查詢語言與索引語言不相符，則結果可能無法預測。

Windows Search 隨附一組妥善定義的文字分隔。 Windows Vista 和更新版本支援傳統的斷詞工具和字幹分析器元件。 如果無法判斷檔的語言，Windows Search 會嘗試偵測語言以找出最適當的斷詞工具。 Windows Search 嘗試偵測語言，方法是呼叫 [**GetSystemPreferredUILanguages**](/windows/win32/api/winnls/nf-winnls-getsystempreferreduilanguages) 函式來判斷前多個消費者介面 (的 mui) 語言 (通常是系統 UI 語言，除非) 安裝 MUI 語言套件。 如果該呼叫成功，則會使用第一個 MUI 語言的斷詞工具。 如果呼叫 **GetSystemPreferredUILanguages** 失敗，Windows Search 會呼叫 [**GetSystemDefaultLCID**](/windows/win32/api/winnls/nf-winnls-getsystemdefaultlcid) 函式，並使用與該地區設定相關聯的斷詞工具，藉以抓取系統地區設定。

如果未安裝語言的斷詞工具，Windows Search 使用 **中性** 的斷詞工具來中斷空白字元。

您可以透過登錄移除語言，如下列範例所示。

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            ContentIndex
               Language
                  Dutch_Dutch
                     (Default)
                     Locale
                     NoiseFile
                     StemmerClass = CLSID
                     WBreakerClass = CLSID
```

> [!TIP]
> 如果您對登錄進行變更，請重新開機 Windows Search。

 

當 Windows Search 需要新的斷詞工具時，會讀取 (CLSID) 的類別識別碼，並快取具現化的斷詞工具。

您可以藉由執行 [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) 介面，建立語言的自訂斷詞工具。 Windows Search 接著會在建立內容索引和執行查詢時，呼叫 **IWordBreaker** 方法。

索引內容的地區設定資訊是從內容來源抓取。 如果來源實施者不知道已編制索引之內容的地區設定，則應該將地區設定設定為 [**\_ 中性地區**](../intl/locale-neutral.md)設定。

例如，如果您 () 、屬性處理常式或通訊協定處理常式的 [**IFilter**](https://www.bing.com/search?q=**IFilter**) 介面執行的篩選處理常式，則應該將已編制索引的內容地區設定設定為 [**\_ 中性地區**](../intl/locale-neutral.md) 設定，除非您有特定的地區設定資訊，並確信其精確度。

> [!TIP]
> 如果索引查詢是以使用者輸入為基礎，則地區設定應該符合使用者輸入的語言。 您可以藉由呼叫 [**GetKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout) 函數來判斷此地區設定。

 

## <a name="languages-supported-by-wordbreakers"></a>文字分隔支援的語言

Windows Search 包含支援下列語言的文字分隔。



| 登錄機碼             | Language (語言)                             | LCID   |
|--------------------------|---------------------------------------------------|--------|
| **阿拉伯文 \_ SaudiArabia**  | 阿拉伯文 (中性)                                   | 0x0001 |
| **孟加拉國文 \_ 預設值**     | 中立 (中性)                                   | 0x0045 |
| **保加利亞文 \_ 預設**   | 保加利亞文 (保加利亞)                              | 0x0402 |
| **加泰羅尼亞文 \_ 預設**     | 加泰蘭文 (加泰蘭)                                 | 0x0403 |
| **中文 \_ HongKong**    | 中文 (香港特別行政區、中國)                      | 0x0C04 |
| **簡體中文 \_**  | 簡體中文                              | 0x0804 |
| **繁體中文 \_** | 繁體中文                             | 0x0404 |
| **克羅地亞 \_ 預設值**    | 克羅埃西亞文 (克羅埃西亞)                                | 0x041A |
| **捷克文 \_ 預設值**       | 捷克文 (捷克共和國)                            | 0x0405 |
| **丹麥文 \_ 預設值**      | 丹麥文 (丹麥)                                  | 0x0406 |
| **荷蘭文 \_ 荷蘭文**         | 荷蘭文 (荷蘭)                               | 0x0413 |
| **英文 \_ UK**          | 英文 (英國)                          | 0x0809 |
| **\_美國英文**          | 英文 (美國)                           | 0x0409 |
| **芬蘭文 \_ 預設值**     | 芬蘭文 (芬蘭)                                 | 0x040B |
| **法文 \_ 法文**       | 法文 (法國)                                   | 0x040C |
| **德文 \_ 德文**       | 德文 (德國)                                  | 0x0407 |
| **希臘文 \_ 預設**       | 希臘文 (希臘)                                    | 0x0408 |
| **古吉拉特文 \_ 預設**    | 古吉拉特文 (印度)                                  | 0x0447 |
| **希伯來文 \_ 預設值**      | 希伯來文 (中性)                                   | 0x000D |
| **印度文 \_ 預設值**       | 印度文 (印度)                                     | 0x0439 |
| **匈牙利文 \_ 預設值**   | 匈牙利文 (匈牙利)                               | 0x040E |
| **冰島文 \_ 預設**   | 冰島文 (冰島)                               | 0x040F |
| **印尼文 \_ 預設**  | 印尼文 (印尼)                            | 0x0421 |
| **義大利文 \_ 義大利文**     | 義大利文 (義大利)                                   | 0x0410 |
| **日文 \_ 預設值**    | 日文 (日本)                                  | 0x0411 |
| **德文 \_ 預設值**     | 坎那達文 (印度)                                   | 0x044B |
| **韓文 \_ 預設值**      | 韓文 (韓國)                                    | 0x0412 |
| **拉脫維亞文 \_ 預設值**     | 拉脫維亞文 (拉脫維亞)                                  | 0x0426 |
| **立陶宛文 \_ 預設值**  | 立陶宛文 (立陶宛文)                            | 0x0427 |
| **馬來 \_ 馬來西亞**      | 馬來文 (馬來西亞)                                  | 0x043E |
| **馬拉雅德的 \_ 預設值**   | 馬拉雅德 (中性)                                | 0x004C |
| **馬拉地文的 \_ 預設值**     | 馬拉提文 (印度)                                   | 0x044E |
| **挪威文 \_ 博克瑪律文**    | 挪威文 (巴克摩，挪威)                        | 0x0414 |
| **波蘭文 \_ 預設值**      | 波蘭文 (波蘭)                                   | 0x0415 |
| **葡萄牙文 \_ 葡萄牙文** | 葡萄牙文 (葡萄牙)                             | 0x0816 |
| **巴西葡萄牙文 \_**   | 葡萄牙文 (巴西)                               | 0x0416 |
| **旁遮普文 \_ 預設值**     | 旁遮普語 (印度)                                   | 0x0446 |
| **羅馬尼亞文 \_ 預設值**    | 羅馬尼亞文 (羅馬尼亞)                                | 0x0418 |
| **俄文 \_ 預設**     | 俄文 (中性)                                  | 0x0019 |
| **塞爾維亞 \_ 文（斯拉夫）**    | 塞爾維亞文 (塞爾維亞和黑山，之前的斯拉夫文)  | 0x0C1A |
| **塞爾維亞文 \_ 拉丁文**       | 塞爾維亞文 (塞爾維亞和黑山、前、拉丁)     | 0x081A |
| **斯洛伐克文 \_ 預設**      | 斯洛伐克文 (斯洛伐克)                                 | 0x041B |
| **斯洛維尼亞 \_ 預設值**   | 斯洛維尼亞文 (斯洛維尼亞)                              | 0x0424 |
| **西班牙文 \_ 新式**      | 西班牙文 (西班牙，新式排序)                       | 0x0C0A |
| **瑞典文 \_ 預設值**     | 瑞典文 (瑞典)                                  | 0x041D |
| **泰米爾 \_ 預設值**       | 坦米爾文 (印度)                                     | 0x0449 |
| **泰泰 \_ 預設值**      | 特拉古文 (印度)                                    | 0x044A |
| **泰文 \_ 預設值**        | 泰文 (泰國)                                   | 0x041E |
| **土耳其文 \_ 預設值**     | 土耳其文 (土耳其)                                  | 0x041F |
| **烏克蘭 \_ 預設值**   | 烏克蘭文 (烏克蘭)                               | 0x0422 |
| **烏爾 \_ 預設值**        | 烏都文 (巴基斯坦)                                   | 0x0420 |
| **越南文 \_ 預設值**  | 越南文 (越南)                              | 0x042A |



 

> [!Note]  
> 資料表中某些語言的 Lcid 是使用語言識別項、語言識別項和排序識別碼來產生的。

 

如需語言和相關識別碼的詳細資訊，請參閱 [語言識別項常數和字串](../intl/language-identifier-constants-and-strings.md)。

> [!Note]  
> 不保證所有這些語言登錄機碼都會出現在任何指定的電腦上。 視使用者的設定而定，任何給定語言的斷詞工具可能會安裝或可能不會安裝在電腦上。

 

**從 Windows 8.1 開始**，使用文字分隔的慣用方法是透過 WinRT API [**WordsSegmenter 類別**](/uwp/api/Windows.Data.Text.WordsSegmenter?view=winrt-19041)。

## <a name="additional-resources"></a>其他資源

-   如需有關如何針對其他語言和地區設定執行和使用自訂斷詞工具和字幹分析器的詳細資訊，請參閱 [Windows Search 中的擴充語言資源](extending-language-resources-in-windows-search.md)。
-   如果您需要識別某段文字的語言，您可以使用 Windows 7 和更新版本中提供的語言自動偵測 (LAD) 。 如需詳細資訊，請參閱 (ELS) 的 [擴充語言服務](../intl/extended-linguistic-services.md) 。
-   如需有關管理、查詢和擴充索引的詳細資訊，請參閱《 [Windows Search 開發人員指南》](-search-developers-guide-entry-page.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Search 概觀](-search-3x-wds-overview.md)
</dt> <dt>

[Windows Search 做為開發平台](-search-3x-wds-development-ovr.md)
</dt> <dt>

[搭配 Shell 資料和 Windows Search 使用 Managed 程式碼](-search-3x-wds-managed-code.md)
</dt> </dl>

 

 
