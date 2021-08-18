---
description: 在事件查詢中使用內子句來指定輪詢間隔或群組間隔。
ms.assetid: e2fc7627-fb3d-4966-b38b-441333868ae3
ms.tgt_platform: multiple
title: 在子句內
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee35350a52ef6af1aa22aacf775d22b3c7629fb479967a74aed1408aa5e1f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757598"
---
# <a name="within-clause"></a>在子句內

事件取用者會在事件查詢中使用 in 子句來指定 *輪詢間隔* 或 *群組間隔*。

輪詢間隔是 Windows Management Instrumentation (WMI) 用來輪詢[內部事件](determining-the-type-of-event-to-receive.md)之類別的資料提供者的間隔，而查詢的事件則是成員。 這個間隔是事件告知必須傳遞之前所能夠等待的最長時間。 當取用者需要對類別進行變更的通知，且事件提供者無法使用時，取用者會在內建子句中使用輪詢間隔。 取用者會註冊內部事件並包含輪詢間隔。

若要指定輪詢間隔，請在 WHERE 子句之前放置內的子句，如下所示：


```sql
SELECT * FROM IntrinsicEventClass WITHIN interval  WHERE property = value
```



IntrinsicEventClass 是內部事件類別，其事件為成員、間隔是輪詢間隔，而值則是取用者需要通知的屬性值。

輪詢間隔是浮點數，而且可以是小數以接受小於1秒的值。 不過，間隔應代表幾秒鐘的時間，而不是非常小的值（例如0.001），因為指定太小的值可能會導致 WMI 拒絕不正確語句，因為輪詢的資源密集性質。 因為大部分的事件取用者不需要立即通知，所以建議使用超過5分鐘的間隔。

下列查詢範例會要求 WMI 每隔10秒檢查一次，以進行 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別實例的變更。 如果在指定的輪詢間隔內修改了類別的實例，就會針對每個修改傳送一個通知事件。


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 10  WHERE TargetInstance ISA "Win32_LogicalDisk"
```



視查詢而定，事件提供者和 WMI 可以共用提供事件的工作。 例如，支援 [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)和 [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md)系統類別事件的事件提供者，而不是 [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md)系統類別的事件。 下列查詢可讓事件提供者在事件發生時產生建立和修改事件，並在建立事件時加以傳遞。 此查詢也可讓 WMI 使用輪詢機制，每 10 (10) 秒產生 **\_ \_ InstanceDeletionEvent** 事件。


```sql
SELECT * FROM __InstanceOperationEvent WITHIN 10  WHERE TargetInstance ISA "MyOwnClass"
```



您也可以使用內子句來指定群組間隔。 群組間隔是一種不帶正負號的32位整數，可指定在接收初始事件之後，WMI 應該收集類似事件的時間週期。 當這段時間過期時，WMI 會傳遞匯總事件，由所有類似的事件組成。 如需詳細資訊，請參閱 [Group 子句](group-clause.md)。

註冊經常發生之事件的事件取用者，會搭配使用群組間隔與內子句。 將群組加入至事件查詢中的 WHERE 子句，會導致 WMI 傳送一個匯總事件，而不是多個事件。 匯總事件是以 [**\_ \_ AggregateEvent**](--aggregateevent.md)系統類別表示。

若要指定群組間隔，請將內的子句放在 GROUP 子句之後。


```sql
SELECT * FROM EventClass WHERE property = value GROUP WITHIN Interval
```



EventClass 是事件所屬的事件類別，值是取用者需要通知的屬性值，而間隔是群組間隔。

如需詳細資訊，請參閱 [決定要接收的事件種類](determining-the-type-of-event-to-receive.md)。

只有當您具有系統管理員許可權時，才能使用輪詢查詢來建立永久事件取用者。

 

 
