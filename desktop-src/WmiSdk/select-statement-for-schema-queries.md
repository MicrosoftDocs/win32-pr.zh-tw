---
description: 架構資料查詢會使用 SELECT 語句，其語法與資料查詢類似。
ms.assetid: e7150aaa-5829-4d64-a13b-39f83adc5b98
ms.tgt_platform: multiple
title: 架構查詢的 SELECT 語句
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd08cffa3fccc9a8cc2bf50452dcefcc1b7bfc0a62e512069b2db098bc6d13c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315672"
---
# <a name="select-statement-for-schema-queries"></a>架構查詢的 SELECT 語句

架構資料查詢會使用 SELECT 語句，其語法與 [資料查詢](select-statement-for-data-queries.md)類似。 差別在於使用稱為「中繼類別」的特殊類別 \_ ，這會將查詢識別為架構查詢。

下列範例會要求目前命名空間內的所有類別定義。


```sql
SELECT * FROM meta_class
```



架構查詢僅支援 " \* "。 為了縮小傳回的定義範圍，提供者可以加入指定特定類別的 WHERE 子句。

下列範例示範如何加入 WHERE 子句來指定特定類別。


```sql
SELECT * FROM meta_class WHERE __this ISA "Win32_LogicalDisk"
```



**\_ \_ 所謂的** 特殊屬性會識別架構查詢的目標類別。 請注意，ISA 運算子必須搭配 **\_ \_ 這個** 屬性使用，才能要求目標類別子類別的定義。 上述查詢會傳回 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別的定義和其所有子類別的定義。

下列範例顯示如何使用 **\_ \_ 類別** 系統屬性來要求單一類別的類別定義。


```sql
SELECT * FROM meta_class WHERE __Class = "Win32_LogicalDisk"
```



此查詢相當於呼叫 [**iwbemservices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 或 [**Iwbemservices：： GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) 方法，並將物件路徑參數設定為 "Win32 \_ LogicalDisk"。

下列 VBScript 程式碼範例會捕獲最上層 WMI 類別的所有子類別。 \_ \_ 時代 WMI 系統屬性會保存類別衍生自最上層類別的名稱，您可以使用此名稱來取得衍生自最上層類別之命名空間中的所有類別，包括該類別。


```VB
' Retrieve immediate child classes for Cim_DataFile

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _ 
    ("Select * From meta_class " _
    & "Where __Dynasty = 'Win32_CurrentTime'")

For Each objClass In colClasses 
    WScript.Echo objClass.SystemProperties_("__Class")
Next
```



下列 VBScript 會抓取 WMI 類別的直屬子類別。


```VB
' Retrieve immediate child classes for Cim_DataFile

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _ 
    ("Select * From meta_class " _
    & "Where __Superclass = 'Cim_DataFile'")

For Each objClass In colClasses 
    WScript.Echo objClass.SystemProperties_("__Class")
Next
```



下列 VBScript 會抓取最上層類別。 針對 WMI 命名空間中的所有最上層類別， \_ \_ 超級類別系統屬性為 Null。 因此，您可以藉由搜尋 Null 超類別來取得最上層類別。


```VB
 Retrieve top level classes in root\cimv2

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _
    ("Select * From meta_class Where __Superclass Is Null")

For Each objClass In colClasses
    WScript.Echo objClass.SystemProperties_("__Class")

```



 

 
