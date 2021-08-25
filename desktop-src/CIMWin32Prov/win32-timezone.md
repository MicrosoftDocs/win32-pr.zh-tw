---
description: Win32 \_ 時區&\# 8194;WMI 類別代表執行 Windows 之電腦系統的時區資訊，其中包含轉換成日光節約時間轉換所需的變更。
ms.assetid: c1c7731e-768f-42ea-a36c-57b00df6848e
ms.tgt_platform: multiple
title: Win32_TimeZone 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TimeZone
- Win32_TimeZone.Caption
- Win32_TimeZone.Description
- Win32_TimeZone.SettingID
- Win32_TimeZone.Bias
- Win32_TimeZone.DaylightBias
- Win32_TimeZone.DaylightDay
- Win32_TimeZone.DaylightDayOfWeek
- Win32_TimeZone.DaylightHour
- Win32_TimeZone.DaylightMillisecond
- Win32_TimeZone.DaylightMinute
- Win32_TimeZone.DaylightMonth
- Win32_TimeZone.DaylightName
- Win32_TimeZone.DaylightSecond
- Win32_TimeZone.DaylightYear
- Win32_TimeZone.StandardBias
- Win32_TimeZone.StandardDay
- Win32_TimeZone.StandardDayOfWeek
- Win32_TimeZone.StandardHour
- Win32_TimeZone.StandardMillisecond
- Win32_TimeZone.StandardMinute
- Win32_TimeZone.StandardMonth
- Win32_TimeZone.StandardName
- Win32_TimeZone.StandardSecond
- Win32_TimeZone.StandardYear
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 02b6d9d5c6100a652cf50096f5ef513fc164cfcfd2d8036e8444adc702459d1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827658"
---
# <a name="win32_timezone-class"></a>Win32 \_ 時區類別

**Win32 \_ 時區** [WMI 類別](../wmisdk/retrieving-a-class.md)代表執行 Windows 之電腦系統的時區資訊，其中包含轉換成日光節約時間轉換所需的變更。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_TimeZone : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  sint32 Bias;
  sint32 DaylightBias;
  uint32 DaylightDay;
  uint8  DaylightDayOfWeek;
  uint32 DaylightHour;
  uint32 DaylightMillisecond;
  uint32 DaylightMinute;
  uint32 DaylightMonth;
  string DaylightName;
  uint32 DaylightSecond;
  uint32 DaylightYear;
  uint32 StandardBias;
  uint32 StandardDay;
  uint8  StandardDayOfWeek;
  uint32 StandardHour;
  uint32 StandardMillisecond;
  uint32 StandardMinute;
  uint32 StandardMonth;
  string StandardName;
  uint32 StandardSecond;
  uint32 StandardYear;
};
```

## <a name="members"></a>成員

**Win32 \_ 時區** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ 時區** 類別具有這些屬性。

<dl> <dt>

**偏差**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 時間結構 \| [**時區 \_ \_ 資訊**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| 偏差」 ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( 「分鐘」 ) 
</dt> </dl>

本地時間轉譯的目前偏差。 偏差是國際標準時間 (UTC) 和本地時間之間的差異。 UTC 和本地時間之間的所有翻譯都是根據下列公式： UTC = 本地時間偏差。 這是必要屬性。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) 
</dt> </dl>

目前物件的簡短文字描述。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**DaylightBias**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 時間結構 \| [**時區 \_ \_ 資訊**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightBias」 ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( 「分鐘」 ) 
</dt> </dl>

在日光節約時間發生的本地時間轉譯期間所使用的偏差值。 如果未提供 **DaylightDay** 屬性的值，則會忽略這個屬性。 這個屬性的值會新增至 **偏差** 屬性，以形成日光節約時間所使用的偏差。 在大部分的時區中，此屬性的值為-60。

</dd> <dt>

**DaylightDay**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate.wyear \| wDay" ) 
</dt> </dl>

當此作業系統發生從標準時間到日光節約時間的轉換時， **DaylightMonth** 的 **DaylightDayOfWeek** 。

範例：如果轉換日 (**DaylightDayOfWeek**) 發生在星期日，則值 "1" 表示 **DaylightMonth** 的第一個星期日，"2" 表示第二個星期日，依此類推。 值 "5" 表示當月的最後一個 **DaylightDayOfWeek** 。

</dd> <dt>

**DaylightDayOfWeek**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate.wyear \| wDayOfWeek" ) 
</dt> </dl>

從標準時間到日光節約時間的轉換在作業系統上進行轉換時的星期幾。

<dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**星期日** (0) 


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**星期一** (1) 


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**星期二** (2) 


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**星期三** (3) 


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**星期四** (4) 


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**星期五** (5) 


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**星期六** (6) 


</dt> <dd></dd> </dl>

範例：1

</dd> <dt>

**DaylightHour**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate.wyear \| wHour" ) 
</dt> </dl>

從標準時間到日光節約時間的轉換在作業系統上進行轉換的一天中的小時。

範例：2

</dd> <dt>

**DaylightMillisecond**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate.wyear \| wMilliseconds" ) 
</dt> </dl>

從標準時間到日光節約時間的轉換在作業系統上進行轉換時的 **DaylightSecond** 毫秒。

</dd> <dt>

**DaylightMinute**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate.wyear \| wMinute" ) 
</dt> </dl>

從標準時間到日光節約時間的轉換在作業系統上進行轉換時的 **DaylightHour** 分鐘。

範例：59

</dd> <dt>

**DaylightMonth**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate.wyear \| wMonth" ) 
</dt> </dl>

從標準時間到日光節約時間的轉換發生在作業系統上的月份。

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

1 **月** (1) 


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

**二月** (2) 


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

3 **月** (3) 


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

**四月** (4) 


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

5 **月** (5) 


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

6 **月** (6) 


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

7 **月** (7) 


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

8 **月** (8) 


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

9 **月** (9) 


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

10 **月** (10) 


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

11 **月** (11) 


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

12 **月** (12) 


</dt> <dd></dd> </dl>

</dd> <dt>

**DaylightName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 時間結構 \| [**時區 \_ \_ 資訊**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightName" ) 
</dt> </dl>

當日光節約時間生效時，所要表示的時區。

範例： "EDT" (東部日光節約時間) 

</dd> <dt>

**DaylightSecond**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate.wyear \| wSecond" ) 
</dt> </dl>

從標準時間到日光節約時間的轉換在作業系統上進行轉換時， **DaylightMinute** 的第二個。

範例：59

</dd> <dt>

**DaylightYear**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate.wyear \| daylightdate.wyear" ) 
</dt> </dl>

日光節約時間生效的年份。 這個屬性不是必要的。

範例：1997

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目前物件的文字描述。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 
</dt> </dl>

已知目前物件的識別碼。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**StandardBias**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 時間結構 \| [**時區 \_ \_ 資訊**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardBias」 ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( 「分鐘」 ) 
</dt> </dl>

日光節約時間未生效時要使用的偏差值。 如果未提供 **StandardDay** 的值，則會忽略這個屬性。 這個屬性的值會加入至 **偏差** 屬性，以在標準時間內形成偏差。

範例：0

</dd> <dt>

**StandardDay**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate.wyear \| wDay" ) 
</dt> </dl>

當作業系統上的日光節約時間轉換成標準時間時， **StandardMonth** 的 **StandardDayOfWeek** 。

如果轉換日 (**StandardDayOfWeek**) 發生在星期日，則值 "1" 表示 **StandardMonth** 的第一個星期日，"2" 表示第二個星期日，依此類推。 值 "5" 表示當月的最後一個 **StandardDayOfWeek** 。

</dd> <dt>

**StandardDayOfWeek**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate.wyear \| wDayOfWeek" ) 
</dt> </dl>

當作業系統上的日光節約時間轉換為標準時間時，該周的第幾天。

<dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**星期日** (0) 


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**星期一** (1) 


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**星期二** (2) 


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**星期三** (3) 


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**星期四** (4) 


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**星期五** (5) 


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**星期六** (6) 


</dt> <dd></dd> </dl>

</dd> <dt>

**StandardHour**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate.wyear \| wHour" ) 
</dt> </dl>

從日光節約時間轉換到標準時間時，在作業系統上進行轉換的一天中的小時。

範例：11

</dd> <dt>

**StandardMillisecond**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate.wyear \| wMilliseconds" ) 
</dt> </dl>

從日光節約時間轉換到標準時間時的 **StandardSecond** 毫秒。

</dd> <dt>

**StandardMinute**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate.wyear \| wMinute" ) 
</dt> </dl>

從日光節約時間轉換到標準時間的 **StandardDay** 時，在作業系統上進行轉換時的分鐘數。

範例：59

</dd> <dt>

**StandardMonth**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate.wyear \| wMonth" ) 
</dt> </dl>

從日光節約時間轉換到標準時間時，在作業系統上進行轉換的月份。

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

1 **月** (1) 


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

**二月** (2) 


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

3 **月** (3) 


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

**四月** (4) 


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

5 **月** (5) 


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

6 **月** (6) 


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

7 **月** (7) 


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

8 **月** (8) 


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

9 **月** (9) 


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

10 **月** (10) 


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

11 **月** (11) 


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

12 **月** (12) 


</dt> <dd></dd> </dl>

</dd> <dt>

**StandardName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardName" ) 
</dt> </dl>

標準時間生效時所表示的時區名稱。

範例： "EST" (東部標準時間) 

</dd> <dt>

**StandardSecond**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate.wyear \| wSecond" ) 
</dt> </dl>

**StandardMinute** 從日光節約時間轉換到標準時間時，在作業系統上進行轉換的第二個。

範例：59

</dd> <dt>

**StandardYear**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate.wyear \| daylightdate.wyear" ) 
</dt> </dl>

當標準時間生效時的年份。 這個屬性不是必要的。

範例：1997

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ 時區** 類別衍生自 [**CIM \_ 設定**](cim-setting.md)。

撰寫 WMI 查詢時，您不能使用標準日期時間格式，例如10/18/2002。 相反地，您必須將查詢中使用的任何日期轉換為 UTC 格式。 這需要兩個步驟： 1) 您必須判斷您的時區和格林威治標準時間之間的時差 (差異（以分鐘為) 單位），以及 2) 您必須將10/18/2002 轉換成 UTC 值。

判斷與格林尼治平均時間的位移

無可否認地，WMI 讓您難以處理日期和時間;幸運的是，WMI 至少能讓您輕鬆判斷您的時區和格林威治標準時間之間的時差。 WMI 類別 Win32 \_ 時區包含會傳回 GMT 位移的屬性偏差。


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 Wscript.Echo "Offset: "& objTimeZone.Bias
Next
```



將日期轉換為 UTC 值

決定 GMT 時差之後，您必須將標準日期（例如10/18/2002）轉換成 UTC 日期。 若要將標準日期轉換成 UTC 日期，您可以使用 VBScript 日期函數（例如年、月和日）來隔離組成 UTC 日期的個別元件。 當這些元件有個別值之後，您可以使用與任何其他字串值相同的方式來串連它們。 UTC 日期會視為字串，因為 GMT 位移必須附加至結尾。 如果日期顯示為數字，則此值為：

`20011018113047.000000-480`

為了清楚) 起見，會錯誤地將錯誤地視為數學方程式 (括弧：

`(20011018113047.000000) - (480)`

例如，在日期10/18/2002 中，個別的元件為：

-   年：2002
-   月：10
-   Day：18

腳本必須結合這三個值，字串 "113047.000000" (代表時間，包括毫秒) ，以及用來衍生 UTC 日期的 GMT 位移。 例如，為了清楚) 起見，請再次加入 (括弧：

`(2002) & (10) & (18) & (113047.000000) & (-480)`

> [!Note]  
> 您可以使用 VBScript 函數 Hour、Minute 和 Second 來轉換 UTC 日期的時間部分。 因此，時間 11:30:47 A.M。 會轉換成113047。

 

有一個複雜的因素。 此月份必須在字串中佔用5和6的位置;day 必須花費7和8的位置。 這在第10天和第18天都沒問題。 但是，您要如何取得7月5日 (的第5天) 來填滿必要的位置呢？ 答案是將前置零加到每個值，因此將7變更為07，以及5到05。

若要這樣做，請使用 VBScript Len 函數來檢查月和日) 的字元數 (的長度。 如果長度為 1 (表示只有一個字元) ，請新增前置零。 因此：


```VB
If Len(dtmMonth) = 1 Then
    dtmMonth = "0" & dtmMonth
End If
```



## <a name="examples"></a>範例

下列 VBScript 範例會將目前的日期轉換為 UTC 日期。


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 strBias = objTimeZone.Bias
Next

dtmCurrentDate = Date
dtmTargetDate = Year(dtmCurrentDate)

dtmMonth = Month(dtmCurrentDate)
If Len(dtmMonth) = 1 Then
 dtmMonth = "0" & dtmMonth
End If

dtmTargetDate = dtmTargetDate & dtmMonth

dtmDay = Day(dtmCurrentDate)
If Len(dtmDay) = 1 Then
 dtmDay = "0" & dtmDay
End If

dtmTargetDate = dtmTargetDate & dtmDay & "000000.000000"
dtmTargetDate = dtmTargetDate & Cstr(strBias)
```



下列 VBScript 會 sampledetermines GMT 位移，然後將指定的目前日期轉換 (在此案例中，10/18/2002) 為 UTC 日期時間格式。 轉換日期之後，該值會用來搜尋電腦，並傳回在10/18/2002 之後建立的所有資料夾清單。


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 strBias = objTimeZone.Bias
Next

dtmCurrentDate = "10/18/2002"
dtmTargetDate = Year(dtmCurrentDate)

dtmMonth = Month(dtmCurrentDate)
If Len(dtmMonth) = 1 Then
 dtmMonth = "0" & dtmMonth
End If

dtmTargetDate = dtmTargetDate & dtmMonth

dtmDay = Day(dtmCurrentDate)
If Len(dtmDay) = 1 Then
 dtmDay = "0" & dtmDay
End If

dtmTargetDate = dtmTargetDate & dtmDay & "000000.000000"
dtmTargetDate = dtmTargetDate & Cstr(strBias)

Set colFolders = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE CreationDate < '" & _
 dtmtargetDate & "'")
For Each objFolder in colFolders
 Wscript.Echo objFolder.Name
Next
```



下列 VBScript 程式碼範例會顯示 Win32 \_ 時區實例的設定。


```VB
Dim arDayOrWeek(7)
arDayOrWeek(0) = "Sunday"
arDayOrWeek(1) = "Monday"
arDayOrWeek(2) = "Tuesday"
arDayOrWeek(3) = "Wednesday"
arDayOrWeek(4) = "Thursday"
arDayOrWeek(5) = "Friday"
arDayOrWeek(6) = "Saturday"

Dim arMonth(13)
arMonth(1) = "January"
arMonth(2) = "Feburary"
arMonth(3) = "March"
arMonth(4) = "April"
arMonth(5) = "May"
arMonth(6) = "June"
arMonth(7) = "July"
arMonth(8) = "August"
arMonth(9) = "September"
arMonth(10) = "October"
arMonth(11) = "November"
arMonth(12) = "December"

strComputer = "."
wmiQuery = "Select * from Win32_TimeZone"
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")
Set colItems = objWMIService.ExecQuery(wmiQuery)

For Each objItem in colItems
    WScript.Echo "Day of Week setting is: " _
        & objItem.dayLightDayOfWeek _
        & " which is: " & arDayOrWeek(objItem.DaylightDayOfWeek)
    WScript.Echo "Hour: " & objItem.DaylightHour 
    WScript.Echo "Month: " & objItem.DaylightMonth _
        & " which is: " & arMonth(objItem.DaylightMonth )
    WScript.Echo "Description: " & objItem.DaylightName 
    WScript.Echo "The transition from DLS to Standard occurs: " 
    WScript.Echo "Day of Week setting is: " _
        & objItem.standardDayOfWeek _
        & " which is: " & arDayOrWeek(objItem.DaylightDayOfWeek)
    WScript.Echo "Hour: " & objItem.StandardHour 
    WScript.Echo "Month: " & objItem.StandardMonth _ 
        & " which is: " & arMonth(objItem.StandardMonth )
    WScript.Echo "Description: " & objItem.StandardName 
Next

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 設定**](cim-setting.md)
</dt> <dt>

[作業系統類別](./operating-system-classes.md)
</dt> <dt>

[**SWbemDateTime**](../wmisdk/swbemdatetime.md)
</dt> <dt>

[日期和時間格式](../wmisdk/date-and-time-format.md)
</dt> <dt>

[WMI 工作：日期和時間](../wmisdk/wmi-tasks--dates-and-times.md)
</dt> </dl>

 

 
