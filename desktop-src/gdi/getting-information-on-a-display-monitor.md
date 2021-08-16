---
description: 下列程式碼範例顯示如何使用 EnumDisplayDevices 來取得顯示監視器的資訊。
ms.assetid: 8c2420de-292f-481e-b06b-54cc174a8faf
title: 取得顯示監視器的資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4b446b379d1d90dd32eedb47d356d2de0fb9e07d1f30eba9e65e470a3f24e82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117886721"
---
# <a name="getting-information-on-a-display-monitor"></a>取得顯示監視器的資訊

下列程式碼範例顯示如何使用 [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) 來取得顯示監視器的資訊。


```C++
BOOL GetDisplayMonitorInfo(int nDeviceIndex, LPSTR lpszMonitorInfo)
{
    FARPROC EnumDisplayDevices;
    HINSTANCE  hInstUser32;
    DISPLAY_DEVICE DispDev; 
    char szSaveDeviceName[33];  // 32 + 1 for the null-terminator 
    BOOL bRet = TRUE;
        HRESULT hr;
    
    hInstUser32 = LoadLibrary("c:\\windows\User32.DLL");
    if (!hInstUser32) return FALSE;  
    
    // Get the address of the EnumDisplayDevices function 
    EnumDisplayDevices = (FARPROC)GetProcAddress(hInstUser32,"EnumDisplayDevicesA");
    if (!EnumDisplayDevices) {
        FreeLibrary(hInstUser32);
        return FALSE;
    }

    ZeroMemory(&DispDev, sizeof(DispDev));
    DispDev.cb = sizeof(DispDev); 
    
    // After the first call to EnumDisplayDevices,  
    // DispDev.DeviceString is the adapter name 
    if (EnumDisplayDevices(NULL, nDeviceIndex, &DispDev, 0)) 
        {  
                hr = StringCchCopy(szSaveDeviceName, 33, DispDev.DeviceName);
                if (FAILED(hr))
                {
                // TODO: write error handler 
                }
        
        // After second call, DispDev.DeviceString is the  
        // monitor name for that device  
        EnumDisplayDevices(szSaveDeviceName, 0, &DispDev, 0);   
        
                // In the following, lpszMonitorInfo must be 128 + 1 for  
                // the null-terminator. 
                hr = StringCchCopy(lpszMonitorInfo, 129, DispDev.DeviceString);
                if (FAILED(hr))
                {
                // TODO: write error handler 
                }
                
    } else    {
        bRet = FALSE;
    }

    FreeLibrary(hInstUser32);

    return bRet;
}
```



 

 



