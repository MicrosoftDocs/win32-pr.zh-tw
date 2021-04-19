---
description: 表示支援之頻率範圍特性的容器。
ms.assetid: eb07c10b-8d92-40bb-8a93-ebc5db46cfd3
title: FrequencyRangeDescriptor 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FrequencyRangeDescriptor
- FrequencyRangeDescriptor.Origin
- FrequencyRangeDescriptor.MinVSyncNumerator
- FrequencyRangeDescriptor.MinVSyncDenominator
- FrequencyRangeDescriptor.MaxVSyncNumerator
- FrequencyRangeDescriptor.MaxVSyncDenominator
- FrequencyRangeDescriptor.MinHSyncNumerator
- FrequencyRangeDescriptor.MinHSyncDenominator
- FrequencyRangeDescriptor.MaxHSyncNumerator
- FrequencyRangeDescriptor.MaxHSyncDenominator
- FrequencyRangeDescriptor.ConstraintType
- FrequencyRangeDescriptor.ActiveWidth
- FrequencyRangeDescriptor.ActiveHeight
- FrequencyRangeDescriptor.MaxPixelRate
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: d18bee8a69fd8663ea54973d6e4e8219f5f74e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972629"
---
# <a name="frequencyrangedescriptor-class"></a>FrequencyRangeDescriptor 類別

**FrequencyRangeDescriptor** WMI 類別代表支援的頻率範圍之特性的容器。 這個類別的實例是 [**WmiMonitorListedFrequencyRanges**](wmimonitorlistedfrequencyranges.md)中 **MonitorFreqRanges** 陣列的元素。

## <a name="syntax"></a>語法

``` syntax
class FrequencyRangeDescriptor
{
  uint8  Origin;
  uint32 MinVSyncNumerator;
  uint32 MinVSyncDenominator;
  uint32 MaxVSyncNumerator;
  uint32 MaxVSyncDenominator;
  uint32 MinHSyncNumerator;
  uint32 MinHSyncDenominator;
  uint32 MaxHSyncNumerator;
  uint32 MaxHSyncDenominator;
  uint32 ConstraintType;
  uint32 ActiveWidth;
  uint32 ActiveHeight;
  uint32 MaxPixelRate;
};
```

## <a name="members"></a>成員

**FrequencyRangeDescriptor** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**FrequencyRangeDescriptor** 類別具有這些屬性。

<dl> <dt>

**ActiveHeight**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

現用影像的高度（以圖元為單位）。

</dd> <dt>

**ActiveWidth**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

現用影像的寬度（以圖元為單位）。

</dd> <dt>

**ConstraintType**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

頻率範圍的條件約束類型。

</dd> <dt>

**MaxHSyncDenominator**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

最大水準同步分母。

</dd> <dt>

**MaxHSyncNumerator**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

千赫茲 (KHz) 的最大水準同步分子。

</dd> <dt>

**MaxPixelRate**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

以赫茲為單位的最大圖元速率 (Hz) 。

</dd> <dt>

**MaxVSyncDenominator**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

最大垂直同步分母。

</dd> <dt>

**MaxVSyncNumerator**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

最大垂直同步分子，以赫茲 (Hz) 。

</dd> <dt>

**MinHSyncDenominator**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

水準同步分母的最小值。

</dd> <dt>

**MinHSyncNumerator**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

中的最小水準同步分子，千赫茲 (KHz) 。

</dd> <dt>

**MinVSyncDenominator**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

最低垂直同步分母。

</dd> <dt>

**MinVSyncNumerator**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

最小的垂直同步分子，以赫茲 (Hz) 。

</dd> <dt>

**起源**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

起源。

</dd> </dl>

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

 

 




