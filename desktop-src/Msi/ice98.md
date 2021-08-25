---
description: ICE98 會驗證 ODBC 資料來源之 ODBCDataSource 資料表的描述欄位。 它會使用 SQLValidDSN 函式來檢查只使用有效的字元，而且描述不超過允許的最大長度。
ms.assetid: ed78db96-10a1-4e42-9147-2309c9ca9c6e
title: ICE98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23f8a627b057e6c235fdb57a4f2d5d2b2cf6274e528ef4945c6a6323e1888427
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894688"
---
# <a name="ice98"></a>ICE98

ICE98 會驗證 ODBC 資料來源之 [ODBCDataSource 資料表](odbcdatasource-table.md) 的描述欄位。 它會使用 **SQLValidDSN** 函式來檢查只使用有效的字元，而且描述不超過允許的最大長度。

## <a name="result"></a>結果

ICE98 會張貼下列警告。



| ICE98 警告                    | 描述                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 資料來源名稱無效。 | [ODBCDataSource 資料表](odbcdatasource-table.md)之 Description 資料行中的值可能包含不正確字元或太長，這表示它超過了 SQL \_ 的最大 \_ DSN \_ 長度32。 |



 

## <a name="example"></a>範例

ICE98 會報告下列範例警告：

``` syntax
The data source name is invalid: !
The data source name is invalid: <String of length > 32>
```

[ODBCDataSource 資料表](odbcdatasource-table.md) (部分) 



| DataSource | 描述                      |
|------------|----------------------------------|
| BadChar    | !                                |
| TooLong    | <String of length > 32> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> <dt>

[ODBCDataSource 資料表](odbcdatasource-table.md)
</dt> </dl>

 

 



