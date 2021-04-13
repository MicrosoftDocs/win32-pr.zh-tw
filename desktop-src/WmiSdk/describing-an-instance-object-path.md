---
description: 實例物件路徑描述特定命名空間內指定類別之實例的位置。
ms.assetid: 78a194f0-cd21-4622-9242-be7e430b96c0
ms.tgt_platform: multiple
title: 描述實例物件路徑
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f977359ea9c3c4346052f1edd076c0cce5544441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319795"
---
# <a name="describing-an-instance-object-path"></a>描述實例物件路徑

實例物件路徑描述特定命名空間內指定類別之實例的位置。

您可以有數種不同類型的實例物件路徑：

-   完整

    完整的實例物件路徑會將類別的索引鍵屬性名稱和值附加至完整類別物件路徑。

    下列範例會顯示完整實例物件路徑的定義。

    ``` syntax
    \\Server\Namespace:Class.KeyName="KeyValue"
    ```

-   相對

    相對物件路徑會參考位於目前伺服器上目前命名空間的實例。 相對路徑包含類別名稱，後面接著此實例之索引鍵屬性的名稱和值。

    下列範例會顯示相對實例物件路徑的定義。

    ``` syntax
    MyClass.MyProp="e:"
    ```

-   相對於單一金鑰

    對於僅有一個屬性指定為索引鍵的類別，您可以省略索引鍵屬性的名稱。

    下列範例顯示具有單一索引鍵之相對實例物件路徑的定義。

    ``` syntax
    MyClass="e:"
    ```

-   相對於多個索引鍵

    使用逗號來區別具有多個索引鍵的實例索引鍵。

    下列範例會顯示具有多個索引鍵之相對實例物件路徑的定義。

    ``` syntax
    MyOtherClass.FirstKey=1,SecondKey=2
    ```

-   相對於單一類別

    單一類別的相對物件路徑包含類別名稱，後面接著 "= @" 標記法。

    下列範例會顯示單一類別之相對實例物件路徑的定義。

    ``` syntax
    MySingletonClass=@
    ```

下列程式描述如何取出類別實例。

**若要取出類別實例**

1.  使用 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) 函式的呼叫，初始化包含物件路徑的字串。
2.  初始化將接收實例的物件。
3.  透過呼叫 [**IWbemServices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 或 [**Iwbemservices：： GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)來取出物件。

    若要使用 [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)，您必須執行 [**IWbemSink**](swbemsink.md) 介面。

\#本主題稍後所列的程式碼需要下列 include 語句，才能正確編譯。


```C++
#include <wbemidl.h>
```



下列程式碼範例說明如何使用物件路徑來取出類別實例。


```C++
IWbemServices* pWbemSvcs = 0;

BSTR Path = SysAllocString(L"ComPort=2");    
IWbemClassObject *pComPort = 0;
pWbemSvcs->GetObject(Path, 0, 0, &pComPort, 0);
```



針對指定多個屬性做為索引鍵之類別的實例，WMI 不需要在物件路徑中有特定的索引鍵屬性順序。 您只需要指定物件路徑中每個屬性的值。

下列程式碼範例描述兩個對等的索引鍵描述。

``` syntax
MyClass.IntVal=33,StrVal="AAA"
MyClass.StrVal="AAA",IntVal=33
```

 

 
