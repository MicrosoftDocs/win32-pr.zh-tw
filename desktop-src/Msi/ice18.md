---
description: ICE18 會驗證用來作為元件之索引鍵路徑的任何空白目錄都列在 CreateFolder 資料表中。
ms.assetid: de31b893-831b-4a6d-809a-c4a3056b8a66
title: ICE18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ca102e8fdec5e30283cd879ddb5677a2bba79f90ba5a9a790ea50923e0aeedb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581138"
---
# <a name="ice18"></a>ICE18

ICE18 會驗證用來作為元件之索引鍵路徑的任何空白目錄都列在 [CreateFolder 資料表](createfolder-table.md)中。

如果 [元件資料表](component-table.md) 的 KeyPath 資料行是 Null，這表示目錄資料行中所列的目錄 \_ 是該元件的金鑰路徑。 因為安裝程式所建立的資料夾是空的，所以當它變成空白時，此資料夾必須列在 [CreateFolder 表格](createfolder-table.md) 中，以防止安裝程式每次都嘗試安裝。

請勿使 SystemFolder 目錄成為元件的金鑰路徑。 因為每個作業系統上都有這個資料夾，所以安裝程式一律會偵測到元件是否存在的金鑰路徑。 在此情況下，金鑰路徑應該是檔案、登錄專案或 ODBC 資料來源。

執行驗證 ICE18 時，會先檢查下列條件是否成立：

-   [元件資料表](component-table.md)的 KeyPath 資料行包含 Null 值。
-   檔案 [資料表](file-table.md)中沒有列出元件的檔案。
-   [RemoveFile 資料表](removefile-table.md)中沒有列出元件的檔案，而且 DirProperty 中的值與 \_ [元件資料表](component-table.md)的目錄資料行相同。
-   [DuplicateFile 資料表](duplicatefile-table.md)中沒有列出元件的檔案，而且 DestFolder 中的值與 \_ [元件資料表](component-table.md)的目錄資料行相同。
-   [MoveFile 資料表](movefile-table.md)中沒有列出元件的檔案，而且 DestFolder 中的值與 \_ [元件資料表](component-table.md)的目錄資料行相同。

如果這些都是 true，則 ICE18 會驗證下列各項：

-   \_ [CreateFolder 資料表](createfolder-table.md)的 component 資料行與[component 資料表](component-table.md)的 component 資料行具有相同的值。
-   CreateFolder 資料表的目錄資料 \_ 行與 \_ [Component 資料表](component-table.md)的目錄資料行具有相同的值。

## <a name="result"></a>結果

如果安裝套件將目錄指定為未列于 [CreateFolder 資料表](createfolder-table.md)中之元件的金鑰路徑，ICE18 會張貼錯誤訊息。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



