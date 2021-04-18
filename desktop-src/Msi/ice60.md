---
description: ICE60 會驗證 Windows Installer 資料庫的檔案資料表。
ms.assetid: 95d9b8b4-0b65-451a-8629-f0b276d6e35d
title: ICE60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26c6f296fd514f582a699a5f839a7e145169e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978039"
---
# <a name="ice60"></a>ICE60

ICE60 會檢查 [File 資料表](file-table.md) 中的檔案是否符合下列條件：

-   如果檔案不是字型且具有版本，則必須有語言。
-   ICE60 會檢查 [MsiFileHash 資料表](msifilehash-table.md)中沒有列出任何已建立版本的檔案。

若無法修正 ICE60 回報的警告，通常會導致在產品修復完成時不必要地重新安裝檔案。 發生這種情況的原因是，要在修復中安裝的檔案和磁片上的現有檔案都有相同的版本 (它們是相同的檔案) 但不同的語言。 File 資料表將語言列為 null，但檔案本身在資源中具有語言值。 根據檔案 [版本控制規則](file-versioning-rules.md)，安裝程式會優先處理要安裝的檔案，因此重新複製不必要。

## <a name="result"></a>結果

如果檔案 [資料表](file-table.md) 中不是字型且擁有版本的檔案沒有語言，ICE60 會張貼警告或錯誤。

如果已建立 MsiFileHash 資料表中所列的檔案版本，ICE60 會張貼下列錯誤。

``` syntax
ERROR: "The file [1] is Versioned. It cannot be hashed"
```

## <a name="example"></a>範例

ICE60 會針對所顯示的範例報告下列錯誤和警告。  (檔 B 是字型;其他檔案則不是。 ) 

``` syntax
WARNING: The file FileE is not a Font, and its version is not a companion file reference. It should have a language specified in the Language column.
```

>filea.docx 具有版本和語言;因此，不會產生警告或錯誤。

>fileb.docx 具有版本，但沒有語言。 但是，不會產生警告或錯誤，因為它是字型。

FileC 是隨附的參考，因此不需要有語言。 不會產生警告或錯誤。

歸檔沒有任何版本，因此不需要有語言。 不會產生警告或錯誤。

檔案具有版本，但沒有語言。 因此會產生警告。

若要修正此警告，請將語言新增至檔案。

檔案應該盡可能在版本資源中儲存語言值。 如果檔案為中性語言，請使用 [LANGID](column-data-types.md) 0。

[File Table](file-table.md) (>fileb.docx 是字型;其他檔案則不是。 ) 



| 檔案  | 版本 | 語言 |
|-------|---------|----------|
| >filea.docx | 1.0     | 1033     |
| >fileb.docx | 1.0     |          |
| FileC | >filea.docx   |          |
| 提交 |         |          |
| 檔案 | 1.0     |          |



 

[字型資料表](font-table.md)



| 檔案  | FontTitle  |
|-------|------------|
| >fileb.docx | 字型標題 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



