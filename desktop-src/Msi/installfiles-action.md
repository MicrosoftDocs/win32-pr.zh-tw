---
description: InstallFiles 動作會將檔案資料表中指定的檔案從來源目錄複寫到目的地目錄。
ms.assetid: 187ad82f-13f5-4ea3-913c-2ae7561a6ee6
title: InstallFiles 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8df2a62deb253314e84e72cd84e88052f1175db7451807c3f266542e29c10c7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629929"
---
# <a name="installfiles-action"></a>InstallFiles 動作

InstallFiles 動作會將檔案資料表中指定的檔案從來源目錄複寫到目的地目錄。

## <a name="sequence-restrictions"></a>順序限制

InstallFiles 動作必須在 [InstallValidate](installvalidate-action.md) 動作之後，以及任何與檔案相依的動作之前。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述                      |
|-------|-------------------------------------------------|
| \[1\] | 已安裝檔案的識別碼。                   |
| \[6\] | 已安裝檔案的大小（以位元組為單位）。                |
| \[9\] | 保存已安裝檔案的目錄識別碼。 |



 

## <a name="remarks"></a>備註

InstallFiles 動作會在 [File 資料表](file-table.md)中指定的檔案上運作。 每個檔案都會根據 [元件資料表](component-table.md)中檔案相關元件的安裝狀態進行安裝。 只有元件的元件會解析為 **msiInstallStatelocal** 狀態時，才有資格進行複製。

InstallFiles 動作會執行檔案資料表的下列資料行。

-   FileName 資料行指定目的檔案名。
-   版本資料行指定檔案版本。
-   [屬性] 欄指定檔案和安裝屬性旗標位。
-   File 資料行指定唯一的檔案 token。
-   FileSize 資料行指定未壓縮的檔案大小（以位元組為單位）。
-   [語言] 資料行指定檔案語言識別項。
-   [順序] 資料行指定媒體上的序號。

InstallFiles 動作會執行元件資料表的下列資料行。

-   目錄資料 \_ 行指定 [目錄資料表](directory-table.md) 專案的參考。
-   元件資料行指定元件專案的唯一名稱。

只有在下列其中一項為真時，才會複製指定的檔案：

-   檔案目前未安裝在本機電腦上。
-   檔案是在本機電腦上，但版本號碼比檔案 [資料表](file-table.md)中的檔案還要低。
-   檔案是在本機電腦上，但沒有相關聯的版本號碼。

每個要複製之檔案的來原始目錄都是由 sourceMode 所決定，而這會依媒體資料表的 [封包] 資料行中的值而定。 如需來源模式的完整討論，請參閱 [媒體資料表](media-table.md)。

如果要複製之檔案的來原始目錄位於卸載式媒體（例如磁片或 CD-ROM）上，則 InstallFiles 動作會先確認已插入適當的來源媒體，然後再嘗試複製檔案。 InstallFiles 會使用與媒體資料表的 VolumeLabel 資料行中所指定值相符的 [*磁片區卷*](v-gly.md) 標，搜尋相同卸載型別的媒體。 如果找到相符的已載入磁片區，則會繼續進行檔案複製程式。 如果找不到相符項，對話方塊會要求使用者插入適當的媒體。 在此情況下，對話方塊會使用媒體資料表的 DiskPrompt 資料行中所找到的媒體名稱做為提示的一部分。

必須小心，因為 InstallFiles 動作可以刪除原始檔案，而不是取代它。 當 InstallFiles 動作取代較舊的檔案，且使用者選擇忽略錯誤時，就會發生此錯誤。 安裝程式的預設行為是在確定已正確複製新檔案之前，先刪除舊的檔案。

如需安裝程式所使用的檔案版本控制規則，請參閱檔案 [版本控制規則](file-versioning-rules.md)。

 

 



