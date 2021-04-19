---
description: 針對 Windows 7，Windows 可攜式裝置支援裝置服務的下列方法屬性。 這些屬性是由 IPortableDeviceServiceCapabilities：： GetMethodAttributes 方法傳回。
ms.assetid: b920e037-7737-4a18-b4f1-5c59e0a857dd
title: '方法屬性 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Method
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: fe638bcd0d87af7b16bfb4f202f21cea97908fcd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998774"
---
# <a name="method-attributes"></a>方法屬性

針對 Windows 7，Windows 可攜式裝置支援裝置服務的下列方法屬性。 這些屬性是由 [**IPortableDeviceServiceCapabilities：： GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) 方法傳回。




| 屬性                                      | VarType         | Description                                                                                                               |
|------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ 方法 \_ 屬性 \_ 存取**             | **VT \_ CLSID**   | 需要的方法存取。                                                                                               |
| **WPD \_ 方法 \_ 屬性 \_ 相關聯的 \_ 格式** | **VT \_ CLSID**   | 與方法相關聯的格式，如果沒有相關聯的格式，則為 **GUID \_ Null** 。                                |
| **WPD \_ 方法 \_ 屬性 \_ 名稱**               | **VT \_ LPWSTR**  | 字串，指定方法的腳本易記名稱。 有效字元為英數位元 \[ a-zA-Z0-9 \] 和 ' \_ '。 |
| **WPD \_ 方法 \_ 屬性 \_ 參數**         | **VT \_ 不明** | 包含方法參數的 [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) 介面。    |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性和屬性**](properties-and-attributes.md)
</dt> </dl>

 

 




