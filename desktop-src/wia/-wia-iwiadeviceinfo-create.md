---
description: DeviceInfo 物件的 Create 方法會連線到 DeviceInfo 物件所指定的 Windows 映像取得 (WIA) 裝置，並傳回代表該裝置的專案物件。
ms.assetid: 57f3698c-3f9f-4775-8b53-a65a5591aa3d
title: DeviceInfo. Create 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.Create
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 1efc36ea8794de4b64c9af616320b09d547f6490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974139"
---
# <a name="deviceinfocreate-method"></a>DeviceInfo. Create 方法

[**DeviceInfo**](-wia-deviceinfo.md)物件的 **Create** 方法會連線到 **DeviceInfo** 物件所指定的 Windows 映像取得 (WIA) 裝置，並傳回代表該裝置的 [**專案**](-wia-item.md)物件。

## <a name="syntax"></a>語法


```JScript
retVal = DeviceInfo.Create()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **IWiaDispatchItem**

這個方法會傳回代表所建立裝置的 [**專案**](-wia-item.md) 物件。

## <a name="remarks"></a>備註

列舉 [**裝置**](-wia-iwia-devices.md)集合之後，請使用 **create** 方法來建立與 WIA 硬體裝置的連接。 方法會傳回代表 (根專案) 之裝置的 [**專案**](-wia-item.md) 物件。

## <a name="examples"></a>範例

下列範例將示範 **Create** 方法的使用方式。


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objItem = objDeviceInfo.Create()
Next
</SCRIPT>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (4.90 版或更新版本) </dt> </dl> |



 

 




