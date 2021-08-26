---
description: 此範例說明包含兩個等的 .cub 檔案配置。 安裝程式會執行序列中的自訂動作： ICE01 和 ICE08。
ms.assetid: 609cd16a-4421-4082-855d-229f5ba7117b
title: 範例 .cub 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7aadbaca8bde7091f38d5ce8ccc39926ec6c595aa33e65e488136e89cccfc81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039658"
---
# <a name="sample-cub-file"></a>範例 .cub 檔案

此範例說明 [包含兩個](internal-consistency-evaluators-ices.md)等的 .cub 檔案配置。 安裝程式會執行序列中的自訂動作： ICE01 和 ICE08。

自訂動作 ICE01 是 [自訂動作類型 1](custom-action-type-1.md)。 它是在 .cub 檔案中儲存為數據流的 DLL 進入點。 此資料流程會列在 ice.dll 的二進位資料表中。

自訂動作 ICE08 是 [自訂動作類型 6](custom-action-type-6.md)。 它是 VBScript 中函式的進入點，會在 .cub 檔案中儲存為數據流。 此資料流程會以 ice.vbs 的形式列于二進位資料表中。

[二進位資料表](binary-table.md)



| 名稱    | 資料                               |
|---------|------------------------------------|
| ice.vbs | ice.vbs 的未格式化二進位資料 |
| ice.dll | ice.dll 的未格式化二進位資料 |



 

[CustomAction 資料表](customaction-table.md)



| 動作 | 類型 | 來源  | 目標 |
|--------|------|---------|--------|
| ICE01  | 1    | ice.dll | ICE01  |
| ICE08  | 6    | ice.vbs | ICE02  |



 

\_ICESequence 資料表



| 動作 | 條件 | 順序 |
|--------|-----------|----------|
| ICE01  |           | 10       |
| ICE08  |           | 20       |



 

\_特殊資料表

ICE01 和 ICE08 不需要包含特殊的處理資料表。 當 .cub 檔案包含特殊資料表時，它們也必須包含在 \_ 驗證資料表中。

[\_驗證資料表](-validation-table.md)



| 資料表         | 資料行    | Nullable | MinValue | MaxValue | KeyTable | KeyColumn | 類別                         | 集合 | 描述 |
|---------------|-----------|----------|----------|----------|----------|-----------|----------------------------------|-----|-------------|
| Binary        | 名稱      | N        |          |          |          |           | [識別碼](identifier.md)     |     |             |
| Binary        | 資料      | N        |          |          |          |           | [二進位](binary.md)             |     |             |
| CustomAction  | 動作    | N        |          |          |          |           | [識別碼](identifier.md)     |     |             |
| CustomAction  | 類型      | N        |          |          |          |           | [整數](integer.md)           |     |             |
| CustomAction  | 來源    | Y        |          |          |          |           | [CustomSource](customsource.md) |     |             |
| CustomAction  | 目標    | Y        |          |          |          |           | [格式 化](formatted.md)       |     |             |
| \_ICESequence | 動作    | N        |          |          |          |           | [識別碼](identifier.md)     |     |             |
| \_ICESequence | 條件 | Y        |          |          |          |           | [Condition](condition.md)       |     |             |
| \_ICESequence | 順序  | Y        |          |          |          |           | [整數](integer.md)           |     |             |



 

 

 



