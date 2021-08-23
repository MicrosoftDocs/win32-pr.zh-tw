---
description: 建議將所有永久的訂閱編譯到 \\ 根訂用帳戶 \\ 命名空間中。
ms.assetid: 6d4ccc86-f29f-4ca5-bea5-c77ee07d7789
ms.tgt_platform: multiple
title: 執行跨命名空間的永久事件訂閱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b175f89a4a686aa47818daf3479d521306f6190fb245222c4c21c17ca6470dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757948"
---
# <a name="implementing-cross-namespace-permanent-event-subscriptions"></a>執行跨命名空間的永久事件訂閱

建議將所有永久的訂閱編譯到 \\ 根訂用帳戶 \\ 命名空間中。 這可防止需要將永久取用者編譯成所使用的每個命名空間，這表示只有一個命名空間可尋找永久訂閱。 使用 [**\_ \_ >eventfilter**](--eventfilter.md)的 **EventNamespace** 屬性來執行跨命名空間的訂用帳戶。

使用 [**CommandLineEventConsumer**](commandlineeventconsumer.md)時，請務必保護您所啟動的可執行檔。 如果可執行檔不在安全的位置，或使用強式存取控制清單來保護 (ACL) ，任何人都可以使用自己的可執行檔來取代您的可執行檔。 如需 Acl 的詳細資訊，請參閱 [在 c + + 中建立新物件的安全描述項](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--)。

下列受控物件格式 (MOF) 程式碼範例顯示跨命名空間的訂用帳戶。

``` syntax
#pragma namespace("\\root\\subscription")

instance of __EventFilter as $FLT
{
  Name = "Filter";
  Query = "SELECT * FROM __InstanceModificationEvent "
          "WHERE TargetInstance ISA \"Win32_LocalTime\" "
          "AND TargetInstance.Hour = 8 "
          "AND TargetInstance.Minute = 0 "
          "AND TargetInstance.Second = 0 "
          "AND TargetInstance.DayOfWeek = 6";
  QueryLanguage = "WQL";
  EventNamespace = "root\\cimv2";
};

instance of CommandLineEventConsumer as $CONS
{
  ExecutablePath = "cmd.exe";
  ShowWindowCommand = 7;
  RunInteractively = true;
};

instance of __FilterToConsumerBinding
{
  Consumer = $CONS;
  Filter = $FLT;
};
```

 

 
