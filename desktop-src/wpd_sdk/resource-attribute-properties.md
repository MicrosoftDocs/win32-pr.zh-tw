---
description: Windows 可攜式裝置支援下列資源屬性內容。
ms.assetid: 9b90db8a-e833-48cf-b484-70ac5ac32a76
title: '資源屬性屬性 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Resource
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 64f4f394fcd91d50f323a8e46a9556daa6a8dbff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000952"
---
# <a name="resource-attribute-properties"></a>資源屬性屬性

Windows 可攜式裝置支援下列資源屬性內容。



| 屬性                                    | VarType         | Description                                                                                                                                                               |
|---------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ 資源 \_ 屬性 \_ 資源 \_ 金鑰** | **VT \_ 不明** | 這是包含單一值的 [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) ，這是用來識別資源的索引鍵。                     |
| **WPD \_ 資源 \_ 屬性 \_ 格式**        | **VT \_ CLSID**   | 指定資源格式的 GUID 值。 如需 Windows 可攜式裝置所定義之格式的清單，請參閱 [物件格式](object-format-guids.md) 。 |
| **WPD \_ 資源 \_ 屬性 \_ 總 \_ 大小**   | **VT \_ UI8**     | 資源資料的大小總計（以位元組為單位）。                                                                                                                            |



 

## <a name="remarks"></a>備註

這些屬性是由 [**IPortableDeviceResources：： GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes) 方法傳回。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPortableDeviceResources::GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes)
</dt> <dt>

[**WPD 屬性和屬性**](properties-and-attributes.md)
</dt> </dl>

 

 




