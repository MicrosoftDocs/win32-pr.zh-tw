---
title: DXCoreAdapterProperty
description: 定義指定 DXCore 介面卡屬性的常數。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 645f0a890aac9a50cdf2987c0736a85142a91aff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967268"
---
# <a name="dxcoreadapterproperty-enum"></a>DXCoreAdapterProperty 列舉

定義指定 DXCore 介面卡屬性的常數。 將下列其中一個常數傳遞給 [IDXCoreAdapter：： GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) 方法，以取得接收對應屬性值所需的緩衝區大小;然後，將相同的常數傳遞給 [IDXCoreAdapter：： GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md) 方法，以在您配置的緩衝區中取得屬性的值。

## <a name="syntax"></a>Syntax

```cpp
enum class DXCoreAdapterProperty : uint32_t
{
  InstanceLuid = 0,
  DriverVersion = 1,
  DriverDescription = 2,
  HardwareID = 3,
  KmdModelVersion = 4,
  ComputePreemptionGranularity = 5,
  GraphicsPreemptionGranularity = 6,
  DedicatedAdapterMemory = 7,
  DedicatedSystemMemory = 8,
  SharedSystemMemory = 9,
  AcgCompatible = 10,
  IsHardware = 11,
  IsIntegrated = 12,
  IsDetachable = 13
};
```

## <a name="constants"></a>常數

### <a name="instanceluid"></a>InstanceLuid

指定 <em>InstanceLuid</em> adapter 屬性，其中包含代表介面卡的本機唯一識別碼。 此值在此介面卡的存留期內會維持不變。 介面卡的 LUID 會在重新開機、驅動程式升級或裝置停用/啟用時變更。

<em>InstanceLuid</em>介面卡屬性的類型為<a href="/windows/win32/api/winnt/ns-winnt-luid">LUID</a>。

### <a name="driverversion"></a>DriverVersion

指定包含驅動程式版本的 <em>DriverVersion</em> 介面卡內容，以 <b>文字</b>s 表示為 <b>LARGE_INTEGER</b>。

<em>DriverVersion</em>介面卡屬性有類型<b>Uint64_t</b>，代表布林值。

### <a name="driverdescription"></a>DriverDescription

指定<em>DriverDescription</em> adapter 屬性，其中包含以<a href="/windows/win32/intl/unicode">utf-8</a>編碼方式描述驅動程式之 CHAR （以 Null 結束的<b>字元</b>陣列）。

<em>DriverDescription</em>介面卡屬性的類型為<b>char *</b>。

### <a name="hardwareid"></a>Sensors

指定代表 PnP 硬體識別碼部分的 <em>sensors</em> 介面卡屬性。

<em>Sensors</em>介面卡屬性的類型為<a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcorehardwareid">DXCoreHardwareID</a>。

### <a name="kmdmodelversion"></a>KmdModelVersion

指定代表驅動程式型號的 <em>KmdModelVersion</em> 介面卡屬性。

<em>KmdModelVersion</em>介面卡屬性具有類型<a href="/windows-hardware/drivers/ddi/content/d3dkmthk/ne-d3dkmthk-_qai_driverversion">D3DKMT_DRIVERVERSION</a>。

### <a name="computepreemptiongranularity"></a>ComputePreemptionGranularity

指定 <em>ComputePreemptionGranularity</em> 介面卡屬性，代表計算優先的資料細微性。

<em>ComputePreemptionGranularity</em>介面卡屬性有類型<b>uint16_t</b>，表示<a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_compute_preemption_granularity">D3DKMDT_COMPUTE_PREEMPTION_GRANULARITY</a>值。

### <a name="graphicspreemptiongranularity"></a>GraphicsPreemptionGranularity

指定代表圖形優先的資料細微性的 <em>GraphicsPreemptionGranularity</em> 介面卡屬性。

<em>GraphicsPreemptionGranularity</em>介面卡屬性有類型<b>uint16_t</b>，表示<a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_graphics_preemption_granularity">D3DKMDT_GRAPHICS_PREEMPTION_GRANULARITY</a>值。

### <a name="dedicatedadaptermemory"></a>DedicatedAdapterMemory

指定 [ <em>DedicatedAdapterMemory</em> 介面卡] 屬性，代表未與 CPU 共用的專用介面卡記憶體位元組數目。

<em>DedicatedVideoMemory</em>介面卡屬性具有類型<b>uint64_t</b>。

### <a name="dedicatedsystemmemory"></a>DedicatedSystemMemory

指定 <em>DedicatedSystemMemory</em> adapter 屬性，代表未與 CPU 共用的專用系統記憶體位元組數目。 在開機時，系統會從可用的系統記憶體配置此記憶體。

<em>DedicatedSystemMemory</em>介面卡屬性具有類型<b>uint64_t</b>。

### <a name="sharedsystemmemory"></a>SharedSystemMemory

指定 <em>SharedSystemMemory</em> adapter 屬性，代表共用系統記憶體的位元組數目。 這是在操作期間，介面卡可能耗用的系統記憶體最大值。 驅動程式在管理和使用視訊記憶體時所耗用的任何偶發記憶體，都是額外的。

<em>SharedSystemMemory</em>介面卡屬性具有類型<b>uint64_t</b>。

### <a name="acgcompatible"></a>AcgCompatible

指定 [ <em>AcgCompatible</em> 介面卡] 屬性，指出介面卡是否與強制執行任意程式碼防護的進程相容。

<em>AcgCompatible</em>介面卡屬性的類型為<b>bool</b>。

### <a name="ishardware"></a>IsHardware

指定 [ <em>IsHardware</em> 介面卡] 屬性，以決定這是否為硬體配接器。 不是硬體配接器的介面卡是軟體配接器。

<em>IsHardware</em>介面卡屬性的類型為<b>bool</b>。

### <a name="isintegrated"></a>IsIntegrated

指定 [ <em>IsIntegrated</em> 介面卡] 屬性，以決定是否將介面卡報告為整合式圖形處理器， (iGPU) 。

<em>IsIntegrated</em>介面卡屬性的類型為<b>bool</b>。

### <a name="isdetachable"></a>IsDetachable

指定 [ <em>IsDetachable</em> 介面卡] 屬性，以判斷介面卡是否已回報為可卸離或卸載。

<em>IsDetachable</em>介面卡屬性的類型為<b>bool</b>。

<b>請注意</b>。 即使 <a href="/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty">IDXCoreAdapter：： GetProperty</a> 指出 `false` 此屬性，介面卡仍具有可回報為已移除的功能，例如發生故障或驅動程式更新。

## <a name="see-also"></a>另請參閱

[IDXCoreAdapter：： GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md)、 [IDXCoreAdapter：： GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)