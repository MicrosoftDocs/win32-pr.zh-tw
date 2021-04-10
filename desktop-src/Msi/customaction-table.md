---
description: CustomAction 資料表提供將自訂程式碼和資料整合至安裝的方法。 所執行程式碼的來源可以是包含在資料庫內的資料流程、最近安裝的檔案，或現有的可執行檔。
ms.assetid: 0f47abc1-4e06-4ddc-9ea1-9afb9f27d499
title: CustomAction 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c8cbfa6500743e2a2ad89627447da1907f6f48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690839"
---
# <a name="customaction-table"></a>CustomAction 資料表

CustomAction 資料表提供將自訂程式碼和資料整合至安裝的方法。 所執行程式碼的來源可以是包含在資料庫內的資料流程、最近安裝的檔案，或現有的可執行檔。

CustomAction 資料表具有下列資料行。



| Column       | 類型                               | 答案 | Nullable |
|--------------|------------------------------------|-----|----------|
| 動作       | [識別碼](identifier.md)       | Y   | N        |
| 類型         | [整數](integer.md)             | N   | N        |
| 來源       | [CustomSource](customsource.md)   | N   | Y        |
| 目標       | [格式 化](formatted.md)         | N   | Y        |
| ExtendedType | [DoubleInteger](doubleinteger.md) | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>行動
</dt> <dd>

動作的名稱。 此動作通常會出現在順序資料表中，除非由另一個自訂動作呼叫。 如果名稱符合任何內建的動作，則永遠不會呼叫自訂動作。

主表索引鍵。

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>類型
</dt> <dd>

旗標位的欄位，指定自訂動作和選項的基本類型。 如需基本類型清單，請參閱 [所有自訂動作類型的摘要清單](summary-list-of-all-custom-action-types.md) 。 請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)、 [自訂動作執行排程選項](custom-action-execution-scheduling-options.md)、 [自訂動作隱藏目標選項](custom-action-hidden-target-option.md)，以及 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)。

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>源
</dt> <dd>

另一個資料表中的屬性名稱或外部索引鍵。 如需可能的自訂動作來源的討論，請參閱 [自訂動作來源](custom-action-sources.md) 和 [所有自訂動作類型的摘要清單](summary-list-of-all-custom-action-types.md)。 例如，來源資料行可能會在下列其中一個資料表的第一個資料行中包含一個外部索引鍵，其中包含自訂動作程式碼的來源。

用來呼叫現有可執行檔的[目錄資料表](directory-table.md)。

用來呼叫剛剛安裝之可執行檔和 Dll 的檔案[資料表](file-table.md)。

用於呼叫可執行檔、Dll 和儲存在資料庫中之資料的[二進位資料表](binary-table.md)。

[屬性工作表](property-table.md) ，用於呼叫屬性所持有之路徑的可執行檔。

</dd> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>目標
</dt> <dd>

視自訂動作的基本類型而定的執行參數。 如需每個自訂動作類型的說明，請參閱 [所有自訂動作類型的摘要清單](summary-list-of-all-custom-action-types.md) 。 例如，根據自訂動作而定，此欄位可能包含下列各項。



| 目標                                    | 自訂動作                         |
|-------------------------------------------|---------------------------------------|
| 需要 (進入點)                     | 呼叫 DLL。                        |
| 具有引數 (必要) 的可執行檔名稱 | 呼叫現有的可執行檔。       |
| 命令列引數 (選擇性)          | 呼叫剛剛安裝的可執行檔。 |
| 目的檔案名 (必要)                | 從自訂資料建立檔案。     |
| Null                                      | 執行腳本。                |



 

</dd> <dt>

<span id="ExtendedType"></span><span id="extendedtype"></span><span id="EXTENDEDTYPE"></span>ExtendedType
</dt> <dd>

在此欄位中輸入 **msidbCustomActionTypePatchUninstall** 值，以使用 [自訂動作修補程式卸載選項](custom-action-patch-uninstall-option.md)來指定自訂動作。

**[Windows Installer 4.0 及更早版本](not-supported-in-windows-installer-4-0.md)：** 不支援。 從 Windows Installer 4.5 開始，可以使用此選項。

</dd> </dl>

如需詳細資訊，請參閱 [自訂動作](custom-actions.md)底下的所有主題。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE12](ice12.md)  
[ICE27](ice27.md)  
[ICE46](ice46.md)  
[ICE63](ice63.md)  
[ICE68](ice68.md)  
[ICE72](ice72.md)  
[ICE75](ice75.md)  
[ICE77](ice77.md)  
[ICE80](ice80.md)  
[ICE88](ice88.md)  
[ICE93](ice93.md)  
</dl>

 

 



