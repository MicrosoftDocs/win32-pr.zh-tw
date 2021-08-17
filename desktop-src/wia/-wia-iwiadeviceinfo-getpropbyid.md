---
description: DeviceInfo 物件的 GetPropById 方法會使用裝置屬性的識別碼來傳回其值。
ms.assetid: 9c68e6af-446c-4750-89e6-70862b23b296
title: DeviceInfo. GetPropById 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.GetPropById
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: c996989661703c4a9c7416cd63904c376fdb7fcca3071d4558551bdd78470d3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208784"
---
# <a name="deviceinfogetpropbyid-method"></a>DeviceInfo. GetPropById 方法

[**DeviceInfo**](-wia-deviceinfo.md)物件的 **GetPropById** 方法會使用裝置屬性的識別碼來傳回其值。

## <a name="syntax"></a>語法


```JScript
retVal = DeviceInfo.GetPropById(
  Id
)
```



## <a name="parameters"></a>參數

<dl> <dt>

 \[ 中的識別碼\]
</dt> <dd>

類型： **[WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md)**

指定屬性的識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **VARIANT**

這個方法會傳回 *識別碼* 所指定之屬性的值。

## <a name="remarks"></a>備註

您可以使用這個方法，從識別碼中找出裝置屬性的值。 如需屬性識別碼的清單，請參閱 [WIA 屬性常數定義](-wia-wia-property-constant-definitions.md)。 如需 Windows 映像取得 (wia) 屬性本身的相關資訊，請參閱[wia 屬性常數](-wia-wia-property-constants.md)。

針對 Microsoft Visual Basic 的應用程式，請新增「Windows 影像取得1.01 型別程式庫」的參考。 該檔案中定義的下列常數適用于此方法：

``` syntax
const DeviceID = 2
const Manufacturer = 3
const Description = 4
const Type = 5
const Port = 6
const Name = 7
const Server = 8
const RemoteDevID = 9
const UIClassID = 10
```

## <a name="examples"></a>範例

下列範例示範如何使用 **GetPropById** 方法來取得屬性值。


```JScript
<SCRIPT LANGUAGE="VBScript">
const WIA_DIP_DEV_TYPE = 5
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim PropValue
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    PropValue = objDeviceInfo.GetPropById(WIA_DIP_DEV_TYPE)
Next
</SCRIPT>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (4.90 版或更新版本) </dt> </dl> |



 

 




