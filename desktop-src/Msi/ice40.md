---
description: ICE40 會進行其他驗證。
ms.assetid: 1f2ba2a1-0170-4434-88fd-a5d1ca8b67c4
title: ICE40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17617fe5748fcba5ae0edab414ad1bc83c2e5c22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115756"
---
# <a name="ice40"></a>ICE40

ICE40 會進行其他驗證。

## <a name="result"></a>結果

ICE40 文章的警告如下：

-   已覆寫 [**REINSTALLMODE**](reinstallmode.md) 屬性。
-   [RemoveIniFile 資料表](removeinifile-table.md)有一個不含值的刪除標記專案。
-   .Msi 檔案遺漏 [錯誤資料表](error-table.md) ，且 [**頁面計數摘要**](page-count-summary.md) 屬性小於或等於100。 這項 ICE 警告已淘汰，因為 Windows Installer 不需要套件具有錯誤資料表。 您可以使用 Msimsg.dll 來取出錯誤訊息。

## <a name="example"></a>範例

[屬性工作表](property-table.md)



| 屬性                               | 值 |
|----------------------------------------|-------|
| [**REINSTALLMODE**](reinstallmode.md) | A     |



 

[RemoveIniFile 資料表](removeinifile-table.md)



| RemoveIniFile                          | 動作 | 值 |
|----------------------------------------|--------|-------|
| [**REINSTALLMODE**](reinstallmode.md) | 4      |       |



 

## <a name="results"></a>結果

ICE40 會報告下列錯誤。



| ICE40 錯誤                                                                                           | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**REINSTALLMODE**](reinstallmode.md) 定義于屬性工作表中。 這可能會造成問題。 | 在 .msi 檔案中定義 [**REINSTALLMODE**](reinstallmode.md) 屬性可能會導致非預期的行為。 若要修正這個錯誤，請不要定義這個屬性。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| RemoveIniFile 專案 Remove1 必須有值，因為動作是「刪除標記」 (4) 。                | [RemoveIniFile 資料表](removeinifile-table.md)的 RemoveIniFile 資料行中有一個刪除標記動作，但沒有在 [值] 資料行中指定要刪除的標記。                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 遺漏錯誤資料表。 只會產生數值錯誤訊息。                              | 這項 ICE 警告已淘汰，因為 Windows Installer 不需要套件具有 [錯誤資料表](error-table.md)。 您可以使用 Msimsg.dll 來取出錯誤訊息。<br/> 此警告表示 .msi 檔案遺漏 [錯誤資料表](error-table.md) ，且 [ [**頁面計數摘要**](page-count-summary.md) ] 屬性小於或等於100。 <br/> 若要修正這個錯誤，請使用目前版本的 Windows Installer，或將錯誤資料表加入至安裝套件，並在 [訊息] 資料行中撰寫格式化範本以取得錯誤訊息。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 




