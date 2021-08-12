---
description: 下表將識別自訂動作的基本類型，並顯示每個類型之 CustomAction 資料表的 [類型]、[來源] 和 [目標] 欄位中的值。
ms.assetid: 8713451e-c0e7-4bec-bfb6-dfe4125d5a44
title: 自訂動作類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf0be8a9465c9a3567a867bab911d7539e8700219515c86bb5a8fc2b7d5eff68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624303"
---
# <a name="custom-action-types"></a>自訂動作類型

下表將識別自訂動作的基本類型，並顯示每個類型之 [CustomAction](customaction-table.md) 資料表的 [類型]、[來源] 和 [目標] 欄位中的值。 您可以在類型資料行中包含選擇性旗標位，以修改基本自訂動作。 如需選項和值的描述，請參閱下列各項：

-   [自訂動作傳回處理選項](custom-action-return-processing-options.md)
-   [自訂動作執行排程選項](custom-action-execution-scheduling-options.md)
-   [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)
-   [自訂動作修補卸載選項](custom-action-patch-uninstall-option.md)

使用基本自訂動作類型的連結，以取得描述和每種類型可用的選項。



| 基本自訂動作類型                                                                                                                           | 類型 | 來源                                                                                                                              | 目標                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [自訂動作類型 1](custom-action-type-1.md)儲存在二進位資料表資料流程中的 DLL 檔案。<br/>                                               | 1    | [二元](binary-table.md)資料表的索引鍵。                                                                                            | DLL 進入點。                                                                                                                           |
| [自訂動作類型 2](custom-action-type-2.md)儲存在二進位資料表資料流程中的 EXE 檔案。<br/>                                               | 2    | [二元](binary-table.md)資料表的索引鍵。                                                                                            | 命令列字串。                                                                                                                       |
| [自訂動作類型 5](custom-action-type-5.md)JScript 儲存在二進位資料表資料流程中的檔案。<br/>                                           | 5    | [二元](binary-table.md)資料表的索引鍵。                                                                                            | 可以呼叫的選擇性 JScript 函數。                                                                                           |
| [自訂動作類型 6](custom-action-type-6.md)儲存在二進位資料表資料流程中的 VBScript 檔案。<br/>                                          | 6    | [二元](binary-table.md)資料表的索引鍵。                                                                                            | 可以呼叫的選擇性 VBScript 函數。                                                                                          |
| [自訂動作類型 17](custom-action-type-17.md)隨產品安裝的 DLL 檔案。<br/>                                            | 17   | 檔案資料表 [的](file-table.md) 索引鍵。                                                                                                | DLL 進入點。                                                                                                                           |
| [自訂動作類型 18](custom-action-type-18.md)隨產品安裝的 EXE 檔案。<br/>                                            | 18   | 檔案資料表 [的](file-table.md) 索引鍵。                                                                                                | 命令列字串。                                                                                                                       |
| [自訂動作類型 19](custom-action-type-19.md)顯示指定的錯誤訊息，並傳回失敗，並終止安裝。<br/> | 19   | Blank                                                                                                                               | [格式化](formatted.md) 的文字字串。 [錯誤](error-table.md)資料表中的常值訊息或索引。                           |
| [自訂動作類型 21](custom-action-type-21.md)JScript 與產品一起安裝的檔案。<br/>                                        | 21   | 檔案資料表 [的](file-table.md) 索引鍵。                                                                                                | 可以呼叫的選擇性 JScript 函數。                                                                                           |
| [自訂動作類型 22](custom-action-type-22.md)隨產品安裝的 VBScript 檔案。<br/>                                       | 22   | 檔案資料表 [的](file-table.md) 索引鍵。                                                                                                | 可以呼叫的選擇性 VBScript 函數。                                                                                          |
| [自訂動作類型 34](custom-action-type-34.md)EXE 檔案具有參考目錄的路徑。<br/>                                       | 34   | 索引鍵至 [目錄](directory-table.md) 表。 這是執行的工作目錄。                                         | 目標資料行的 [格式](formatted.md) ，並包含可執行檔的完整路徑和名稱，後面接著選擇性引數。 |
| [自訂動作類型 35](custom-action-type-35.md)具有格式化文字的目錄集。<br/>                                                    | 35   | [目錄](directory-table.md)資料表的索引鍵。 指定的目錄是由目標欄位中的格式化字串所設定。   | 格式化的文字字串。                                                                                                                   |
| [自訂動作類型 37](custom-action-type-37.md)JScript 儲存在此順序資料表中的文字。<br/>                                           | 37   | Null                                                                                                                                | JScript 程式碼的字串。                                                                                                                  |
| [自訂動作類型 38](custom-action-type-38.md)這個順序資料表中儲存的 VBScript 文字。<br/>                                          | 38   | Null                                                                                                                                | VBScript 程式碼的字串。                                                                                                                 |
| [自訂動作類型 50](custom-action-type-50.md)EXE 檔案，其中包含由屬性值指定的路徑。<br/>                                 | 50   | [屬性工作表的](property-table.md)屬性名稱或索引鍵。                                                                       | 命令列字串。                                                                                                                       |
| [自訂動作類型 51](custom-action-type-51.md)具有格式化文字的屬性集。<br/>                                                     | 51   | [屬性工作表的](property-table.md)屬性名稱或索引鍵。 這個屬性是由目標欄位中的格式化字串所設定。 | 格式化的文字字串。                                                                                                                   |
| [自訂動作類型 53](custom-action-type-53.md)JScript 屬性值所指定的文字。<br/>                                           | 53   | [屬性工作表的](property-table.md)屬性名稱或索引鍵。                                                                       | 可以呼叫的選擇性 JScript 函數。                                                                                           |
| [自訂動作類型 54](custom-action-type-54.md)由屬性值指定的 VBScript 文字。<br/>                                          | 54   | [屬性工作表的](property-table.md)屬性名稱或索引鍵。                                                                       | 可以呼叫的選擇性 VBScript 函數。                                                                                          |



 

此外，下列自訂動作類型可用於並行安裝：

-   [自訂動作類型7](custom-action-type-7.md)
-   [自訂動作類型23](custom-action-type-23.md)
-   [自訂動作類型39](custom-action-type-39.md)

 

 




