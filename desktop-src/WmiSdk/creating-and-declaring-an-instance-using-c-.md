---
description: 您可以透過 IWbemServices 介面，在 c + + 中建立實例。
ms.assetid: ee54c1ef-bc91-4771-8c11-9ee3aacd8112
ms.tgt_platform: multiple
title: 使用 c + + 建立和宣告實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd316975c68625383a9d2a2d1fe2fc389d30494a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997889"
---
# <a name="creating-and-declaring-an-instance-using-c"></a>使用 c + + 建立和宣告實例

您可以透過 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 介面，在 c + + 中建立實例。

本主題中的程式碼範例需要下列 \# include 語句才能正確編譯。


```C++
#include <wbemidl.h>
```



下列程式描述如何建立現有類別的實例。

**若要建立現有類別的實例**

1.  藉由呼叫 [**IWbemServices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 或 [**Iwbemservices：： GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) 方法，來取出現有類別的定義。

    下列程式碼範例會示範如何使用 [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 和 [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) 方法，取得可存取類別定義的 [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) 介面指標。

    ```C++
    // The pSv variable is of type IWbemServices *

    IWbemClassObject *pNewInstance = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
                  &pExampleClass, &pResult);
    SysFreeString(PathToClass);
    ```

    

2.  藉由呼叫 [**IWbemClassObject：： SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) 方法來建立新的實例。

    下列程式碼範例示範如何建立新的實例，然後釋放類別。

    ```C++
    pExampleClass->SpawnInstance(0, &pNewInstance);
    pExampleClass->Release();  // Don't need the class any more
    ```

    

3.  藉由呼叫 [**IWbemClassObject：:P**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) 的 ui 方法，設定任何未繼承類別定義之值的屬性值。

    類別的每個實例都會繼承針對該類別定義的所有屬性。 但是，如果您選擇，可以指定不同的屬性值。

    如果現有的類別有索引鍵屬性，您應該將屬性設定為 **Null** 或保證的唯一值。 如果您將索引鍵設定為 **Null** ，而且索引鍵是字串，則 [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) 或 [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) 會在內部產生並指派 GUID 給金鑰。 如此一來，為索引鍵屬性指定 **Null** ，可讓您建立不會覆寫任何先前實例的唯一實例。

    下列程式碼範例顯示如何設定範例實例類別的 [**Index**](swbemrefreshableitem-index.md) 屬性值。

    ```C++
    VARIANT v;
    VariantInit(&v);

    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"IX100");

    BSTR KeyProp = SysAllocString(L"Index");
    pNewInstance->Put(KeyProp, 0, &v, 0);
    SysFreeString(KeyProp);
    VariantClear(&v);
    ```

    

4.  透過呼叫 [**IWbemClassObject：： GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset)，設定任何相關限定詞的值。

    [**GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset)方法會傳回 [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset)介面的指標，該介面會用來存取類別或實例的限定詞。 如果類別限定詞的類別為 **EnableOverride**，您可以為類別定義的辨識符號指定不同的值。 您無法修改或刪除具有設定為 **DisableOverride** 之類別的類別限定詞。 如需詳細資訊，請參閱 [限定詞](qualifier-flavors.md)類別。

    您也可以選擇為實例類別定義其他限定詞。 您可以針對不需要出現在類別宣告中的實例或實例屬性，定義其他限定詞。

5.  藉由呼叫 [**iwbemservices：:P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) 或 [**Iwbemservices：:P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) 方法來儲存實例。

    WMI 會將實例儲存在目前的 WMI 命名空間中。 因此，實例的完整路徑會相依于命名空間，這通常是根 \\ 預設值。 在此程式碼範例中，完整路徑名稱會是 \\ \\ 。 \\根 \\ 預設值：範例. Index = "IX100"。

    下列程式碼範例顯示如何儲存實例。

    ```C++
        hRes = pSvc->PutInstance(pNewInstance, 0, pCtx, &pResult);
        pNewInstance->Release();
    ```

    

將實例儲存至 WMI 會鎖定實例的數個屬性。

具體而言，您無法在 WMI 基礎結構內的實例存在之後，透過 WMI API 執行下列任何作業：

-   變更實例所屬類別的父類別。
-   新增或移除屬性。
-   變更屬性類型。
-   新增或移除索引 [**鍵**](standard-qualifiers.md) 或 **索引** 限定詞。
-   新增或移除 [**單一**](standard-wmi-qualifiers.md)、 **動態** 或 [**抽象**](standard-qualifiers.md) 的限定詞。

下列程式碼範例結合了先前程式中所討論的程式碼範例，示範如何使用 WMI API 建立實例。


```C++
void CreateInstance (IWbemServices *pSvc)
{
    IWbemClassObject *pNewInstance = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    // Get the class definition.
    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
                 &pExampleClass, &pResult);
    SysFreeString(PathToClass);

    if (hRes != 0)
       return;

    // Create a new instance.
    pExampleClass->SpawnInstance(0, &pNewInstance);
    pExampleClass->Release();  // Don't need the class any more

    VARIANT v;
    VariantInit(&v);

    // Set the Index property (the key).
    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"IX100");

    BSTR KeyProp = SysAllocString(L"Index");
    pNewInstance->Put(KeyProp, 0, &v, 0);
    SysFreeString(KeyProp);
    VariantClear(&v);

    // Set the IntVal property.
    V_VT(&v) = VT_I4;
    V_I4(&v) = 1001;  
    
    BSTR Prop = SysAllocString(L"IntVal");
    pNewInstance->Put(Prop, 0, &v, 0);
    SysFreeString(Prop);
    VariantClear(&v);    
    
    // Other properties acquire the 'default' value specified
    // in the class definition unless otherwise modified here.

    // Write the instance to WMI. 
    hRes = pSvc->PutInstance(pNewInstance, 0, pCtx, &pResult);
    pNewInstance->Release();
}
```



 

 



