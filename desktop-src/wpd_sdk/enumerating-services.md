---
description: 列舉服務
ms.assetid: 6ee6eecb-3812-45c6-8b27-7dfd6fa82758
title: 列舉服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2eca8221a9a34bf9e921bcaca00eac99f2a75d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984257"
---
# <a name="enumerating-services"></a><span data-ttu-id="38b1c-103">列舉服務</span><span class="sxs-lookup"><span data-stu-id="38b1c-103">Enumerating Services</span></span>

<span data-ttu-id="38b1c-104">WpdServicesApiSample 應用程式包含的程式碼會示範應用程式如何列舉目前連接至電腦的任何裝置上找到的所有連絡人服務。</span><span class="sxs-lookup"><span data-stu-id="38b1c-104">The WpdServicesApiSample application includes code that demonstrates how an application can enumerate all of the Contacts services found on any of the devices currently connected to a computer.</span></span>

<span data-ttu-id="38b1c-105">當使用者在命令列中選擇 [0] 選項時，應用程式會叫用在 ServiceEnumeration .cpp 模組中找到的 **EnumerateContactsServices** 方法。</span><span class="sxs-lookup"><span data-stu-id="38b1c-105">When the user chooses option "0" at the command line, the application invokes the **EnumerateContactsServices** method that is found in the ServiceEnumeration.cpp module.</span></span> <span data-ttu-id="38b1c-106">此方法會顯示所有支援 Contacts 服務的連線裝置清單。</span><span class="sxs-lookup"><span data-stu-id="38b1c-106">This method displays a list of all connected devices that support the Contacts service.</span></span>

<span data-ttu-id="38b1c-107">例如，如果 WpdServiceSampleDriver 是唯一安裝的裝置，應用程式會傳回三個資料欄位： ( 「範例裝置」 ) 的易記名稱、製造商 ( 「Windows 可攜式裝置群組」 ) ，以及描述 ( 「連絡人服務裝置2000」 ) 。</span><span class="sxs-lookup"><span data-stu-id="38b1c-107">For example, if the WpdServiceSampleDriver is the only installed device, the application returns three fields of data: a Friendly Name ("Sample Device"), a Manufacturer ("Windows Portable Devices Group"), and, a Description ("Contacts Service Device 2000").</span></span>

<span data-ttu-id="38b1c-108">**EnumerateContactsServices** 方法會完成下列工作：</span><span class="sxs-lookup"><span data-stu-id="38b1c-108">The **EnumerateContactsServices** method accomplishes the following tasks:</span></span>

-   <span data-ttu-id="38b1c-109">建立 [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) 介面來處理已安裝裝置的列舉。</span><span class="sxs-lookup"><span data-stu-id="38b1c-109">Creates an [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface to handle enumeration of installed devices.</span></span>
-   <span data-ttu-id="38b1c-110">建立 [**IPortableDeviceServiceManager**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager) 介面，以處理每個裝置上的服務列舉。</span><span class="sxs-lookup"><span data-stu-id="38b1c-110">Creates an [**IPortableDeviceServiceManager**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager) interface to handle enumeration of the services on each device.</span></span>
-   <span data-ttu-id="38b1c-111">逐一查看已安裝的裝置、搜尋 Contacts 服務，然後顯示任何支援此服務之裝置的裝置資訊。</span><span class="sxs-lookup"><span data-stu-id="38b1c-111">Iterates through the installed devices, searching for the Contacts service, and displays the device information for any device that supports this service.</span></span>

<span data-ttu-id="38b1c-112">下列程式碼說明 **EnumerateContactsServices** 方法。</span><span class="sxs-lookup"><span data-stu-id="38b1c-112">The following code illustrates the **EnumerateContactsServices** method.</span></span>


```C++
// Enumerates all Contacts Services, displaying the associated device of each service.
void EumerateContactsServices(CAtlArray<PWSTR>& ContactsServicePnpIDs)
{
    HRESULT                                 hr              = S_OK;
    DWORD                                   cPnpDeviceIDs   = 0;
    PWSTR*                                  pPnpDeviceIDs   = NULL;
    CComPtr<IPortableDeviceManager>         pPortableDeviceManager;
    CComPtr<IPortableDeviceServiceManager>  pServiceManager;

    // CoCreate the IPortableDeviceManager interface to enumerate
    // portable devices and to get information about them.
    hr = CoCreateInstance(CLSID_PortableDeviceManager,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&pPortableDeviceManager));

    if (FAILED(hr))
    {
        printf("! Failed to CoCreateInstance CLSID_PortableDeviceManager, hr = 0x%lx\n",hr);
    }        

    // Retrieve the IPortableDeviceServiceManager interface to enumerate device services.
    if (SUCCEEDED(hr))
    {
        hr = pPortableDeviceManager->QueryInterface(IID_PPV_ARGS(&pServiceManager));
        if (FAILED(hr))
        {
            printf("! Failed to QueryInterface IID_IPortableDeviceServiceManager, hr = 0x%lx\n",hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        // First, pass NULL as the PWSTR array pointer to get the total number
        // of devices found on the system.
        hr = pPortableDeviceManager->GetDevices(NULL, &cPnpDeviceIDs);

        if (FAILED(hr))
        {
            printf("! Failed to get number of devices on the system, hr = 0x%lx\n",hr);
        }

        if (SUCCEEDED(hr) && (cPnpDeviceIDs > 0))
        {
            // Second, allocate an array to hold the PnPDeviceID strings returned from
            // the IPortableDeviceManager::GetDevices method
            pPnpDeviceIDs = new (std::nothrow) PWSTR[cPnpDeviceIDs];

            if (pPnpDeviceIDs != NULL)
            {
                DWORD dwIndex = 0;

                hr = pPortableDeviceManager->GetDevices(pPnpDeviceIDs, &cPnpDeviceIDs);
                if (SUCCEEDED(hr))
                {   
                    // For each device found, find the contacts service
                    for (dwIndex = 0; dwIndex < cPnpDeviceIDs; dwIndex++)
                    {
                        DWORD   cPnpServiceIDs = 0;
                        PWSTR   pPnpServiceID  = NULL;

                        // First, pass NULL as the PWSTR array pointer to get the total number
                        // of contacts services (SERVICE_Contacts) found on the device.
                        // To find the total number of all services on the device, use GUID_DEVINTERFACE_WPD_SERVICE.
                        hr = pServiceManager->GetDeviceServices(pPnpDeviceIDs[dwIndex], SERVICE_Contacts, NULL, &cPnpServiceIDs);
                        
                        if (SUCCEEDED(hr) && (cPnpServiceIDs > 0))
                        {                               
                            // For simplicity, we are only using the first contacts service on each device
                            cPnpServiceIDs = 1;
                            hr = pServiceManager->GetDeviceServices(pPnpDeviceIDs[dwIndex], SERVICE_Contacts, &pPnpServiceID, &cPnpServiceIDs);

                            if (SUCCEEDED(hr))
                            {
                                // We've found the service, display it and save its PnP Identifier
                                ContactsServicePnpIDs.Add(pPnpServiceID);

                                printf("[%d] ", static_cast<DWORD>(ContactsServicePnpIDs.GetCount()-1));

                                // Display information about the device that contains this service.
                                DisplayDeviceInformation(pServiceManager, pPnpServiceID);

                                // ContactsServicePnpIDs now owns the memory for this string
                                pPnpServiceID = NULL;
                            }
                            else
                            {
                                printf("! Failed to get the first contacts service from '%ws, hr = 0x%lx\n",pPnpDeviceIDs[dwIndex],hr);
                            }
                        }
                    }
                }

                // Free all returned PnPDeviceID strings
                FreePortableDevicePnPIDs(pPnpDeviceIDs, cPnpDeviceIDs);

                // Delete the array of PWSTR pointers
                delete [] pPnpDeviceIDs;
                pPnpDeviceIDs = NULL;

            }
            else
            {
                printf("! Failed to allocate memory for PWSTR array\n");
            }            
        }
    }
    
    printf("\n%d Contacts Device Service(s) found on the system\n\n", static_cast<DWORD>(ContactsServicePnpIDs.GetCount()));
}
```



## <a name="related-topics"></a><span data-ttu-id="38b1c-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="38b1c-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38b1c-114">**IPortableDeviceManager 介面**</span><span class="sxs-lookup"><span data-stu-id="38b1c-114">**IPortableDeviceManager Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)
</dt> <dt>

[<span data-ttu-id="38b1c-115">**IPortableDeviceServiceManager 介面**</span><span class="sxs-lookup"><span data-stu-id="38b1c-115">**IPortableDeviceServiceManager Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)
</dt> <dt>

[<span data-ttu-id="38b1c-116">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="38b1c-116">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



