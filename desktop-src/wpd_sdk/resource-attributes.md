---
description: Windows 可攜式裝置支援下列資源屬性。
ms.assetid: 0cbf8777-5cea-4839-a4c3-366bb9e18488
title: '資源屬性 (PortableDevice .h) '
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
ms.openlocfilehash: 300add64d332dbc509bef6ec5bb2ad124f7a6b3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996259"
---
# <a name="resource-attributes"></a>資源屬性

Windows 可攜式裝置支援下列資源屬性。 下列方法會傳回這些屬性：

-   [**IPortableDeviceResources::GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfixedpropertyattributes)



| 屬性                                                  | VarType      | Description                                                                                                                                 |
|------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ 資源 \_ 屬性 \_ 可以 \_ 刪除**                  | **VT \_ BOOL** | 布林值，指定用戶端是否有權刪除資源。 如果不存在，則會假設為 false。                |
| **WPD \_ 資源 \_ 屬性 \_ 可以 \_ 讀取**                    | **VT \_ BOOL** | 布林值，指定用戶端是否有許可權開啟資源以進行讀取存取。 如果不存在，則會假設為 False。  |
| **WPD \_ 資源 \_ 屬性 \_ 可以 \_ 寫入**                   | **VT \_ BOOL** | 布林值，指定用戶端是否有許可權開啟資源以進行寫入存取。 如果不存在，則會假設為 false。 |
| **WPD \_ 資源 \_ 屬性 \_ 最佳 \_ 讀取 \_ 緩衝區 \_ 大小**  | **VT \_ UI4**  | 呼叫端應用於從資源緩衝讀取的建議緩衝區大小。                                                  |
| **WPD \_ 資源 \_ 屬性 \_ 最佳 \_ 寫入 \_ 緩衝區 \_ 大小** | **VT \_ UI4**  | 呼叫端應該在資源上用於緩衝寫入的建議緩衝區大小。                                                   |
| **WPD \_ 資源 \_ 屬性 \_ 總 \_ 大小**                  | **VT \_ UI8**  | 資源資料的大小總計（以位元組為單位）。                                                                                              |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性**](properties-and-attributes.md)
</dt> </dl>

 

 




