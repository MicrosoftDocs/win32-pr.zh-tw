---
description: 產生物件的 XML 表示。
ms.assetid: 06d2b532-7ab2-489d-9021-27b5187c8f2b
ms.tgt_platform: multiple
title: 以 XML 表示物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9698c54eeff61517a1389ceea14bc2415727f085
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986842"
---
# <a name="representing-objects-in-xml"></a>以 XML 表示物件

WMI 中的 XML 編碼器元件會產生物件的 XML 標記法。

在 c + + 中，您可以使用 [**IWbemObjectTextSrc. GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) 方法的呼叫來啟動 XML 編碼器，並指定要以 XML 表示的物件，以及要在標記法中使用的文字格式。 如需詳細資訊和程式碼範例，請參閱使用 C/c + + 以 XML 編碼物件。

在 VBScript 或 Visual Basic 中，若要將 XML 實例的資料編碼，請呼叫 [**SWbemObjectEx. GetText**](swbemobjectex-gettext-.md)。 如需詳細資訊和程式碼範例，請參閱使用 VBScript 以 XML 編碼物件。

本主題將討論下列各節：

-   [使用 C 或 c + + 編碼物件](#encode-an-object-using-c-or-c)
-   [使用 VBScript 編碼物件](#encode-an-object-using-vbscript)
-   [相關主題](#related-topics)

## <a name="encode-an-object-using-c-or-c"></a>使用 C 或 c + + 編碼物件

<span id="to_encode_an_object_in_xml_using_c_c_"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_C_C_"></span>

下列程式說明如何使用 C 或 c + + 以 XML 編碼物件。

**使用 C 或 c + + 以 XML 編碼物件**

1.  設定您的程式以存取 WMI 資料。

    由於 WMI 是以 COM 技術為基礎，因此您必須對 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 和 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 函數執行必要的呼叫，才能存取 WMI。 如需詳細資訊，請參閱 [初始化 WMI 應用程式的 COM](initializing-com-for-a-wmi-application.md)。

2.  （選擇性）建立 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) 物件，並將它初始化。

    除非您需要變更預設操作，否則不需要建立 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) 物件。 XML 編碼器會使用內容物件來控制物件的 XML 標記法中包含的資訊量。

    下表列出可為內容物件指定的選擇性值。

    

    <table>
    <thead>
    <tr class="header">
    <th>值/類型</th>
    <th>意義</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>&quot;LocalOnly &quot; <strong>VT_BOOL</strong></td>
    <td>若 <strong>為 TRUE</strong>，則只有在類別中本機定義的屬性和方法會出現在產生的 XML 中。 預設值為 <strong>FALSE</strong>。</td>
    </tr>
    <tr class="even">
    <td>&quot;IncludeQualifiers &quot; <strong>VT_BOOL</strong></td>
    <td>若 <strong>為 TRUE</strong>，則會在產生的 XML 中包含類別、實例、屬性和方法限定詞。 預設值為 <strong>FALSE</strong>。</td>
    </tr>
    <tr class="odd">
    <td>&quot;ExcludeSystemProperties &quot; <strong>VT_BOOL</strong></td>
    <td>若 <strong>為 TRUE</strong>，則會將 WMI 系統屬性從輸出中篩選掉。 預設值為 <strong>FALSE</strong>。</td>
    </tr>
    <tr class="even">
    <td>&quot;PathLevel &quot; <strong>VT_I4</strong></td>
    <td><dl> 0 = <CLASS> 產生或 <INSTANCE> 元素。<br />
1 = <VALUE.NAMEDOBJECT> 產生元素。<br />
2 = <VALUE.OBJECTWITHLOCALPATH> 產生元素。<br />
3 = <VALUE.OBJECTWITHPATH> 產生。<br />
    </dl> 預設值是 0 (零)。<br/></td>
    </tr>
    </tbody>
    </table>

    

     

    下列程式碼範例顯示如何初始化內容物件，以包含限定詞和排除系統屬性。

    ```C++
    VARIANT vValue;
    IWbemContext *pContext = NULL;
    HRESULT hr = CoCreateInstance (CLSID_WbemContext, 
                           NULL, 
                           CLSCTX_INPROC_SERVER,
                           IID_IWbemContext, 
                           (void**) &pContext);
    if (FAILED(hr))
    {
      printf("Create context failed with %x\n", hr);
      return hr;
    }

    // Generate a <VALUE.OBJECTWITHLOCALPATH> element
    VariantInit(&vValue);
    vValue.vt = VT_I4;
    vValue.lVal = 2;
    pContext->SetValue(L"PathLevel", 0, &vValue);
    VariantClear(&vValue);

    // Include qualifiers
    VariantInit(&vValue);
    vValue.vt = VT_BOOL;
    vValue.boolVal = VARIANT_TRUE;
    pContext->SetValue(L"IncludeQualifiers", 0, &vValue);
    VariantClear(&vValue);

    // Exclude system properties
    VariantInit(&vValue);
    vValue.vt = VT_BOOL;
    vValue.boolVal = VARIANT_TRUE;
    pContext->SetValue(L"ExcludeSystemProperties", 0, &vValue);
    VariantClear(&vValue);
    ```

    

3.  取得要在 XML 中編碼之類別或實例的參考。

    在您初始化 COM 並連接至 WMI 之後，請呼叫 [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 來取得指定之類別或實例的參考。 如果您使用 BSTR 來指定類別或實例，請呼叫 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)所配置的記憶體。

    下列程式碼範例會抓取 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 實例的參考。

    ```C++
    HRESULT hr = NULL;
    IWbemClassObject *pClass = NULL;
    BSTR strObj = SysAllocString(L"Win32_LogicalDisk");

    hr = pConnection->GetObject(strObj, 
                                0, 
                                NULL, 
                                &pClass, 
                                NULL);

    SysFreeString(strObj);
    if (FAILED(hr))
    {
      printf("GetObject failed with %x\n",hr)
      return hr;
    }
    ```

    

4.  建立 [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) 物件。

    擁有物件的參考之後，您必須使用 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)的呼叫來建立 [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc)物件。 **IWbemObjectTextSrc** 物件是用來產生實際的 XML 文字。

    下列程式碼範例示範如何透過呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)來建立 [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc)物件。

    ```C++
    HRESULT hr = NULL;
    IWbemObjectTextSrc *pSrc = NULL;

    hr = CoCreateInstance (CLSID_WbemObjectTextSrc, 
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_IWbemObjectTextSrc, 
                           (void**) &pSrc);

    if (FAILED(hr))
    {
        printf("CoCreateInstance of IWbemObjectTextSrc failed %x\n",hr);
        return hr;
    }
    ```

    

5.  叫用 [**IWbemObjectTextSrc. GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) 方法，以取得物件的 XML 標記法。

    在設定物件表示的內容、取得物件的參考，以及建立 [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) 物件之後，您就可以藉由呼叫 [**IWbemObjectTextSrc. GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) 方法，來產生指定之物件的 XML 標記法。

    下列 c + + 範例程式碼會產生 *pClass* 所參考之物件的 XML 標記法。 XML 標記法會在 *strText* 中傳回。 [**GetText**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc)的第三個參數指定要用於 XML 的文字格式，而且必須是 wmi \_ obj \_ text \_ CIM \_ dtd \_ 2 \_ 0 (0x1) 或 wmi \_ obj \_ text \_ wmi \_ dtd \_ 2 \_ 0 (0x2) 。 如需這些值的詳細資訊，請參閱 [**IWbemObjectTextSrc：： GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) 參數值。

    ```C++
    HRESULT hr = NULL;
    BSTR strText = NULL;
    hr = pSrc->GetText(0, 
                       pClass, 
                       WMI_OBJ_TEXT_CIM_DTD_2_0,
                       pContext, 
                       &strText);

    // Perform a task with strText
    SysFreeString(strText);

    if (FAILED(hr))
    {
      printf("GetText failed with %x\n", hr);
      return hr;
    }
    ```

    

下列 c + + 範例程式碼包含上一個程式中的所有步驟，並將 XML 中的 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別編碼，包括類別、屬性和方法限定詞，以及排除系統屬性。


```C++
// The following #define statement is needed so that 
// the proper values are loaded by the #include files.
#define _WIN32_WINNT 0x0500

#include <stdio.h>
#include <wbemcli.h>
#pragma comment(lib, "wbemuuid.lib")

// Initialize the context object
// ---------------------------------------------
void FillUpContext(IWbemContext *pContext)
{
  VARIANT vValue;

  // IncludeQualifiers
  VariantInit(&vValue);
  vValue.vt = VT_BOOL;
  vValue.boolVal = VARIANT_FALSE;
  pContext->SetValue(L"IncludeQualifiers", 0, &vValue);
  VariantClear(&vValue);

  VariantInit(&vValue);
  vValue.vt = VT_I4;
  vValue.lVal = 0;
  pContext->SetValue(L"PathLevel", 0, &vValue);
  VariantClear(&vValue);

  // ExcludeSystemProperties
  VariantInit(&vValue);
  vValue.vt = VT_BOOL;
  vValue.boolVal = VARIANT_TRUE;
  pContext->SetValue(L"ExcludeSystemProperties", 0, &vValue);
  VariantClear(&vValue);
}

// Main method ... drives the program
// ---------------------------------------------
int _cdecl main(int argc, char * argv[])
{
  BSTR strNs = NULL;
  BSTR strObj = NULL;
  BSTR strText = NULL;

  if(FAILED(CoInitialize(NULL)))
    return 1;
  HRESULT hr = E_FAIL;
  IWbemObjectTextSrc *pSrc = NULL;

  IWbemLocator *pL = NULL;
  if(SUCCEEDED(hr = CoCreateInstance (CLSID_WbemLocator, 
                                      NULL, 
                                      CLSCTX_INPROC_SERVER,
                                      IID_IWbemLocator, 
                                      (void**) &pL)))
  {
    // Create a context object
    IWbemContext *pContext = NULL;
    if(SUCCEEDED(hr = CoCreateInstance (CLSID_WbemContext, 
                                        NULL, 
                                        CLSCTX_INPROC_SERVER,
                                        IID_IWbemContext, 
                                        (void**) &pContext)))
    {
      FillUpContext(pContext);
      IWbemServices *pConnection = NULL;
      strNs = SysAllocString(L"root\\cimv2");
      strText = NULL;
      if(SUCCEEDED(hr = pL->ConnectServer(strNs, 
                                          NULL, 
                                          NULL, 
                                          NULL, 
                                          0, 
                                          NULL, 
                                          NULL, 
                                          &pConnection)))
      {
        IWbemClassObject *pClass = NULL;
        strObj = SysAllocString(L"Win32_LogicalDisk");

        if(SUCCEEDED(hr = CoCreateInstance (CLSID_WbemObjectTextSrc, 
                                            NULL,
                                            CLSCTX_INPROC_SERVER,
                                            IID_IWbemObjectTextSrc, 
                                            (void**) &pSrc)))
        {
          // Test for GetObject
          if(SUCCEEDED(hr = pConnection->GetObject(strObj, 
                                                   0, 
                                                   NULL, 
                                                   &pClass, 
                                                   NULL)))
          {
            if(SUCCEEDED(hr = pSrc->GetText(0, 
                                            pClass, 
                                            WMI_OBJ_TEXT_CIM_DTD_2_0,
                                            pContext, 
                                            &strText)))
            {
              printf("GETOBJECT SUCCEEDED\n");
              printf("==========================================\n");
              wprintf(strText);
              pContext->Release();
              pClass->Release();
            }
            else
            {
              printf("GetText failed with %x\n", hr);
              // Free up the object
              pContext->Release();
              pClass->Release();
            }
          }
          else
            printf("GetObject failed with %x\n", hr);
        }
        else
          printf("CoCreateInstance on WbemObjectTextSrc failed with %x\n", hr);
      }
      else
        printf("ConnectServer on root\\cimv2 failed with %x\n", hr);
    }
    else
      printf("CoCreateInstance on Context failed with %x\n", hr);
  }
  else
    printf("CoCreateInstance on Locator failed with %x\n", hr);

// Clean up memory
  if (strNs != NULL)
    SysFreeString(strNs);
  if (strObj != NULL)
    SysFreeString(strObj);
  if (strText != NULL)
    SysFreeString(strText);
  if (pSrc != NULL)
    pSrc->Release();
  if (pL != NULL)
    pL->Release();
  return 0;
}
```



## <a name="encode-an-object-using-vbscript"></a>使用 VBScript 編碼物件

<span id="to_encode_an_object_in_xml_using_vbscript"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_VBSCRIPT"></span>

下列程式描述如何使用 VBScript 以 XML 編碼物件。

**使用 VBScript 以 XML 編碼物件**

1.  （選擇性）建立 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，並將它初始化，以便設定 XML 表示所需的內容值。

    下列程式碼範例會示範值如何指示 XML 編碼器產生 <的值。OBJECTWITHLOCALPATH> 專案，包括所有的限定詞，以及在建立物件的 XML 標記法時排除系統屬性。

    ```VB
    ' Create an optional SWbemNamedValueSet object
    set context = CreateObject("wbemscripting.SWbemNamedValueSet")

    ' Initialize the value set object to set the context
    ' Generate a <VALUE.OBJECTWITHLOCALPATH> element
    context.add "PathLevel", 2 
    context.add "IncludeQualifiers", true 
    context.add "ExcludeSystemProperties", true '
    ```

    

2.  取出物件或類別的實例以在 XML 中表示。

    下列程式碼範例會抓取物件的實例。

    ```VB
    ' Retrieve the object/class to be represented in XML
    set myObj = GetObject("winmgmts:\\.\root\cimv2:win32_LogicalDisk")
    ```

    

3.  叫用在上一個步驟中建立之實例的 [**GetText \_**](swbemobjectex-gettext-.md)方法，並使用1做為參數來指定對應到 CIM dtd 2.0 版的文字格式，或2指定對應至 WMI dtd 2.0 版的文字格式。 如果您在步驟1中建立了 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，請將它包含在參數清單中做為第三個參數。

    下列程式碼範例顯示如何叫用實例 [**的 \_ GetText**](swbemobjectex-gettext-.md)方法。

    ```VB
    ' Get the XML representation of the object
    strText = myObj.GetText_(2,,context)

    ' If you have not used a SWbemNamedValueSet object
    ' enter the following line.
    strText = myObj.GetText_(2)
    ```

    

4.  （選擇性）藉由建立 XML 檔物件模型 (DOM) 物件，然後將 XML 文字載入其中，來驗證步驟3中所產生的 XML 是否為格式正確的 XML。

    下列程式碼範例示範如何建立及初始化 XML DOM 物件，並將 XML 文字載入其中。

    ```VB
    ' Create an XMLDOM object
    set xml = CreateObject("Microsoft.xmldom")

    ' Initialize the XMLDOM object so results are returned synchronously
    xml.async = false

    ' Load the XML into the XMLDOM object
    xml.loadxml strText
    ```

    

5.  輸出物件的 XML 標記法。

    下列程式碼範例顯示如何使用 wscript.echo 來輸出 XML。

    ```VB
    wscript.echo strText
    ```

    

    如果您選擇使用 XML DOM 來確認產生的 XML 格式是否正確，請以下列程式碼取代前一行。

    ```VB
    wscript.echo xml.xml
    ```

    

下列 VBScript 程式碼範例包含上述程式中的所有步驟，並以 XML 編碼 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別，包括類別、屬性和方法限定詞，以及排除系統屬性。


```VB
' Create optional SWbemNamedValueSet object
set context = CreateObject("Wbemscripting.SWbemNamedValueSet")

' Initialize the context object
context.add "PathLevel", 2
context.add "IncludeQualifiers", true
context.add "ExcludeSystemProperties", true

' Retrieve the object/class to be represented in XML
set myObj = GetObject("winmgmts:\\.\root\cimv2:Win32_LogicalDisk")

' Get the XML representation of the object
strText = myObj.GetText_(2,,context)
' If you have not used a SWbemNamedValueSet object 
'   use the following line
'   strText = myObj.GetText(2)

' Print the XML representation
wscript.echo strText

' If you choose to use the XML DOM to verify 
'   that the XML generated is well-formed, replace the last
'   line in the above code example with the following lines:

' Create an XMLDOM object
set xml = CreateObject("Microsoft.xmldom")

' Initialize the XMLDOM object so results are 
'   returned synchronously
xml.async = false

' Load the XML into the XMLDOM object
xml.loadxml strText

' Print the XML representation
wscript.echo xml.xml
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 WMI](using-wmi.md)
</dt> </dl>

 

