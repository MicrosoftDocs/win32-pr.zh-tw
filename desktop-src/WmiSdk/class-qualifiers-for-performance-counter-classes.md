---
description: 指定與 WMI 效能計數器類別對應的效能物件相關資訊。
ms.assetid: 7b8b7f00-95d8-4c1e-8638-157d0f4c7c32
ms.tgt_platform: multiple
title: 效能計數器類別的類別限定詞
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5b8168dcc0523c629202ac4d5c4a0ea51ecc8bd68d5ac4498fb38059b940fd83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118820092"
---
# <a name="class-qualifiers-for-performance-counter-classes"></a>效能計數器類別的類別限定詞

類別限定詞指定與 WMI [效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes) 對應的效能物件相關資訊。 如需詳細資訊，請參閱 [監視效能資料](monitoring-performance-data.md)。

-   [原始和格式化 PerformanceClasses 的限定詞](#qualifiers-for-raw-and-formatted-performanceclasses)
-   [原始效能類別的限定詞](#)
-   [格式化效能類別的限定詞](#)
-   [相關主題](#related-topics)


「WbemPerfClass」提供者會自動將效能計數器特定的限定詞附加至根 CIMv2 中的 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 類別和屬性 \\ 。

這項資訊適用于類別的所有實例。 具有永遠 **為 False** 的 **布林** 值的某些限定詞可能不會出現在特定類別上。

## <a name="qualifiers-for-raw-and-formatted-performanceclasses"></a>原始和格式化 PerformanceClasses 的限定詞

下列限定詞適用于所有衍生自 [**win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 和 [**win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)的類別。

<dl> <dt>

<span id="Cooked"></span><span id="cooked"></span><span id="COOKED"></span>**熟**
</dt> <dd>

**boolean**

指出類別是否包含處理後的資料。

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**
</dt> <dd>

**string**

效能物件名稱。 如需相關資訊，請參閱 [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal)。

</dd> <dt>

<span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**
</dt> <dd>

**sint32**

不提供詳細資料。 一律包含100的值。

</dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>**動態**
</dt> <dd>

**boolean**

一律設定為 **True** ，因為實例一律為動態。

</dd> <dt>

<span id="GenericPerfCtr"></span><span id="genericperfctr"></span><span id="GENERICPERFCTR"></span>**GenericPerfCtr**
</dt> <dd>

**boolean**

指出類別是否來自舊版效能程式庫。 一律設定為 **True**。

</dd> <dt>

<span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**
</dt> <dd>

**sint32**

索引不再有效。 此辨識符號一律為零。

</dd> <dt>

<span id="HiPerf_"></span><span id="hiperf_"></span><span id="HIPERF_"></span>**HiPerf** 
</dt> <dd>

**boolean**

指出類別是高效能類別。 一律設定為 **True**。

</dd> <dt>

<span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**現場**
</dt> <dd>

**sint32**

地區設定識別項。 值一律為 1033 (美式英文) 。

</dd> <dt>

<span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**
</dt> <dd>

**int32**

索引不再有效。 此辨識符號一律為零。

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**供應商**
</dt> <dd>

**string**

執行個體提供者的名稱。 值為 "WbemPerfV2"。

</dd> <dt>

<span id="RegistryKey"></span><span id="registrykey"></span><span id="REGISTRYKEY"></span>**RegistryKey**
</dt> <dd>

**string**

**HKEY \_ 本機 \_ 電腦 \\ CurrentControlSet \\ 服務** 機碼中的驅動程式名稱，可在此機碼中找到效能金鑰。 此名稱也是提供效能計數器之服務的名稱。

</dd> <dt>

<span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**單身 人士**
</dt> <dd>

**boolean**

若 **為 True**，表示只有類別的單一實例存在。

</dd> </dl>

## <a name="qualifiers-for-raw-performance-classes"></a>原始效能類別的限定詞

下列限定詞適用于所有衍生自 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)的類別。

<dl> <dt>

<span id="Costly"></span><span id="costly"></span><span id="COSTLY"></span>**昂貴**
</dt> <dd>

**boolean**

指出取得這個類別的實例是否為成本高昂的作業。 對於在 \_ 類別名稱結尾附加「高成本」的類別，一律設定為 True。

</dd> <dt>

<span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**
</dt> <dd>

**uint32**

不提供詳細資料。 一律包含100的值。

</dd> <dt>

<span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**
</dt> <dd>

**boolean**

值一律為 **False**。

</dd> </dl>

## <a name="qualifiers-for-formatted-performance-classes"></a>格式化效能類別的限定詞

下列限定詞適用于所有衍生自 [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)的類別。

<dl> <dt>

<span id="AutoCook"></span><span id="autocook"></span><span id="AUTOCOOK"></span>**AutoCook**
</dt> <dd>

**int32**

指出類別實例中的值會自動從對應的原始資料類別計算。 值一律為1。

</dd> <dt>

<span id="AutoCook_RawClass"></span><span id="autocook_rawclass"></span><span id="AUTOCOOK_RAWCLASS"></span>**AutoCook \_ RawClass**
</dt> <dd>

**string**

用於計算格式化類別之原始類別的名稱。 這是必要的限定詞。

</dd> </dl>

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

 

 
