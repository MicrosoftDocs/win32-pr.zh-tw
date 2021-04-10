---
description: ICE45 會驗證資料庫中的位欄位資料行是否未將任何保留的位設定為1。
ms.assetid: 43fa5e9c-2059-4217-8f8e-c194e37f238a
title: ICE45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0651d94c296ae14f66b562841c3c4e2bca7b8e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192447"
---
# <a name="ice45"></a>ICE45

ICE45 會驗證資料庫中的位欄位資料行是否未將任何保留的位設定為1。

保留的位在目前的安裝程式版本中不提供任何功能，但在未來的版本中可能會提供。 它們應該設定為0，以與 Windows Installer 的未來版本相容。

## <a name="result"></a>結果

如果下列任何一份資料表包含位欄位，並將保留的位設定為1，ICE45 就會張貼錯誤訊息。

-   [BBControl 資料表](bbcontrol-table.md)
-   [對話方塊資料表](dialog-table.md)
-   [功能資料表](feature-table.md)
-   [檔資料表](file-table.md)
-   [MoveFile 資料表](movefile-table.md)
-   [ModuleConfiguration 資料表](moduleconfiguration-table.md)
-   [ODBCDataSource 資料表](odbcdatasource-table.md)
-   [修補資料表](patch-table.md)
-   [RemoveFile 資料表](removefile-table.md)
-   [ServiceControl 資料表](servicecontrol-table.md)
-   [ServiceInstall 資料表](serviceinstall-table.md)
-   [樣式表單](textstyle-table.md)

如果 [控制資料表](control-table.md) 包含位欄位，並將保留的位設定為1，則 ICE45 會張貼兩個警告訊息的其中一個。

## <a name="example"></a>範例

ICE45 會針對所顯示的範例報告下列錯誤。

``` syntax
Row 'File1' in table 'File' has bits set in the 'Attributes' 
    column that are reserved. They must be 0 to ensure 
    compatibility with future installer versions.
```

ICE45 會針對所顯示的範例報告下列警告。

``` syntax
Row 'Dialog1.Edit2' in table 'Control' has bits set in the 'Attribute' 
    column that are reserved. They should be 0 to ensure compatibility 
    with future installer versions.
```

[檔資料表](file-table.md) (部分) 



| 檔案  | 屬性 |
|-------|------------|
| File1 | 128        |



 

[控制資料表](control-table.md) (部分) 



| 對話  | 控制 | 屬性 |
|---------|---------|------------|
| Dialog1 | Edit1   | 2097152    |
| Dialog1 | Edit2   | 1048576    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



