---
description: 針對 Windows 7，Windows 可攜式裝置支援裝置服務事件的下列屬性。 這些屬性是由 IPortableDeviceServiceCapabilities：： GetEventAttributes 方法傳回。
ms.assetid: 2c71c3ec-842b-44f7-b127-5750883b33ba
title: '事件屬性 (PortableDevice) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 68a5964a4f64899d4aa116002b1feb14ce360498
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999077"
---
# <a name="event-attributes-portabledeviceh"></a>事件屬性 (PortableDevice) 

針對 Windows 7，Windows 可攜式裝置支援裝置服務事件的下列屬性。 這些屬性是由 [**IPortableDeviceServiceCapabilities：： GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) 方法傳回。




| 屬性                             | VarType         | Description                                                                                                              |
|---------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ 事件 \_ 屬性 \_ 名稱**       | **VT \_ LPWSTR**  | 字串，指定事件的腳本易記名稱。 有效字元為英數位元 \[ a-zA-Z0-9 \] 和 ' \_ '。 |
| **WPD \_ 事件 \_ 屬性 \_ 選項**    | **VT \_ 不明** | 包含事件選項的 [**IPortableDeviceValues**](iportabledevicevalues.md) 。                               |
| **WPD \_ 事件 \_ 屬性 \_ 參數** | **VT \_ 不明** | 包含事件參數的 [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) 。              |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性和屬性**](properties-and-attributes.md)
</dt> </dl>

 

 




