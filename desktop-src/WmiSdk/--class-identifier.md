---
description: 知名的識別碼 \_ \_ 類別會參考每個 WMI 物件上的虛擬屬性，該物件表示目前物件的類別。
ms.assetid: a1d0e934-c5b5-4554-9d6e-3881064419ca
ms.tgt_platform: multiple
title: __CLASS 識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0b4db6cacb6943619cf6468cf7f03d4a4c08278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115660"
---
# <a name="__class-identifier"></a>\_\_類別識別碼

知名的識別碼 \_ \_ 類別會參考每個 WMI 物件上的虛擬屬性，該物件表示目前物件的類別。

使用 \_ \_ [WHERE](where-clause.md)子句中的類別，從結果集中篩選出衍生類別的任何物件。 例如，下列查詢的結果集不僅包含類別為 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)的物件，也包含其類別衍生自 **win32 \_ LogicalDisk** 的物件。


```sql
SELECT * FROM Win32_LogicalDisk
```



在下列範例中，在 \_ \_ **WHERE** 子句中使用類別會篩選出衍生自 [**win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)之類別的所有物件，因為其類別不是 **win32 \_ LogicalDisk**。


```sql
SELECT * FROM Win32_LogicalDisk   WHERE __CLASS = "Win32_LogicalDisk"
```



\_ \_ 不論是否有任何子類別，在要求提供特定類別實例的提供者中使用類別。

 

 
