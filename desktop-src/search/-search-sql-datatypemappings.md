---
description: 下表列出 variant 資料類型與 OLE DB 資料類型之間的對應。
ms.assetid: 213458bf-b847-4ced-8a92-686b4eee6d07
title: 資料類型對應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e25e909755c87b15526b97488285a0cf688e15dab64073fad603efc190f382b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462592"
---
# <a name="data-type-mappings"></a>資料類型對應

下表列出 variant 資料類型與 OLE DB 資料類型之間的對應。




| Variant 資料類型 | OLE DB 資料類型 |
|-------------------|------------------|
| VT \_ BOOL          | DBTYPE \_ BOOL     |
| VT \_ BSTR          | DBTYPE \_ BSTR     |
| VT \_ BYREF         | DBTYPE \_ BYREF    |
| VT \_ CY            | DBTYPE \_ CY       |
| VT \_ 日期          | DBTYPE \_ 日期     |
| VT \_ DECIMAL       | DBTYPE \_ DECIMAL  |
| VT \_ 空白         | DBTYPE \_ 空白    |
| VT \_ FILETIME      | DBTYPE \_ FILETIME |
| VT \_ GUID          | DBTYPE \_ GUID     |
| VT \_ I1            | DBTYPE \_ I1       |
| VT \_ I2            | DBTYPE \_ I2       |
| VT \_ I4            | DBTYPE \_ I4       |
| VT \_ I8            | DBTYPE \_ I8       |
| VT \_ Null          | DBTYPE \_ Null     |
| VT \_ R4            | DBTYPE \_ R4       |
| VT \_ R8            | DBTYPE \_ UI8      |
| VT \_ 向量        | DBTYPE \_ 向量   |
| VT \_ WSTR          | DBTYPE \_ WSTR     |



 

下表列出 XML 資料類型與 OLE DB 資料類型之間的對應。



| Variant 資料類型 | OLE DB 資料類型 |
|-------------------|------------------|
| 站。BASE64        | DBTYPE \_ 位元組    |
| 站。十六進位           | DBTYPE \_ I8       |
| BOOLEAN           | DBTYPE \_ BOOL     |
| CHAR              | DBTYPE \_ STR      |
| 日期              | DBTYPE \_ 日期     |
| DATETIME          | DBTYPE \_ 日期     |
| DATETIME。TZ       | DBTYPE \_ 日期     |
| 已修正14。4        | DBTYPE \_ R4       |
| FLOAT             | DBTYPE \_ R8       |
| I1                | DBTYPE \_ I1       |
| I2                | DBTYPE \_ I2       |
| I4                | DBTYPE \_ I4       |
| I8                | DBTYPE \_ I8       |
| INT               | DBTYPE \_ I8       |
| LONG              | DBTYPE \_ I4       |
| NUMBER            | DBTYPE \_ R8       |
| R4                | DBTYPE \_ R4       |
| R8                | DBTYPE \_ R8       |
| STRING            | DBTYPE \_ WSTR     |
| TIME              | DBTYPE \_ FILETIME |
| 時間。TZ           | DBTYPE \_ FILETIME |
| UI1               | DBTYPE \_ UI2      |
| UI2               | DBTYPE \_ UI2      |
| UI4               | DBTYPE \_ UI4      |
| UI8               | DBTYPE \_ UI8      |
| URI               | DBTYPE \_ WSTR     |
| UUID              | DBTYPE \_ GUID     |



 

您可以將字串資料轉換成其他資料類型。 如需詳細資訊，請參閱 [轉換資料行的資料類型](-search-sql-castingdatacolumntype.md)。

 

 



