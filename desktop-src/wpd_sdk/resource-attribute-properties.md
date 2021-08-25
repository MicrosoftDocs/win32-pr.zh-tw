---
description: Windows可攜式裝置支援下列資源屬性內容。
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
ms.openlocfilehash: 956cd349089afb00a1350bf32e8f06acd5747599f6d5a731e4bf5d8dd1c96295
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928068"
---
# <a name="resource-attribute-properties"></a>資源屬性屬性

Windows可攜式裝置支援下列資源屬性內容。



| 屬性                                    | VarType         | 描述                                                                                                                                                               |
|---------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ 資源 \_ 屬性 \_ 資源 \_ 金鑰** | **VT \_ 不明** | 這是包含單一值的 [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) ，這是用來識別資源的索引鍵。                     |
| **WPD \_ 資源 \_ 屬性 \_ 格式**        | **VT \_ CLSID**   | 指定資源格式的 GUID 值。 請參閱[物件格式](object-format-guids.md)，以取得 Windows 可攜式裝置所定義的格式清單。 |
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

 

 




