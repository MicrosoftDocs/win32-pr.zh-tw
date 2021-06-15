---
title: " (WMP SDK) 列舉裝置"
description: 此範例程式碼顯示的函式會藉由建立指標的陣列（每個都代表一個裝置）來列舉裝置。
ms.assetid: 0236a629-c09a-4687-a8ba-fa05107fab33
keywords:
- Windows Media Player，可攜式裝置
- Windows Media Player 物件模型，可攜式裝置
- 物件模型，可攜式裝置
- Windows Media Player 的 ActiveX 控制項、可攜式裝置
- ActiveX 控制項、可攜式裝置
- Windows Media Player Mobile ActiveX 控制項、可攜式裝置
- Windows Media Player Mobile、可攜式裝置
- 可攜式裝置，列舉
- 列舉，可攜式裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d44f71fa26f40983424ced70280d9c03e0892a00
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068435"
---
# <a name="enumerating-devices"></a>列舉裝置

Windows Media Player 使用 **IWMPSyncDevice** 介面表示可攜式裝置。 下列範例程式碼顯示的函式會建立 **IWMPSyncDevice** 指標的陣列。 陣列中的每個指標都代表 Windows Media Player 有預存資訊的裝置。 裝置不需要連線到電腦，也不需要與目前的 Windows Media Player 實例合作。

每當您收到 **>deviceconnect** 事件或 **DeviceDisconnect** 事件時，您應該列舉裝置。

下列函式會列舉裝置。 *BConnectedOnly* 參數會指定是否只列舉目前連線到使用者電腦的裝置。


```C++
STDMETHODIMP CMainDlg::EnumDevices(BOOL bConnectedOnly)
{
    HRESULT hr = S_OK;
    CComPtr<IWMPSyncServices>  spSyncServices;
    long cDeviceArray = 0;  // Size to make the array
    long cAllDevices = 0;  // Count of all devices
    long cDeviceIndex = 0; // Index for adding devices to array.
    CComPtr<IWMPSyncDevice> spTempDevice;
    VARIANT_BOOL vbIsConnected = VARIANT_FALSE;

    // Delete any existing array.
    FreeDeviceArray();

    // Retrieve a pointer to IWMPSyncServices.
    hr = m_spPlayer->QueryInterface(&spSyncServices);

    if(SUCCEEDED(hr) && spSyncServices.p)
    {  
        hr = spSyncServices->get_deviceCount(&cAllDevices);
    }

    if(SUCCEEDED(hr) && cAllDevices > 0)
    {
        if(bConnectedOnly)
        {
            // Count the number of connected devices.
            for(long i = 0; i < cAllDevices; i++)
            {     
                spTempDevice.Release();
                hr = spSyncServices->getDevice(i, &spTempDevice);

                if(SUCCEEDED(hr) && spTempDevice.p)
                {
                    spTempDevice->get_connected(&vbIsConnected);

                    if(vbIsConnected == VARIANT_TRUE)
                    {
                        // Count only the connected devices.
                        cDeviceArray++;
                    }
                }
            }
        }
        else
        {
            cDeviceArray = cAllDevices;
        }

        if(cDeviceArray == 0)
        {
            return hr;
        }

        // Cache the device count.
        m_cDevices = cDeviceArray;

        // Create a new device array.
        m_ppWMPDevices = new IWMPSyncDevice*[cDeviceArray];
        if(!m_ppWMPDevices)
        {
            return E_OUTOFMEMORY;
        }
        
        ZeroMemory(m_ppWMPDevices, sizeof (IWMPSyncDevice*) * cDeviceArray);

        // Fill the array.
        for(long i = 0; i < cAllDevices; i++)
        {
            spTempDevice.Release();
            hr = spSyncServices->getDevice(i, &spTempDevice);
            if(SUCCEEDED(hr) && spTempDevice.p)
            {
                spTempDevice->get_connected(&vbIsConnected);

                if( (bConnectedOnly && vbIsConnected == VARIANT_TRUE) ||
                     !bConnectedOnly )
                {
                    // Add the device to the custom array.
                    spTempDevice.CopyTo(&m_ppWMPDevices[cDeviceIndex++]);
                }
            }
        }
    }

    return hr;
}
```



您可以使用類似的程式碼來取出其他這類裝置清單。 例如，您可以使用 [IWMPSyncDevice：： get \_ 狀態](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) 來建立有合作關係的裝置陣列。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMPEvents2：:D eviceConnect**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-deviceconnect)
</dt> <dt>

[**IWMPEvents2：:D eviceDisconnect**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-devicedisconnect)
</dt> <dt>

[**IWMPSyncDevice 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[**IWMPSyncDevice：：取得 \_ 連接**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected)
</dt> <dt>

[**IWMPSyncServices 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
</dt> <dt>

[**使用可攜式裝置**](working-with-portable-devices.md)
</dt> </dl>

 

 




