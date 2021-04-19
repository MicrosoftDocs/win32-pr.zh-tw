---
description: 針對 Windows 7，Windows 可攜式裝置支援裝置服務的方法和事件的下列參數屬性。
ms.assetid: a7708c60-758a-4fb6-8ef9-074ecdc9cf60
title: '參數屬性 (PortableDevice) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Parameter
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 113b2b35a5b6e61cd2cc1d3666d1a13fbade5ec7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982259"
---
# <a name="parameter-attributes"></a>參數屬性

針對 Windows 7，Windows 可攜式裝置支援裝置服務的方法和事件的下列參數屬性。 這些方法會傳回這些屬性：

-   [**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes)
-   [**IPortableDeviceServiceCapabilities::GetEventParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventparameterattributes)




| 屬性                                            | VarType         | Description                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ 參數 \_ 屬性 \_ 預設 \_ 值**        | VT \_ *XXXX*      | 參數的預設值。                                                                                                                                                         |
| **WPD \_ 參數 \_ 屬性 \_ 列舉 \_ 元素** | **VT \_ 不明** | [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)介面，其中包含參數的列舉值。                                   |
| **WPD \_ 參數 \_ 屬性 \_ 表單**                  | **VT \_ UI4**     | 允許的有效參數值形式。                                                                                                                                                 |
| **WPD \_ 參數 \_ 屬性 \_ \_ 大小上限**             | **VT \_ UI8**     | 參數的大小上限（以位元組為單位）。                                                                                                                                               |
| **WPD \_ 參數 \_ 屬性 \_ 名稱**                  | **VT \_ LPWSTR**  | 字串，指定事件或方法參數的腳本易記名稱。 有效字元為英數位元 \[ a-zA-Z0-9 \] 和 ' \_ '。                                                 |
| **WPD \_ 參數 \_ 屬性 \_ 順序**                 | **VT \_ UI4**     | 以零為基底的參數順序索引，讓順序值0對應至第一個參數。                                                                                       |
| **WPD \_ 參數 \_ 屬性 \_ 範圍 \_ 最小值**            | VT \_ *XXXX*      | 表單 WPD \_ 參數 \_ 屬性 \_ 表單範圍之參數的最大值 \_ 。                                                                                                       |
| **WPD \_ 參數 \_ 屬性 \_ 範圍 \_ 最大值**            | VT \_ *XXXX*      | 表單 WPD \_ 參數 \_ 屬性 \_ 表單範圍之參數的最小值 \_ 。                                                                                                       |
| **WPD \_ 參數 \_ 屬性 \_ 範圍 \_ 步驟**           | VT \_ *XXXX*      | 表單 WPD \_ 參數 \_ 屬性 \_ 表單範圍的參數步驟值 \_ 。                                                                                                          |
| **WPD \_ 參數 \_ 屬性 \_ 正則 \_ 運算式**   | **VT \_ LPWSTR**  | 正則運算式，為表單 WPD \_ 參數 \_ 屬性 \_ 表單 \_ 正則 \_ 運算式的參數指定可接受的值。                                                      |
| **WPD \_ 參數 \_ 屬性 \_ 使用 \_ 類型**           | **VT \_ UI4**     | 整數，指定方法參數的使用方式，例如 in/out。有效的值為 [**WPD \_ 參數 \_ 使用 \_ 類型**](wpd-parameter-usage-types.md) 列舉類型。 |
| **WPD \_ 參數 \_ 屬性 \_ VARTYPE**               | **VT \_ UI4**     | 參數 VarType。                                                                                                                                                                      |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性和屬性**](properties-and-attributes.md)
</dt> </dl>

 

 




