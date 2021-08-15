---
description: DeviceInfo 物件的集合，代表安裝在電腦上的所有裝置。
ms.assetid: 2f124188-2b66-46cc-9b26-bfef3709a1af
title: Wia. Devices 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.Devices
- SafeWia.Devices
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: b6cf843d92b5ce2260578b653a1163526b22fb735c01542d772b2687ca890dc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208921"
---
# <a name="wiadevices-property"></a>Wia. Devices 屬性

[**DeviceInfo**](-wia-deviceinfo.md)物件的集合，代表安裝在電腦上的所有裝置。 唯讀。

> [!Note]  
> 這個集合是以0為基礎。

 

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Wia.Devices
```



## <a name="property-value"></a>屬性值

## <a name="examples"></a>範例

下列範例說明如何使用 **裝置** 集合來列舉系統上的裝置。


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
 
Set objWia = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    ! Do something with the DeviceInfo object
Next
</SCRIPT>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (4.90 版或更新版本) </dt> </dl> |



 

 




