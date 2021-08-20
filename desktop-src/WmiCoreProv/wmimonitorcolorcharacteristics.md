---
description: 代表 CIE 的國際委員會 (電腦監視器的) 色彩特性。
ms.assetid: 476aefae-11c0-46be-a2bb-83fbafd70421
title: WmiMonitorColorCharacteristics 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorColorCharacteristics
- WmiMonitorColorCharacteristics.Active
- WmiMonitorColorCharacteristics.Blue
- WmiMonitorColorCharacteristics.DefaultWhite
- WmiMonitorColorCharacteristics.Green
- WmiMonitorColorCharacteristics.InstanceName
- WmiMonitorColorCharacteristics.Red
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 1f0aa544b9c48e437259e313d80f443da85241b9d73e8ea820cdce099e38ddda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110850"
---
# <a name="wmimonitorcolorcharacteristics-class"></a>WmiMonitorColorCharacteristics 類別

**WmiMonitorColorCharacteristics** 類別代表照明上的國際委員會 (CIE 電腦監視器) 色彩特性。 資料對應至視頻電子產品標準關聯的 [色彩特性] 區塊中的資料 ([) 增強的擴充顯示器顯示識別資料 (E EDID) 結構。

## <a name="syntax"></a>語法

``` syntax
class WmiMonitorColorCharacteristics : MSMonitorClass
{
  boolean  Active;
  XYZinCIE Blue;
  XYZinCIE DefaultWhite;
  XYZinCIE Green;
  string   InstanceName;
  XYZinCIE Red;
};
```

## <a name="members"></a>成員

**WmiMonitorColorCharacteristics** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**WmiMonitorColorCharacteristics** 類別具有這些屬性。

<dl> <dt>

**使用中**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

表示使用中的監視器。

</dd> <dt>

**藍色**
</dt> <dd> <dl> <dt>

資料類型： **[ **XYZinCIE**](xyzincie.md)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

Blue 的 CIE 座標，由 [**XYZinCIE**](xyzincie.md) 類別的實例所表示。

</dd> <dt>

**DefaultWhite**
</dt> <dd> <dl> <dt>

資料類型： **[ **XYZinCIE**](xyzincie.md)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

預設的白色 CIE 座標。

</dd> <dt>

**綠色**
</dt> <dd> <dl> <dt>

資料類型： **[ **XYZinCIE**](xyzincie.md)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

CIE 以 [**XYZinCIE**](xyzincie.md) 類別的實例表示的綠色座標。

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

特定監視實例的名稱。

</dd> <dt>

**紅色**
</dt> <dd> <dl> <dt>

資料類型： **[ **XYZinCIE**](xyzincie.md)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

CIE 的紅色座標，由 [**XYZinCIE**](xyzincie.md) 類別的實例所表示。

</dd> </dl>

## <a name="remarks"></a>備註

Chromaticity 和白色點值會使用編碼格式來表示為小數數位。 此格式精確到千位位置（長度為10個位）。 最重要的位 (MSB) 代表 2 ^-1 和最不重要的位 (LSB) 分別代表 2 ^-10 個係數。 電子 EDID v1. x 結構中儲存值的有效位數應精確為實際值的 +/-0.005。

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

 

 




