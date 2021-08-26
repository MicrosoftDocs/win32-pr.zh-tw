---
description: 針對 WMI 提供者建立新 WMI 基類的建議方式，是在受控物件格式 (MOF) 檔中。
ms.assetid: d46060aa-77c3-4f51-b4a7-2c3612f2bc5c
ms.tgt_platform: multiple
title: 建立 WMI 基類
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4780279f00eea403b330400c490da75adfa097406796cd0b14f15f9861411bfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071508"
---
# <a name="creating-a-wmi-base-class"></a>建立 WMI 基類

針對 WMI 提供者建立新 WMI 基類的建議方式，是在受控物件格式 (MOF) 檔中。 您也可以使用 [適用于 WMI 的 COM API 來](com-api-for-wmi.md)建立基類。 雖然您可以在腳本中建立基底或衍生類別，但沒有提供資料給類別及其子類別的提供者，但類別並不實用。

本主題將討論下列各節：

-   [使用 MOF 建立基類](#creating-a-base-class-using-mof)
-   [使用 c + + 建立基類](#creating-a-base-class-with-c)
-   [相關主題](#related-topics)

## <a name="creating-a-base-class-using-mof"></a>使用 MOF 建立基類

WMI 類別通常依賴繼承。 在建立基類之前，請先檢查通用訊息模型 (可從分散式管理工作強制執行的 CIM) 類別 ([ [DMTF](https://www.dmtf.org/) ]) 。

如果有許多衍生類別會使用相同的屬性，請將這些屬性和方法放在基類中。 您可以在 WMI 類別中定義的最大屬性數目是1024。

建立基類時，請觀察下列類別名稱的方針清單：

-   使用大寫和小寫字母。
-   以字母開頭的類別名稱。
-   請勿使用開頭或尾端的底線。
-   將所有剩餘的字元定義為字母、數位或底線。
-   使用一致的命名慣例。

    雖然並非必要，但類別的良好命名慣例是以底線聯結的兩個元件。 有可能的話，廠商名稱應該構成名稱的前半部分，而描述性的類別名稱應該是第二個部分。

> [!Note]  
> 在執行提供者期間，無法變更類別。 您必須停止活動、變更類別，然後重新開機 Windows 管理服務。 目前無法偵測類別變更。

 

在 MOF 中，藉由使用 **class** 關鍵字命名來建立基類，但不表示父類別。

**使用 MOF 程式碼建立基類**

1.  使用 **類別** 關鍵字搭配新類別的名稱，後面加上一對大括弧和分號。 在大括弧之間加入類別的屬性和方法。 提供的程式碼範例如下。

    下列程式碼範例顯示如何定義基類。

    ``` syntax
    class MyClass_BaseDisk
    {
    };
    ```

    下列程式碼範例顯示基類的定義不正確。

    ``` syntax
    class MyClass_BaseDisk : CIM_LogicalDisk
    {
    };
    ```

2.  在 class 關鍵字之前加入任何類別 [*限定詞*](gloss-q.md) ，以修改類別的使用方式。 在方括弧之間放置限定詞。 如需修改類別之限定詞的詳細資訊，請參閱 [WMI 限定詞](wmi-qualifiers.md)。 使用 **抽象** 限定詞表示您無法直接建立此類別的實例。 抽象類別通常用來定義數個衍生類別將使用的屬性或方法。 如需詳細資訊，請參閱 [建立衍生類別](creating-a-derived-class.md)。

    下列程式碼範例會將類別定義為抽象，並定義將提供資料的提供者。 **ToSubClass** 限定詞類別表示 **提供者**[*辨識符號中*](gloss-f.md)的資訊是由衍生類別繼承。

    ``` syntax
    [Abstract, Provider("MyProvider") : ToSubClass]
    class MyClass_BaseDisk
    {
    };
    ```

3.  將類別的屬性和方法加入至屬性或方法名稱之前的方括弧內。 如需詳細資訊，請參閱 [新增屬性](adding-a-property.md) 和 [建立方法](creating-a-method.md)。 您可以使用 MOF 限定詞來修改這些屬性和方法。 如需詳細資訊，請參閱 [新增限定詞](adding-a-qualifier.md)。

    下列程式碼範例示範如何使用 MOF 限定詞來修改屬性和方法。

    ``` syntax
    [read : ToSubClass, key : ToSubClass ] string DeviceID;
      [read : ToSubClass] uint32 State;
      [read : ToSubclass, write : ToSubClass] uint64 LimitUsers;
    ```

4.  以 mof 副檔名儲存 MOF 檔案。
5.  藉由在檔案上執行 [**Mofcomp.exe**](mofcomp.md) ，向 WMI 註冊類別。

    **mofcomp.exe** *newmof mof*

    如果您未使用 **-N** 參數或預處理器命令 \# [**pragma 命名**](pragma-namespace.md)空間來指定命名空間，則編譯的 MOF 類別將會儲存在存放庫的根 \\ 預設命名空間中。 如需詳細資訊，請參閱 [**mofcomp.exe**](mofcomp.md)。

下列程式碼範例結合了先前程式中討論的 MOF 程式碼範例，並說明如何 \\ 使用 MOF 在根 cimv2 命名空間中建立基類。

``` syntax
#pragma namespace("\\\\.\\Root\\cimv2")

[Abstract, Provider("MyProvider") : ToSubClass]
class MyClass_BaseDisk
{
  [read : ToSubClass, key : ToSubClass ] string DeviceID;
  [read : ToSubClass] uint32 State;
  [read : ToSubClass, write : ToSubClass] uint64 LimitUsers;
};
```

如需詳細資訊，請參閱 [建立衍生類別](creating-a-derived-class.md) 以取得衍生自這個基類的動態類別範例。

## <a name="creating-a-base-class-with-c"></a>使用 c + + 建立基類

使用 WMI API 建立基類主要是一系列的 Put 命令，其定義類別並向 WMI 註冊類別。 此 API 的主要目的是要讓用戶端應用程式建立基類。 不過，您也可以讓提供者使用此 API 來建立基類。 例如，如果您認為提供者的 MOF 程式碼將無法正確安裝，您可以指示您的提供者在 WMI 儲存機制中自動建立正確的類別。 如需提供者的詳細資訊，請參閱 [撰寫類別提供者](writing-a-class-provider.md)。

> [!Note]  
> 在執行提供者期間，無法變更類別。 您必須停止活動、變更類別，然後重新開機 Windows 管理服務。 目前無法偵測類別變更。

 

程式碼需要下列參考才能正確編譯。


```C++
#include <wbemidl.h>
```



您可以使用 [適用于 WMI 的 COM API](com-api-for-wmi.md)，以程式設計方式建立新的基類。

**使用 WMI API 建立新的基類**

1.  藉由呼叫 [**IWbemServices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 方法，並將 *strObjectPath* 參數設定為 **null** 值，以抓取新類別的定義。

    下列程式碼範例示範如何取出新類別的定義。

    ```C++
    IWbemServices* pSvc = 0;
    IWbemContext* pCtx = 0;
    IWbemClassObject* pNewClass = 0;
    IWbemCallResult* pResult = 0;
    HRESULT hRes = pSvc->GetObject(0, 0, pCtx, &pNewClass, &pResult);
    ```

    

2.  藉由設定 **\_ \_ 類別** 系統屬性並呼叫 [**IWbemClassObject：:P**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)的 ui 方法，來建立類別的名稱。

    下列程式碼範例顯示如何藉由設定 **\_ \_ 類別** 系統屬性來命名類別。

    ```C++
    VARIANT v;
    VariantInit(&v);
    V_VT(&v) = VT_BSTR;

    V_BSTR(&v) = SysAllocString(L"Example");
    BSTR Class = SysAllocString(L"__CLASS");
    pNewClass->Put(Class, 0, &v, 0);
    SysFreeString(Class);
    VariantClear(&v);
    ```

    

3.  藉由呼叫 [**IWbemClassObject：:P**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)]，以建立索引鍵屬性。

    下列程式碼範例說明如何建立索引屬性，該屬性在步驟4中標示為 [**索引**](swbemrefreshableitem-index.md) 鍵屬性。

    ```C++
      BSTR KeyProp = SysAllocString(L"Index");
      pNewClass->Put(KeyProp, 0, NULL, CIM_STRING);
    ```

    

4.  先呼叫 [**IWbemClassObject：： GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset)方法，然後呼叫 [**IWbemQualifierSet：:P**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put)的 ui 方法，以將 [**金鑰**](standard-qualifiers.md)標準限定詞附加至索引鍵屬性。

    下列程式碼範例示範如何將 [**金鑰**](standard-qualifiers.md) 標準限定詞附加至索引鍵屬性。

    ```C++
      IWbemQualifierSet *pQual = 0;
      pNewClass->GetPropertyQualifierSet(KeyProp, &pQual);
      SysFreeString(KeyProp);

      V_VT(&v) = VT_BOOL;
      V_BOOL(&v) = VARIANT_TRUE;
      BSTR Key = SysAllocString(L"Key");

      pQual->Put(Key, &v, 0);   // Flavors not required for Key 
      SysFreeString(Key);

      // No longer need the qualifier set for "Index"
      pQual->Release();   
      VariantClear(&v);
    ```

    

5.  使用 [**IWbemClassObject：:P 的內容**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)，建立類別的其他屬性。

    下列程式碼範例說明如何建立其他屬性。

    ```C++
      V_VT(&v) = VT_BSTR;
      V_BSTR(&v) = SysAllocString(L"<default>");
      BSTR OtherProp = SysAllocString(L"OtherInfo");
      pNewClass->Put(OtherProp, 0, &v, CIM_STRING);
      SysFreeString(OtherProp);
      VariantClear(&v);

      OtherProp = SysAllocString(L"IntVal");
      pNewClass->Put(OtherProp, 0, NULL, CIM_SINT32); // NULL is default
      SysFreeString(OtherProp);
    ```

    

6.  藉由呼叫 [**IWbemServices：:P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)來註冊新的類別。

    因為您無法在註冊新類別之後定義索引鍵和索引，所以在呼叫 [**PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)之前，請確定您已定義所有屬性。

    下列程式碼範例說明如何註冊新的類別。

    ```C++
      hRes = pSvc->PutClass(pNewClass, 0, pCtx, &pResult);
      pNewClass->Release();
    ```

    

下列程式碼範例結合了先前程式中所討論的程式碼範例，並說明如何使用 WMI API 建立基類。


```C++
void CreateClass(IWbemServices *pSvc)
{
  IWbemClassObject *pNewClass = 0;
  IWbemContext *pCtx = 0;
  IWbemCallResult *pResult = 0;

  // Get a class definition. 
  // ============================
  HRESULT hRes = pSvc->GetObject(0, 0, pCtx, &pNewClass, &pResult);
  VARIANT v;
  VariantInit(&v);

  // Create the class name.
  // ============================
  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"Example");
  BSTR Class = SysAllocString(L"__CLASS");
  pNewClass->Put(Class, 0, &v, 0);
  SysFreeString(Class);
  VariantClear(&v);

  // Create the key property. 
  // ============================
  BSTR KeyProp = SysAllocString(L"Index");
  pNewClass->Put(KeyProp, 0, NULL, CIM_STRING);

  // Attach Key qualifier to mark the "Index" property as the key.
  // ============================
  IWbemQualifierSet *pQual = 0;
  pNewClass->GetPropertyQualifierSet(KeyProp, &pQual);
  SysFreeString(KeyProp);

  V_VT(&v) = VT_BOOL;
  V_BOOL(&v) = VARIANT_TRUE;
  BSTR Key = SysAllocString(L"Key");

  pQual->Put(Key, &v, 0);   // Flavors not required for Key 
  SysFreeString(Key);

  // No longer need the qualifier set for "Index"
  pQual->Release();     
  VariantClear(&v);

  // Create other properties.
  // ============================
  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"<default>");
  BSTR OtherProp = SysAllocString(L"OtherInfo");
  pNewClass->Put(OtherProp, 0, &v, CIM_STRING);
  SysFreeString(OtherProp);
  VariantClear(&v);

  OtherProp = SysAllocString(L"IntVal");
  pNewClass->Put(OtherProp, 0, NULL, CIM_SINT32); // NULL is default
  SysFreeString(OtherProp);
  
  // Register the class with WMI
  // ============================
  hRes = pSvc->PutClass(pNewClass, 0, pCtx, &pResult);
  pNewClass->Release();
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立類別](creating-a-class.md)
</dt> </dl>

 

 



