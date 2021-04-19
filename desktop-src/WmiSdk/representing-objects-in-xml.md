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
# <a name="representing-objects-in-xml"></a><span data-ttu-id="2a807-103">以 XML 表示物件</span><span class="sxs-lookup"><span data-stu-id="2a807-103">Representing Objects in XML</span></span>

<span data-ttu-id="2a807-104">WMI 中的 XML 編碼器元件會產生物件的 XML 標記法。</span><span class="sxs-lookup"><span data-stu-id="2a807-104">The XML encoder component in WMI generates XML representations of objects.</span></span>

<span data-ttu-id="2a807-105">在 c + + 中，您可以使用 [**IWbemObjectTextSrc. GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) 方法的呼叫來啟動 XML 編碼器，並指定要以 XML 表示的物件，以及要在標記法中使用的文字格式。</span><span class="sxs-lookup"><span data-stu-id="2a807-105">In C++, you can start the XML encoder with a call to the [**IWbemObjectTextSrc.GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) method, specifying the object to be represented in XML and the text format to use in the representation.</span></span> <span data-ttu-id="2a807-106">如需詳細資訊和程式碼範例，請參閱使用 C/c + + 以 XML 編碼物件。</span><span class="sxs-lookup"><span data-stu-id="2a807-106">For more information and a code example, see To encode an object in XML using C/C++.</span></span>

<span data-ttu-id="2a807-107">在 VBScript 或 Visual Basic 中，若要將 XML 實例的資料編碼，請呼叫 [**SWbemObjectEx. GetText**](swbemobjectex-gettext-.md)。</span><span class="sxs-lookup"><span data-stu-id="2a807-107">In VBScript or Visual Basic, to encode data for an XML instance, call [**SWbemObjectEx.GetText**](swbemobjectex-gettext-.md).</span></span> <span data-ttu-id="2a807-108">如需詳細資訊和程式碼範例，請參閱使用 VBScript 以 XML 編碼物件。</span><span class="sxs-lookup"><span data-stu-id="2a807-108">For more information and a code example, see To encode an object in XML using VBScript.</span></span>

<span data-ttu-id="2a807-109">本主題將討論下列各節：</span><span class="sxs-lookup"><span data-stu-id="2a807-109">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="2a807-110">使用 C 或 c + + 編碼物件</span><span class="sxs-lookup"><span data-stu-id="2a807-110">Encode an Object Using C or C++</span></span>](#encode-an-object-using-c-or-c)
-   [<span data-ttu-id="2a807-111">使用 VBScript 編碼物件</span><span class="sxs-lookup"><span data-stu-id="2a807-111">Encode an Object Using VBScript</span></span>](#encode-an-object-using-vbscript)
-   [<span data-ttu-id="2a807-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="2a807-112">Related topics</span></span>](#related-topics)

## <a name="encode-an-object-using-c-or-c"></a><span data-ttu-id="2a807-113">使用 C 或 c + + 編碼物件</span><span class="sxs-lookup"><span data-stu-id="2a807-113">Encode an Object Using C or C++</span></span>

<span id="to_encode_an_object_in_xml_using_c_c_"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_C_C_"></span>

<span data-ttu-id="2a807-114">下列程式說明如何使用 C 或 c + + 以 XML 編碼物件。</span><span class="sxs-lookup"><span data-stu-id="2a807-114">The following procedure describes how to encode an object in XML using C or C++.</span></span>

<span data-ttu-id="2a807-115">**使用 C 或 c + + 以 XML 編碼物件**</span><span class="sxs-lookup"><span data-stu-id="2a807-115">**To encode an object in XML using C or C++**</span></span>

1.  <span data-ttu-id="2a807-116">設定您的程式以存取 WMI 資料。</span><span class="sxs-lookup"><span data-stu-id="2a807-116">Set up your program to access WMI data.</span></span>

    <span data-ttu-id="2a807-117">由於 WMI 是以 COM 技術為基礎，因此您必須對 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 和 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 函數執行必要的呼叫，才能存取 WMI。</span><span class="sxs-lookup"><span data-stu-id="2a807-117">Because WMI is based on COM technology, you must perform the requisite calls to the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) functions to access WMI.</span></span> <span data-ttu-id="2a807-118">如需詳細資訊，請參閱 [初始化 WMI 應用程式的 COM](initializing-com-for-a-wmi-application.md)。</span><span class="sxs-lookup"><span data-stu-id="2a807-118">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

2.  <span data-ttu-id="2a807-119">（選擇性）建立 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) 物件，並將它初始化。</span><span class="sxs-lookup"><span data-stu-id="2a807-119">Optionally, create an [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object and initialize it.</span></span>

    <span data-ttu-id="2a807-120">除非您需要變更預設操作，否則不需要建立 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) 物件。</span><span class="sxs-lookup"><span data-stu-id="2a807-120">You do not need to create the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object unless you need to change the default operation.</span></span> <span data-ttu-id="2a807-121">XML 編碼器會使用內容物件來控制物件的 XML 標記法中包含的資訊量。</span><span class="sxs-lookup"><span data-stu-id="2a807-121">The context object is used by the XML encoder to control the amount of information included in the object's XML representation.</span></span>

    <span data-ttu-id="2a807-122">下表列出可為內容物件指定的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="2a807-122">The following table lists the optional values that can be specified for the context object.</span></span>

    

    <table>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="2a807-123">值/類型</span><span class="sxs-lookup"><span data-stu-id="2a807-123">Value/type</span></span></th>
    <th><span data-ttu-id="2a807-124">意義</span><span class="sxs-lookup"><span data-stu-id="2a807-124">Meaning</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="2a807-125">&quot;LocalOnly &quot; <strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="2a807-125">&quot;LocalOnly&quot; <strong>VT_BOOL</strong></span></span></td>
    <td><span data-ttu-id="2a807-126">若 <strong>為 TRUE</strong>，則只有在類別中本機定義的屬性和方法會出現在產生的 XML 中。</span><span class="sxs-lookup"><span data-stu-id="2a807-126">When <strong>TRUE</strong>, only properties and methods defined locally in the class are present in the resulting XML.</span></span> <span data-ttu-id="2a807-127">預設值為 <strong>FALSE</strong>。</span><span class="sxs-lookup"><span data-stu-id="2a807-127">The default value is <strong>FALSE</strong>.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="2a807-128">&quot;IncludeQualifiers &quot; <strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="2a807-128">&quot;IncludeQualifiers&quot; <strong>VT_BOOL</strong></span></span></td>
    <td><span data-ttu-id="2a807-129">若 <strong>為 TRUE</strong>，則會在產生的 XML 中包含類別、實例、屬性和方法限定詞。</span><span class="sxs-lookup"><span data-stu-id="2a807-129">When <strong>TRUE</strong>, class, instance, properties, and method qualifiers are included in the resulting XML.</span></span> <span data-ttu-id="2a807-130">預設值為 <strong>FALSE</strong>。</span><span class="sxs-lookup"><span data-stu-id="2a807-130">The default value is <strong>FALSE</strong>.</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="2a807-131">&quot;ExcludeSystemProperties &quot; <strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="2a807-131">&quot;ExcludeSystemProperties&quot; <strong>VT_BOOL</strong></span></span></td>
    <td><span data-ttu-id="2a807-132">若 <strong>為 TRUE</strong>，則會將 WMI 系統屬性從輸出中篩選掉。</span><span class="sxs-lookup"><span data-stu-id="2a807-132">When <strong>TRUE</strong>, WMI system properties are filtered out of the output.</span></span> <span data-ttu-id="2a807-133">預設值為 <strong>FALSE</strong>。</span><span class="sxs-lookup"><span data-stu-id="2a807-133">The default value is <strong>FALSE</strong>.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="2a807-134">&quot;PathLevel &quot; <strong>VT_I4</strong></span><span class="sxs-lookup"><span data-stu-id="2a807-134">&quot;PathLevel&quot; <strong>VT_I4</strong></span></span></td>
    <td><dl> <span data-ttu-id="2a807-135">0 = <CLASS> 產生或 <INSTANCE> 元素。</span><span class="sxs-lookup"><span data-stu-id="2a807-135">0 = A <CLASS> or <INSTANCE> element is generated.</span></span><br />
<span data-ttu-id="2a807-136">1 = <VALUE.NAMEDOBJECT> 產生元素。</span><span class="sxs-lookup"><span data-stu-id="2a807-136">1 = A <VALUE.NAMEDOBJECT> element is generated.</span></span><br />
<span data-ttu-id="2a807-137">2 = <VALUE.OBJECTWITHLOCALPATH> 產生元素。</span><span class="sxs-lookup"><span data-stu-id="2a807-137">2 = A <VALUE.OBJECTWITHLOCALPATH> element is generated.</span></span><br />
<span data-ttu-id="2a807-138">3 = <VALUE.OBJECTWITHPATH> 產生。</span><span class="sxs-lookup"><span data-stu-id="2a807-138">3 = A <VALUE.OBJECTWITHPATH> is generated.</span></span><br />
    </dl> <span data-ttu-id="2a807-139">預設值是 0 (零)。</span><span class="sxs-lookup"><span data-stu-id="2a807-139">The default is 0 (zero).</span></span><br/></td>
    </tr>
    </tbody>
    </table>

    

     

    <span data-ttu-id="2a807-140">下列程式碼範例顯示如何初始化內容物件，以包含限定詞和排除系統屬性。</span><span class="sxs-lookup"><span data-stu-id="2a807-140">The following code example shows how the context object is initialized to include qualifiers and exclude system properties.</span></span>

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

    

3.  <span data-ttu-id="2a807-141">取得要在 XML 中編碼之類別或實例的參考。</span><span class="sxs-lookup"><span data-stu-id="2a807-141">Get a reference to the class or instance to encode in XML.</span></span>

    <span data-ttu-id="2a807-142">在您初始化 COM 並連接至 WMI 之後，請呼叫 [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 來取得指定之類別或實例的參考。</span><span class="sxs-lookup"><span data-stu-id="2a807-142">After you have initialized COM and are connected to WMI, call [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) to retrieve a reference to the specified class or instance.</span></span> <span data-ttu-id="2a807-143">如果您使用 BSTR 來指定類別或實例，請呼叫 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="2a807-143">If you used a BSTR to specify the class or instance, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free up the memory allocated by [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring).</span></span>

    <span data-ttu-id="2a807-144">下列程式碼範例會抓取 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 實例的參考。</span><span class="sxs-lookup"><span data-stu-id="2a807-144">The following code example retrieves a reference to an [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) instance.</span></span>

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

    

4.  <span data-ttu-id="2a807-145">建立 [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) 物件。</span><span class="sxs-lookup"><span data-stu-id="2a807-145">Create an [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) object.</span></span>

    <span data-ttu-id="2a807-146">擁有物件的參考之後，您必須使用 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)的呼叫來建立 [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc)物件。</span><span class="sxs-lookup"><span data-stu-id="2a807-146">After you have a reference to an object you must create the [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) object with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="2a807-147">**IWbemObjectTextSrc** 物件是用來產生實際的 XML 文字。</span><span class="sxs-lookup"><span data-stu-id="2a807-147">The **IWbemObjectTextSrc** object is used to generate the actual XML text.</span></span>

    <span data-ttu-id="2a807-148">下列程式碼範例示範如何透過呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)來建立 [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc)物件。</span><span class="sxs-lookup"><span data-stu-id="2a807-148">The following code example shows how to create an [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) object by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

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

    

5.  <span data-ttu-id="2a807-149">叫用 [**IWbemObjectTextSrc. GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) 方法，以取得物件的 XML 標記法。</span><span class="sxs-lookup"><span data-stu-id="2a807-149">Invoke the [**IWbemObjectTextSrc.GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) method to get an XML representation of an object.</span></span>

    <span data-ttu-id="2a807-150">在設定物件表示的內容、取得物件的參考，以及建立 [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) 物件之後，您就可以藉由呼叫 [**IWbemObjectTextSrc. GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) 方法，來產生指定之物件的 XML 標記法。</span><span class="sxs-lookup"><span data-stu-id="2a807-150">After setting the context for the object's representation, getting a reference to the object, and creating an [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) object, you are ready to generate an XML representation of the specified object by calling the [**IWbemObjectTextSrc.GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) method.</span></span>

    <span data-ttu-id="2a807-151">下列 c + + 範例程式碼會產生 *pClass* 所參考之物件的 XML 標記法。</span><span class="sxs-lookup"><span data-stu-id="2a807-151">The following C++ example code generates an XML representation of the object referenced by *pClass*.</span></span> <span data-ttu-id="2a807-152">XML 標記法會在 *strText* 中傳回。</span><span class="sxs-lookup"><span data-stu-id="2a807-152">The XML representation is returned in *strText*.</span></span> <span data-ttu-id="2a807-153">[**GetText**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc)的第三個參數指定要用於 XML 的文字格式，而且必須是 wmi \_ obj \_ text \_ CIM \_ dtd \_ 2 \_ 0 (0x1) 或 wmi \_ obj \_ text \_ wmi \_ dtd \_ 2 \_ 0 (0x2) 。</span><span class="sxs-lookup"><span data-stu-id="2a807-153">The third parameter of [**GetText**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) specifies the text format to be used for the XML and must be either WMI\_OBJ\_TEXT\_CIM\_DTD\_2\_0 (0x1) or WMI\_OBJ\_TEXT\_WMI\_DTD\_2\_0 (0x2).</span></span> <span data-ttu-id="2a807-154">如需這些值的詳細資訊，請參閱 [**IWbemObjectTextSrc：： GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) 參數值。</span><span class="sxs-lookup"><span data-stu-id="2a807-154">For more information about these values, see [**IWbemObjectTextSrc::GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) Parameter Values.</span></span>

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

    

<span data-ttu-id="2a807-155">下列 c + + 範例程式碼包含上一個程式中的所有步驟，並將 XML 中的 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別編碼，包括類別、屬性和方法限定詞，以及排除系統屬性。</span><span class="sxs-lookup"><span data-stu-id="2a807-155">The following C++ example code includes all of the steps in the previous procedure and encodes the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in XML including class, property, and method qualifiers and excluding system properties.</span></span>


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



## <a name="encode-an-object-using-vbscript"></a><span data-ttu-id="2a807-156">使用 VBScript 編碼物件</span><span class="sxs-lookup"><span data-stu-id="2a807-156">Encode an Object Using VBScript</span></span>

<span id="to_encode_an_object_in_xml_using_vbscript"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_VBSCRIPT"></span>

<span data-ttu-id="2a807-157">下列程式描述如何使用 VBScript 以 XML 編碼物件。</span><span class="sxs-lookup"><span data-stu-id="2a807-157">The following procedure describes how to encode an object in XML using VBScript.</span></span>

<span data-ttu-id="2a807-158">**使用 VBScript 以 XML 編碼物件**</span><span class="sxs-lookup"><span data-stu-id="2a807-158">**To encode an object in XML using VBScript**</span></span>

1.  <span data-ttu-id="2a807-159">（選擇性）建立 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，並將它初始化，以便設定 XML 表示所需的內容值。</span><span class="sxs-lookup"><span data-stu-id="2a807-159">Optionally, create an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object and initialize it so as to set the context values required for the XML representation.</span></span>

    <span data-ttu-id="2a807-160">下列程式碼範例會示範值如何指示 XML 編碼器產生 <的值。OBJECTWITHLOCALPATH> 專案，包括所有的限定詞，以及在建立物件的 XML 標記法時排除系統屬性。</span><span class="sxs-lookup"><span data-stu-id="2a807-160">The following code example shows how the values instruct the XML encoder to generate a <VALUE.OBJECTWITHLOCALPATH> element, including all of the qualifiers and excluding system properties when it constructs the XML representation of the object.</span></span>

    ```VB
    ' Create an optional SWbemNamedValueSet object
    set context = CreateObject("wbemscripting.SWbemNamedValueSet")

    ' Initialize the value set object to set the context
    ' Generate a <VALUE.OBJECTWITHLOCALPATH> element
    context.add "PathLevel", 2 
    context.add "IncludeQualifiers", true 
    context.add "ExcludeSystemProperties", true '
    ```

    

2.  <span data-ttu-id="2a807-161">取出物件或類別的實例以在 XML 中表示。</span><span class="sxs-lookup"><span data-stu-id="2a807-161">Retrieve an instance of the object or class to represent in XML.</span></span>

    <span data-ttu-id="2a807-162">下列程式碼範例會抓取物件的實例。</span><span class="sxs-lookup"><span data-stu-id="2a807-162">The following code example retrieves an instance of the object.</span></span>

    ```VB
    ' Retrieve the object/class to be represented in XML
    set myObj = GetObject("winmgmts:\\.\root\cimv2:win32_LogicalDisk")
    ```

    

3.  <span data-ttu-id="2a807-163">叫用在上一個步驟中建立之實例的 [**GetText \_**](swbemobjectex-gettext-.md)方法，並使用1做為參數來指定對應到 CIM dtd 2.0 版的文字格式，或2指定對應至 WMI dtd 2.0 版的文字格式。</span><span class="sxs-lookup"><span data-stu-id="2a807-163">Invoke the [**GetText\_**](swbemobjectex-gettext-.md) method of the instance created in the preceding step, using 1 as the parameter to specify the text format that corresponds to CIM DTD version 2.0, or 2 to specify the text format that corresponds to WMI DTD version 2.0.</span></span> <span data-ttu-id="2a807-164">如果您在步驟1中建立了 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，請將它包含在參數清單中做為第三個參數。</span><span class="sxs-lookup"><span data-stu-id="2a807-164">If you created the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object in Step 1, include it in the parameter list as the third parameter.</span></span>

    <span data-ttu-id="2a807-165">下列程式碼範例顯示如何叫用實例 [**的 \_ GetText**](swbemobjectex-gettext-.md)方法。</span><span class="sxs-lookup"><span data-stu-id="2a807-165">The following code example shows how to invoke the [**GetText\_**](swbemobjectex-gettext-.md) method of the instance.</span></span>

    ```VB
    ' Get the XML representation of the object
    strText = myObj.GetText_(2,,context)

    ' If you have not used a SWbemNamedValueSet object
    ' enter the following line.
    strText = myObj.GetText_(2)
    ```

    

4.  <span data-ttu-id="2a807-166">（選擇性）藉由建立 XML 檔物件模型 (DOM) 物件，然後將 XML 文字載入其中，來驗證步驟3中所產生的 XML 是否為格式正確的 XML。</span><span class="sxs-lookup"><span data-stu-id="2a807-166">Optionally, validate that the XML generated in Step 3 is well-formed XML, by creating and initializing an XML Document Object Model (DOM) object and then load the XML text into it.</span></span>

    <span data-ttu-id="2a807-167">下列程式碼範例示範如何建立及初始化 XML DOM 物件，並將 XML 文字載入其中。</span><span class="sxs-lookup"><span data-stu-id="2a807-167">The following code example shows how to create and initialize an XML DOM object and load the XML text into it.</span></span>

    ```VB
    ' Create an XMLDOM object
    set xml = CreateObject("Microsoft.xmldom")

    ' Initialize the XMLDOM object so results are returned synchronously
    xml.async = false

    ' Load the XML into the XMLDOM object
    xml.loadxml strText
    ```

    

5.  <span data-ttu-id="2a807-168">輸出物件的 XML 標記法。</span><span class="sxs-lookup"><span data-stu-id="2a807-168">Output the XML representation of the object.</span></span>

    <span data-ttu-id="2a807-169">下列程式碼範例顯示如何使用 wscript.echo 來輸出 XML。</span><span class="sxs-lookup"><span data-stu-id="2a807-169">The following code example shows how to use wscript to output the XML.</span></span>

    ```VB
    wscript.echo strText
    ```

    

    <span data-ttu-id="2a807-170">如果您選擇使用 XML DOM 來確認產生的 XML 格式是否正確，請以下列程式碼取代前一行。</span><span class="sxs-lookup"><span data-stu-id="2a807-170">If you chose to use XML DOM to verify that the XML generated is well-formed, replace the previous line with the following.</span></span>

    ```VB
    wscript.echo xml.xml
    ```

    

<span data-ttu-id="2a807-171">下列 VBScript 程式碼範例包含上述程式中的所有步驟，並以 XML 編碼 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別，包括類別、屬性和方法限定詞，以及排除系統屬性。</span><span class="sxs-lookup"><span data-stu-id="2a807-171">The following VBScript code example includes all of the steps in the preceding procedure and encodes the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in XML, including class, property, and method qualifiers and excluding system properties.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="2a807-172">相關主題</span><span class="sxs-lookup"><span data-stu-id="2a807-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a807-173">使用 WMI</span><span class="sxs-lookup"><span data-stu-id="2a807-173">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

