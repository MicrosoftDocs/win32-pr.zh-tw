---
description: ICE48 會檢查是否已硬式編碼至屬性工作表中的本機路徑的目錄。
ms.assetid: 9dcc2475-23a3-4f77-8828-4d0a036670d4
title: ICE48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c9c9ace086d044109e5f9b91bbc471c37094de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975157"
---
# <a name="ice48"></a>ICE48

ICE48 會檢查是否已硬式編碼至 [屬性工作表](property-table.md)中的本機路徑的目錄。

請勿將目錄路徑硬式編碼到本機磁片磁碟機，因為電腦上的本機磁片磁碟機設定不同。 如果將應用程式部署到大量的電腦上，而這些電腦的相關部分全都相同，則這種作法可能是可接受的。

## <a name="result"></a>結果

ICE48 會在屬性工作表中有硬式編碼至本機路徑的目錄時張貼錯誤訊息。

## <a name="example"></a>範例

ICE48 會針對所顯示的範例報告下列警告。

``` syntax
Directory 'Dir1' appears to be hardcoded in the property 
    table to a local drive.
```

[目錄資料表](directory-table.md) (部分) 



| 目錄 | 目錄 \_ 父系 | DefaultDir |
|-----------|-------------------|------------|
| Dir1      |                   | SourceDir  |



 

[屬性工作表](property-table.md) (部分) 



| 屬性 | 值      |
|----------|------------|
| Dir1     | d： \\ 來源 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



