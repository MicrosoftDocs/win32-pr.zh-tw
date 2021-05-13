---
description: Wia 物件的 Create 方法會連接到指定的 Windows 映像取得 (WIA) 裝置，並傳回代表該裝置的專案物件。
ms.assetid: c33c635a-159c-4ac3-8ad5-6f21a1986702
title: Wia. 建立方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.Create
- SafeWia.Create
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: d22d45e473cec1d5186c300f97cbdb4661237ab9
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841329"
---
# <a name="wiacreate-method"></a>Wia. 建立方法

[**Wia**](-wia-wia.md)物件的 **Create** 方法會連接到指定的 WINDOWS 映射取得 (Wia) 裝置，並傳回代表該裝置的 [**專案**](-wia-item.md)物件。

## <a name="syntax"></a>語法


```JScript
retVal = Wia.Create(
  Device
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*裝置* \[在\]
</dt> <dd>

類型： **VARIANT \***

指定要連接的 WIA 裝置。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **IWiaDispatchItem**

如果成功，這個方法會傳回代表 WIA 硬體裝置 (根專案) 的 [**專案**](-wia-item.md) 物件。

## <a name="remarks"></a>備註

*Device* 參數會指定 [**DeviceInfo**](-wia-deviceinfo.md)物件，方法是傳遞物件本身、其在集合物件中的索引，或其 [**Id**](-wia-iwiadeviceinfo-id.md)屬性的值。 傳遞 **Nothing** 以顯示允許使用者選取裝置的對話方塊。

## <a name="examples"></a>範例

下列 VBScript 範例示範如何使用 **Create** 方法。

第一個範例會將 [**DeviceInfo**](-wia-deviceinfo.md) 物件傳遞至 **Create** 方法。 請注意，傳遞物件的 [**Id**](-wia-iwiadeviceinfo-id.md) 屬性會導致完全相同的行為。


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objItem = objWia.Create(objDeviceInfo)
Next
</SCRIPT>
```



在下一個範例中，呼叫應用程式會將集合中 [**DeviceInfo**](-wia-deviceinfo.md) 物件的索引傳遞給 **Create** 方法。


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objItem
 
Set objWia = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For i = 0 To objDeviceInfoCollection.Count-1
    Set objItem = objWia.Create(i)
Next
</SCRIPT>
```



下一個範例會傳遞 **Nothing** 給 **Create** 方法，以顯示可讓使用者選取裝置的對話方塊。


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objItem
 
Set objWia = objWia.Create(Nothing)
</SCRIPT>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (4.90 版或更新版本) </dt> </dl> |



 

 




