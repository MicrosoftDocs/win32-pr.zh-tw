---
description: 若要建立 WMI 方法提供者，您必須 \_ \_ 使用 MethodProviderRegistration 的實例，註冊代表提供者的 Win32Provider 實例 \_ \_ 。
ms.assetid: 1cfb16ae-8dcf-437d-b779-db2f30bb0d34
ms.tgt_platform: multiple
title: 註冊方法提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a399f90c6fc6f97e9ada8051055505b43885da3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193635"
---
# <a name="registering-a-method-provider"></a>註冊方法提供者

若要建立 WMI [*方法提供者*](gloss-m.md)，您必須使用 [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md)的實例，註冊代表提供者的 [**\_ \_ Win32Provider**](--win32provider.md)實例。 建立 [**\_ \_ Win32Provider**](--win32provider.md)的實例之後，您必須向 WMI 註冊該提供者。 如果您是 COM 物件，則您的提供者必須向作業系統和 WMI 註冊。 下列程式假設您已依照 [註冊提供者](registering-a-provider.md)中所述的方式來執行註冊程式。

下列程式說明如何註冊方法提供者。

**註冊方法提供者**

1.  建立描述提供者之 [**\_ \_ Win32Provider**](--win32provider.md)類別的實例。

    [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md)系統類別繼承 [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md)父類別的許多屬性，不過，與方法提供者相關的唯一屬性是 [**\_ \_ Win32Provider**](--win32provider.md)實例的物件路徑。

2.  建立 [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md)類別的實例，以描述提供者的功能集。

    請務必使用 [**動態**](dynamic-qualifier.md) 和 [**提供者**](/windows/desktop/api/Provider/nl-provider-provider) 辨識符號來標記類別。 **動態** 限定詞表示 WMI 應該使用提供者來取出類別實例。 **提供者** 辨識符號會指定 WMI 應使用的提供者名稱。

下列程式碼範例說明如何註冊方法提供者。

``` syntax
  instance of __Win32Provider as $P
  {
    Name    = "MethProvider" ;
    ClsId   = "{E30EC6A0-23CF-11d1-8FDE-0000F804AA5C}" ;
  };    

  instance of __MethodProviderRegistration
  {
    Provider = $P;
  };
```

 

 



