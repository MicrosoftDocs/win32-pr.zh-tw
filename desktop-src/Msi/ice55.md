---
description: ICE55 會驗證所有 LockPermission 物件都存在，而且具有有效的許可權值。
ms.assetid: e23e43ce-942f-4f6b-b5fd-cf366f7a7fe5
title: ICE55
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044b9993c6c50dce32c04f98d8e000f0faae4280d244c4656d7b0cbed7b49749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635139"
---
# <a name="ice55"></a>ICE55

ICE55 會驗證所有 LockPermission 物件都存在，而且具有有效的許可權值。

## <a name="result"></a>結果

ICE55 會在 [LockPermissions 資料表](lockpermissions-table.md) 中所列的 LockObject 不存在或許可權資料行中未指定許可權層級時，張貼錯誤。

## <a name="example"></a>範例

ICE55 會報告範例的下列錯誤。

``` syntax
LockObject 'File1'.'File'.''.'guest' in the LockPermissions table 
    has a null Permission value. 
Could not find item 'File3' in table 'File' which is referenced 
    in the LockPermissions table.
```

[LockPermissions 資料表](lockpermissions-table.md) (部分) 



| LockObject | 資料表 | 網域 | 使用者  | 權限 |
|------------|-------|--------|-------|------------|
| File1      | 檔案  |        | guest |            |
| File3      | 檔案  |        | guest | 1          |



 

[檔資料表](file-table.md) (部分) 



| 檔案  | 版本 | 語言 |
|-------|---------|----------|
| File1 | File2   |          |
| File2 | 1.0.0.0 | 1033     |



 

物件 File1 在許可權資料行中具有 null。 每個資料列都必須有 [許可權] 資料行中的值。 若要修正這個錯誤，請在此資料行中指定數值。 如果這個物件不需要任何許可權，您應該移除該資料列。

LockPermissions 資料表中所述的物件 File3 不會列在 File 資料表中。 若要修正這個錯誤，請參考有效的物件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



