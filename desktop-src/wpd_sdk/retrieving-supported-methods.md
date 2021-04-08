---
description: 正在抓取支援的服務方法
ms.assetid: 783a6552-9b22-4af4-9252-b443e2624687
title: 正在抓取支援的服務方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6029af655a8835a4eee887d919c534856062ff13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850387"
---
# <a name="retrieving-supported-service-methods"></a>正在抓取支援的服務方法

服務方法會封裝每個服務定義和實行的功能。 它們是每種服務類型的特定類型，並以唯一的 GUID 表示。

例如，連絡人服務會定義 **BeginSync** 方法，讓應用程式呼叫以準備裝置來同步處理連絡人物件，並使用 **EndSync** 方法來通知裝置同步處理已完成。

應用程式可以使用 [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) 介面，以程式設計方式查詢支援的方法，並存取這些方法及其屬性。

服務方法不應與 WPD 命令混淆。 WPD 命令是標準 WPD 設備磁碟機介面 (DDI) 的一部分，而且是 WPD 應用程式與驅動程式之間的通訊機制。 命令是預先定義的，依類別分組（例如，WPD \_ 類別 \_ 通用），並以 PROPERTYKEY 結構表示。 如需詳細資訊，請參閱 [**命令**](commands.md) 主題。

WpdServicesApiSample 應用程式包含的程式碼會示範應用程式如何使用下表中的介面，來取得指定連絡人服務所支援的方法。



|                                                                                      |                                                                                                                |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 介面                                                                            | 描述                                                                                                    |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | 用來取出 **IPortableDeviceServiceCapabilities** 介面，以存取支援的服務方法。 |
| [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | 提供支援的方法、方法屬性和方法參數的存取權。                             |
| [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | 包含支援的方法清單。                                                                        |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                               | 包含方法和指定方法之參數的屬性。                                      |
| [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)                 | 包含指定方法的參數。                                                                    |



 

當使用者在命令列選擇選項 "5" 時，應用程式會叫用在 ServiceMethods .cpp 模組中找到的 **ListSupportedMethods** 方法。

請注意，在抓取事件清單之前，範例應用程式會在連線的裝置上開啟連絡人服務。

在 WPD 中，方法的名稱、存取權限、參數和相關資料會加以描述。 範例應用程式會顯示使用者易記名稱，例如 "CustomMethod" 或 GUID。 方法名稱或 GUID 後面接著存取資料 ( 「讀取/寫入」 ) 、任何相關格式的名稱，以及參數資料。 此資料包含參數名稱、使用方式、VARTYPE 和表單。

ServiceMethods .cpp 模組中的五個方法支援對指定連絡人服務的方法 (和相關資料) 的抓取： **ListSupportedMethods**、 **DisplayMethod**、 **DisplayMethodAccess**、 **DisplayFormat** 和 **DisplayMethodParameters**。 **ListSupportedMethods** 方法會抓取支援的方法計數和每個方法的 GUID 識別碼;然後，它會呼叫 **DisplayMethod** 方法。 **DisplayMethod** 方法會呼叫 [**IPortableDeviceServiceCapapbilities：： GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes)方法，以取得指定方法的選項、參數等等。 在 **DisplayMethod** 抓取方法資料之後，它會轉譯名稱 (或 GUID) 、存取限制、相關聯的格式 (如果有任何) 和參數描述。 **DisplayMethodAccess**、 **DisplayFormat** 和 **DisplayMethodParameters** 是可轉譯其各自資料欄位的 helper 函式。

**ListSupportedMethods** 方法會叫用 [**IPortableDeviceService：：功能**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities)方法來取出 [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)介面。 使用這個介面，它會藉由呼叫 [**IPortableDeviceServiceCapabilities：： GetSupportedMethods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) 方法來抓取支援的方法。 **GetSupportedMethods** 方法會抓取服務所支援之每個方法的 guid，並將該 guid 複製到 [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)物件中。

下列程式碼會使用 **ListSupportedMethods** 方法。


```C++
// List all supported methods on the service
void ListSupportedMethods(IPortableDeviceService* pService)
{
    HRESULT hr              = S_OK;
    DWORD   dwNumMethods    = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pMethods;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceCapabilities interface from the IPortableDeviceService interface to
    // access the service capabilities-specific methods.
    hr = pService->Capabilities(&pCapabilities);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceCapabilities from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Get all methods supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedMethods(&pMethods);
        if (FAILED(hr))
        {
            printf("! Failed to get supported methods from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported methods found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pMethods->GetCount(&dwNumMethods);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported methods, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Methods Found on the service\n\n", dwNumMethods);

    // Loop through each method and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumMethods; dwIndex++)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);
            hr = pMethods->GetAt(dwIndex, &pv);

            if (SUCCEEDED(hr))
            {
                // We have a method.  It is assumed that
                // methods are returned as VT_CLSID VarTypes.
                if (pv.puuid != NULL)
                {
                    DisplayMethod(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }    
}
```



在 **ListSupportedMethods** 方法為指定服務所支援的每個事件取得 GUID 之後，它會叫用 **DisplayMethod** 方法來抓取方法特定屬性。 這些屬性包括：方法的腳本易記名稱、必要的存取限制、任何相關的格式和參數清單。

**DisplayMethod** 方法會叫用 [**IPortableDeviceServiceCapabilities：： GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes)方法，以取得指定方法的屬性集合。 然後，它會呼叫 [**IPortableDeviceValues：： GetStringValue**](iportabledevicevalues-getstringvalue.md) 方法，以取得方法的名稱。 **DisplayMethod** 會呼叫 [**IPortableDeviceValues：： GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md)以取得存取 restrctions。 之後，它會呼叫 [**IPortableDeviceValues：： GetGuidValue**](iportabledevicevalues-getguidvalue.md) 來取得任何相關聯的格式。 最後， **DisplayMethod** 會呼叫 [**IPortableDeviceValues：： GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) 來取出參數資料。 它會將這些方法所傳回的資料傳遞至 **DisplayMethodAccess**、 **DisplayFormat** 和 **DisplayMethodParameters** helper 函式，以轉譯指定方法的資訊。

下列程式碼會使用 **DisplayMethod** 方法。


```C++
// Display basic information about a method
void DisplayMethod(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Method)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    // Get the method attributes which describe the method
    HRESULT hr = pCapabilities->GetMethodAttributes(Method, &pAttributes);
    if (FAILED(hr))
    {
        printf("! Failed to get the method attributes, hr = 0x%lx\n",hr);
    }

    if (SUCCEEDED(hr))
    {
        PWSTR   pszMethodName  = NULL;
        DWORD   dwMethodAccess = WPD_COMMAND_ACCESS_READ;
        GUID    guidFormat     = GUID_NULL;

        CComPtr<IPortableDeviceValues>          pOptions;
        CComPtr<IPortableDeviceKeyCollection>   pParameters;

        // Display the name of the method if available. Otherwise, fall back to displaying the GUID.
        hr = pAttributes->GetStringValue(WPD_METHOD_ATTRIBUTE_NAME, &pszMethodName);
        if (SUCCEEDED(hr))
        {
            printf("%ws", pszMethodName);
        }
        else
        {
            printf("%ws", (PWSTR)CGuidToString(Method));
        }       

        // Display the method access if available, otherwise default to WPD_COMMAND_ACCESS_READ access
        hr = pAttributes->GetUnsignedIntegerValue(WPD_METHOD_ATTRIBUTE_ACCESS, &dwMethodAccess);
        if (FAILED(hr))
        {
            dwMethodAccess = WPD_COMMAND_ACCESS_READ;
            hr = S_OK;
        }
        printf("\n\tAccess: ");
        DisplayMethodAccess(dwMethodAccess);

        // Display the associated format if specified.
        // Methods that have an associated format may only be supported for that format.
        // Methods that don't have associated formats generally apply to the entire service.
        hr = pAttributes->GetGuidValue(WPD_METHOD_ATTRIBUTE_ASSOCIATED_FORMAT, &guidFormat);
        if (SUCCEEDED(hr))
        {
            printf("\n\tAssociated Format: ");
            DisplayFormat(pCapabilities, guidFormat);
        }

        // Display the method parameters, if available
        hr = pAttributes->GetIPortableDeviceKeyCollectionValue(WPD_METHOD_ATTRIBUTE_PARAMETERS, &pParameters);
        if (SUCCEEDED(hr))
        {
            DisplayMethodParameters(pCapabilities, Method, pParameters);
        }
        
        CoTaskMemFree(pszMethodName);
        pszMethodName = NULL;

    }
}
```



**DisplayMethodAccess** helper 函式會接收包含方法存取選項的 DWORD 值。 它會將此值與 WPD \_ 命令 \_ 存取 \_ READ 和 WPD \_ 命令存取 READWRITE 進行比較， \_ \_ 以判斷方法的存取權限。 它會使用結果來呈現字串，指出指定方法的存取限制。

下列程式碼會使用 **DisplayMethodAccess** helper 函數。


```C++
void DisplayMethodAccess(
    DWORD   dwAccess)
{
    switch(static_cast<WPD_COMMAND_ACCESS_TYPES>(dwAccess))
    {
        case WPD_COMMAND_ACCESS_READ:
            printf("Read");
            break;
            
        case WPD_COMMAND_ACCESS_READWRITE:
            printf("Read/Write");
            break;

        default:
            printf("Unknown Access");
            break;
    }
}
```



**DisplayMethod** helper 函式會接收 [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)物件和方法的 GUID 做為參數。 使用 **IPortableDeviceServiceCapabilities** 物件，它會叫用 [**IPortableDeviceServiceCapabilities：： GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) 方法，以抓取方法屬性並在應用程式的主控台視窗中轉譯它們。

**DisplayMethodParameters** helper 函式會接收 [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)物件、方法的 GUID，以及包含方法參數的 IPortableDeviceKeyCollection 物件。 使用 [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) 物件，它會叫用 [**IPortableDeviceServiceCapabilities：： GetMethodParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes) 方法來取出參數的名稱、使用方式、VARTYPE 和表單。 它會在應用程式的主控台視窗中呈現此資訊。

下列程式碼會使用 **DisplayMethodParameters** helper 函數。


```C++
// Display the method parameters.
void DisplayMethodParameters(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Method,
    IPortableDeviceKeyCollection*       pParameters)
{
    DWORD   dwNumParameters = 0;

    // Get the number of parameters for this event.
    HRESULT hr = pParameters->GetCount(&dwNumParameters);
    if (FAILED(hr))
    {
        printf("! Failed to get number of parameters, hr = 0x%lx\n",hr);
    }

    printf("\n\t%d Method Parameters:\n", dwNumParameters);

    // Loop through each parameter and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumParameters; dwIndex++)
        {
            PROPERTYKEY parameter;
            hr = pParameters->GetAt(dwIndex, &parameter);

            if (SUCCEEDED(hr))
            {
                CComPtr<IPortableDeviceValues> pAttributes;

                // Display the parameter's Name, Usage, Vartype, and Form
                hr = pCapabilities->GetMethodParameterAttributes(Method, parameter, &pAttributes);
                if (FAILED(hr))
                {
                    printf("! Failed to get the method parameter attributes, hr = 0x%lx\n",hr);
                }

                if (SUCCEEDED(hr))
                {
                    PWSTR   pszParameterName    = NULL;
                    DWORD   dwAttributeVarType  = 0;
                    DWORD   dwAttributeForm     = WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED;
                    DWORD   dwAttributeUsage    = (DWORD)-1;

                    hr = pAttributes->GetStringValue(WPD_PARAMETER_ATTRIBUTE_NAME, &pszParameterName);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tName: %ws\n", pszParameterName);
                    }
                    else
                    {
                        printf("! Failed to get the method parameter name, hr = 0x%lx\n",hr);
                    }

                    // Read the WPD_PARAMETER_ATTRIBUTE_USAGE value, if specified. 
                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_USAGE, &dwAttributeUsage);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tUsage: ");
                        DisplayParameterUsage(dwAttributeUsage);
                        printf("\n");
                    }
                    else
                    {
                        printf("! Failed to get the method parameter usage, hr = 0x%lx\n",hr);
                    }

                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_VARTYPE, &dwAttributeVarType);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tVARTYPE: ");
                        DisplayVarType(static_cast<VARTYPE>(dwAttributeVarType));
                        printf("\n");
                    }
                    else
                    {
                        printf("! Failed to get the method parameter VARTYPE, hr = 0x%lx\n",hr);
                    }

                    // Read the WPD_PARAMETER_ATTRIBUTE_FORM value.
                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_FORM, &dwAttributeForm);
                    if (FAILED(hr))
                    {
                        // If the read fails, assume WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED
                        dwAttributeForm = WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED;
                        hr = S_OK;
                    }

                    printf("\t\tForm: ");
                    DisplayParameterForm(dwAttributeForm);
                    printf("\n");

                    CoTaskMemFree(pszParameterName);
                    pszParameterName = NULL;
                }
                
                printf("\n");
            }
        }
    }
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[**IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



