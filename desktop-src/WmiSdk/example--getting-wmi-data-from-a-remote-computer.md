---
description: 您可以使用本主題中的程式和程式碼範例來建立完整的 WMI 用戶端應用程式，以執行 COM 初始化、連接至遠端電腦上的 WMI、取得資料半同步方式，然後清除。
ms.assetid: 30e65b9e-9372-46d1-843a-bda0d6ec1c69
ms.tgt_platform: multiple
title: 範例：從遠端電腦取得 WMI 資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c3375bd25073defa92358f697ee4165ddb57793
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980782"
---
# <a name="example-getting-wmi-data-from-a-remote-computer"></a><span data-ttu-id="47b91-103">範例：從遠端電腦取得 WMI 資料</span><span class="sxs-lookup"><span data-stu-id="47b91-103">Example: Getting WMI Data from a Remote Computer</span></span>

<span data-ttu-id="47b91-104">您可以使用本主題中的程式和程式碼範例來建立完整的 WMI 用戶端應用程式，以執行 COM 初始化、連接至遠端電腦上的 WMI、取得資料半同步方式，然後清除。</span><span class="sxs-lookup"><span data-stu-id="47b91-104">You can use the procedure and code examples in this topic to create a complete WMI client application that performs COM initialization, connects to WMI on a remote computer, gets data semisynchronously, and then cleans up.</span></span> <span data-ttu-id="47b91-105">如需有關如何從本機電腦取得資料的詳細資訊，請參閱 [範例：從本機電腦取得 WMI 資料](example--getting-wmi-data-from-the-local-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="47b91-105">For more information about how to get data from the local computer, see [Example: Getting WMI Data from the Local Computer](example--getting-wmi-data-from-the-local-computer.md).</span></span> <span data-ttu-id="47b91-106">如需如何以非同步方式取得資料的詳細資訊，請參閱 [範例：以非同步方式從本機電腦取得 WMI 資料](example--getting-wmi-data-from-the-local-computer-asynchronously.md)。</span><span class="sxs-lookup"><span data-stu-id="47b91-106">For more information about how to get the data asynchronously, see [Example: Getting WMI Data from the Local Computer Asynchronously](example--getting-wmi-data-from-the-local-computer-asynchronously.md).</span></span>

> [!Note]  
> <span data-ttu-id="47b91-107">如果您嘗試連接到遠端電腦，請參閱[從遠端連線到 WMI](connecting-to-wmi-remotely-starting-with-vista.md)的資訊。</span><span class="sxs-lookup"><span data-stu-id="47b91-107">If you are trying to connect to a remote computer refer to the information in[Connecting to WMI Remotely](connecting-to-wmi-remotely-starting-with-vista.md).</span></span>

 

<span data-ttu-id="47b91-108">下列程式顯示如何執行 WMI 應用程式。</span><span class="sxs-lookup"><span data-stu-id="47b91-108">The following procedure shows how to execute the WMI application.</span></span> <span data-ttu-id="47b91-109">步驟1到5包含設定和連線至 WMI 所需的所有步驟，而步驟6和7則是查詢及接收資料的位置。</span><span class="sxs-lookup"><span data-stu-id="47b91-109">Steps 1 through 5 contain all of the steps required to set up and connect to WMI, and steps 6 and 7 are where data is queried and received.</span></span>

<span data-ttu-id="47b91-110">**從遠端電腦取得 WMI 資料**</span><span class="sxs-lookup"><span data-stu-id="47b91-110">**To get WMI data from a remote computer**</span></span>

1.  <span data-ttu-id="47b91-111">使用 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)的呼叫初始化 COM 參數。</span><span class="sxs-lookup"><span data-stu-id="47b91-111">Initialize COM parameters with a call to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    <span data-ttu-id="47b91-112">如需詳細資訊，請參閱 [初始化 WMI 應用程式的 COM](initializing-com-for-a-wmi-application.md)。</span><span class="sxs-lookup"><span data-stu-id="47b91-112">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

2.  <span data-ttu-id="47b91-113">藉由呼叫 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)來初始化 COM 進程安全性。</span><span class="sxs-lookup"><span data-stu-id="47b91-113">Initialize COM process security by calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

    <span data-ttu-id="47b91-114">如需詳細資訊，請參閱 [使用 c + + 設定預設進程安全性層級](setting-the-default-process-security-level-using-c-.md)。</span><span class="sxs-lookup"><span data-stu-id="47b91-114">For more information, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md).</span></span>

3.  <span data-ttu-id="47b91-115">藉由呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)來取得 WMI 的初始定位器。</span><span class="sxs-lookup"><span data-stu-id="47b91-115">Obtain the initial locator to WMI by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="47b91-116">如需詳細資訊，請參閱 [建立與 WMI 命名空間的連接](creating-a-connection-to-a-wmi-namespace.md)。</span><span class="sxs-lookup"><span data-stu-id="47b91-116">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

4.  <span data-ttu-id="47b91-117">藉 [](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) \\ \\ \\ 由呼叫 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)，取得遠端電腦上根 cimv2 命名空間的 IWbemServices 指標。</span><span class="sxs-lookup"><span data-stu-id="47b91-117">Obtain a pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) for the \\\\root\\cimv2 namespace on a remote computer by calling [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span> <span data-ttu-id="47b91-118">連線到遠端電腦時，您需要知道您要連接之遠端電腦的電腦名稱稱、網域、使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="47b91-118">When connecting to a remote computer, you need to know the computer name, domain, user name, and password of the remote computer you are connecting to.</span></span> <span data-ttu-id="47b91-119">這些屬性都會傳遞至 **IWbemLocator：： ConnectServer** 方法。</span><span class="sxs-lookup"><span data-stu-id="47b91-119">These attributes are all passed into the **IWbemLocator::ConnectServer** method.</span></span> <span data-ttu-id="47b91-120">此外，請確認嘗試連線到遠端電腦之電腦上的使用者名稱，在遠端電腦上具有正確的存取權限。</span><span class="sxs-lookup"><span data-stu-id="47b91-120">Also, ensure the user name on the computer that is trying to connect to the remote computer has the correct access privileges on the remote computer.</span></span> <span data-ttu-id="47b91-121">如需詳細資訊，請參閱 [透過 Windows 防火牆連接](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista)。</span><span class="sxs-lookup"><span data-stu-id="47b91-121">For more information, see [Connecting Through Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span></span> <span data-ttu-id="47b91-122">若要連接到本機電腦，請參閱 [範例：從本機電腦取得 Wmi 資料](example--getting-wmi-data-from-the-local-computer.md) 及 [建立 wmi 命名空間的連接](creating-a-connection-to-a-wmi-namespace.md)。</span><span class="sxs-lookup"><span data-stu-id="47b91-122">To connect to the local computer, see [Example: Getting WMI Data from the Local Computer](example--getting-wmi-data-from-the-local-computer.md) and [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

    <span data-ttu-id="47b91-123">處理使用者名稱和密碼時，建議使用者提示輸入資訊、使用資訊，然後刪除資訊，如此一來，未經授權的使用者就不會攔截資訊。</span><span class="sxs-lookup"><span data-stu-id="47b91-123">When handling user names and passwords, it is recommended that the user be prompted for the information, use the information, and then delete the information, so that there is less of a chance of the information being intercepted by an unauthorized user.</span></span> <span data-ttu-id="47b91-124">下列範例程式碼中的步驟4使用 [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) 取得使用者名稱和密碼，然後使用 [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) 在 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)中使用該資訊。</span><span class="sxs-lookup"><span data-stu-id="47b91-124">Step 4 in the example code below uses [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) to get the user name and password, and then uses [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) to get rid of the information after it is used in [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span> <span data-ttu-id="47b91-125">如需詳細資訊，請參閱 MSDN 上的 [處理密碼](/windows/desktop/SecBP/handling-passwords) 和 [要求使用者提供認證](/windows/desktop/SecBP/asking-the-user-for-credentials) 。</span><span class="sxs-lookup"><span data-stu-id="47b91-125">For more information, see [Handling Passwords](/windows/desktop/SecBP/handling-passwords) and [Asking the User for Credentials](/windows/desktop/SecBP/asking-the-user-for-credentials) on MSDN.</span></span>

5.  <span data-ttu-id="47b91-126">建立 [COAUTHIDENTITY](/windows/win32/api/wtypesbase/ns-wtypesbase-coauthidentity) 結構，以提供用來設定 proxy 安全性的認證。</span><span class="sxs-lookup"><span data-stu-id="47b91-126">Create a [COAUTHIDENTITY](/windows/win32/api/wtypesbase/ns-wtypesbase-coauthidentity) structure to provide credentials for setting the proxy security.</span></span>
6.  <span data-ttu-id="47b91-127">設定 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy 安全性，讓 WMI 服務可以藉由呼叫 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)來模擬用戶端。</span><span class="sxs-lookup"><span data-stu-id="47b91-127">Set [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy security so WMI service can impersonate the client by calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="47b91-128">如需詳細資訊，請參閱 [設定 WMI 連接的安全性層級](setting-the-security-levels-on-a-wmi-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="47b91-128">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

7.  <span data-ttu-id="47b91-129">使用 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 指標來發出 WMI 要求。</span><span class="sxs-lookup"><span data-stu-id="47b91-129">Use the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer to make requests of WMI.</span></span> <span data-ttu-id="47b91-130">執行查詢以取得作業系統的名稱，以及藉由呼叫 [**IWbemServices：： ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)來取得可用的實體記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="47b91-130">A query is executed to obtain the name of the operating system and the amount of free physical memory by calling [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).</span></span>

    <span data-ttu-id="47b91-131">下列 WQL 查詢是其中一個方法引數。</span><span class="sxs-lookup"><span data-stu-id="47b91-131">The following WQL query is one of the method arguments.</span></span>

    `SELECT * FROM Win32_OperatingSystem`

    <span data-ttu-id="47b91-132">此查詢的結果會儲存在 [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) 指標中。</span><span class="sxs-lookup"><span data-stu-id="47b91-132">The result of this query is stored in an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) pointer.</span></span> <span data-ttu-id="47b91-133">這可讓您使用 **IEnumWbemClassObject** 介面來半同步方式查詢中的資料物件。</span><span class="sxs-lookup"><span data-stu-id="47b91-133">This allows the data objects from the query to be retrieved semisynchronously with the **IEnumWbemClassObject** interface.</span></span> <span data-ttu-id="47b91-134">如需詳細資訊，請參閱 [列舉 WMI](enumerating-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="47b91-134">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span> <span data-ttu-id="47b91-135">若要以非同步方式取得資料，請參閱 [範例：以非同步方式從本機電腦取得 WMI 資料](example--getting-wmi-data-from-the-local-computer-asynchronously.md)。</span><span class="sxs-lookup"><span data-stu-id="47b91-135">For getting the data asynchronously, see [Example: Getting WMI Data from the Local Computer Asynchronously](example--getting-wmi-data-from-the-local-computer-asynchronously.md).</span></span>

    <span data-ttu-id="47b91-136">如需提出 WMI 要求的詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)、 [查詢 WMI](querying-wmi.md)，以及 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="47b91-136">For more information about making requests of WMI, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Querying WMI](querying-wmi.md), and [Calling a Method](calling-a-method.md).</span></span>

8.  <span data-ttu-id="47b91-137">設定 [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) 列舉值 proxy 安全性。</span><span class="sxs-lookup"><span data-stu-id="47b91-137">Set [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) enumerator proxy security.</span></span> <span data-ttu-id="47b91-138">使用完畢後，請務必清除記憶體中的認證。</span><span class="sxs-lookup"><span data-stu-id="47b91-138">Make sure to erase the credentials from memory after you have finished using them.</span></span>

    <span data-ttu-id="47b91-139">如需詳細資訊，請參閱 [在 IWbemServices 和其他 proxy 上設定安全性](setting-the-security-on-iwbemservices-and-other-proxies.md)。</span><span class="sxs-lookup"><span data-stu-id="47b91-139">For more information, see [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

9.  <span data-ttu-id="47b91-140">取得並顯示 WQL 查詢的資料。</span><span class="sxs-lookup"><span data-stu-id="47b91-140">Get and display the data from the WQL query.</span></span> <span data-ttu-id="47b91-141">[**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)指標會連結到查詢所傳回的資料物件，而且可以使用 [**IEnumWbemClassObject：： Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next)方法來抓取資料物件。</span><span class="sxs-lookup"><span data-stu-id="47b91-141">The [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) pointer is linked to the data objects that the query returned, and the data objects can be retrieved with the [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) method.</span></span> <span data-ttu-id="47b91-142">這個方法會將資料物件連結至傳遞給方法的 [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) 指標。</span><span class="sxs-lookup"><span data-stu-id="47b91-142">This method links the data objects to an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer that is passed into the method.</span></span> <span data-ttu-id="47b91-143">您可以使用 [**IWbemClassObject：： get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) 方法，從資料物件取得所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="47b91-143">Use the [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) method to get the desired information from the data objects.</span></span>

    <span data-ttu-id="47b91-144">下列程式碼範例會用來 `Name` 從資料物件取得屬性，這個屬性會提供作業系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="47b91-144">The following code example is used to get the `Name` property from the data object, which provides the name of the operating system.</span></span>

    ```C++
    VARIANT vtProp;

    // Get the value of the Name property
    hr = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
    wcout << " OS Name : " << vtProp.bstrVal << endl;
    ```

    

    <span data-ttu-id="47b91-145">一旦屬性的值 `Name` 儲存在 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) 變數中 `vtProp` ，就可以對使用者顯示。</span><span class="sxs-lookup"><span data-stu-id="47b91-145">Once the value of the `Name` property is stored in the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) variable `vtProp`, it can then be displayed to the user.</span></span>

    <span data-ttu-id="47b91-146">下列程式碼範例會示範如何再次使用 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) 變數來儲存和顯示可用實體記憶體數量的值。</span><span class="sxs-lookup"><span data-stu-id="47b91-146">The following code example shows how the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) variable can be used again to store and display the value of the amount of free physical memory.</span></span>

    ```C++
    hr = pclsObj->Get(L"FreePhysicalMemory",
        0, &vtProp, 0, 0);
    wcout << " Free physical memory (in kilobytes): "
        << vtProp.uintVal << endl;
    ```

    

    <span data-ttu-id="47b91-147">如需詳細資訊，請參閱 [列舉 WMI](enumerating-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="47b91-147">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span>

<span data-ttu-id="47b91-148">下列程式碼範例示範如何從遠端電腦取得 WMI 資料半同步方式。</span><span class="sxs-lookup"><span data-stu-id="47b91-148">The following code example shows how to get WMI data semisynchronously from a remote computer.</span></span>


```C++
#define _WIN32_DCOM
#define UNICODE
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
#pragma comment(lib, "credui.lib")
#pragma comment(lib, "comsuppw.lib")
#include <wincred.h>
#include <strsafe.h>

int __cdecl main(int argc, char **argv)
{
    HRESULT hres;

    // Step 1: --------------------------------------------------
    // Initialize COM. ------------------------------------------

    hres =  CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hres))
    {
        cout << "Failed to initialize COM library. Error code = 0x" 
            << hex << hres << endl;
        return 1;                  // Program has failed.
    }

    // Step 2: --------------------------------------------------
    // Set general COM security levels --------------------------

    hres =  CoInitializeSecurity(
        NULL, 
        -1,                          // COM authentication
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication 
        RPC_C_IMP_LEVEL_IDENTIFY,    // Default Impersonation  
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities 
        NULL                         // Reserved
        );

                      
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. Error code = 0x" 
            << hex << hres << endl;
        CoUninitialize();
        return 1;                    // Program has failed.
    }
    
    // Step 3: ---------------------------------------------------
    // Obtain the initial locator to WMI -------------------------

    IWbemLocator *pLoc = NULL;

    hres = CoCreateInstance(
        CLSID_WbemLocator,             
        0, 
        CLSCTX_INPROC_SERVER, 
        IID_IWbemLocator, (LPVOID *) &pLoc);
 
    if (FAILED(hres))
    {
        cout << "Failed to create IWbemLocator object."
            << " Err code = 0x"
            << hex << hres << endl;
        CoUninitialize();
        return 1;                 // Program has failed.
    }

    // Step 4: -----------------------------------------------------
    // Connect to WMI through the IWbemLocator::ConnectServer method

    IWbemServices *pSvc = NULL;

    // Get the user name and password for the remote computer
    CREDUI_INFO cui;
    bool useToken = false;
    bool useNTLM = true;
    wchar_t pszName[CREDUI_MAX_USERNAME_LENGTH+1] = {0};
    wchar_t pszPwd[CREDUI_MAX_PASSWORD_LENGTH+1] = {0};
    wchar_t pszDomain[CREDUI_MAX_USERNAME_LENGTH+1];
    wchar_t pszUserName[CREDUI_MAX_USERNAME_LENGTH+1];
    wchar_t pszAuthority[CREDUI_MAX_USERNAME_LENGTH+1];
    BOOL fSave;
    DWORD dwErr;

    memset(&cui,0,sizeof(CREDUI_INFO));
    cui.cbSize = sizeof(CREDUI_INFO);
    cui.hwndParent = NULL;
    // Ensure that MessageText and CaptionText identify
    // what credentials to use and which application requires them.
    cui.pszMessageText = TEXT("Press cancel to use process token");
    cui.pszCaptionText = TEXT("Enter Account Information");
    cui.hbmBanner = NULL;
    fSave = FALSE;

    dwErr = CredUIPromptForCredentials( 
        &cui,                             // CREDUI_INFO structure
        TEXT(""),                         // Target for credentials
        NULL,                             // Reserved
        0,                                // Reason
        pszName,                          // User name
        CREDUI_MAX_USERNAME_LENGTH+1,     // Max number for user name
        pszPwd,                           // Password
        CREDUI_MAX_PASSWORD_LENGTH+1,     // Max number for password
        &fSave,                           // State of save check box
        CREDUI_FLAGS_GENERIC_CREDENTIALS |// flags
        CREDUI_FLAGS_ALWAYS_SHOW_UI |
        CREDUI_FLAGS_DO_NOT_PERSIST);  

    if(dwErr == ERROR_CANCELLED)
    {
        useToken = true;
    }
    else if (dwErr)
    {
        cout << "Did not get credentials " << dwErr << endl;
        pLoc->Release();     
        CoUninitialize();
        return 1;      
    }

    // change the computerName strings below to the full computer name
    // of the remote computer
    if(!useNTLM)
    {
        StringCchPrintf(pszAuthority, CREDUI_MAX_USERNAME_LENGTH+1, L"kERBEROS:%s", L"COMPUTERNAME");
    }

    // Connect to the remote root\cimv2 namespace
    // and obtain pointer pSvc to make IWbemServices calls.
    //---------------------------------------------------------
   
    hres = pLoc->ConnectServer(
        _bstr_t(L"\\\\COMPUTERNAME\\root\\cimv2"),
        _bstr_t(useToken?NULL:pszName),    // User name
        _bstr_t(useToken?NULL:pszPwd),     // User password
        NULL,                              // Locale             
        NULL,                              // Security flags
        _bstr_t(useNTLM?NULL:pszAuthority),// Authority        
        NULL,                              // Context object 
        &pSvc                              // IWbemServices proxy
        );
    
    if (FAILED(hres))
    {
        cout << "Could not connect. Error code = 0x" 
             << hex << hres << endl;
        pLoc->Release();     
        CoUninitialize();
        return 1;                // Program has failed.
    }

    cout << "Connected to ROOT\\CIMV2 WMI namespace" << endl;


    // step 5: --------------------------------------------------
    // Create COAUTHIDENTITY that can be used for setting security on proxy

    COAUTHIDENTITY *userAcct =  NULL ;
    COAUTHIDENTITY authIdent;

    if( !useToken )
    {
        memset(&authIdent, 0, sizeof(COAUTHIDENTITY));
        authIdent.PasswordLength = wcslen (pszPwd);
        authIdent.Password = (USHORT*)pszPwd;

        LPWSTR slash = wcschr (pszName, L'\\');
        if( slash == NULL )
        {
            cout << "Could not create Auth identity. No domain specified\n" ;
            pSvc->Release();
            pLoc->Release();     
            CoUninitialize();
            return 1;               // Program has failed.
        }

        StringCchCopy(pszUserName, CREDUI_MAX_USERNAME_LENGTH+1, slash+1);
        authIdent.User = (USHORT*)pszUserName;
        authIdent.UserLength = wcslen(pszUserName);

        StringCchCopyN(pszDomain, CREDUI_MAX_USERNAME_LENGTH+1, pszName, slash - pszName);
        authIdent.Domain = (USHORT*)pszDomain;
        authIdent.DomainLength = slash - pszName;
        authIdent.Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;

        userAcct = &authIdent;

    }

    // Step 6: --------------------------------------------------
    // Set security levels on a WMI connection ------------------

    hres = CoSetProxyBlanket(
       pSvc,                           // Indicates the proxy to set
       RPC_C_AUTHN_DEFAULT,            // RPC_C_AUTHN_xxx
       RPC_C_AUTHZ_DEFAULT,            // RPC_C_AUTHZ_xxx
       COLE_DEFAULT_PRINCIPAL,         // Server principal name 
       RPC_C_AUTHN_LEVEL_PKT_PRIVACY,  // RPC_C_AUTHN_LEVEL_xxx 
       RPC_C_IMP_LEVEL_IMPERSONATE,    // RPC_C_IMP_LEVEL_xxx
       userAcct,                       // client identity
       EOAC_NONE                       // proxy capabilities 
    );

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket. Error code = 0x" 
            << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 7: --------------------------------------------------
    // Use the IWbemServices pointer to make requests of WMI ----

    // For example, get the name of the operating system
    IEnumWbemClassObject* pEnumerator = NULL;
    hres = pSvc->ExecQuery(
        bstr_t("WQL"), 
        bstr_t("Select * from Win32_OperatingSystem"),
        WBEM_FLAG_FORWARD_ONLY | WBEM_FLAG_RETURN_IMMEDIATELY, 
        NULL,
        &pEnumerator);
    
    if (FAILED(hres))
    {
        cout << "Query for operating system name failed."
            << " Error code = 0x" 
            << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 8: -------------------------------------------------
    // Secure the enumerator proxy
    hres = CoSetProxyBlanket(
        pEnumerator,                    // Indicates the proxy to set
        RPC_C_AUTHN_DEFAULT,            // RPC_C_AUTHN_xxx
        RPC_C_AUTHZ_DEFAULT,            // RPC_C_AUTHZ_xxx
        COLE_DEFAULT_PRINCIPAL,         // Server principal name 
        RPC_C_AUTHN_LEVEL_PKT_PRIVACY,  // RPC_C_AUTHN_LEVEL_xxx 
        RPC_C_IMP_LEVEL_IMPERSONATE,    // RPC_C_IMP_LEVEL_xxx
        userAcct,                       // client identity
        EOAC_NONE                       // proxy capabilities 
        );

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket on enumerator. Error code = 0x" 
             << hex << hres << endl;
        pEnumerator->Release();
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // When you have finished using the credentials,
    // erase them from memory.
    SecureZeroMemory(pszName, sizeof(pszName));
    SecureZeroMemory(pszPwd, sizeof(pszPwd));
    SecureZeroMemory(pszUserName, sizeof(pszUserName));
    SecureZeroMemory(pszDomain, sizeof(pszDomain));


    // Step 9: -------------------------------------------------
    // Get the data from the query in step 7 -------------------
 
    IWbemClassObject *pclsObj = NULL;
    ULONG uReturn = 0;
   
    while (pEnumerator)
    {
        HRESULT hr = pEnumerator->Next(WBEM_INFINITE, 1, 
            &pclsObj, &uReturn);

        if(0 == uReturn)
        {
            break;
        }

        VARIANT vtProp;

        // Get the value of the Name property
        hr = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
        wcout << " OS Name : " << vtProp.bstrVal << endl;

        // Get the value of the FreePhysicalMemory property
        hr = pclsObj->Get(L"FreePhysicalMemory",
            0, &vtProp, 0, 0);
        wcout << " Free physical memory (in kilobytes): "
            << vtProp.uintVal << endl;
        VariantClear(&vtProp);

        pclsObj->Release();
        pclsObj = NULL;
    }

    // Cleanup
    // ========
    
    pSvc->Release();
    pLoc->Release();
    pEnumerator->Release();
    if( pclsObj )
    {
        pclsObj->Release();
    }
    
    CoUninitialize();

    return 0;   // Program successfully completed.
    
}
```



 

 
