---
description: ICE54 會檢查使用隨附檔案作為其金鑰路徑的元件。
ms.assetid: 94fcabfe-4500-42f2-acea-13b9a6681ca6
title: ICE54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00658bb62b5c29b25f9fb653e216920fc776ba6df0e3fc2f8b47bbdf715040b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946605"
---
# <a name="ice54"></a>ICE54

ICE54 會檢查使用隨附檔案作為其金鑰路徑的元件。

元件的金鑰路徑檔案不能從不同的檔案衍生其版本。 這可能會導致某些檔案無法安裝。 如需隨附檔案的詳細資訊，請參閱檔案 [表格](file-table.md) 。

## <a name="result"></a>結果

如果有任何元件的金鑰路徑檔案衍生自另一個檔案的版本，ICE54 會張貼警告。

## <a name="example"></a>範例

ICE54 會針對所顯示的範例傳回下列警告。

``` syntax
Component 'Component1' uses file 'File1' as its KeyPath, but the file's version is provided by the file 'File2'.
```

[元件資料表](component-table.md) (部分) 



| 元件  | 屬性 | KeyPath |
|------------|-----------|---------|
| Component1 | 0         | File1   |



 

[檔資料表](file-table.md) (部分) 



| 檔案  | 版本 | 語言 |
|-------|---------|----------|
| File1 | File2   |          |
| File2 | 1.0.0.0 | 1033     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



