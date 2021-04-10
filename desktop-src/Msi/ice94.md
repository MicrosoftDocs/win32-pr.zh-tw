---
description: ICE94 會檢查快速鍵資料表、功能資料表和 MsiAssembly 資料表，如果有任何 unadvertised 快速鍵指向全域組件快取中的元件檔案，則會張貼警告。
ms.assetid: 9b1b25b5-b190-47c2-8d43-fa3964e87a6f
title: ICE94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ce52e88a31e246eb4d69defba77b64c2955eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194395"
---
# <a name="ice94"></a>ICE94

ICE94 會檢查 [快速鍵資料表](shortcut-table.md)、 [功能資料表](feature-table.md)和 [MsiAssembly 資料表](msiassembly-table.md) ，如果有任何 unadvertised 快速鍵指向全域組件快取中的元件檔案，則會張貼警告。 如果快速鍵資料表的 [目標] 欄位中的專案不是功能資料表中的一項功能，則會 unadvertised 快捷方式。 如果快速鍵資料表之 [元件] 欄位中的專案 \_ 也列在 [MsiAssembly] 資料表中，快捷方式會指向元件檔案。 如果 MsiAssembly 資料表的 [檔案 \_ 應用程式] 欄位中的專案是空的，則元件檔會在全域組件快取中。

## <a name="result"></a>結果

ICE94 會張貼下列警告。



| ICE94 警告                                                                                | Description                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| 未公告的快捷方式 ' \[ 2 \] ' 會指向全域組件快取中的元件檔案。 | Unadvertised 快捷方式指向全域組件快取中的元件檔案。 |



 

## <a name="example"></a>範例

ICE94 會報告此範例的下列錯誤：

``` syntax
The non-advertised shortcut 'shortcut1' points to an assembly file in the global assembly cache.
```

 (部分) 的[快捷方式資料表](shortcut-table.md)



| 快速鍵  | 元件\_ | 目標    |
|-----------|-------------|-----------|
| shortcut1 | c1          | \[1\] |
| shortcut2 | c2          | feature1  |
| shortcut3 | c3          | \[file2\] |



 

[功能表](feature-table.md) (部分) 



| 功能  |
|----------|
| feature1 |



 

[MsiAssembly 資料表](msiassembly-table.md) (部分) 



| 元件\_ | 檔 \_ 應用程式 |
|-------------|-------------------|
| c1          |                   |
| c2          |                   |
| c3          | fa1               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



