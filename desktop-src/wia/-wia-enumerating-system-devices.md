---
description: 使用 IWiaDevMgr：： EnumDeviceInfo (或 IWiaDevMgr2：：) EnumDeviceInfo 方法來列舉安裝在系統上的 Windows 映像取得 (WIA) 裝置。
ms.assetid: 6465a33e-1b3b-4142-a58f-b27e9c95cd3e
title: 列舉系統裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d2d65879cd1fc8466f4ada638281ef496636b19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944320"
---
# <a name="enumerating-system-devices"></a>列舉系統裝置

使用 [**IWiaDevMgr：： EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (或 [**IWiaDevMgr2：：) EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md) 方法來列舉安裝在系統上的 WINDOWS 映射取得 (WIA) 裝置。 這個方法會建立裝置屬性的列舉物件，並將指標傳回給列舉物件所支援的 [**IEnumWIA \_ 開發人員 \_ 資訊**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) 介面。

然後，您可以使用 [**IEnumWIA \_ DEV \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) 介面的方法，為系統上安裝的每個裝置取得 [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) 介面指標。

WiaSSamp 範例應用程式中的下列程式碼示範如何建立系統上裝置的列舉物件，並逐一查看這些裝置：


```
    HRESULT EnumerateWiaDevices( IWiaDevMgr *pWiaDevMgr ) //XP or earlier
    HRESULT EnumerateWiaDevices( IWiaDevMgr2 *pWiaDevMgr ) //Vista or later
    
    {
        //
        // Validate arguments
        //
        if (NULL == pWiaDevMgr)
        {
            return E_INVALIDARG;
        }

        //
        // Get a device enumerator interface
        //
        IEnumWIA_DEV_INFO *pWiaEnumDevInfo = NULL;
        HRESULT hr = pWiaDevMgr->EnumDeviceInfo( WIA_DEVINFO_ENUM_LOCAL, &pWiaEnumDevInfo );
        if (SUCCEEDED(hr))
        {
            //
            // Loop until you get an error or pWiaEnumDevInfo->Next returns
            // S_FALSE to signal the end of the list.
            //
            while (S_OK == hr)
            {
                //
                // Get the next device's property storage interface pointer
                //
                IWiaPropertyStorage *pWiaPropertyStorage = NULL;
                hr = pWiaEnumDevInfo->Next( 1, &pWiaPropertyStorage, NULL );

                //
                // pWiaEnumDevInfo->Next will return S_FALSE when the list is
                // exhausted, so check for S_OK before using the returned
                // value.
                //
                if (hr == S_OK)
                {
                    //
                    // Do something with the device's IWiaPropertyStorage*
                    //

                    //
                    // Release the device's IWiaPropertyStorage*
                    //
                    pWiaPropertyStorage->Release();
                    pWiaPropertyStorage = NULL;
                }
            }

            //
            // If the result of the enumeration is S_FALSE (which
            // is normal), change it to S_OK.
            //
            if (S_FALSE == hr)
            {
                hr = S_OK;
            }

            //
            // Release the enumerator
            //
            pWiaEnumDevInfo->Release();
            pWiaEnumDevInfo = NULL;
        }

        //
        // Return the result of the enumeration
        //
        return hr;
    }
```



WIA \_ >lnk-devinfo \_ ENUM \_ LOCAL 是一個 WIA 常數，代表這個參數唯一有效的值。

在此範例中，參數 **pWiaDevMgr** 會指向之前呼叫 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)之後的 [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (或 [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) 介面實例。

應用程式會呼叫 [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (或 [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) 指標 **PWiaDevMgr** 的 [**IWiaDevMgr：： EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (或 [**IWiaDevMgr2：：) EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md)方法，其會以 [**pWiaEnumDevInfo \_ 開發人員 \_ 資訊**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)介面指標的位址填滿 **IEnumWIA** 。

如果呼叫成功，應用程式就會呼叫 [**IEnumWIA \_ dev \_ Info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)指標的 [**IEnumWIA \_ DEV \_ info：： Reset**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-reset)方法。 **PWiaEnumDevInfo** 變數可確保列舉會從開頭開始。

如果此呼叫成功，應用程式會重複呼叫 [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)指標 **pWiaEnumDevInfo** 的 [**IEnumWIA \_ DEV \_ info：： Next**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-next)方法來逐一查看系統上的裝置，直到該方法不再傳回 S \_ OK （表示列舉已完成）。

每次呼叫 **pWiaEnumDevInfo->Next** 會填滿 **pWiaPropertyStorage** 的 [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) 介面指標，其中包含特定裝置的屬性資訊。

 

 
