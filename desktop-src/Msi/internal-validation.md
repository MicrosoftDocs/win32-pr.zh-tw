---
description: 撰寫安裝封裝時，您可以使用 MsiViewModify 函式或 View. Modify 方法，以確定您輸入的資料語法正確。
ms.assetid: c960e9df-dcd6-44d2-8662-40a1dea81f45
title: 內部驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca3c1a9e6f7b7e35b4d7d91287af64eff7812de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112260"
---
# <a name="internal-validation"></a>內部驗證

撰寫安裝封裝時，您可以使用 [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) 函式或 View. Modify 方法，以確定您輸入的資料語法正確。 如需詳細資訊，請參閱 [**Modify 方法**](view-modify.md)。 在最低層級，資料庫資料表的資料行可以儲存整數 (短或長) 、字串或二進位資料。 但是，安裝封裝需要特定資料表中的特定整數或字串。 這些規格會保留在[ \_ 驗證資料表](-validation-table.md)中。 例如， [file 資料表](file-table.md) 的 FileName 資料行是字串資料行，但是它會特別儲存檔案名。 因此，您的專案不應該只是字串，但也應該遵循命名檔案的需求。

與 [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) 函數搭配使用的各種驗證列舉值，允許在不同層級進行立即驗證。 MSIMODIFY \_ validate \_ FIELD enum 可以用來驗證記錄的個別欄位。 它不會驗證外鍵。 MSIMODIFY \_ VALIDATE 列舉會驗證整個資料列，並包含外鍵驗證。 如果您要在資料表中插入新的資料列，請使用 MSIMODIFY \_ VALIDATE \_ new 列舉來確認您要加入有效的資料，以及使用唯一的主鍵。 如果主鍵不是唯一的，插入會失敗。 如果使用其中一個驗證列舉呼叫 **MsiViewModify** 時傳回錯誤，您可以對 [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora) 進行重複呼叫以診斷問題。 **MsiViewGetError** 會指出發生錯誤的資料行，以及列舉值以協助修正問題。 如需詳細資訊，請參閱 [**GetError 方法**](view-geterror.md)。

您也可以使用內部驗證，以確保其他作者將資料正確地輸入您的自訂資料表。 \_使用自訂資料表名稱和資料行名稱做為主要索引鍵，將自訂資料表的每個資料行加入至驗證資料表。 在 [驗證] 資料表的 [描述] 資料行中，提供每個資料行的描述或用途 \_ 。 使用可為 Null、MinValue、int32.maxvalue、KeyTable、KeyColumn、Category 和 Set 資料行，為每個資料行輸入適用的需求：

-   如果資料行可為 Null，請輸入 ' Y '。 如果沒有，請輸入 ' N '。
-   如果資料行是整數資料行，而且可以包含整數的範圍，請使用 MinValue 和 Timespan.maxvalue 資料行來輸入該範圍。
-   外鍵資料行是使用 KeyTable 和 KeyColumn 資料行來識別。
-   若為字串資料行，請指定類別目錄，例如檔案名、GUID 或識別碼。 如需詳細資訊，請參閱 [資料行資料類型](column-data-types.md)。
-   如果資料只能與特定數目的值相關 (字串或整數) ，請使用 Set 資料行來列出可接受的值。

除了您的資料 \_ 行是指定的型別，您也可以在驗證資料表中填入資料表、資料行和描述)  (的資料行清單。  (請注意，您不需要填入所有的資料行。 ) 



| 類型    | 資料行                                                          |
|---------|------------------------------------------------------------------|
| 整數 | Nullable、MinValue、int32.maxvalue、KeyTable、KeyColumn、Set           |
| String  | Nullable、KeyTable、KeyColumn、Category、Set、MinValue、int32.maxvalue |
| Binary  | 可為 null、類別 (分類必須是 "Binary" )                    |



 

撰寫環境可能會使用 MSIMODIFY \_ 驗證 \_ 刪除。 此列舉假設您想要刪除資料列。 未執行任何欄位或外鍵驗證。 此列舉實際上會執行反向外鍵驗證。 它會檢查 \_ 驗證資料表中是否有「已刪除」資料列所屬之資料表的 KeyTable 和 KeyColumn 資料行中的參考。 如果有資料行列出包含「已刪除」資料列做為潛在外鍵的資料表，它會迴圈處理該資料行，以查看是否有任何值參考「已刪除」資料列中的值。 傳回錯誤表示您藉由刪除資料列來中斷資料庫的關聯式完整性。

 

 



