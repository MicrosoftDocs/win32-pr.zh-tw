---
description: ICEM07 會確認順序資料表中的檔案順序符合 MergeModule.CABinet 中的檔順序。
ms.assetid: 5778e0c5-2f8d-4562-9c93-d6f6890a74e9
title: ICEM07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 696d5c92671c3a8347cb43714d43e646a3e14f33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849651"
---
# <a name="icem07"></a>ICEM07

ICEM07 會確認順序資料表中的檔案順序符合 [MergeModule.CABinet](mergemodule-cabinet.md)中的檔順序。

Merge module 會儲存在合併模組中，名為 Mergemod 的 .cub 檔中，而不是在包含用於封裝驗證的 Ices-003 的 .cub 檔案中。

## <a name="result"></a>結果

如果檔案資料表中的檔案順序與封包檔中的順序不符，ICEM07 會張貼錯誤。

## <a name="example"></a>範例

IC0M07 會針對所顯示的範例張貼下列錯誤訊息。

``` syntax
The file 'FileB.GUID1' appears to be out of sequence. It has position 3 
in the CAB, but not when the file table is ordered by sequence number.
```

[FileTable](file-table.md)



| 檔案          | 順序 |
|---------------|----------|
| >filea.docx.*GUID1* | 1        |
| >fileb.docx.*GUID1* | 8        |
| FileC.*GUID1* | 52       |



 

Embedded [MergeModule.CABinet](mergemodule-cabinet.md)



| 檔案          |
|---------------|
| >filea.docx.*GUID1* |
| FileC.*GUID1* |
| 提交。*GUID1* |
| >fileb.docx.*GUID1* |



 

雖然檔案資料表中的檔案序號不需要是連續的，而且封包檔中可以有額外的檔案，但是檔案資料表中所有檔案的相對順序必須符合 [MergeModule.CABinet](mergemodule-cabinet.md)中的順序。 若要修正這個錯誤，請將 >fileb.docx 的序號變更為 FileC 後的順序，以符合封包中的檔案順序，或以正確的順序重建 CAB 檔。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Merge Module ICE 參考](merge-module-ice-reference.md)
</dt> </dl>

 

 



