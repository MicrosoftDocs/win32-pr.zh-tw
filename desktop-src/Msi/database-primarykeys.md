---
description: 資料庫物件的 PrimaryKeys 屬性會傳回記錄物件，其中包含欄位0中的資料表名稱和資料行名稱， (在對應至其資料行編號的後續欄位中) 的主鍵。
ms.assetid: 9aeafda4-65b8-4469-a391-eb25ca72459d
title: PrimaryKeys 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.PrimaryKeys
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: dc266bc2e563e6f32b7ff9b8c7c8cb0df69b723d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995501"
---
# <a name="databaseprimarykeys-property"></a>PrimaryKeys 屬性

資料庫物件的 **PrimaryKeys** 屬性會傳回 [**記錄**](record-object.md)物件，其中包含欄位0中的資料表名稱和 [**資料**](database-object.md)行名稱， (在對應至其資料行編號的後續欄位中) 的主鍵。 記錄的欄位計數是主鍵資料行的計數。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Database.PrimaryKeys
```



## <a name="property-value"></a>屬性值

現有資料表的必要名稱。 如果資料表不存在，就會產生錯誤。

## <a name="remarks"></a>備註

**PrimaryKeys** 屬性不能與 [ \_ Tables 資料表](-tables-table.md)或 [ \_ Columns 資料表](-columns-table.md)搭配使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase 定義為 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




