---
title: " (WPD) 列舉裝置"
description: 瞭解應用程式如何使用 EnumerateAllDevices 函式來列舉裝置，該函式會取得已連線裝置的計數和裝置特定的資訊。
ms.assetid: 28ded3cf-b0c8-4c90-ab39-efc879adb6e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6465b04e6f1a18a0bdb74f0ce883cf9161371fb6
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068594"
---
# <a name="enumerating-devices-wpd"></a><span data-ttu-id="109bd-103"> (WPD) 列舉裝置</span><span class="sxs-lookup"><span data-stu-id="109bd-103">Enumerating devices (WPD)</span></span>

<span data-ttu-id="109bd-104">大部分的應用程式所完成的第一項工作，就是連線到電腦的裝置列舉。</span><span class="sxs-lookup"><span data-stu-id="109bd-104">The first task completed by most applications is the enumeration of the devices connected to the computer.</span></span> <span data-ttu-id="109bd-105">[**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)介面支援此工作，以及抓取裝置資訊 (例如製造商、易記名稱和描述) ）。</span><span class="sxs-lookup"><span data-stu-id="109bd-105">This task, and the retrieval of device information (such as manufacturer, friendly name, and description), is supported by the [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface.</span></span>

<span data-ttu-id="109bd-106">DeviceEnumeration 中的 EnumerateAllDevices 函式包含的程式碼會示範如何抓取已連接的裝置計數，以及在抓取計數之後，針對每個連線的裝置抓取裝置特定資訊。</span><span class="sxs-lookup"><span data-stu-id="109bd-106">The EnumerateAllDevices function in the DeviceEnumeration.cpp module contains code that demonstrates the retrieval of the count of connected devices and, once the count is retrieved, the retrieval of device-specific information for each connected device.</span></span>

<span data-ttu-id="109bd-107">EnumerateAllDevices 函式會完成四項主要工作：</span><span class="sxs-lookup"><span data-stu-id="109bd-107">The EnumerateAllDevices function accomplishes four primary tasks:</span></span>

1.  <span data-ttu-id="109bd-108">建立便攜裝置管理員物件。</span><span class="sxs-lookup"><span data-stu-id="109bd-108">Creates the portable device manager object.</span></span>
2.  <span data-ttu-id="109bd-109">抓取已連線裝置的計數。</span><span class="sxs-lookup"><span data-stu-id="109bd-109">Retrieves a count of connected devices.</span></span>
3.  <span data-ttu-id="109bd-110">針對連線的裝置) 抓取裝置資訊 (。</span><span class="sxs-lookup"><span data-stu-id="109bd-110">Retrieves device information (for the connected devices).</span></span>
4.  <span data-ttu-id="109bd-111">釋出裝置資訊時使用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="109bd-111">Frees the memory used when retrieving the device information.</span></span>

<span data-ttu-id="109bd-112">下列各節將更詳細地說明這四項工作。</span><span class="sxs-lookup"><span data-stu-id="109bd-112">Each of these four tasks is described in more detail in the following sections.</span></span>

<span data-ttu-id="109bd-113">裝置列舉程式的第一個步驟是建立便攜裝置管理員物件。</span><span class="sxs-lookup"><span data-stu-id="109bd-113">The first step in the device enumeration process is the creation of a portable device manager object.</span></span> <span data-ttu-id="109bd-114">這是藉由呼叫 CoCreateInstance 函式並傳遞類別識別碼 (物件的 CLSID) 來完成，指定程式碼將在其中執行的內容，指定 IPortableDeviceManager 介面的參考識別碼，然後提供可接收 IPortableDeviceManager 介面指標的指標變數。</span><span class="sxs-lookup"><span data-stu-id="109bd-114">This is done by calling the CoCreateInstance function and passing the class identifier (CLSID) for the object, specifying the context in which the code will run, specifying a reference identifier for the IPortableDeviceManager interface, and then supplying a pointer variable that receives the IPortableDeviceManager interface pointer.</span></span>


```C++
HRESULT hr = CoCreateInstance(CLSID_PortableDeviceManager,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&pPortableDeviceManager));
if (FAILED(hr))
{
    printf("! Failed to CoCreateInstance CLSID_PortableDeviceManager, hr = 0x%lx\n",hr);
}
```



<span data-ttu-id="109bd-115">一旦您取得 [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) 介面指標，就可以開始在此介面上呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="109bd-115">Once you obtain an [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface pointer, you can begin calling methods on this interface.</span></span> <span data-ttu-id="109bd-116">在 EnumerateAllDevices 函數中呼叫的第一個方法是 [**IPortableDeviceManager：： GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices)。</span><span class="sxs-lookup"><span data-stu-id="109bd-116">The first method called in the EnumerateAllDevices function is [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices).</span></span> <span data-ttu-id="109bd-117">當呼叫這個方法時，第一個引數設定為 **Null** 時，會傳回已連線裝置的計數。</span><span class="sxs-lookup"><span data-stu-id="109bd-117">When this method is called with the first argument set to **NULL**, it returns the count of connected devices.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pPortableDeviceManager->GetDevices(NULL, &cPnPDeviceIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get number of devices on the system, hr = 0x%lx\n",hr);
    }
}

// Report the number of devices found.  NOTE: we will report 0, if an error
// occured.

printf("\n%d Windows Portable Device(s) found on the system\n\n", cPnPDeviceIDs);
```



<span data-ttu-id="109bd-118">取得已連線裝置的計數之後，您可以使用此值來抓取每個已連線裝置的裝置資訊。</span><span class="sxs-lookup"><span data-stu-id="109bd-118">After you have retrieved the count of connected devices, you can use this value to retrieve device information for each connected device.</span></span> <span data-ttu-id="109bd-119">此程式一開始會將字串指標的陣列傳遞為第一個引數，並將此陣列可保存的元素數目計數作為第二個引數， (此計數至少應等於可用裝置數目) 。</span><span class="sxs-lookup"><span data-stu-id="109bd-119">This process begins by passing an array of string pointers as the first argument and a count of the number of elements that this array can hold as the second argument (this count should at least be equal to the number of available devices).</span></span>

<span data-ttu-id="109bd-120">這個方法所傳回的字串是連接裝置的隨插即用名稱。</span><span class="sxs-lookup"><span data-stu-id="109bd-120">The strings returned by this method are the Plug and Play names of the connected devices.</span></span> <span data-ttu-id="109bd-121">這些名稱接著會傳遞給 [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) 介面上的其他方法，以抓取裝置特定的資訊，例如易記名稱、製造商名稱和裝置描述。</span><span class="sxs-lookup"><span data-stu-id="109bd-121">These names, in turn, are passed to other methods on the [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface to retrieve device-specific information such as the friendly name, the manufacturer's name, and the device description.</span></span> <span data-ttu-id="109bd-122"> (當應用程式呼叫 [**IPortableDevice：： open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) 方法時，也會使用這些名稱來開啟裝置的連線。 ) </span><span class="sxs-lookup"><span data-stu-id="109bd-122">(These names are also used to open a connection to the device when an application calls the [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) method.)</span></span>


```C++
if (SUCCEEDED(hr) && (cPnPDeviceIDs > 0))
{
    pPnpDeviceIDs = new (std::nothrow) PWSTR[cPnPDeviceIDs];
    if (pPnpDeviceIDs != NULL)
    {
        DWORD dwIndex = 0;

        hr = pPortableDeviceManager->GetDevices(pPnpDeviceIDs, &cPnPDeviceIDs);
        if (SUCCEEDED(hr))
        {
            // For each device found, display the devices friendly name,
            // manufacturer, and description strings.
            for (dwIndex = 0; dwIndex < cPnPDeviceIDs; dwIndex++)
            {
                printf("[%d] ", dwIndex);
                DisplayFriendlyName(pPortableDeviceManager, pPnpDeviceIDs[dwIndex]);
                printf("    ");
                DisplayManufacturer(pPortableDeviceManager, pPnpDeviceIDs[dwIndex]);
                printf("    ");
                DisplayDescription(pPortableDeviceManager, pPnpDeviceIDs[dwIndex]);
            }
        }
        else
        {
            printf("! Failed to get the device list from the system, hr = 0x%lx\n",hr);
        }
```



<span data-ttu-id="109bd-123">一旦您抓取裝置資訊之後，您將需要釋放與字串指標陣列所指向之字串相關聯的記憶體。</span><span class="sxs-lookup"><span data-stu-id="109bd-123">Once you've retrieved the device information, you will need to free the memory associated with the strings pointed to by the array of string pointers.</span></span> <span data-ttu-id="109bd-124">您也必須刪除此陣列。</span><span class="sxs-lookup"><span data-stu-id="109bd-124">You will also need to delete this array.</span></span>


```C++
for (dwIndex = 0; dwIndex < cPnPDeviceIDs; dwIndex++)
{
    CoTaskMemFree(pPnpDeviceIDs[dwIndex]);
    pPnpDeviceIDs[dwIndex] = NULL;
}

// Delete the array of PWSTR pointers
delete [] pPnpDeviceIDs;
pPnpDeviceIDs = NULL;
```



## <a name="related-topics"></a><span data-ttu-id="109bd-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="109bd-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="109bd-126">**IPortableDeviceManager 介面**</span><span class="sxs-lookup"><span data-stu-id="109bd-126">**IPortableDeviceManager Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)
</dt> <dt>

[<span data-ttu-id="109bd-127">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="109bd-127">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



