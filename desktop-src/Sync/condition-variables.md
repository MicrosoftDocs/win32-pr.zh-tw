---
description: 條件變數是同步處理原始物件，可讓執行緒等候，直到發生特定條件為止。 條件變數是無法跨進程共用的使用者模式物件。
ms.assetid: fef9bab0-cd69-4812-869a-b43a10772d86
title: 條件變數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711fad7d80c1c5e06fc6e496198cd298b190daba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980408"
---
# <a name="condition-variables"></a>條件變數

條件變數是同步處理原始物件，可讓執行緒等候，直到發生特定條件為止。 條件變數是無法跨進程共用的使用者模式物件。

條件變數可讓執行緒以不可部分完成的方式釋放鎖定，並進入睡眠狀態。 它們可與重要區段或超薄讀取器/寫入器搭配使用 (SRW) 鎖定。 條件變數支援「喚醒一個」或「喚醒所有」等候中線程的作業。 喚醒執行緒之後，它會重新取得執行緒進入睡眠狀態時所釋放的鎖定。

請注意，呼叫端必須配置 **條件 \_ 變數** 結構，並將它初始化，方法是呼叫 [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) (，以動態方式初始化結構) 或將常數 **條件 \_ 變數 \_ INIT** 指派給結構變數 (以靜態方式) 初始化結構。

**Windows Server 2003 和 WINDOWS XP：** 不支援條件變數。

以下是條件變數函數。



| Condition 變數函式                                        | Description                                                                                                    |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) | 初始化條件變數。                                                                              |
| [**SleepConditionVariableCS**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablecs)       | 在指定的條件變數上進入睡眠狀態，並以不可部分完成的作業形式釋放指定的重要區段。 |
| [**SleepConditionVariableSRW**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablesrw)     | 在指定的條件變數上進入睡眠狀態，並以不可部分完成的作業形式釋放指定的 SRW 鎖定。         |
| [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable)       | 喚醒所有等候指定條件變數的執行緒。                                                 |
| [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable)             | 喚醒等候指定條件變數的單一執行緒。                                             |



 

下列虛擬程式碼示範條件變數的一般使用模式。

``` syntax
CRITICAL_SECTION CritSection;
CONDITION_VARIABLE ConditionVar;

void PerformOperationOnSharedData()
{ 
   EnterCriticalSection(&CritSection);

   // Wait until the predicate is TRUE

   while( TestPredicate() == FALSE )
   {
      SleepConditionVariableCS(&ConditionVar, &CritSection, INFINITE);
   }

   // The data can be changed safely because we own the critical 
   // section and the predicate is TRUE

   ChangeSharedData();

   LeaveCriticalSection(&CritSection);

   // If necessary, signal the condition variable by calling
   // WakeConditionVariable or WakeAllConditionVariable so other
   // threads can wake
}
```

例如，在讀取器/寫入器鎖定的執行中，此函式 `TestPredicate` 會驗證目前的鎖定要求與現有的擁有者是否相容。 如果是，則取得鎖定;否則，睡眠。 如需更詳細的範例，請參閱 [使用條件變數](using-condition-variables.md)。

條件變數會受限於未與明確喚醒) 和遭竊的假喚醒 (， (另一個執行緒會在喚醒執行緒) 之前執行管理。 因此，您應該在睡眠作業傳回之後，重新檢查述詞 (通常會在 **while** 迴圈中) 。

您可以使用 [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable) 或 [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable) 來喚醒其他執行緒，其方式是在與條件變數相關聯的鎖定內部或外部。 通常最好先釋放鎖定再喚醒其他執行緒，以減少內容切換的數目。

使用多個具有相同鎖定的條件變數通常很方便。 例如，讀取器/寫入器鎖定的執行可能會使用單一重要區段，但會針對讀取器和寫入器分隔線件變數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用條件變數](using-condition-variables.md)
</dt> </dl>

 

 
