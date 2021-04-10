---
description: 部分實例抓取是 WMI 只會抓取實例的屬性子集。
ms.assetid: 6cc26b26-adc9-4a8a-b51e-9db94eb4295f
ms.tgt_platform: multiple
title: 正在抓取 WMI 實例的一部分
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9d547ec2bbb7e3b53e22177cc0c48794dff22a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192081"
---
# <a name="retrieving-part-of-a-wmi-instance"></a><span data-ttu-id="2b74d-103">正在抓取 WMI 實例的一部分</span><span class="sxs-lookup"><span data-stu-id="2b74d-103">Retrieving Part of a WMI Instance</span></span>

<span data-ttu-id="2b74d-104">部分實例抓取是 WMI 只會抓取實例的屬性子集。</span><span class="sxs-lookup"><span data-stu-id="2b74d-104">A partial-instance retrieval is when WMI retrieves only a subset of the properties of an instance.</span></span> <span data-ttu-id="2b74d-105">例如，WMI 只能取出 **名稱** 和索引 **鍵** 屬性。</span><span class="sxs-lookup"><span data-stu-id="2b74d-105">For example, WMI could retrieve only the **Name** and **Key** properties.</span></span> <span data-ttu-id="2b74d-106">部分實例抓取最常見的用法是在具有多個屬性的大型列舉上。</span><span class="sxs-lookup"><span data-stu-id="2b74d-106">The most common use of partial-instance retrieval is on large enumerations that have multiple properties.</span></span>

## <a name="retrieving-part-of-a-wmi-instance-using-powershell"></a><span data-ttu-id="2b74d-107">使用 PowerShell 來取出 WMI 實例的一部分</span><span class="sxs-lookup"><span data-stu-id="2b74d-107">Retrieving Part of a WMI Instance Using PowerShell</span></span>

<span data-ttu-id="2b74d-108">您可以使用 [>get-wmiobject 取得](https://technet.microsoft.com/library/dd315379.aspx)實例的個別屬性。屬性本身可以透過數種方式來抓取和顯示。</span><span class="sxs-lookup"><span data-stu-id="2b74d-108">You can retrieve an individual property of an instance by using [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx); the property itself can be retrieved and displayed a number of ways.</span></span> <span data-ttu-id="2b74d-109">如同抓取實例，PowerShell 預設會傳回指定類別的所有實例;如果您只想要取出單一實例，就必須指定特定的值。</span><span class="sxs-lookup"><span data-stu-id="2b74d-109">As with retrieving an instance, PowerShell will by default return all instances of a given class; you must specify a specific value if you wish to retrieve only a single instance.</span></span>

<span data-ttu-id="2b74d-110">下列程式碼範例會顯示 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別之實例的磁片區序號。</span><span class="sxs-lookup"><span data-stu-id="2b74d-110">The following code example displays the volume serial number for an instance of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>


```PowerShell
(Get-WmiObject -class Win32_logicalDisk).DeviceID

#or

Get-WmiObject -class Win32_LogicalDisk | format-list DeviceID

#or

$myDisk = Get-WmiObject -class Win32_LogicalDisk
$myDisk.DeviceID
```



## <a name="retrieving-part-of-a-wmi-instance-using-c-systemmanagement"></a><span data-ttu-id="2b74d-111">使用 c # (System. 管理) 來抓取 WMI 實例的一部分</span><span class="sxs-lookup"><span data-stu-id="2b74d-111">Retrieving Part of a WMI Instance Using C# (System.Management)</span></span>

<span data-ttu-id="2b74d-112">您可以使用特定實例的詳細資料來建立新的 [system.management.managementobject](/dotnet/api/system.management.managementobject) ，藉以取得實例的個別屬性。</span><span class="sxs-lookup"><span data-stu-id="2b74d-112">You can retrieve an individual property of an instance by creating a new [ManagementObject](/dotnet/api/system.management.managementobject) using the details of a specific instance.</span></span> <span data-ttu-id="2b74d-113">然後，您可以使用 [GetPropertyValue](/dotnet/api/system.management.managementbaseobject.getpropertyvalue#System_Management_ManagementBaseObject_GetPropertyValue_System_String_) 方法，以隱含方式抓取實例的一或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="2b74d-113">You can then implicitly retrieve one or more properties of the instance with the [GetPropertyValue](/dotnet/api/system.management.managementbaseobject.getpropertyvalue#System_Management_ManagementBaseObject_GetPropertyValue_System_String_) method.</span></span>

> [!Note]  
> <span data-ttu-id="2b74d-114">**系統管理** 是用來存取 WMI 的原始 .net 命名空間;不過，這個命名空間中的 Api 通常會較慢，而且也不會相對於其較新式的 **Microsoft 管理元件** 對應專案。</span><span class="sxs-lookup"><span data-stu-id="2b74d-114">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="2b74d-115">下列程式碼範例會顯示 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別之實例的磁片區序號。</span><span class="sxs-lookup"><span data-stu-id="2b74d-115">The following code example displays the volume serial number for an instance of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>


```CSharp
using System.Management;
...
ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
string myProperty = myDisk.GetPropertyValue("VolumeSerialNumber").ToString();
Console.WriteLine(myProperty);
```



## <a name="retrieving-part-of-a-wmi-instance-using-vbscript"></a><span data-ttu-id="2b74d-116">使用 VBScript 取出 WMI 實例的一部分</span><span class="sxs-lookup"><span data-stu-id="2b74d-116">Retrieving Part of a WMI Instance Using VBScript</span></span>

<span data-ttu-id="2b74d-117">您可以使用 [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)來取得實例的個別屬性。</span><span class="sxs-lookup"><span data-stu-id="2b74d-117">You can retrieve an individual property of an instance by using [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>

<span data-ttu-id="2b74d-118">下列程式碼範例會顯示 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別之實例的磁片區序號。</span><span class="sxs-lookup"><span data-stu-id="2b74d-118">The following code example displays the volume serial number for an instance of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>


```VB
MsgBox (GetObject("WinMgmts:Win32_LogicalDisk='C:'").VolumeSerialNumber)
```



## <a name="retrieving-part-of-a-wmi-instance-using-c"></a><span data-ttu-id="2b74d-119">使用 c + + 取出 WMI 實例的一部分</span><span class="sxs-lookup"><span data-stu-id="2b74d-119">Retrieving Part of a WMI Instance Using C++</span></span>

<span data-ttu-id="2b74d-120">下列程式是用來要求使用 c + + 的部分實例抓取。</span><span class="sxs-lookup"><span data-stu-id="2b74d-120">The following procedure is used to request a partial-instance retrieval using C++.</span></span>

<span data-ttu-id="2b74d-121">**使用 c + + 要求部分實例抓取**</span><span class="sxs-lookup"><span data-stu-id="2b74d-121">**To request a partial-instance retrieval using C++**</span></span>

1.  <span data-ttu-id="2b74d-122">使用對 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)的呼叫來建立 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)物件。</span><span class="sxs-lookup"><span data-stu-id="2b74d-122">Create an [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="2b74d-123">內容物件是 WMI 用來將更多資訊傳遞給 WMI 提供者的物件。</span><span class="sxs-lookup"><span data-stu-id="2b74d-123">A context object is an object that WMI uses to pass in more information to a WMI provider.</span></span> <span data-ttu-id="2b74d-124">在此情況下，您會使用 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) 物件來指示提供者處理部分實例抓取。</span><span class="sxs-lookup"><span data-stu-id="2b74d-124">In this case, you are using the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object to instruct the provider to process a partial-instance retrieval.</span></span>

2.  <span data-ttu-id="2b74d-125">新增 \_ \_ 取得 \_ 延伸模組、 \_ \_ 取得 \_ EXT \_ 用戶端 \_ 要求，以及任何其他命名值，這些值會描述您想要取得給 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="2b74d-125">Add \_\_GET\_EXTENSIONS, \_\_GET\_EXT\_CLIENT\_REQUEST, and any other named values that describe the properties you want to retrieve to the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object.</span></span>

    <span data-ttu-id="2b74d-126">下表列出您在抓取呼叫中使用的不同命名值。</span><span class="sxs-lookup"><span data-stu-id="2b74d-126">The following table lists the different named values use in your retrieval call.</span></span>

    

    | <span data-ttu-id="2b74d-127">命名值</span><span class="sxs-lookup"><span data-stu-id="2b74d-127">Named value</span></span>                              | <span data-ttu-id="2b74d-128">Description</span><span class="sxs-lookup"><span data-stu-id="2b74d-128">Description</span></span>                                                                                                                                                                                                                                                                 |
    |------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="2b74d-129">\_\_取得 \_ 延伸模組</span><span class="sxs-lookup"><span data-stu-id="2b74d-129">\_\_GET\_EXTENSIONS</span></span><br/>           | <span data-ttu-id="2b74d-130">**VT \_BOOL** 設定為 **VARIANT \_ TRUE**。</span><span class="sxs-lookup"><span data-stu-id="2b74d-130">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="2b74d-131">用來表示正在使用部分實例抓取作業。</span><span class="sxs-lookup"><span data-stu-id="2b74d-131">Used to signal that partial-instance retrieval operations are being used.</span></span> <span data-ttu-id="2b74d-132">如此一來，就不需要列舉整個內容物件，即可進行快速、單一檢查。</span><span class="sxs-lookup"><span data-stu-id="2b74d-132">This allows a quick, single check without having to enumerate the entire context object.</span></span> <span data-ttu-id="2b74d-133">如果使用任何其他值，則這個值必須是。</span><span class="sxs-lookup"><span data-stu-id="2b74d-133">If any of the other values are used, this one must be.</span></span><br/> |
    | <span data-ttu-id="2b74d-134">\_\_取得 \_ EXT \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="2b74d-134">\_\_GET\_EXT\_PROPERTIES</span></span><br/>      | <span data-ttu-id="2b74d-135">列出要抓取之屬性的字串 [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) 。</span><span class="sxs-lookup"><span data-stu-id="2b74d-135">[**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of strings listing the properties to be retrieved.</span></span> <span data-ttu-id="2b74d-136">\_ \_ 只能以 GET \_ EXT 索引鍵 \_ \_ 同時指定。</span><span class="sxs-lookup"><span data-stu-id="2b74d-136">Cannot be simultaneously specified with \_\_GET\_EXT\_KEYS\_ONLY.</span></span><br/> <span data-ttu-id="2b74d-137">星號 " \* " 是 \_ \_ GET \_ EXT 屬性的無效屬性名稱 \_ 。</span><span class="sxs-lookup"><span data-stu-id="2b74d-137">An asterisk "\*" is an invalid property name for \_\_GET\_EXT\_PROPERTIES.</span></span><br/>                    |
    | <span data-ttu-id="2b74d-138">\_\_\_僅取得 EXT \_ 金鑰 \_</span><span class="sxs-lookup"><span data-stu-id="2b74d-138">\_\_GET\_EXT\_KEYS\_ONLY</span></span><br/>      | <span data-ttu-id="2b74d-139">**VT \_BOOL** 設定為 **VARIANT \_ TRUE**。</span><span class="sxs-lookup"><span data-stu-id="2b74d-139">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="2b74d-140">表示只應該在傳回的物件中提供索引鍵。</span><span class="sxs-lookup"><span data-stu-id="2b74d-140">Indicates that only keys should be provided in the returned object.</span></span> <span data-ttu-id="2b74d-141">無法同時以 \_ \_ GET \_ EXT 屬性指定 \_ 。</span><span class="sxs-lookup"><span data-stu-id="2b74d-141">Cannot be simultaneously specified with \_\_GET\_EXT\_PROPERTIES.</span></span> <span data-ttu-id="2b74d-142">相反地，優先于 \_ \_ GET \_ EXT \_ 屬性。</span><span class="sxs-lookup"><span data-stu-id="2b74d-142">Instead, takes precedence over \_\_GET\_EXT\_PROPERTIES.</span></span><br/>                            |
    | <span data-ttu-id="2b74d-143">\_\_取得 \_ EXT \_ 用戶端 \_ 要求</span><span class="sxs-lookup"><span data-stu-id="2b74d-143">\_\_GET\_EXT\_CLIENT\_REQUEST</span></span><br/> | <span data-ttu-id="2b74d-144">**VT \_BOOL** 設定為 **VARIANT \_ TRUE**。</span><span class="sxs-lookup"><span data-stu-id="2b74d-144">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="2b74d-145">指出呼叫端是指將值寫入內容物件中，而不是從另一個相依作業傳播的呼叫端。</span><span class="sxs-lookup"><span data-stu-id="2b74d-145">Indicates that the caller was the one who wrote the value into the context object and that it was not propagated from another dependent operation.</span></span><br/>                                                                        |

    

     

3.  <span data-ttu-id="2b74d-146">透過 *pCtx* 參數，將 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)內容物件傳遞到 [**iwbemservices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)、 [**iwbemservices：： GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)、 [**IWbemServices：： CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum)或 [**iwbemservices：： CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)的任何呼叫。</span><span class="sxs-lookup"><span data-stu-id="2b74d-146">Pass the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) context object into any calls to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum), or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) through the *pCtx* parameter.</span></span>

    <span data-ttu-id="2b74d-147">傳遞 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) 物件會指示提供者允許部分實例的檢索。</span><span class="sxs-lookup"><span data-stu-id="2b74d-147">Passing the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object instructs the provider to allow partial-instance retrievals.</span></span> <span data-ttu-id="2b74d-148">在完整實例抓取中，您會將 *pCtx* 設定為 **null** 值。</span><span class="sxs-lookup"><span data-stu-id="2b74d-148">In a full-instance retrieval, you would set *pCtx* to a **null** value.</span></span> <span data-ttu-id="2b74d-149">如果提供者不支援部分實例抓取，您將會收到錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2b74d-149">If the provider does not support partial-instance retrieval, you will receive an error message.</span></span>

<span data-ttu-id="2b74d-150">如果提供者無法符合部分實例作業，則提供者會像您未輸入內容物件一樣繼續進行，否則會傳回 **WBEM \_ E \_ 不支援的 \_ 參數**。</span><span class="sxs-lookup"><span data-stu-id="2b74d-150">If the provider cannot comply with the partial-instance operation, the provider either proceeds as if you did not enter the context object, or else returns **WBEM\_E\_UNSUPPORTED\_PARAMETER**.</span></span>

<span data-ttu-id="2b74d-151">下列範例說明如何執行 [**win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)的完整實例抓取，然後執行 **win32 \_ LogicalDisk 標題** 屬性的部分實例抓取。</span><span class="sxs-lookup"><span data-stu-id="2b74d-151">The following example describes how to perform a full instance retrieval of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), and then performs a partial-instance retrieval of the **Win32\_LogicalDisk.Caption** property.</span></span>


```C++
#include <stdio.h>
#define _WIN32_DCOM
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
#include <iostream>
using namespace std;
#include <comdef.h>


void main(void)
{
    HRESULT hr;
    _bstr_t bstrNamespace;
    IWbemLocator *pWbemLocator = NULL;
    IWbemServices *pServices = NULL;
    IWbemClassObject *pDrive = NULL;
    

    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);

    hr = CoInitializeSecurity(NULL, -1, NULL, NULL,
                         RPC_C_AUTHN_LEVEL_CONNECT,
                         RPC_C_IMP_LEVEL_IMPERSONATE,
                         NULL, EOAC_NONE, 0);
 
    if (FAILED(hr))
    {
       CoUninitialize();
       cout << "Failed to initialize security. Error code = 0x" 
            << hex << hr << endl;
       return;
    }

    hr = CoCreateInstance(CLSID_WbemLocator, NULL, 
                          CLSCTX_INPROC_SERVER, IID_IWbemLocator, 
                          (void**) &pWbemLocator);
    if( FAILED(hr) ) 
    {
        CoUninitialize();
        printf("failed CoCreateInstance\n");
        return;
    }
    
    bstrNamespace = L"root\\cimv2";
    hr = pWbemLocator->ConnectServer(bstrNamespace, 
              NULL, NULL, NULL, 0, NULL, NULL, &pServices);
    if( FAILED(hr) ) 
    {
        pWbemLocator->Release();
        CoUninitialize();
        printf("failed ConnectServer\n");
        return;
    }
    pWbemLocator->Release();
    printf("Successfully connected to namespace.\n");

    
    BSTR bstrPath = 
         SysAllocString(L"Win32_LogicalDisk.DeviceID=\"C:\"");
   // *******************************************************//
   // Perform a full-instance retrieval. 
   // *******************************************************//
    hr = pServices->GetObject(bstrPath,
                              0,0, &pDrive, 0);
    if( FAILED(hr) )
    { 
        pServices->Release();
        CoUninitialize();
        printf("failed GetObject\n");
        return;
    }    
    // Display the object
    BSTR  bstrDriveObj;
    hr = pDrive->GetObjectText(0, &bstrDriveObj);
    printf("%S\n\n", bstrDriveObj);

    pDrive->Release();
    pDrive = NULL;

   // *****************************************************//
   // Perform a partial-instance retrieval. 
   // *****************************************************//
    
    IWbemContext  *pctxDrive; // Create context object
    hr = CoCreateInstance(CLSID_WbemContext, NULL, 
                          CLSCTX_INPROC_SERVER, IID_IWbemContext, 
                          (void**) &pctxDrive);
    if (FAILED(hr))
    {
        pServices->Release();
        pDrive->Release();    
        CoUninitialize();
        printf("create instance failed for context object.\n");
        return;
    }
    
    VARIANT  vExtensions;
    VARIANT  vClient;
    VARIANT  vPropertyList;
    VARIANT  vProperty;
    SAFEARRAY  *psaProperties;
    SAFEARRAYBOUND saBounds;
    LONG  lArrayIndex = 0;
    
    // Add named values to the context object. 
    VariantInit(&vExtensions);
    V_VT(&vExtensions) = VT_BOOL;
    V_BOOL(&vExtensions) = VARIANT_TRUE;
    hr = pctxDrive->SetValue(_bstr_t(L"__GET_EXTENSIONS"), 
        0, &vExtensions);
    VariantClear(&vExtensions);

    VariantInit(&vClient);
    V_VT(&vClient) = VT_BOOL;
    V_BOOL(&vClient) = VARIANT_TRUE;
    hr = pctxDrive->SetValue(_bstr_t(L"__GET_EXT_CLIENT_REQUEST"), 
       0, &vClient);
    VariantClear(&vClient);
    // Create an array of properties to return.
    saBounds.cElements = 1;
    saBounds.lLbound = 0;
    psaProperties = SafeArrayCreate(VT_BSTR, 1, &saBounds);

    // Add the Caption property to the array.
    VariantInit(&vProperty);
    V_VT(&vProperty) = VT_BSTR;
    V_BSTR(&vProperty) = _bstr_t(L"Caption");
    SafeArrayPutElement(psaProperties, &lArrayIndex, 
       V_BSTR(&vProperty));
    VariantClear(&vProperty);
    
    VariantInit(&vPropertyList);
    V_VT(&vPropertyList) = VT_ARRAY | VT_BSTR;
    V_ARRAY(&vPropertyList) = psaProperties;
    // Put the array in the named value __GET_EXT_PROPERTIES.
    hr = pctxDrive->SetValue(_bstr_t(L"__GET_EXT_PROPERTIES"), 
        0, &vPropertyList);
    VariantClear(&vPropertyList);
    SafeArrayDestroy(psaProperties);

    // Pass the context object as the pCtx parameter of GetObject.
    hr = pServices->GetObject(bstrPath, 0, pctxDrive, &pDrive, 0);
    if( FAILED(hr) )
    { 
        pServices->Release();
        CoUninitialize();
        printf("failed property GetObject\n");
        return;
    }    
    // Display the object
    hr = pDrive->GetObjectText(0, &bstrDriveObj);
    printf("%S\n\n", bstrDriveObj);

    SysFreeString(bstrPath);

    VARIANT vFileSystem;
    // Attempt to get a property that was not requested.
    // The following should return a NULL property if
    // the partial-instance retrieval succeeded.

    hr = pDrive->Get(_bstr_t(L"FileSystem"), 0,
                       &vFileSystem, NULL, NULL);

    if( FAILED(hr) )
    { 
        pServices->Release();
        pDrive->Release();    
        CoUninitialize();
        printf("failed get for file system\n");
        return;
    }    
 
    if (V_VT(&vFileSystem) == VT_NULL)
        printf("file system variable is null - expected\n");
    else
        printf("FileSystem = %S\n", V_BSTR(&vFileSystem));
    
    VariantClear(&vFileSystem);

    pDrive->Release();    
    pctxDrive->Release();
    pServices->Release();
    pServices = NULL;    // MUST be set to NULL
    CoUninitialize();
    return;  // -- program successfully completed
};
```



<span data-ttu-id="2b74d-152">執行時，上述程式碼範例會寫入下列資訊。</span><span class="sxs-lookup"><span data-stu-id="2b74d-152">When executed, the previous code example writes the following information.</span></span> <span data-ttu-id="2b74d-153">第一個物件描述來自于完整實例的抓取。</span><span class="sxs-lookup"><span data-stu-id="2b74d-153">The first object description is from the full-instance retrieval.</span></span> <span data-ttu-id="2b74d-154">第二個物件描述是來自部分實例的抓取。</span><span class="sxs-lookup"><span data-stu-id="2b74d-154">The second object description is from the partial-instance retrieval.</span></span> <span data-ttu-id="2b74d-155">最後一個區段會顯示，如果您要求的屬性不是在原始的 [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)呼叫中要求的，則會收到 **null** 值。</span><span class="sxs-lookup"><span data-stu-id="2b74d-155">The last section shows that you receive a **null** value if you request a property that was not requested in the original [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) call.</span></span>

``` syntax
Successfully connected to namespace

instance of Win32_LogicalDisk
{
        Caption = "C:";
        Compressed = FALSE;
        CreationClassName = "Win32_LogicalDisk";
        Description = "Local Fixed Disk";
        DeviceID = "C:";
        DriveType = 3;
        FileSystem = "NTFS";
        FreeSpace = "3085668352";
        MaximumComponentLength = 255;
        MediaType = 12;
        Name = "C:";
        Size = "4581445632";
        SupportsFileBasedCompression = TRUE;
        SystemCreationClassName = "Win32_ComputerSystem";
        SystemName = "TITUS";
        VolumeName = "titus-c";
        VolumeSerialNumber = "7CB4B90E";
};

instance of Win32_LogicalDisk
{
        Caption = "C:";
        CreationClassName = "Win32_LogicalDisk";
        Description = "Local Fixed Disk";
        DeviceID = "C:";
        DriveType = 3;
        MediaType = 12;
        Name = "C:";
        SystemCreationClassName = "Win32_ComputerSystem";
        SystemName = "MySystem";
};
```

<span data-ttu-id="2b74d-156">上述範例會產生下列輸出。</span><span class="sxs-lookup"><span data-stu-id="2b74d-156">The following output is generated by the previous example.</span></span>

``` syntax
file system variable is null - expected
Press any key to continue
```

 

