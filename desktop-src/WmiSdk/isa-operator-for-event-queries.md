---
description: ISA 運算子是可用於事件查詢的 WQL 特定運算子。 當事件查詢的 WHERE 子句中包含 ISA 時，它會要求類別階層內所有類別的事件通知，而不是特定事件類別。
ms.assetid: 68b7a903-a206-4491-95c4-4a412537f6f5
ms.tgt_platform: multiple
title: 事件查詢的 ISA 運算子
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0acdd262492bfd876867bdfa7e13fd50e5380270
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027169"
---
# <a name="isa-operator-for-event-queries"></a><span data-ttu-id="eab70-104">事件查詢的 ISA 運算子</span><span class="sxs-lookup"><span data-stu-id="eab70-104">ISA Operator for Event Queries</span></span>

<span data-ttu-id="eab70-105">ISA 運算子是可用於事件查詢的 WQL 特定運算子。</span><span class="sxs-lookup"><span data-stu-id="eab70-105">The ISA operator is a WQL-specific operator that can be used in event queries.</span></span> <span data-ttu-id="eab70-106">當事件查詢的 [WHERE 子句](where-clause.md) 中包含 ISA 時，它會要求類別階層內所有類別的事件通知，而不是特定事件類別。</span><span class="sxs-lookup"><span data-stu-id="eab70-106">When ISA is included in the [WHERE clause](where-clause.md) of an event query, it requests notification of events for all classes within a class hierarchy, rather than a specific event class.</span></span>

<span data-ttu-id="eab70-107">下列範例會針對所有衍生自 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別之類別成員的實例，要求每10分鐘的實例修改事件通知。</span><span class="sxs-lookup"><span data-stu-id="eab70-107">The following example requests notification every 10 minutes of instance modification events for all instances that are members of any class derived from the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
WHERE TargetInstance ISA "Win32_LogicalDisk"
```



<span data-ttu-id="eab70-108">如需有關使用 ISA 搭配事件查詢的詳細資訊，請參閱使用 [win32 \_ LocalTime 或 Win32 \_ UTCTime 建立計時器事件](./creating-a-timer-event-with-win32-localtime-or-win32-utctime.md)。</span><span class="sxs-lookup"><span data-stu-id="eab70-108">For more information on using ISA with an event query, see [Creating a Timer Event with Win32\_LocalTime or Win32\_UTCTime](./creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).</span></span>

 

 
