---
title: " (WPD) 列舉裝置"
description: 列舉裝置
ms.assetid: 28ded3cf-b0c8-4c90-ab39-efc879adb6e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2738398de7f3bfb6aa1ea88175ff30241b4dbb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997250"
---
# <a name="enumerating-devices-wpd"></a> (WPD) 列舉裝置

大部分的應用程式所完成的第一項工作，就是連線到電腦的裝置列舉。 [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)介面支援此工作，以及抓取裝置資訊 (例如製造商、易記名稱和描述) ）。

DeviceEnumeration 中的 EnumerateAllDevices 函式包含的程式碼會示範如何抓取已連接的裝置計數，以及在抓取計數之後，針對每個連線的裝置抓取裝置特定資訊。

EnumerateAllDevices 函式會完成四項主要工作：

1.  建立便攜裝置管理員物件。
2.  抓取已連線裝置的計數。
3.  針對連線的裝置) 抓取裝置資訊 (。
4.  釋出裝置資訊時使用的記憶體。

下列各節將更詳細地說明這四項工作。

裝置列舉程式的第一個步驟是建立便攜裝置管理員物件。 這是藉由呼叫 CoCreateInstance 函式並傳遞類別識別碼 (物件的 CLSID) 來完成，指定程式碼將在其中執行的內容，指定 IPortableDeviceManager 介面的參考識別碼，然後提供可接收 IPortableDeviceManager 介面指標的指標變數。


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



一旦您取得 [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) 介面指標，就可以開始在此介面上呼叫方法。 在 EnumerateAllDevices 函數中呼叫的第一個方法是 [**IPortableDeviceManager：： GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices)。 當呼叫這個方法時，第一個引數設定為 **Null** 時，會傳回已連線裝置的計數。


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



取得已連線裝置的計數之後，您可以使用此值來抓取每個已連線裝置的裝置資訊。 此程式一開始會將字串指標的陣列傳遞為第一個引數，並將此陣列可保存的元素數目計數作為第二個引數， (此計數至少應等於可用裝置數目) 。

這個方法所傳回的字串是連接裝置的隨插即用名稱。 這些名稱接著會傳遞給 [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) 介面上的其他方法，以抓取裝置特定的資訊，例如易記名稱、製造商名稱和裝置描述。  (當應用程式呼叫 [**IPortableDevice：： open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) 方法時，也會使用這些名稱來開啟裝置的連線。 ) 


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



一旦您抓取裝置資訊之後，您將需要釋放與字串指標陣列所指向之字串相關聯的記憶體。 您也必須刪除此陣列。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IPortableDeviceManager 介面**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)
</dt> <dt>

[**程式設計指南**](programming-guide.md)
</dt> </dl>

 

 



