---
description: 所有具體原始效能計數器類別的抽象基類。
ms.assetid: 3c457996-54d9-4425-8a57-15176d027e3a
ms.tgt_platform: multiple
title: Win32_PerfRawData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PerfRawData
- Win32_PerfRawData.Caption
- Win32_PerfRawData.Description
- Win32_PerfRawData.Name
- Win32_PerfRawData.Frequency_Object
- Win32_PerfRawData.Frequency_PerfTime
- Win32_PerfRawData.Frequency_Sys100NS
- Win32_PerfRawData.Timestamp_Object
- Win32_PerfRawData.Timestamp_PerfTime
- Win32_PerfRawData.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: f6500706b7e2298ad98aa894e33436b0306e406e003562fcb6533265abd0b2be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020126"
---
# <a name="win32_perfrawdata-class"></a>Win32 \_ PerfRawData 類別

所有具體原始效能計數器類別的抽象基類。

若要顯示在 [系統監視器] 中，效能計數器類別必須新增至根 \\ cimv2 命名空間，並衍生自 **Win32 \_ PerfRawData**。 這些類別中的資料是由高效能 [效能計數器提供者](../wmisdk/performance-counter-provider.md)所提供。

從 **Win32 \_ PerfRawData** 衍生類別時，會繼承下列屬性：

-   **時間戳記 \_ PerfTime**
-   **時間戳記 \_ Sys100NS**
-   **Timestamp \_ 物件**
-   **頻率 \_ PerfTime**
-   **頻率 \_ Sys100NS**
-   **Frequency \_ 物件**

在每個案例中，屬性都必須由提供者填寫，否則無法在系統監視器中顯示該類別。 這些屬性是用來計算效能資料取用者的計數器類型公式。

下列語法簡化自 MOF 程式碼，並顯示所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[abstract, AMENDMENT]
class Win32_PerfRawData : Win32_Perf
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

**Win32 \_ PerfRawData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ PerfRawData** 類別具有這些屬性。

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

**Win32 \_ PerfRawData** 類別是衍生自 [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)的 [**win32 \_ Perf**](win32-perf.md)。

所有衍生自 Win32 效能的類別都是設計來搭配 [*複習*](../wmisdk/gloss-r.md)物件使用。 [**\_**](win32-perf.md) 如需如何以 c + + 程式設計語言建立及使用重新整理程式物件的詳細資訊，請參閱使用 [c + + 存取效能資料](../wmisdk/accessing-performance-data-in-c--.md)。 如需如何在腳本程式設計語言中建立及使用重新整理程式物件的詳細資訊，請參閱 [在腳本中重新整理 WMI 資料](../wmisdk/refreshing-wmi-data-in-scripts.md)。

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

 

 
