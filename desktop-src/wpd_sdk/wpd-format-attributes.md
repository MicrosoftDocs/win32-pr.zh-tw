---
description: 針對 Windows 7，Windows 可攜式裝置在裝置服務上支援下列格式的屬性。 這些屬性是由 IPortableDeviceServiceCapabilities：： GetFormatAttributes 方法傳回。
ms.assetid: 53282e01-54da-4adf-8a09-2086d6398275
title: '格式屬性 (PortableDevice) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Format
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 559f731ec7d61007b05e4625ff67488b5ef482fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990657"
---
# <a name="format-attributes"></a>格式屬性

針對 Windows 7，Windows 可攜式裝置在裝置服務上支援下列格式的屬性。 這些屬性是由 [**IPortableDeviceServiceCapabilities：： GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) 方法傳回。




| **Attribute**                        | **VarType**    | **說明**                                                                                                           |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ 格式 \_ 屬性 \_ MIMETYPE** | **VT \_ LPWSTR** | MIME 類型的格式。                                                                                                     |
| **WPD \_ 格式 \_ 屬性 \_ 名稱**     | **VT \_ LPWSTR** | 字串，指定格式的腳本易記名稱。 有效字元為英數位元 \[ a-zA-Z0-9 \] 和 ' \_ '。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性和屬性**](properties-and-attributes.md)
</dt> </dl>

 

 




