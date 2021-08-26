---
description: 效能計數器類別 Win32 \_ PerfRawData 和 win32 PerfFormattedData 的基類 \_ 。
ms.assetid: c754b619-a70f-4a56-8a43-2b36c8f8370b
ms.tgt_platform: multiple
title: Win32_Perf 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Perf
- Root\CIMV2.Win32_Perf.Caption
- Root\CIMV2.Win32_Perf.Description
- Root\CIMV2.Win32_Perf.Name
- Root\CIMV2.Win32_Perf.Frequency_Object
- Root\CIMV2.Win32_Perf.Frequency_PerfTime
- Root\CIMV2.Win32_Perf.Frequency_Sys100NS
- Root\CIMV2.Win32_Perf.Timestamp_Object
- Root\CIMV2.Win32_Perf.Timestamp_PerfTime
- Root\CIMV2.Win32_Perf.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: 356fdba0e2ebb7fb202f4996daa6b1929cd61fc67b028f67e8b041748306c0ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972238"
---
# <a name="win32_perf-class"></a>Win32 效能 \_ 類別

效能計數器類別 [**Win32 \_ PerfRawData**](win32-perfrawdata.md) 和 [**win32 \_ PerfFormattedData**](win32-perfformatteddata.md)的基類。

**Win32 \_Performance 會定義性能** 計數器類別的 [**CounterType**](../wmisdk/countertype-qualifier.md) 演算法中所使用的時間戳記和頻率屬性。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
[abstract, AMENDMENT]
class Win32_Perf : CIM_StatisticalInformation
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

**Win32 效能 \_** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 效能 \_** 類別具有這些屬性。

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

</dd> <dt>

**頻率 \_ PerfTime**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

**Frequency \_ PerfTime** 屬性每秒的頻率（以刻度為單位）。 您可以藉由呼叫 Windows 函數 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)來取得值。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

</dd> <dt>

**頻率 \_ Sys100NS**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

**時間戳記 \_ Sys100NS** 屬性 (10000000) 的每秒刻度頻率。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

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

</dd> <dt>

**時間戳記 \_ PerfTime**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

High 效能計數器時間戳記。 您可以藉由呼叫 Windows 函數 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)來取得值。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

</dd> <dt>

**時間戳記 \_ Sys100NS**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

100毫微秒單位的時間戳記值。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 效能 \_** 類別衍生自 [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                             |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                     |
| DLL<br/>                      | <dl> <dt>WmiPerfInst.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)
</dt> <dt>

[效能計數器類別](performance-counter-classes.md)
</dt> <dt>

[存取 WMI 預先安裝的效能類別](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[WMI 工作：效能監視](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[存取腳本中的效能資料](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
