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
# <a name="using-the-device-power-api"></a><span data-ttu-id="8ab34-103">使用裝置電源 API</span><span class="sxs-lookup"><span data-stu-id="8ab34-103">Using the Device Power API</span></span>

<span data-ttu-id="8ab34-104">使用裝置電來源程式設計專案來管理裝置在系統處於睡眠狀態時的執行方式。</span><span class="sxs-lookup"><span data-stu-id="8ab34-104">Use the Device Power programming elements to manage the way devices perform while the system is in a sleep state.</span></span>

## <a name="opening-and-closing-the-device-list"></a><span data-ttu-id="8ab34-105">開啟和關閉裝置清單</span><span class="sxs-lookup"><span data-stu-id="8ab34-105">Opening and closing the device list</span></span>

<span data-ttu-id="8ab34-106">開啟和關閉裝置清單在 CPU 時間方面是成本高昂的流程。</span><span class="sxs-lookup"><span data-stu-id="8ab34-106">Opening and closing the device list is a costly process in terms of CPU time.</span></span> <span data-ttu-id="8ab34-107">只有當應用程式需要多次查詢裝置清單時，才需要執行這項作業的 [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) 和 [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) 函數。</span><span class="sxs-lookup"><span data-stu-id="8ab34-107">The [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) and [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) functions that do this are only necessary if the application needs to query the device list multiple times.</span></span>

<span data-ttu-id="8ab34-108">如果呼叫 [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) ，則必須在裝置清單查詢完成時呼叫 [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) 。</span><span class="sxs-lookup"><span data-stu-id="8ab34-108">If [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) is called, [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) must be called when device-list queries are complete.</span></span> <span data-ttu-id="8ab34-109">如果 **DevicePowerOpen** 已明確開啟 [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices)和 [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) ，則不會關閉該裝置清單。</span><span class="sxs-lookup"><span data-stu-id="8ab34-109">[**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) and [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) will not close the device list if it has been explicitly opened by **DevicePowerOpen**.</span></span>

## <a name="enumerating-devices"></a><span data-ttu-id="8ab34-110">列舉裝置</span><span class="sxs-lookup"><span data-stu-id="8ab34-110">Enumerating devices</span></span>

<span data-ttu-id="8ab34-111">[**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices)函式會偵測裝置清單是否開啟，如果不是，則會開啟該清單。</span><span class="sxs-lookup"><span data-stu-id="8ab34-111">The [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) function detects whether the device list is open, and if not, opens it.</span></span> <span data-ttu-id="8ab34-112">**DevicePowerEnumDevices** 會根據指定的搜尋準則來列舉裝置。</span><span class="sxs-lookup"><span data-stu-id="8ab34-112">**DevicePowerEnumDevices** enumerates the devices based on the specified search criteria.</span></span> <span data-ttu-id="8ab34-113">如果裝置已開啟裝置清單，則會在函式傳回之前關閉。</span><span class="sxs-lookup"><span data-stu-id="8ab34-113">If the device list was opened by the function, it is closed before the function returns.</span></span>

## <a name="enabling-and-disabling-a-device-from-waking-the-system"></a><span data-ttu-id="8ab34-114">啟用及停用裝置，使其無法喚醒系統</span><span class="sxs-lookup"><span data-stu-id="8ab34-114">Enabling and disabling a device from waking the system</span></span>

<span data-ttu-id="8ab34-115">[**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate)函式類似于 [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices)，會偵測裝置清單是否為開啟狀態，如果不是，則會開啟該功能。</span><span class="sxs-lookup"><span data-stu-id="8ab34-115">The [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) function, similar to [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices), detects whether the device list is open, and if not, opens it.</span></span> <span data-ttu-id="8ab34-116">**DevicePowerSetDeviceState** 接著會為指定的裝置設定指定的準則。</span><span class="sxs-lookup"><span data-stu-id="8ab34-116">**DevicePowerSetDeviceState** then sets the specified criteria for the specified device.</span></span> <span data-ttu-id="8ab34-117">如果裝置已開啟裝置清單，則會在函式傳回之前關閉。</span><span class="sxs-lookup"><span data-stu-id="8ab34-117">If the device list was opened by the function, it is closed before the function returns.</span></span>

## <a name="example-code"></a><span data-ttu-id="8ab34-118">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="8ab34-118">Example Code</span></span>

<span data-ttu-id="8ab34-119">下列範例示範如何使用裝置電源 API。</span><span class="sxs-lookup"><span data-stu-id="8ab34-119">The following example demonstrates the use of the Device Power API.</span></span>


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



<span data-ttu-id="8ab34-120">在此範例中，裝置清單會開啟一次，並關閉一次。</span><span class="sxs-lookup"><span data-stu-id="8ab34-120">In this example the device list is opened once, and closed once.</span></span> <span data-ttu-id="8ab34-121">如果未呼叫 [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) 和 [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) 函式，則裝置清單會在每次呼叫 [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) 和 [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate)時開啟和關閉。</span><span class="sxs-lookup"><span data-stu-id="8ab34-121">If the [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) and [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) functions were not called, the device list would have been opened and closed by each call to [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) and [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate).</span></span> <span data-ttu-id="8ab34-122">藉由使用 **DevicePowerOpen** 和 **DevicePowerClose** ，我們將開啟裝置清單兩次不必要的時間儲存。</span><span class="sxs-lookup"><span data-stu-id="8ab34-122">By using **DevicePowerOpen** and **DevicePowerClose** we saved opening the device list two unnecessary times.</span></span>

 

 



