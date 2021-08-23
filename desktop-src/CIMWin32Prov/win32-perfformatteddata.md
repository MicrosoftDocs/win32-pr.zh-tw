---
description: 預先安裝的計算資料類別的抽象基類。
ms.assetid: 4eb6ad42-0f68-44f4-be19-095c51b4b1b6
ms.tgt_platform: multiple
title: Win32_PerfFormattedData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PerfFormattedData
- Win32_PerfFormattedData.Caption
- Win32_PerfFormattedData.Description
- Win32_PerfFormattedData.Name
- Win32_PerfFormattedData.Frequency_Object
- Win32_PerfFormattedData.Frequency_PerfTime
- Win32_PerfFormattedData.Frequency_Sys100NS
- Win32_PerfFormattedData.Timestamp_Object
- Win32_PerfFormattedData.Timestamp_PerfTime
- Win32_PerfFormattedData.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: 55a765102d5fcc40caff41a7fa68184afea114838152dd84157d506a62c15da5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020136"
---
# <a name="win32_perfformatteddata-class"></a>Win32 \_ PerfFormattedData 類別

預先安裝的計算資料類別的抽象基類。 這類類別的範例為 [**Win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk**](../wmisdk/retrieving-raw-and-formatted-performance-data.md)。 這些類別包含高效能[格式化效能 Data Provider](../wmisdk/formatted-performance-data-provider.md)所提供的計算值。

下列語法簡化自 MOF 程式碼，並顯示所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[abstract, AMENDMENT]
class Win32_PerfFormattedData : Win32_Perf
{
  string Caption;
  string Description;
  string Name;
  uint64 Frequency_Object;
  uint64 Frequency_PerfTime;
  uint64 Frequency_Sys100NS;
  uint64 Timestamp_Object;
  uint64 Timestamp_PerfTime;
  uint64 Timestamp_Sys100NS;
};
```

## <a name="members"></a>成員

**Win32 \_ PerfFormattedData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ PerfFormattedData** 類別具有這些屬性。

<dl> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) 
</dt> </dl>

統計資料或度量的簡短文字描述。

這個屬性繼承自 [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

統計資料或度量的文字描述。

這個屬性繼承自 [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)。

</dd> <dt>

**Frequency \_ 物件**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

**Timestamp \_ 物件** 屬性之每秒刻度的頻率。 當子歸類時，提供者會定義這個屬性。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

這個屬性繼承自 [**Win32 \_ Perf**](win32-perf.md)。

</dd> <dt>

**頻率 \_ PerfTime**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

**Frequency \_ PerfTime** 屬性每秒的頻率（以刻度為單位）。 您可以藉由呼叫 Windows 函數 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)來取得值。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

這個屬性繼承自 [**Win32 \_ Perf**](win32-perf.md)。

</dd> <dt>

**頻率 \_ Sys100NS**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

**時間戳記 \_ Sys100NS** 屬性 (10000000) 的每秒刻度頻率。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

這個屬性繼承自 [**Win32 \_ Perf**](win32-perf.md)。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 
</dt> </dl>

統計資料或度量已知的標籤。 子類別化時，可以將這個屬性覆寫為索引鍵屬性。

這個屬性繼承自 [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)。

</dd> <dt>

**Timestamp \_ 物件**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件定義的時間戳記。 提供者會定義他的屬性。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

這個屬性繼承自 [**Win32 \_ Perf**](win32-perf.md)。

</dd> <dt>

**時間戳記 \_ PerfTime**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

High 效能計數器時間戳記。 您可以藉由呼叫 Windows 函數 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)來取得值。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

這個屬性繼承自 [**Win32 \_ Perf**](win32-perf.md)。

</dd> <dt>

**時間戳記 \_ Sys100NS**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

100毫微秒單位的時間戳記值。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

這個屬性繼承自 [**Win32 \_ Perf**](win32-perf.md)。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ PerfFormattedData** 類別是衍生自 [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)的 [**win32 \_ Perf**](win32-perf.md)。 類別可在 **根 \\ cimv2** 命名空間中找到。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                             |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>WmiPerfInst.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ 效能**](win32-perf.md)
</dt> <dt>

[效能計數器類別](performance-counter-classes.md)
</dt> <dt>

[存取 WMI 預先安裝的效能類別](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[WMI 工作：效能監視](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[存取腳本中的效能資料](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
