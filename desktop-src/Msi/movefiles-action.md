---
description: MoveFiles 動作會在使用者的電腦上尋找現有的檔案，並將這些檔案移動或複製到新的位置。
ms.assetid: f08f751d-877b-4b17-8015-7108d5fd8195
title: MoveFiles 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f06db0cef12753652bf94bf05875b2c2f9d4067c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852748"
---
# <a name="movefiles-action"></a>MoveFiles 動作

MoveFiles 動作會在使用者的電腦上尋找現有的檔案，並將這些檔案移動或複製到新的位置。 如果已指定連結至專案的元件要安裝在本機或從來源執行，則 [MoveFiles] 動作會查詢 [MoveFile 資料表](movefile-table.md) ，並在該處移動指定的檔案。

## <a name="sequence-restrictions"></a>順序限制

MoveFiles 動作必須在 [InstallValidate](installvalidate-action.md) 動作之後，以及在 [InstallFiles](installfiles-action.md) 動作之前。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述                  |
|-------|---------------------------------------------|
| \[1\] | 已移動之檔案的識別碼。                   |
| \[6\] | 已安裝檔案的大小（以位元組為單位）。            |
| \[9\] | 保存移動檔案之目錄的識別碼。 |



 

## <a name="remarks"></a>備註

MoveFiles 資料表包含名為 "options" 的資料行，以指定要移動或複製的來源檔案。 移動的原始程式檔會在複製到新位置之後刪除。 如需確切的語法，請參閱 [MoveFile 資料表](movefile-table.md)。

MoveFile 資料表的 SourceFolder 和 DestFolder 資料行是屬性名稱，其值應解析為完整路徑。 這些屬性可以是 [目錄](directory-table.md) 資料表中的任何目錄專案、任何預先定義的資料夾屬性 ([**FavoritesFolder**](favoritesfolder.md)（例如) ），或是 [AppSearch](appsearch-table.md) 資料表中任何專案所設定的屬性。 這些屬性可能包含特定檔案的完整路徑，包含檔案名。 例如，您可以撰寫 AppSearch 資料表來搜尋特定的檔案，並將屬性設定為該檔案的完整路徑。 在此範例中，MoveFile 資料表中的 [未占] 資料行可以保留空白，表示 SourceFolder 屬性中的值包含完整檔案路徑。 分號是轉換、來源和修補程式的清單分隔符號，不應該用於檔案名或路徑中。

MoveFiles 動作不會作用於 MoveFile 資料表中的專案，其中 SourceFolder 或 DestFolder 屬性不會評估為完整路徑。

MoveFiles 動作會嘗試移動或複製來原始目錄中的所有檔案，而這些檔案符合 MoveFiles 資料表的 [失敗的資料行] 中所指定的名稱。 [未通過] 資料行中的名稱可以包含 \* 或？ 允許移動或複製檔群組的萬用字元。 例如，[未使用的資料行] 可能包含 " \* .xls" 的專案，而 MoveFiles 動作則會將每個 Microsoft Excel 活頁簿從來原始目錄移動或複製到目的地。

您可以在 MoveFile 資料表的 DestName 資料行中，指定要提供給目的地檔案的名稱。 如果此資料行保留空白，目的地檔案名會保留原始程式檔名稱。

如果在 \* [MoveFile 資料表](movefile-table.md) 的 [未使用] 資料行中輸入 "" 萬用字元，並在 DestName 資料行中指定目的地檔案名，則所有移動或複製的檔案都會保留來源中的名稱。

卸載產品時，不會刪除 MoveFiles 動作所移動或複製的檔案。

 

 



