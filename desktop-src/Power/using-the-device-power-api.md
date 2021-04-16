---
description: 使用裝置電來源程式設計專案來管理裝置在系統處於睡眠狀態時的執行方式。
ms.assetid: 44479f5d-2e92-4802-a633-3e0bb7d61e94
title: 使用裝置電源 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cabd7a54efc0979360a863dc9c0cf16d69d8d22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513393"
---
# <a name="using-the-device-power-api"></a>使用裝置電源 API

使用裝置電來源程式設計專案來管理裝置在系統處於睡眠狀態時的執行方式。

## <a name="opening-and-closing-the-device-list"></a>開啟和關閉裝置清單

開啟和關閉裝置清單在 CPU 時間方面是成本高昂的流程。 只有當應用程式需要多次查詢裝置清單時，才需要執行這項作業的 [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) 和 [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) 函數。

如果呼叫 [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) ，則必須在裝置清單查詢完成時呼叫 [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) 。 如果 **DevicePowerOpen** 已明確開啟 [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices)和 [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) ，則不會關閉該裝置清單。

## <a name="enumerating-devices"></a>列舉裝置

[**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices)函式會偵測裝置清單是否開啟，如果不是，則會開啟該清單。 **DevicePowerEnumDevices** 會根據指定的搜尋準則來列舉裝置。 如果裝置已開啟裝置清單，則會在函式傳回之前關閉。

## <a name="enabling-and-disabling-a-device-from-waking-the-system"></a>啟用及停用裝置，使其無法喚醒系統

[**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate)函式類似于 [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices)，會偵測裝置清單是否為開啟狀態，如果不是，則會開啟該功能。 **DevicePowerSetDeviceState** 接著會為指定的裝置設定指定的準則。 如果裝置已開啟裝置清單，則會在函式傳回之前關閉。

## <a name="example-code"></a>範例程式碼

下列範例示範如何使用裝置電源 API。


```C++
#define _WIN32_WINNT 0x0600
#include <Windows.h>
#include <PowrProf.h>
#include <stdio.h>
#include <tchar.h>

#pragma comment(lib, "PowrProf.lib")

int __cdecl main()
{
 // Define and initialize our return variables.
 LPWSTR  pRetBuf = NULL;
 ULONG bufSize = MAX_PATH * sizeof(WCHAR);
 ULONG uIndex = 0;
 BOOLEAN bRet = FALSE;

 // Open the device list, querying all devices
 if (!DevicePowerOpen(0)) 
  {
   printf("ERROR: The device database failed to initialize.\n");
   return FALSE;
  }

 // Enumerate the device list, searching for devices that support 
 // waking from either the S1 or S2 sleep state and are currently 
 // present in the system, and not devices that have drivers 
 // installed but are not currently attached to the system, such as 
 // in a laptop docking station.

 pRetBuf = (LPWSTR)LocalAlloc(LPTR, bufSize);

 while (NULL != pRetBuf && 
        0 != (bRet = DevicePowerEnumDevices(uIndex,
           DEVICEPOWER_FILTER_DEVICES_PRESENT,
           PDCAP_WAKE_FROM_S1_SUPPORTED|PDCAP_WAKE_FROM_S2_SUPPORTED,
           (PBYTE)pRetBuf,
           &bufSize)))
  {
   printf("Device name: %S\n", pRetBuf);

   // For the devices we found that have support for waking from 
   // S1 and S2 sleep states, disable them from waking the system.
   bRet = (0 != DevicePowerSetDeviceState((LPCWSTR)pRetBuf, 
                                  DEVICEPOWER_CLEAR_WAKEENABLED, 
                                  NULL));

   if (0 != bRet) 
    {
     printf("Warning: Failed to set device state.\n");
    }
   uIndex++;
  }

 // Close the device list.
 DevicePowerClose();
 if (pRetBuf!= NULL) LocalFree(pRetBuf);
 pRetBuf = NULL;

 return TRUE;
}
```



在此範例中，裝置清單會開啟一次，並關閉一次。 如果未呼叫 [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) 和 [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) 函式，則裝置清單會在每次呼叫 [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) 和 [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate)時開啟和關閉。 藉由使用 **DevicePowerOpen** 和 **DevicePowerClose** ，我們將開啟裝置清單兩次不必要的時間儲存。

 

 



