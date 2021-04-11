---
description: 釋放 IPortableDeviceManager：： GetDevices 或 IPortableDeviceServiceManager：： GetDeviceServices 方法所取出的隨插即用 (PnP) 識別碼。
ms.assetid: b86f7733-81a3-4b60-bb7c-840c75f8d03f
title: 'FreePortableDevicePnPIDs 函式 (PortableDevice) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreePortableDevicePnPIDs
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 58bb5fa33007ed0e167226edf7078d08c2e5c3de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193943"
---
# <a name="freeportabledevicepnpids-function"></a>FreePortableDevicePnPIDs 函式

**FreePortableDevicePnPIDs** helper 函式會釋放 [**IPortableDeviceManager：： GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices)或 [**IPortableDeviceServiceManager：： GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices)方法所抓取的隨插即用 (PnP) 識別碼。

## <a name="syntax"></a>語法


```C++
void FreePortableDevicePnPIDs(
   LPWSTR *pPnPIDs,
   DWORD  cPnPIDs
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pPnPIDs* 
</dt> <dd>

要釋放的隨插即用 (PnP) 識別碼的陣列。

</dd> <dt>

*cPnPIDs* 
</dt> <dd>

*PPnPIDs* 參數所指定之陣列中的識別碼數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

應用程式會負責釋放它所配置的指標陣列。

## <a name="examples"></a>範例


```C++
// Allocate an array of LPWSTR pointers.
    LPWSTR* pPnpDeviceIDs = new LPWSTR[cPnpDeviceIDs];
if (pPnpDeviceIDs != NULL)
{
    hr = pPortableDeviceManager->;GetDevices(pPnpDeviceIDs, &cPnpDeviceIDs);
    if (SUCCEEDED(hr))
    {
        // Free all returned PnPDeviceID strings allocated by IPortableDeviceManager::GetDevices.
     FreePortableDevicePnPIDs(pPnpDeviceIDs, cPnpDeviceIDs);
     // Application is responsible for deleting the array of LPWSTR pointers.
     delete [] pPnpDeviceIDs;
     pPnpDeviceIDs = NULL;      
 }
} 
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                   |
| 標頭<br/>                   | <dl> <dt>PortableDevice。h</dt> </dl> |



 

 




