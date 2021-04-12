---
description: ICE98 會驗證 ODBC 資料來源之 ODBCDataSource 資料表的描述欄位。 它會使用 SQLValidDSN 函式來檢查只使用有效的字元，而且描述不超過允許的最大長度。
ms.assetid: ed78db96-10a1-4e42-9147-2309c9ca9c6e
title: ICE98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bf06e97341bd8f15502b1ea1fe43a975dc9cde2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193312"
---
# <a name="ice98"></a>ICE98

ICE98 會驗證 ODBC 資料來源之 [ODBCDataSource 資料表](odbcdatasource-table.md) 的描述欄位。 它會使用 **SQLValidDSN** 函式來檢查只使用有效的字元，而且描述不超過允許的最大長度。

## <a name="result"></a>結果

ICE98 會張貼下列警告。



| ICE98 警告                    | Description                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 資料來源名稱無效。 | [ODBCDataSource 資料表](odbcdatasource-table.md)之 Description 資料行中的值可能包含不正確字元或太長，這表示它超過 SQL 的 \_ \_ DSN \_ 長度上限32。 |



 

## <a name="example"></a>範例

ICE98 會報告下列範例警告：

``` syntax
The data source name is invalid: !
The data source name is invalid: <String of length > 32>
```

[ODBCDataSource 資料表](odbcdatasource-table.md) (部分) 



| DataSource | Description                      |
|------------|----------------------------------|
| BadChar    | !                                |
| TooLong    | <String of length > 32> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> <dt>

[ODBCDataSource 資料表](odbcdatasource-table.md)
</dt> </dl>

 

 



