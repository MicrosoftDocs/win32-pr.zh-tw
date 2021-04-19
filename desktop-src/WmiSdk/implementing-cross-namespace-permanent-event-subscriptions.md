---
description: 建議將所有永久的訂閱編譯到 \\ 根訂用帳戶 \\ 命名空間中。
ms.assetid: 6d4ccc86-f29f-4ca5-bea5-c77ee07d7789
ms.tgt_platform: multiple
title: 執行跨命名空間的永久事件訂閱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52771e40d4dfb036354c3b37b562b32edd3034ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988894"
---
# <a name="implementing-cross-namespace-permanent-event-subscriptions"></a><span data-ttu-id="a5e8c-103">執行跨命名空間的永久事件訂閱</span><span class="sxs-lookup"><span data-stu-id="a5e8c-103">Implementing Cross-Namespace Permanent Event Subscriptions</span></span>

<span data-ttu-id="a5e8c-104">建議將所有永久的訂閱編譯到 \\ 根訂用帳戶 \\ 命名空間中。</span><span class="sxs-lookup"><span data-stu-id="a5e8c-104">It is recommended that all permanent subscriptions be compiled into the \\root\\subscription namespace.</span></span> <span data-ttu-id="a5e8c-105">這可防止需要將永久取用者編譯成所使用的每個命名空間，這表示只有一個命名空間可尋找永久訂閱。</span><span class="sxs-lookup"><span data-stu-id="a5e8c-105">This prevents the need to compile the permanent consumer into each namespace being used, which means that there is only one namespace to look for permanent subscriptions.</span></span> <span data-ttu-id="a5e8c-106">使用 [**\_ \_ >eventfilter**](--eventfilter.md)的 **EventNamespace** 屬性來執行跨命名空間的訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="a5e8c-106">Use the **EventNamespace** property of [**\_\_EventFilter**](--eventfilter.md) to implement a cross-namespace subscription.</span></span>

<span data-ttu-id="a5e8c-107">使用 [**CommandLineEventConsumer**](commandlineeventconsumer.md)時，請務必保護您所啟動的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="a5e8c-107">When using the [**CommandLineEventConsumer**](commandlineeventconsumer.md), it is important to secure the executable you are launching.</span></span> <span data-ttu-id="a5e8c-108">如果可執行檔不在安全的位置，或使用強式存取控制清單來保護 (ACL) ，任何人都可以使用自己的可執行檔來取代您的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="a5e8c-108">If the executable is not in a secure location, or secured with a strong access control list (ACL), anyone can replace your executable with one of their own.</span></span> <span data-ttu-id="a5e8c-109">如需 Acl 的詳細資訊，請參閱 [在 c + + 中建立新物件的安全描述項](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--)。</span><span class="sxs-lookup"><span data-stu-id="a5e8c-109">For more information about ACLs, see [Creating a Security Descriptor for a New Object in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

<span data-ttu-id="a5e8c-110">下列受控物件格式 (MOF) 程式碼範例顯示跨命名空間的訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="a5e8c-110">The following Managed Object Format (MOF) code example shows a cross-namespace subscription.</span></span>

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

 

 
