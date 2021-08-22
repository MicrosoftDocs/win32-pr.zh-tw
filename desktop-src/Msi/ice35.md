---
description: ICE35 會驗證封裝含儲存在封包檔中壓縮檔案的元件，不會設定為從來源執行。 在 Windows Installer 2.0 或更新版本中，已移除此限制。
ms.assetid: b4df27e2-9790-4b18-a173-25fa8b0ecd4d
title: ICE35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4ee42f97a049b165d41fef7391f0031836865dbf7bafec6b1b5e2fb868e75a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528558"
---
# <a name="ice35"></a>ICE35

ICE35 會驗證封裝含儲存在封 [包](cabinet-files.md) 檔中壓縮檔案的元件，不會設定為從來源執行。 在 Windows Installer 2.0 或更新版本中，已移除此限制。

ICE35 會查詢 [媒體資料表](media-table.md) 的 [封包] 資料行，以判斷壓縮並儲存在封包檔中的檔案。 它會查詢檔案 [資料表](file-table.md) ，以判斷哪些元件包含這些檔案。 最後，它會檢查 [元件資料表](component-table.md) ，以判斷是否已在 [屬性] 資料行中設定從來源執行的位。

## <a name="result"></a>結果

如果有壓縮檔案儲存在屬於元件 [資料表](component-table.md)之 [屬性] 資料行中的 msidbComponentAttributesSourceOnly 位元件的元件，ICE35 會張貼一則錯誤訊息。 在 Windows Installer 2.0 或更新版本中，這會從錯誤變更為警告訊息。 僅支援 Windows Installer 2.0 和更新版本的封裝，會將 \_ 摘要資訊資料流程的 PID PAGECOUNT 屬性設定為至少200的值。

如果有壓縮檔案儲存在屬於元件 [資料表](component-table.md)之 [屬性] 資料行中的 msidbComponentAttributesOptional 位元件的元件，ICE35 會張貼警告訊息。 Windows Installer 2.0 和更新版本已移除此警告訊息。

如果元件中的多個檔案位於封包檔中，ICE35 會針對每個已設定從來源位執行的檔案報告錯誤。

## <a name="example"></a>範例

ICE35 會針對使用早于 Windows Installer 2.0 版的版本，報告下列範例的錯誤和警告。



| ICE35 錯誤                                                                                                | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 錯誤：無法從來源執行元件 Component3，因為它的成員檔案 ' File3 ' 已壓縮。 | 壓縮檔案儲存在封包檔中，且此檔案屬於 [元件資料表](component-table.md)的 [屬性] 資料行中設定 SourceOnly 位的元件。 若要修正這個錯誤，請將 Component2's 屬性值的較低2位變更為 "00" （表示僅限本機），或從 CAB 檔案中移除 File4。<br/>                                                                                                                                                                         |
| 錯誤：無法從來源執行元件 Component3，因為它的成員檔案 ' File3 ' 已壓縮。 | 壓縮檔案儲存在封包檔中，且此檔案屬於 [元件資料表](component-table.md)的 [屬性] 資料行中設定 SourceOnly 位的元件。 由於元件中的檔案並不是來自相同的媒體，因此 ICE35 會針對封包中的元件中的每個檔案報告錯誤。<br/> 若要修正這個錯誤，請將 Component2's 屬性值的較低2位變更為 "00" （表示僅限本機），或從 CAB 檔案中移除 File4。<br/> |



 

[媒體資料表](media-table.md) (部分) 



| DiskID | LastSequence | 內閣   |
|--------|--------------|-----------|
| 1      | 2            |           |
| 2      | 4            | One.cab   |
| 3      | 5            | \#Two.cab |



 

[檔資料表](file-table.md) (部分) 



| 檔案  | 元件\_ | 順序 |
|-------|-------------|----------|
| File1 | Component1  | 1        |
| File2 | Component2  | 2        |
| File3 | Component2  | 3        |
| File4 | Component3  | 4        |
| File5 | Component3  | 5        |



 

[元件資料表](component-table.md) (部分) 



| 元件  | 屬性 |
|------------|------------|
| Component1 | 0          |
| Component2 | 2          |
| Component3 | 1          |



 

 (部分) 的[快捷方式資料表](shortcut-table.md)



| 快速鍵  | 圖示\_ |
|-----------|--------|
| Shortcut1 | Icon2  |



 

請注意，您也可以使用 [摘要資訊資料流程](summary-information-stream.md)的 [[**字數統計摘要**](word-count-summary.md)] 屬性，將檔案標示為已壓縮。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 




