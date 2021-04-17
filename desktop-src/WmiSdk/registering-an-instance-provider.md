---
description: 若要建立 WMI 執行個體提供者，您必須 \_ \_ 使用 InstanceProviderRegistration 的實例，註冊代表提供者的 Win32Provider 實例 \_ \_ 。
ms.assetid: 5ac8e964-606f-4010-84a8-7c0ae6ca2133
ms.tgt_platform: multiple
title: 註冊執行個體提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bde8189559b04f2e45ac8357ab47cc17bd253fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512996"
---
# <a name="registering-an-instance-provider"></a>註冊執行個體提供者

若要建立 WMI [*執行個體提供者*](gloss-i.md)，您必須使用 [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md)的實例，註冊代表提供者的 [**\_ \_ Win32Provider**](--win32provider.md)實例。 如果您是 COM 物件，則您的提供者必須向作業系統和 WMI 註冊。 下列程式假設您已依照 [註冊提供者](registering-a-provider.md)中所述的方式來執行註冊程式。

下列程式說明如何註冊執行個體提供者。

**註冊執行個體提供者**

1.  建立描述提供者之 [**\_ \_ Win32Provider**](--win32provider.md)類別的實例。
2.  建立 [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md)類別的實例，以描述提供者的功能集。

    [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md)類別會繼承 [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md)父類別的許多屬性，其提供布林值，指出支援特定功能和字串陣列以表示查詢支援。

    請務必使用 [**動態**](standard-wmi-qualifiers.md) 和 [**提供者**](/windows/desktop/api/Provider/nl-provider-provider) 辨識符號來標記類別。 辨識符號表示 WMI 應該使用 **動態** 提供者來取出類別實例。 **提供者** 辨識符號會指定 WMI 應使用的提供者名稱。

下列程式碼範例說明如何註冊 [**\_ \_ Win32Provider**](--win32provider.md)和 [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md)實例。

``` syntax
instance of __Win32Provider as $P
{
    Name="TestProv";
    CLSID="{A41602A4-C038-11d1-AEB6-00C04FB68820}";
};

instance of __InstanceProviderRegistration
{
    Provider = $P;
    SupportsGet = TRUE;
    SupportsEnumeration = TRUE;
    QuerySupportLevels = { "WQL:UnarySelect" };
};
```

 

 



