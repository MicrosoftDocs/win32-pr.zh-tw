---
description: 在 WMI 中建立衍生類別非常類似于建立基類。 如同基類，您必須先定義衍生類別，然後向 WMI 註冊衍生類別。
ms.assetid: 8dd483b8-8bc2-4a5c-b981-6c2ffaccdb95
ms.tgt_platform: multiple
title: 建立 WMI 衍生類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cddc2b381346b2765e836bb3606cc06845280c41a7505b872098f383ac0409c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119374868"
---
# <a name="creating-a-wmi-derived-class"></a>建立 WMI 衍生類別

在 WMI 中建立衍生類別非常類似于建立基類。 如同基類，您必須先定義衍生類別，然後向 WMI 註冊衍生類別。 主要的差異在於，您必須先找出您想要從中衍生的父類別。 如需詳細資訊，請參閱 [撰寫類別提供者](writing-a-class-provider.md) 和 [撰寫執行個體提供者](writing-an-instance-provider.md)。

為提供者建立類別的建議方式是在受控物件格式 (MOF) 檔案中。 數個彼此相關的衍生類別應群組為 MOF 檔案，以及它們從中衍生屬性或方法的任何基類。 如果您將每個類別放在個別的 MOF 檔案中，則必須先編譯每個檔案，提供者才能正常運作。

建立類別之後，您必須先刪除類別的所有實例，才能在您的衍生類別上執行下列任何一個活動：

-   變更衍生類別的父類別。
-   新增或移除屬性。
-   變更屬性類型。
-   新增或移除索引 [**鍵**](key-qualifier.md) 或 **索引** 限定詞。
-   新增或移除 [**單一**](standard-wmi-qualifiers.md)、 **動態** 或 [**抽象**](standard-qualifiers.md) 的限定詞。

> [!Note]  
> 若要加入、移除或修改屬性或辨識符號，請呼叫 [**IWbemServices：:P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)或 [**SWbemObject \_**](swbemobject-put-.md) ，並將旗標參數設定為「強制模式」。 只有在父類別為抽象時，才能使用 [**抽象**](standard-qualifiers.md) 限定詞。

 

當您宣告衍生類別時，請遵守下列規則和限制：

-   衍生類別的父類別必須已經存在。

    父類別的宣告可以與衍生類別出現在相同的 MOF 檔案中，也可以出現在不同的檔案中。 如果父類別是未知的，則編譯器會產生執行階段錯誤。

-   衍生類別只能有一個父類別。

    WMI 不支援多重繼承。 不過，父類別可以有許多衍生類別。

-   您可以定義衍生類別的索引，但 WMI 不會使用這些索引。

    因此，在衍生類別上指定索引不會改善衍生類別實例的查詢效能。 您可以針對衍生類別的父類別指定索引屬性，以改善衍生類別的查詢效能。

-   衍生的類別定義可能更複雜，而且可以包含別名、限定詞和辨識符號等功能。

    如需詳細資訊，請參閱 [建立別名](creating-an-alias.md) 和 [新增限定詞](adding-a-qualifier.md)。

-   如果您想要變更限定詞、變更基類屬性的預設值，或使用更強型別來變更基類的參考或内嵌物件屬性，您必須再次宣告整個基類。
-   您可以在 WMI 類別中定義的最大屬性數目是1024。

> [!Note]  
> 在執行提供者期間，無法變更類別。 您必須停止活動、變更類別，然後重新開機 Windows 管理服務。 目前無法偵測類別變更。

 

就像基類一樣，這項技術最常見的用法是用戶端應用程式。 但是，提供者也可以建立衍生類別。 如需詳細資訊，請參閱 [建立基類](creating-a-base-class.md) 和 [撰寫類別提供者](writing-a-class-provider.md)。

本主題中的程式碼範例需要下列 \# include 語句才能正確編譯。


```C++
#include <wbemidl.h>
```



下列程式說明如何使用 c + + 建立衍生類別。

**使用 c + + 建立衍生類別**

1.  找出呼叫 [**IWbemServices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)的基類。

    下列程式碼範例顯示如何找出範例基類。

    ```C++
    // The pSv variable is of type IWbemServices *

    IWbemClassObject *pNewDerivedClass = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, &pExampleClass, &pResult);
    SysFreeString(PathToClass);
    ```

    

2.  呼叫 [**IWbemClassObject：： SpawnDerivedClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass)，從基類建立衍生物件。

    下列程式碼範例顯示如何建立衍生類別物件。

    ```C++
    pExampleClass->SpawnDerivedClass(0, &pNewDerivedClass);
    pExampleClass->Release();  // Don't need the parent class any more
    ```

    

3.  藉由設定 **\_ \_ 類別** 系統屬性並呼叫 [**IWbemClassObject：:P**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)的 ui 方法，來建立類別的名稱。

    下列程式碼範例顯示如何將名稱指派給衍生類別。

    ```C++
    VARIANT v;
    VariantInit(&v);

    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"Example2");
    BSTR Class = SysAllocString(L"__CLASS");
    pNewDerivedClass->Put(Class, 0, &v, 0);
    SysFreeString(Class);
    VariantClear(&v);
    ```

    

4.  使用 IWbemClassObject 來建立其他屬性 [**：:P**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)]。

    下列程式碼範例顯示如何建立其他屬性。

    ```C++
    BSTR OtherProp = SysAllocString(L"OtherInfo2");
    pNewDerivedClass->Put(OtherProp, 0, NULL, CIM_STRING); 
    SysFreeString(OtherProp);
    ```

    

5.  藉由呼叫 [**IWbemServices：:P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)來儲存新的類別。

    下列程式碼範例顯示如何儲存新的衍生類別。

    ```C++
    hRes = pSvc->PutClass(pNewDerivedClass, 0, pCtx, &pResult);
    pNewDerivedClass->Release();
    ```

    

下列程式碼範例結合了先前程式中所討論的程式碼範例，說明如何使用 WMI API 建立衍生類別。


```C++
void CreateDerivedClass(IWbemServices *pSvc)
{
  IWbemClassObject *pNewDerivedClass = 0;
  IWbemClassObject *pExampleClass = 0;
  IWbemContext *pCtx = 0;
  IWbemCallResult *pResult = 0;

  BSTR PathToClass = SysAllocString(L"Example");
  HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
    &pExampleClass, &pResult);
  SysFreeString(PathToClass);

  if (hRes != 0)
    return;

  pExampleClass->SpawnDerivedClass(0, &pNewDerivedClass);
  pExampleClass->Release();  // The parent class is no longer needed

  VARIANT v;
  VariantInit(&v);

  // Create the class name.
  // =====================

  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"Example2");
  BSTR Class = SysAllocString(L"__CLASS");
  pNewDerivedClass->Put(Class, 0, &v, 0);
  SysFreeString(Class);
  VariantClear(&v);

  // Create another property.
  // =======================
  BSTR OtherProp = SysAllocString(L"OtherInfo2");
  // No default value
  pNewDerivedClass->Put(OtherProp, 0, NULL, CIM_STRING); 
  SysFreeString(OtherProp);
  
  // Register the class with WMI. 
  // ============================
  hRes = pSvc->PutClass(pNewDerivedClass, 0, pCtx, &pResult);
  pNewDerivedClass->Release();
}
```



下列程式描述如何使用 MOF 程式碼定義衍生類別。

**使用 MOF 程式碼定義衍生類別**

1.  使用 **class** 關鍵字定義您的衍生類別，後面接著衍生類別的名稱，並以冒號分隔父類別的名稱。

    下列程式碼範例說明衍生類別的實作為。

    ``` syntax
    class MyClass 
    {
        [key] string   strProp;
        sint32   dwProp1;
        uint32       dwProp2;
    };

    class MyDerivedClass : MyClass
    {
        string   strDerivedProp;
        sint32   dwDerivedProp;
    };
    ```

2.  完成時，使用 MOF 編譯器編譯您的 MOF 程式碼。

    如需詳細資訊，請參閱 [編譯 MOF](compiling-mof-files.md)檔案。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立類別](creating-a-class.md)
</dt> </dl>

 

 



