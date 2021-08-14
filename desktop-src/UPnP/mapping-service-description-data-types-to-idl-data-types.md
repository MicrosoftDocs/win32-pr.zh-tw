---
title: 將服務描述資料類型對應至 IDL 資料類型
description: 下表顯示在服務描述中指定的 XML 資料類型與 IDL 中所使用之對應資料類型的對應。
ms.assetid: eeb86177-8c3b-47f1-bbe1-f9aabd2dde76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a34a5ec9ee092091dc00c7cc420b4474a38d8cba0d41c2691943c7dcd5b35e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118347628"
---
# <a name="mapping-service-description-data-types-to-idl-data-types"></a>將服務描述資料類型對應至 IDL 資料類型

下表顯示在服務描述中指定的 XML 資料類型與 IDL 中所使用之對應資料類型的對應。



| XML 資料類型 | IDL 資料類型  |
|---------------|----------------|
| bin.base64    | SAFEARRAY      |
| bin.hex       | SAFEARRAY      |
| boolean       | VARIANT \_ BOOL  |
| char          | wchar \_ t       |
| date          | 日期           |
| dateTime      | 日期           |
| dateTime.tz   | 日期           |
| fixed.14.4    | CY             |
| FLOAT         | FLOAT          |
| i1            | char           |
| i2            | short          |
| i4            | long           |
| int           | long           |
| number        | BSTR           |
| r4            | FLOAT          |
| r8            | double         |
| string        | BSTR           |
| time          | 日期           |
| time.tz       | 日期           |
| ui1           | unsigned char  |
| ui2           | unsigned short |
| ui4           | unsigned long  |
| uri           | BSTR           |
| uuid          | BSTR           |



 

 

 




