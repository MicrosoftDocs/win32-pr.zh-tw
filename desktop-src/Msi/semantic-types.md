---
description: ModuleConfiguration 資料表的 Format、Type 和 CoNtextData 資料行中的下列專案會指定要取代為此資料表之 [名稱] 資料行中所指定的可設定專案之資訊的語義型別。
ms.assetid: f44e234e-b45a-40be-993d-956b8966c321
title: 語義類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 234e5dd929991c2ec5fecbc1d2d1bda72f4fbe52
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882642"
---
# <a name="semantic-types"></a>語義類型

[ModuleConfiguration 資料表](moduleconfiguration-table.md)的 Format、Type 和 CoNtextData 資料行中的下列專案會指定要取代為此資料表之 [名稱] 資料行中所指定的可設定專案之資訊的語義型別。

[文字格式類型](text-format-types.md)



| 格式 | 類型       | CoNtextData                                                 | 說明                                                                                                |
|--------|------------|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| Text   |            |                                                             | 任意文字。 請參閱 [任意文字類型](arbitrary-text-type.md)。                                        |
| Text   | 列舉       | <A>=<a>;<B>=<b>;&lt;C &gt; = &lt; c&gt; | 從集合中選取的值。 請參閱 [列舉類型](enum-type.md)。                                                 |
| Text   | 已格式化  |                                                             | 值符合安裝程式中格式化文字的定義。 請參閱 [格式化型](formatted-type.md)別。 |
| Text   | RTF        |                                                             | RTF 文字字串。 請參閱 [RTF 類型](rtf-type.md)。                                                          |
| Text   | 識別碼 |                                                             | 符合 Windows Installer[識別碼](identifier.md)的文字字串。                              |



 

[整數格式類型](integer-format-types.md)



| 格式  | 類型 | CoNtextData | 說明                                                                  |
|---------|------|-------------|------------------------------------------------------------------------------|
| 整數 |      |             | 任何整數值。 請參閱 [任意整數類型](arbitrary-integer-type.md)。 |



 

[索引鍵格式類型](key-format-types.md)



| 格式 | 類型      | CoNtextData      | 描述                                                                                                            |
|--------|-----------|------------------|------------------------------------------------------------------------------------------------------------------------|
| Key    | 檔案      | AssemblyCoNtext  | 讓使用者可以設定 Win32 或 common language runtime 元件的外鍵。 請參閱 [檔案類型](file-type.md)。 |
| 答案    | Binary    | 點陣圖           | 保存點陣圖以在 UI 中使用之二進位資料表資料列的外鍵。 請參閱 [二進位類型](binary-type.md)。                  |
| 答案    | Binary    | 圖示             | 二中繼資料表資料列的外鍵，其中包含要在 UI 中使用的圖示。 請參閱 [二進位類型](binary-type.md)。                   |
| 答案    | Binary    | EXE              | 保存32位 EXE 之二進位資料表資料列的外鍵。 請參閱 [二進位類型](binary-type.md)。                             |
| 答案    | Binary    | EXE64            | 保存32或64位 EXE 之二進位資料表資料列的外鍵。 請參閱 [二進位類型](binary-type.md)。                       |
| 答案    | 圖示      | ShortcutIcon     | 圖示表格資料列的外鍵，其中包含快速鍵使用的圖示。 請參閱 [圖示類型](icon-type.md)。                |
| 答案    | 對話    | DialogNext       | 對話方塊資料表資料列的外鍵。 請參閱 [對話方塊類型](dialog-type.md)。                                                 |
| 答案    | 對話    | DialogPrev       | 對話方塊資料表資料列的外鍵。 請參閱 [對話方塊類型](dialog-type.md)。                                                 |
| 答案    | 目錄 | IsolationDir     | 隔離的檔案所屬目錄資料表資料列的外鍵。 請參閱 [目錄類型](directory-type.md)。            |
| 答案    | 目錄 | ShortcutLocation | 要在其中安裝快捷方式的目錄資料表資料列的外鍵。 請參閱 [目錄類型](directory-type.md)。   |
| Key    | 屬性  |                  | 屬性資料列的外鍵。 請參閱 [屬性類型](property-type.md)。                                                 |
| Key    | 屬性  | 公開           | 屬性資料列的外鍵。 請參閱 [屬性類型](property-type.md)。                                                 |
| Key    | 屬性  | Private          | 屬性資料列的外鍵。 請參閱 [屬性類型](property-type.md)。                                                 |



 

[位欄位格式類型](bitfield-format-types.md)



| 格式   | 類型 | CoNtextData                                  | 描述                                                                                       |
|----------|------|----------------------------------------------|---------------------------------------------------------------------------------------------------|
| 字元 |      | &lt;mask &gt; ; <A> = <a> ; <B>= b | 變更資料行中的位子集。 查看 [任意](arbitrary-bitfield-type.md)位欄位類型。 |



 

 

 



