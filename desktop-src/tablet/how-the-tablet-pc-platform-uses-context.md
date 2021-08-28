---
description: 建立平板電腦應用程式的開發人員可以利用輸入範圍和內容資訊。
ms.assetid: 74e4e4b2-6ceb-4044-84df-2fff0788267a
title: Tablet PC 平臺如何使用內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c586bf3ffcff8fc92b02bc0b4f5aff79c6bd0bbd66e6f048eab35a78d3be9676
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709278"
---
# <a name="how-the-tablet-pc-platform-uses-context"></a>Tablet PC 平臺如何使用內容

建立平板電腦應用程式的開發人員可以利用輸入範圍和內容資訊。 在應用程式中設定控制項內容資訊的最佳可能解決方案，取決於控制項是否為啟用筆墨，以及應用程式是否已發行至市場。 啟用筆墨的控制項是專為筆跡輸入而設計的控制項，其中的筆墨資料主要是以筆墨的方式收集和保存。 啟用筆墨的應用程式範例包括 Microsoft Windows 筆記本或草擬計畫。 在未啟用筆墨的控制項中，輸入資料會收集並保存為文字，通常是在 Tablet PC 上執行應用程式時使用 Tablet PC 輸入面板。 在控制項中啟用內容資訊的方案如下：

-   [SetInputScope](/windows/win32/api/inputscope/nf-inputscope-setinputscope) api：適用于非啟用筆墨的應用程式和控制項的低層級程式設計方案。 應用程式的二進位檔會受到影響，而且必須重新散發。
-   [**RecognizerCoNtext**](inkrecognizercontext-class.md)物件的「[**智慧**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)標記」和「[**單詞表**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)」屬性：適用于應用程式的程式設計解決方案，此方案具有啟用筆墨的控制項。 應用程式的二進位檔會受到影響，而且必須重新散發。

Tablet PC 輸入面板已從 Windows Vista 開始更新，以利用您在使用[SetInputScope](/windows/win32/api/inputscope/nf-inputscope-setinputscope) api 時所提供的內容資訊。 下表提供哪些 Microsoft 辨識引擎支援哪些輸入範圍的詳細資料。 輸入範圍的資料列中的 "X" 表示該資料行中的辨識器支援輸入範圍。



| 屬性名稱                                     | 英文 (美國) | 英文 (英國) | 德文       | 法文       | 日文     | 韓文       | 簡體中文 | 繁體中文 |
|---------------------------------------------------|-------------------------|--------------------------|--------------|--------------|--------------|--------------|----------------------|-----------------------|
| **為 \_ ADDRESS \_ FULLPOSTALADDRESS**<br/>     | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是 \_ 位址 \_ 郵遞區號**<br/>            | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_位址 \_ 街道**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **為 \_ ADDRESS \_ STATEORPROVINCE**<br/>       | X<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是 \_ 位址 \_ 城市**<br/>                  | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **為 \_ ADDRESS \_ COUNTRYNAME**<br/>           | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **為 \_ ADDRESS \_ COUNTRYSHORTNAME**<br/>      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是 \_ CURRENCY \_ AMOUNTANDSYMBOL**<br/>      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **為 \_ 貨幣 \_ 金額**<br/>               | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是 \_ 日期 \_ FULLDATE**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是 \_ 日期 \_ 月份**<br/>                    | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是 \_ 日期 \_ 日**<br/>                      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是 \_ 日期 \_ 年份**<br/>                     | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是 \_ 日期 \_ MONTHNAME**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是 \_ 日期 \_ DAYNAME**<br/>                  | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **為 \_ 預設值**<br/>                        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是 \_ 電子郵件使用者 \_ 名稱**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是 \_ 電子郵件 \_ SMTPEMAILADDRESS**<br/>        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是 \_ FILE \_ FULLFILEPATH**<br/>             | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是 \_ 檔案名 \_**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **為 \_ LOGINNAME**<br/>                      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是 \_ 數位**<br/>                         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是 \_ 數位**<br/>                         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **為 \_ ONECHAR**<br/>                        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是 \_ 密碼**<br/>                       | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **為 \_ PERSONALNAME \_ FULLNAME**<br/>         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **為 \_ PERSONALNAME \_ 前置詞**<br/>           | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是 \_ PERSONALNAME \_ GIVENNAME**<br/>        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是 \_ PERSONALNAME \_ MIDDLENAME**<br/>       | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是 \_ PERSONALNAME \_ 姓氏**<br/>          | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **為 \_ PERSONALNAME \_ 尾碼**<br/>           | X<br/>            | -<br/>             | X<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是否為 \_ 電話 \_ FULLTELEPHONENUMBER**<br/> | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是否為 \_ 電話 \_ COUNTRYCODE**<br/>         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是否為 \_ 電話 \_ AREACODE**<br/>            | X<br/>            | X<br/>             | X<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是否為 \_ 電話 \_ LOCALNUMBER**<br/>         | X<br/>            | X<br/>             | X<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是 \_ TIME \_ SUBSCRIPTION**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是 \_ 時間 \_ 小時**<br/>                     | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是 \_ TIME \_ MINORSEC**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是 \_ URL**<br/>                            | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是 \_ 數位 \_ 全形**<br/>              | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是英 \_ 數位元 \_ 半形**<br/>        | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是英 \_ 數位元 \_**<br/>        | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是 \_ 貨幣 \_ 中文**<br/>              | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **為 \_ 注音**<br/>                       | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **為 \_ 平假名**<br/>                       | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是 \_ 片假名 \_ 半形**<br/>            | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **為 \_ 片假名 \_ 全形**<br/>            | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **是 \_ 漢字**<br/>                          | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |



 

使用 [SetInputScope](/windows/win32/api/inputscope/nf-inputscope-setinputscope) Api 或 [**RecognizerCoNtext**](inkrecognizercontext-class.md) 物件的「 [**模擬**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) 」屬性來設定內容時，若嘗試針對該語言的辨識器不支援的語言設定輸入範圍，則會導致「Tablet PC 輸入面板」使用預設語言模型做為控制項的內容。 例如，法文辨識器不支援 **\_ 位址 \_ STATEORPROVINCE** 輸入範圍。 如果您將欄位上的內容設定為

`(!IS_ADDRESS_STATEORPROVINCE)|(!IS_ADDRESS_POSTALCODE)`

使用法文辨識器時，產生的內容是預設的語言模型。 若要避免這個問題，請偵測使用中辨識器的語言，並據以設定輸入範圍。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[InputScope 列舉](/windows/win32/api/inputscope/ne-inputscope-inputscope)
</dt> </dl>

 

