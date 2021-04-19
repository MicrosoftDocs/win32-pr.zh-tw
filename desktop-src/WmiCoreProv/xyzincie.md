---
description: 包含在照明上的國際委員會 (CIE) XYZ 色彩空間顯示的座標。
ms.assetid: e44e8a5f-005d-4d58-84e3-135d4e396086
title: XYZinCIE 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- XYZinCIE
- XYZinCIE.X
- XYZinCIE.Y
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: ba7f781a83f3e6ba5aa4683003386a0478d65088
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992081"
---
# <a name="xyzincie-class"></a>XYZinCIE 類別

**XYZinCIE** WMI 類別包含在照明 (CIE) XYZ 色彩空間的國際委員會顯示器座標。

## <a name="syntax"></a>語法

``` syntax
class XYZinCIE : WmiMonitorColorCharacteristics
{
  uint16 X;
  uint16 Y;
};
```

## <a name="members"></a>成員

**XYZinCIE** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**XYZinCIE** 類別具有這些屬性。

<dl> <dt>

**X**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

X 座標。

</dd> <dt>

**Y**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

Y 座標。

</dd> </dl>

## <a name="remarks"></a>備註

[**WmiMonitorColorCharacteristics**](wmimonitorcolorcharacteristics.md)類別包含 **XYZinCIE** 類別的內嵌實例，用以描述監視的色彩特性。

若要根據 x 和 y 值計算 z 座標，請使用 \| \| (x，y，z) \| \| = 1 的關聯性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 命名空間<br/>                | 根 \\ wmi<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




