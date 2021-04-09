---
description: '\_資料表資料表是唯讀的系統資料表，會列出資料庫中的所有資料表。 查詢此資料表，以找出資料表是否存在。'
ms.assetid: d064855b-8c10-476e-9570-cc3ab48ae998
title: _Tables 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2dc3ebafd969a07676f64f674f76c3e16ebe059
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849004"
---
# <a name="_tables-table"></a>\_資料表資料表

\_資料表資料表是唯讀的系統資料表，會列出資料庫中的所有資料表。 查詢此資料表，以找出資料表是否存在。

\_資料表資料表有下列資料行。



| Column | 類型             | 答案 | Nullable |
|--------|------------------|-----|----------|
| Name   | [Text](text.md) | Y   | N        |



 

## <a name="column"></a>Column

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>名字
</dt> <dd>

其中一個資料表的名稱。

</dd> </dl>

## <a name="remarks"></a>備註

因為 \_ 資料表資料表是無法透過 SQL 查詢修改的系統資料表，所以您無法使用 [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) 函數或 [**PrimaryKeys 屬性**](database-primarykeys.md)來取得主鍵。

 

 



