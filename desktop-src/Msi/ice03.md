---
description: ICE03 會根據 \_ .msi 檔案中的驗證資料表和資料庫資料表來驗證資料類型和外鍵。
ms.assetid: e9be1c09-8468-4956-9aa0-12383ade4718
title: ICE03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4814bb8023b32c85e752201909f77bd851ec3545c907c03e1c2349a34117d4e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946642"
---
# <a name="ice03"></a>ICE03

ICE03 會根據 .msi 檔案中的[ \_ 驗證資料表](-validation-table.md)和資料庫資料表來驗證資料類型和外鍵。

## <a name="result"></a>結果

ICE03 會張貼驗證錯誤的下列訊息。



| ICE03 錯誤訊息                                                       | 描述                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 重複的主鍵                                                     | 新資料列的主鍵會複製現有資料列的主鍵。 [ \_ 驗證資料表](-validation-table.md)中的可為 null 資料行，會顯示資料庫中的主鍵。                                                                                              |
| 不是可為 Null 的資料行                                                     | 在[ \_ 驗證資料表](-validation-table.md)中可為 null 的資料行中，未指定為 nullable 的資料表資料行包含的專案為 null。                                                                                                                                |
| 不是有效的外鍵                                                   | 第二個數據表中的外鍵資料行包含不存在於第二個數據表主鍵中的專案。                                                                                                                                                          |
| 值超過 int32.maxvalue                                                    | 資料庫資料表中專案的數值，超過[ \_ 驗證資料表](-validation-table.md)的 [int32.maxvalue] 資料行中為此欄位指定的最大限制。                                                                                                           |
| 值低於 MinValue                                                      | 資料庫資料表中專案的數值小於在[ \_ 驗證資料表](-validation-table.md)的 MinValue 資料行中為此欄位指定的最小限制。                                                                                                      |
| 值不是集合的成員                                             | 資料庫資料表中的專案值不是在[ \_ 驗證資料表](-validation-table.md)的 set 資料行中，為此欄位指定之可接受值集合的成員。                                                                                                  |
| 不正確版本字串                                                    | 請參閱 [版本](version.md) 資料類型。                                                                                                                                                                                                                                                 |
| 所有大寫都需要                                                   | 請參閱 [大寫](uppercase.md) 資料類型。                                                                                                                                                                                                                                             |
| 不正確 GUID 字串                                                       | 請參閱 [GUID](guid.md) 資料類型。                                                                                                                                                                                                                                                       |
| 萬用字元的檔案名/使用方式無效                                      | 資料庫包含不正確檔案名或不正確的萬用字元。 請參閱 [WildCardFilename](wildcardfilename.md) 資料類型。                                                                                                                                                          |
| 無效的識別碼                                                        | 請參閱 [識別碼](identifier.md) 資料類型。                                                                                                                                                                                                                                           |
| 不正確語言識別項                                                       | 資料庫包含不正確數位語言識別項 (LANGID) 。 請參閱 [Language](language.md) 資料類型。 請參閱 [語言識別項常數和字串](../intl/language-identifier-constants-and-strings.md)。 例如，1033適用于美國，而0代表非語言相關。<br/> |
| 不正確檔案名                                                          | 請參閱 [檔案名](filename.md) 資料類型。                                                                                                                                                                                                                                               |
| 不正確完整路徑                                                         | 查看 [路徑](path.md)、 [AnyPath](anypath.md)和 [路徑](paths.md) 資料類型。                                                                                                                                                                                                      |
| 錯誤的條件字串                                                    | 資料庫包含不正確條件字串。 這是一個文字字串，必須根據 [條件陳述式語法](conditional-statement-syntax.md)評估為 TRUE 或 FALSE。 請參閱 [Condition](condition.md) 資料類型。                                           |
| 不正確格式字串                                                     | 請參閱 [格式化](formatted.md) 的資料類型。                                                                                                                                                                                                                                             |
| 範本字串無效                                                   | 請參閱 [範本](template.md) 資料類型。                                                                                                                                                                                                                                               |
| 不正確 DefaultDir 字串                                                 | 請參閱 [DefaultDir](defaultdir.md) 資料類型。                                                                                                                                                                                                                                           |
| 登錄路徑無效                                                     | 請參閱 [RegPath](regpath.md) 資料類型。                                                                                                                                                                                                                                                 |
| 錯誤的 CustomSource 資料                                                     | 請參閱 [CustomSource](customsource.md) 資料類型。                                                                                                                                                                                                                                       |
| 不正確屬性字串                                                   | 請參閱 [屬性](property.md) 資料類型。                                                                                                                                                                                                                                               |
| \_驗證資料表或舊資料庫中遺漏資料                        | 資料庫中的資料行未列在 [ [ \_ 驗證] 資料表](-validation-table.md)的 [資料行] 資料行中。 資料庫與 \_ 驗證資料表不相符                                                                                                           |
| 錯誤的封包語法/名稱                                                   | 請參閱 [封 [包](cabinet.md) ] 資料類型。                                                                                                                                                                                                                                                 |
| \_驗證資料表：不正確分類字串                               | 這是撰寫驗證資料表時發生的錯誤 \_ 。 驗證無法辨識驗證資料表中這個特定資料行所使用的類別目錄字串 \_ 。 請參閱 [資料行資料類型](column-data-types.md) ，並指定有效的分類。                                           |
| \_驗證資料表： KeyTable 資料行中的資料不正確                  | 驗證資料表中的 KeyTable \_ 資料行所參考的資料表不存在於資料庫中。                                                                                                                                                                                     |
| \_驗證資料表：在 MinValue 資料行中，資料行中的值 < | 這是撰寫[ \_ 驗證資料表](-validation-table.md)時發生的錯誤。 Min 必須永遠小於或等於 Max。                                                                                                                                                              |
| 錯誤的快捷方式目標                                                       | 請參閱 [快速鍵](shortcut.md) 資料類型。                                                                                                                                                                                                                                               |
| 資料行) 中允許的字串溢位 (大於長度                 | 字串的長度大於資料行定義所指定的資料行寬度。 請注意，安裝程式不會在內部將資料行寬度限制為指定的值。 請參閱資料 [行定義格式](column-definition-format.md)。                                         |
| 未定義的錯誤                                                           | 未知的錯誤。                                                                                                                                                                                                                                                                            |
| 無法當地語系化資料行                                                | 主鍵資料行不可當地語系化。                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 
