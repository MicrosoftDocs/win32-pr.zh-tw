---
description: ISA 運算子是 WQL 特定的運算子，可用於資料、事件和架構查詢中。
ms.assetid: 0520470c-ebfc-4c45-8a1f-47fd66bf8414
ms.tgt_platform: multiple
title: 適用于架構查詢的 ISA 運算子
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fb50146e4bd1219712c84bc1acec7fc7d50146b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987259"
---
# <a name="isa-operator-for-schema-queries"></a>適用于架構查詢的 ISA 運算子

ISA 運算子是 WQL 特定的運算子，可用於資料、事件和架構查詢中。

當架構查詢的 [WHERE 子句](where-clause.md) 中包含 ISA 時，它會要求將查詢套用至您指定之類別的所有子類別。

例如，下列語句會針對衍生自 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別之任何類別的成員，要求每10分鐘的實例修改事件通知。


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
WHERE TargetInstance ISA "Win32_LogicalDisk"
```



下列查詢會傳回 [**CIM \_ 處理器**](/windows/desktop/CIMWin32Prov/cim-processor) 類別的定義和其所有子類別的定義。


```sql
SELECT * FROM meta_class WHERE __this ISA "CIM_Processor"
```



類別 **中繼 \_ 類別** 會將此識別為架構查詢、呼叫 **\_ \_ 此** 屬性的屬性會識別查詢的目標類別，而 ISA 運算子會要求目標類別之子類別的定義。

 

 
