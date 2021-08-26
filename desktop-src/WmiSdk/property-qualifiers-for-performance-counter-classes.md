---
description: 屬性限定詞會指定屬性所對應之效能計數器的相關資訊。
ms.assetid: f1761f71-af4e-4b89-aba7-b7f294c30ffc
ms.tgt_platform: multiple
title: 效能計數器類別的屬性限定詞
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 105bd010704364dc3865b2e704b3daeaafdb29a772d4f3b3fe036b88da2d43cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996178"
---
# <a name="property-qualifiers-for-performance-counter-classes"></a>效能計數器類別的屬性限定詞

屬性限定詞會指定屬性所對應之效能計數器的相關資訊。

-   [原始和格式化效能類別的屬性限定詞](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [原始效能類別的屬性限定詞](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [格式化效能類別的屬性限定詞](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [如何解讀屬性限定詞](#how-to-interpret-property-qualifiers)
-   [相關主題](#related-topics)

效能計數器是由 WMI [效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes) 效能計數器所代表之效能物件的一部分，而 WbemPerfClass 提供者會自動將這些限定詞附加至根 CIMv2 中的 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 類別和屬性 \\ 。

這項資訊適用于 performance 類別的所有實例。 具有永遠為 false 的 **布林** 值的某些限定詞可能不會出現在特定類別上。

## <a name="property-qualifiers-for-raw-and-formatted-performance-classes"></a>原始和格式化效能類別的屬性限定詞

下列清單會列出套用至類別中的屬性（從 [**win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 或 [**win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)衍生）的限定詞。

<dl> <dt>

<span id="CounterType"></span><span id="countertype"></span><span id="COUNTERTYPE"></span>[**CounterType**](countertype-qualifier.md)
</dt> <dd>

**sint32**

計數器類型列舉中的整數值，如 Winperf .h 或 Perflib 中所定義。 [**CounterType**](countertype-qualifier.md)限定詞表示用來計算屬性所代表計數器之系統監視器中所顯示值的公式或演算法。

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**
</dt> <dd>

**string**

效能計數器名稱，如效能資料協助程式 (PDH) 所指定。

</dd> <dt>

<span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**
</dt> <dd>

**sint32**

未使用。 一律包含0。

</dd> <dt>

<span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**
</dt> <dd>

**sint32**

未使用。 一律包含0。

</dd> </dl>

## <a name="property-qualifiers-for-raw-performance-classes"></a>原始效能類別的屬性限定詞

下列清單會列出套用至衍生自 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)之類別的所有屬性的限定詞。

<dl> <dt>

<span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**
</dt> <dd>

**boolean**

指出此屬性是否為要在清單方塊中使用的預設計數器。 效能計數器版本6.0 的此限定詞預設為 **False** ，因為它們不會提供資料給它。 如需相關資訊，請參閱 [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal)。

</dd> <dt>

<span id="DefaultScale"></span><span id="defaultscale"></span><span id="DEFAULTSCALE"></span>**DefaultScale**
</dt> <dd>

**sint32**

要用於顯示計數器的10乘冪。 若為零，估計的最大值為 10 ^ 0 或1。

</dd> <dt>

<span id="PerfDetail"></span><span id="perfdetail"></span><span id="PERFDETAIL"></span>[**PerfDetail**](perfdetail-qualifier.md)
</dt> <dd>

**sint32**

物件層級的知識。 未使用。 此值一律為100。

</dd> </dl>

## <a name="property-qualifiers-for-formatted-performance-classes"></a>格式化效能類別的屬性限定詞

下列清單會列出套用至衍生自 [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)之類別的所有屬性的限定詞。

<dl> <dt>

<span id="CookingType"></span><span id="cookingtype"></span><span id="COOKINGTYPE"></span>**CookingType**
</dt> <dd>

**string**

用來產生結果的公式類型。 每個計數器類型都會使用其他屬性限定詞來計算顯示為目前屬性值的結果。 **Counter**、 **PerfTimeStamp** 和 **PerfTimeFreq** 限定詞會對應到提供資料的原始類別中的屬性。

如需詳細資訊，請參閱 [CounterType 限定詞](countertype-qualifier.md)。

</dd> <dt>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**計數器**
</dt> <dd>

**string**

在對應的原始類別中，用來做為烹飪公式中之計數器值的必要屬性名稱。 此值必須是對應原始類別中資料來源屬性的屬性名稱。

</dd> <dt>

<span id="PerfTimeStamp"></span><span id="perftimestamp"></span><span id="PERFTIMESTAMP"></span>**PerfTimeStamp**
</dt> <dd>

**string**

原始類別中的屬性名稱，用來做為烹飪公式中的頻率。 如果屬性沒有此限定詞，則會使用類別層級上適當的預設值。 頻率代表時間戳記的每秒刻度。

</dd> <dt>

<span id="PerfTimeFreq"></span><span id="perftimefreq"></span><span id="PERFTIMEFREQ"></span>**PerfTimeFreq**
</dt> <dd>

**string**

原始類別中用來做為烹飪公式中之時間戳記的屬性名稱。 如果屬性沒有此限定詞，則會使用類別層級上適當的預設值。 自動產生的時間戳記可能會在計算中造成錯誤，因為時間戳記是近似值，並且不會考慮封送處理和實際資料收集所產生的額外負荷。

</dd> </dl>

## <a name="how-to-interpret-property-qualifiers"></a>如何解讀屬性限定詞

[**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)類別中的屬性包含 [格式化效能 Data Provider](formatted-performance-data-provider.md)所提供的計算資料。 屬性值是最後計算的結果。 限定詞提供配方。

**計數器** 和 **基底** 限定詞指向資料來源， **CookingType** 會指定用來產生結果的公式。 時間戳記和取樣頻率也來自對應的原始類別，並在 **PerfTimeStamp** 和 **PerfTimeFreq** 中命名。

例如，WMI 提供的其中一個格式化類別（ [**Win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md)）包含名為 **AvgDiskBytesPerRead** 的屬性。 格式化類別中的屬性名稱必須與原始類別中的屬性相同。 **AvgDiskBytesPerRead** 屬性具有下列限定詞。

下列清單列出所有衍生自 [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)之類別的屬性可用的屬性限定詞。



| Qualifier         | 值                     |
|-------------------|---------------------------|
| **CookingType**   | 效能 \_ 平均 \_ 大量       |
| **計數器**       | AvgDiskBytesPerRead       |
| **PerfTimeStamp** | 時間戳記 \_ PerfTime       |
| **PerfTimeFreq**  | 頻率 \_ PerfTime       |
| **PerfIndex**     | 408                       |
| **HelpIndex**     | 409                       |
| **基本**          | AvgDiskBytesPerRead \_ 基底 |



 

**AvgDiskBytesPerRead** 屬性會報告讀取作業期間從磁片傳輸的平均位元組數。 效能 \_ 平均大量的公式 \_ 是：

 (Sample2.xml-Sample1) / (Base Sample2.xml-Base Sample1) 

讀取作業會以 **PerfTimeFreq** 指定的頻率進行取樣，並以 **PerfTimeStamp** 值表示最新的範例。 原始計數器資料（以位元組為單位）取自 [**Win32 \_ PerfRawData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md)類別中的 **AvgDiskBytesPerRead** 屬性。 作業資料的基礎數目取自相同類別中的 **AvgDiskBytesPerRead \_ 基底** 屬性。

如需詳細資訊，請參閱 [取得統計效能資料](obtaining-statistical-performance-data.md) 和 [監視效能資料](monitoring-performance-data.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[監視效能資料](monitoring-performance-data.md)
</dt> <dt>

[WMI 效能類別專用的限定詞](qualifiers-specific-to-wmi-performance-classes.md)
</dt> <dt>

[效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[存取 WMI 預先安裝的效能類別](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[WMI 工作：效能監視](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
