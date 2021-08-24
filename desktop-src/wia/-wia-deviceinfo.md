---
description: DeviceInfo 物件可讓您存取 Windows 映像取得的屬性 (WIA) 硬體裝置。
ms.assetid: b3cf153b-76f8-4822-8d88-331ab91a1116
title: DeviceInfo 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 69b34a97483a8a6ce231890454148c7948f63e4e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467175"
---
# <a name="deviceinfo-object"></a>DeviceInfo 物件

**DeviceInfo** 物件可讓您存取 Windows 映像取得的屬性 (WIA) 硬體裝置。 它也會透過其 [**建立**](-wia-iwiadeviceinfo-create.md) 方法，提供一個方法讓應用程式或腳本連線到裝置，並取得代表裝置的 [**專案**](-wia-item.md) 物件。 使用 [**Devices**](-wia-iwia-devices.md) 方法取得 **DeviceInfo** 物件的集合。

## <a name="members"></a>成員

**DeviceInfo** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**DeviceInfo** 物件有這些方法。



| 方法                                                 | 描述                                                                                                                                                                                                                                              |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**建立**](-wia-iwiadeviceinfo-create.md)           | **DeviceInfo** 物件的 [**Create**](-wia-iwiadeviceinfo-create.md)方法會連接到 **DEVICEINFO** 物件所指定的 WIA 裝置，並傳回代表該裝置的 [**專案**](-wia-item.md)物件。<br/> |
| [**GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md) | **DeviceInfo** 物件的 [**GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md)方法會使用裝置屬性的識別碼來傳回其值。<br/>                                                                                               |



 

### <a name="properties"></a>屬性

**DeviceInfo** 物件具有這些屬性。




| 屬性 | 存取類型 | Description | 
|----------|-------------|-------------|
| <a href="-wia-iwiadeviceinfo-id.md"><strong>Id</strong></a><br /> | 唯讀<br /> | 捕獲 WIA 硬體裝置的識別碼。 <br /> | 
| <a href="-wia-iwiadeviceinfo-manufacturer.md"><strong>製造商</strong></a><br /> | 唯讀<br /> | 抓取此硬體裝置的製造商名稱。<br /> | 
| <a href="-wia-iwiadeviceinfo-name.md"><strong>Name</strong></a><br /> | 唯讀<br /> | 顯示在 UI 中的 WIA 硬體裝置名稱。<br /> | 
| <a href="-wia-iwiadeviceinfo-port.md"><strong>連接埠</strong></a><br /> | 唯讀<br /> | 捕獲 WIA 硬體裝置所連接的埠。<br /> | 
| <a href="-wia-iwiadeviceinfo-type.md"><strong>類型</strong></a><br /> | 唯讀<br /> | 捕獲 WIA 硬體裝置的類型。 可能的值包括： <br /><ul><li>DigitalCamera</li><li>掃描器</li><li>StreamingVideo</li><li>預設</li></ul> | 
| <a href="-wia-iwiadeviceinfo-uiclsid.md"><strong>UIClsid</strong></a><br /> | 唯讀<br /> | 抓取此 WIA 硬體裝置製造商提供之使用者介面的類別識別碼。 值是 GUID 的字串表示。 <br /> | 




 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (4.90 版或更新版本) </dt> </dl> |



 

 




