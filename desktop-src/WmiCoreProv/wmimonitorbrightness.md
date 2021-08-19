---
description: 代表電腦監視器的亮度參數。
ms.assetid: 01fa3efc-2a1d-4405-989f-2c180842c6b9
title: WmiMonitorBrightness 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightness
- WmiMonitorBrightness.Active
- WmiMonitorBrightness.CurrentBrightness
- WmiMonitorBrightness.InstanceName
- WmiMonitorBrightness.Level
- WmiMonitorBrightness.Levels
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 10343b33e5bc1881440af9d13029913d470880289e71b4c7a33fb4748e56ef73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821519"
---
# <a name="wmimonitorbrightness-class"></a>WmiMonitorBrightness 類別

**WmiMonitorBrightness** WMI 類別代表電腦監視器的亮度參數。

## <a name="syntax"></a>語法

``` syntax
class WmiMonitorBrightness : MSMonitorClass
{
  boolean Active;
  uint8   CurrentBrightness;
          InstanceName;
  uint8   Level[];
  uint32  Levels;
};
```

## <a name="members"></a>成員

**WmiMonitorBrightness** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**WmiMonitorBrightness** 類別具有這些屬性。

<dl> <dt>

**使用中**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出目標監視器是否為作用中。

</dd> <dt>

**CurrentBrightness**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目前的亮度。 此值必須是從 *層級* 取得的值。

範例: 100

</dd> <dt>

InstanceName
</dt> <dd> <dl> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引鍵
</dt> </dl>

特定監視實例的名稱。

</dd> <dt>

**Level**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

包含可能的亮度層級的陣列。

範例： \[ 0，1，2，...，100 \] 。

</dd> <dt>

**層級**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

監視器支援的亮度等級總數，如 *層級* 所述。

範例：101

</dd> </dl>

## <a name="examples"></a>範例

如需在 PowerShell 中使用此類別的詳細資訊和程式碼範例，請參閱 [使用 Powershell 報告和設定監視亮度](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx)。

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

 

 




