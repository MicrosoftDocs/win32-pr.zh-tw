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
# <a name="dxcoreadapterproperty-enum"></a><span data-ttu-id="b0888-103">DXCoreAdapterProperty 列舉</span><span class="sxs-lookup"><span data-stu-id="b0888-103">DXCoreAdapterProperty enum</span></span>

<span data-ttu-id="b0888-104">定義指定 DXCore 介面卡屬性的常數。</span><span class="sxs-lookup"><span data-stu-id="b0888-104">Defines constants that specify DXCore adapter properties.</span></span> <span data-ttu-id="b0888-105">將下列其中一個常數傳遞給 [IDXCoreAdapter：： GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) 方法，以取得接收對應屬性值所需的緩衝區大小;然後，將相同的常數傳遞給 [IDXCoreAdapter：： GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md) 方法，以在您配置的緩衝區中取得屬性的值。</span><span class="sxs-lookup"><span data-stu-id="b0888-105">Pass one of these constants to the [IDXCoreAdapter::GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) method to retrieve the buffer size necessary to receive the value of the corresponding property; then pass the same constant to the [IDXCoreAdapter::GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md) method to retrieve the property's value in a buffer that you allocate.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0888-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0888-106">Syntax</span></span>

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

## <a name="constants"></a><span data-ttu-id="b0888-107">常數</span><span class="sxs-lookup"><span data-stu-id="b0888-107">Constants</span></span>

### <a name="instanceluid"></a><span data-ttu-id="b0888-108">InstanceLuid</span><span class="sxs-lookup"><span data-stu-id="b0888-108">InstanceLuid</span></span>

<span data-ttu-id="b0888-109">指定 <em>InstanceLuid</em> adapter 屬性，其中包含代表介面卡的本機唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="b0888-109">Specifies the <em>InstanceLuid</em> adapter property, which contains a locally unique identifier representing the adapter.</span></span> <span data-ttu-id="b0888-110">此值在此介面卡的存留期內會維持不變。</span><span class="sxs-lookup"><span data-stu-id="b0888-110">This value remains constant for the lifetime of this adapter.</span></span> <span data-ttu-id="b0888-111">介面卡的 LUID 會在重新開機、驅動程式升級或裝置停用/啟用時變更。</span><span class="sxs-lookup"><span data-stu-id="b0888-111">The LUID of an adapter changes on reboot, driver upgrade, or device disablement/enablement.</span></span>

<span data-ttu-id="b0888-112"><em>InstanceLuid</em>介面卡屬性的類型為<a href="/windows/win32/api/winnt/ns-winnt-luid">LUID</a>。</span><span class="sxs-lookup"><span data-stu-id="b0888-112">The <em>InstanceLuid</em> adapter property has type <a href="/windows/win32/api/winnt/ns-winnt-luid">LUID</a>.</span></span>

### <a name="driverversion"></a><span data-ttu-id="b0888-113">DriverVersion</span><span class="sxs-lookup"><span data-stu-id="b0888-113">DriverVersion</span></span>

<span data-ttu-id="b0888-114">指定包含驅動程式版本的 <em>DriverVersion</em> 介面卡內容，以 <b>文字</b>s 表示為 <b>LARGE_INTEGER</b>。</span><span class="sxs-lookup"><span data-stu-id="b0888-114">Specifies the <em>DriverVersion</em> adapter property, which contains the driver version, represented in <b>WORD</b>s as a <b>LARGE_INTEGER</b>.</span></span>

<span data-ttu-id="b0888-115"><em>DriverVersion</em>介面卡屬性有類型<b>Uint64_t</b>，代表布林值。</span><span class="sxs-lookup"><span data-stu-id="b0888-115">The <em>DriverVersion</em> adapter property has type <b>uint64_t</b>, representing a Boolean value.</span></span>

### <a name="driverdescription"></a><span data-ttu-id="b0888-116">DriverDescription</span><span class="sxs-lookup"><span data-stu-id="b0888-116">DriverDescription</span></span>

<span data-ttu-id="b0888-117">指定<em>DriverDescription</em> adapter 屬性，其中包含以<a href="/windows/win32/intl/unicode">utf-8</a>編碼方式描述驅動程式之 CHAR （以 Null 結束的<b>字元</b>陣列）。</span><span class="sxs-lookup"><span data-stu-id="b0888-117">Specifies the <em>DriverDescription</em> adapter property, which contains a NULL-terminated array of <b>CHAR</b>s describing the driver, as specified by the driver, in <a href="/windows/win32/intl/unicode">UTF-8</a> encoding.</span></span>

<span data-ttu-id="b0888-118"><em>DriverDescription</em>介面卡屬性的類型為<b>char \*</b>。</span><span class="sxs-lookup"><span data-stu-id="b0888-118">The <em>DriverDescription</em> adapter property has type <b>char\*</b>.</span></span>

### <a name="hardwareid"></a><span data-ttu-id="b0888-119">Sensors</span><span class="sxs-lookup"><span data-stu-id="b0888-119">HardwareID</span></span>

<span data-ttu-id="b0888-120">指定代表 PnP 硬體識別碼部分的 <em>sensors</em> 介面卡屬性。</span><span class="sxs-lookup"><span data-stu-id="b0888-120">Specifies the <em>HardwareID</em> adapter property, which represents the PnP hardware ID parts.</span></span>

<span data-ttu-id="b0888-121"><em>Sensors</em>介面卡屬性的類型為<a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcorehardwareid">DXCoreHardwareID</a>。</span><span class="sxs-lookup"><span data-stu-id="b0888-121">The <em>HardwareID</em> adapter property has type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcorehardwareid">DXCoreHardwareID</a>.</span></span>

### <a name="kmdmodelversion"></a><span data-ttu-id="b0888-122">KmdModelVersion</span><span class="sxs-lookup"><span data-stu-id="b0888-122">KmdModelVersion</span></span>

<span data-ttu-id="b0888-123">指定代表驅動程式型號的 <em>KmdModelVersion</em> 介面卡屬性。</span><span class="sxs-lookup"><span data-stu-id="b0888-123">Specifies the <em>KmdModelVersion</em> adapter property, which represents the driver model.</span></span>

<span data-ttu-id="b0888-124"><em>KmdModelVersion</em>介面卡屬性具有類型<a href="/windows-hardware/drivers/ddi/content/d3dkmthk/ne-d3dkmthk-_qai_driverversion">D3DKMT_DRIVERVERSION</a>。</span><span class="sxs-lookup"><span data-stu-id="b0888-124">The <em>KmdModelVersion</em> adapter property has type <a href="/windows-hardware/drivers/ddi/content/d3dkmthk/ne-d3dkmthk-_qai_driverversion">D3DKMT_DRIVERVERSION</a>.</span></span>

### <a name="computepreemptiongranularity"></a><span data-ttu-id="b0888-125">ComputePreemptionGranularity</span><span class="sxs-lookup"><span data-stu-id="b0888-125">ComputePreemptionGranularity</span></span>

<span data-ttu-id="b0888-126">指定 <em>ComputePreemptionGranularity</em> 介面卡屬性，代表計算優先的資料細微性。</span><span class="sxs-lookup"><span data-stu-id="b0888-126">Specifies the <em>ComputePreemptionGranularity</em> adapter property, which represents the compute preemption granularity.</span></span>

<span data-ttu-id="b0888-127"><em>ComputePreemptionGranularity</em>介面卡屬性有類型<b>uint16_t</b>，表示<a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_compute_preemption_granularity">D3DKMDT_COMPUTE_PREEMPTION_GRANULARITY</a>值。</span><span class="sxs-lookup"><span data-stu-id="b0888-127">The <em>ComputePreemptionGranularity</em> adapter property has type <b>uint16_t</b>, representing a <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_compute_preemption_granularity">D3DKMDT_COMPUTE_PREEMPTION_GRANULARITY</a> value.</span></span>

### <a name="graphicspreemptiongranularity"></a><span data-ttu-id="b0888-128">GraphicsPreemptionGranularity</span><span class="sxs-lookup"><span data-stu-id="b0888-128">GraphicsPreemptionGranularity</span></span>

<span data-ttu-id="b0888-129">指定代表圖形優先的資料細微性的 <em>GraphicsPreemptionGranularity</em> 介面卡屬性。</span><span class="sxs-lookup"><span data-stu-id="b0888-129">Specifies the <em>GraphicsPreemptionGranularity</em> adapter property, which represents the graphics preemption granularity.</span></span>

<span data-ttu-id="b0888-130"><em>GraphicsPreemptionGranularity</em>介面卡屬性有類型<b>uint16_t</b>，表示<a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_graphics_preemption_granularity">D3DKMDT_GRAPHICS_PREEMPTION_GRANULARITY</a>值。</span><span class="sxs-lookup"><span data-stu-id="b0888-130">The <em>GraphicsPreemptionGranularity</em> adapter property has type <b>uint16_t</b>, representing a <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_graphics_preemption_granularity">D3DKMDT_GRAPHICS_PREEMPTION_GRANULARITY</a> value.</span></span>

### <a name="dedicatedadaptermemory"></a><span data-ttu-id="b0888-131">DedicatedAdapterMemory</span><span class="sxs-lookup"><span data-stu-id="b0888-131">DedicatedAdapterMemory</span></span>

<span data-ttu-id="b0888-132">指定 [ <em>DedicatedAdapterMemory</em> 介面卡] 屬性，代表未與 CPU 共用的專用介面卡記憶體位元組數目。</span><span class="sxs-lookup"><span data-stu-id="b0888-132">Specifies the <em>DedicatedAdapterMemory</em> adapter property, which represents the number of bytes of dedicated adapter memory that are not shared with the CPU.</span></span>

<span data-ttu-id="b0888-133"><em>DedicatedVideoMemory</em>介面卡屬性具有類型<b>uint64_t</b>。</span><span class="sxs-lookup"><span data-stu-id="b0888-133">The <em>DedicatedVideoMemory</em> adapter property has type <b>uint64_t</b>.</span></span>

### <a name="dedicatedsystemmemory"></a><span data-ttu-id="b0888-134">DedicatedSystemMemory</span><span class="sxs-lookup"><span data-stu-id="b0888-134">DedicatedSystemMemory</span></span>

<span data-ttu-id="b0888-135">指定 <em>DedicatedSystemMemory</em> adapter 屬性，代表未與 CPU 共用的專用系統記憶體位元組數目。</span><span class="sxs-lookup"><span data-stu-id="b0888-135">Specifies the <em>DedicatedSystemMemory</em> adapter property, which represents the number of bytes of dedicated system memory that are not shared with the CPU.</span></span> <span data-ttu-id="b0888-136">在開機時，系統會從可用的系統記憶體配置此記憶體。</span><span class="sxs-lookup"><span data-stu-id="b0888-136">This memory is allocated from available system memory at boot time.</span></span>

<span data-ttu-id="b0888-137"><em>DedicatedSystemMemory</em>介面卡屬性具有類型<b>uint64_t</b>。</span><span class="sxs-lookup"><span data-stu-id="b0888-137">The <em>DedicatedSystemMemory</em> adapter property has type <b>uint64_t</b>.</span></span>

### <a name="sharedsystemmemory"></a><span data-ttu-id="b0888-138">SharedSystemMemory</span><span class="sxs-lookup"><span data-stu-id="b0888-138">SharedSystemMemory</span></span>

<span data-ttu-id="b0888-139">指定 <em>SharedSystemMemory</em> adapter 屬性，代表共用系統記憶體的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="b0888-139">Specifies the <em>SharedSystemMemory</em> adapter property, which represents the number of bytes of shared system memory.</span></span> <span data-ttu-id="b0888-140">這是在操作期間，介面卡可能耗用的系統記憶體最大值。</span><span class="sxs-lookup"><span data-stu-id="b0888-140">This is the maximum value of system memory that may be consumed by the adapter during operation.</span></span> <span data-ttu-id="b0888-141">驅動程式在管理和使用視訊記憶體時所耗用的任何偶發記憶體，都是額外的。</span><span class="sxs-lookup"><span data-stu-id="b0888-141">Any incidental memory consumed by the driver as it manages and uses video memory is additional.</span></span>

<span data-ttu-id="b0888-142"><em>SharedSystemMemory</em>介面卡屬性具有類型<b>uint64_t</b>。</span><span class="sxs-lookup"><span data-stu-id="b0888-142">The <em>SharedSystemMemory</em> adapter property has type <b>uint64_t</b>.</span></span>

### <a name="acgcompatible"></a><span data-ttu-id="b0888-143">AcgCompatible</span><span class="sxs-lookup"><span data-stu-id="b0888-143">AcgCompatible</span></span>

<span data-ttu-id="b0888-144">指定 [ <em>AcgCompatible</em> 介面卡] 屬性，指出介面卡是否與強制執行任意程式碼防護的進程相容。</span><span class="sxs-lookup"><span data-stu-id="b0888-144">Specifies the <em>AcgCompatible</em> adapter property, which indicates whether the adapter is compatible with processes that enforce Arbitrary Code Guard.</span></span>

<span data-ttu-id="b0888-145"><em>AcgCompatible</em>介面卡屬性的類型為<b>bool</b>。</span><span class="sxs-lookup"><span data-stu-id="b0888-145">The <em>AcgCompatible</em> adapter property has type <b>bool</b>.</span></span>

### <a name="ishardware"></a><span data-ttu-id="b0888-146">IsHardware</span><span class="sxs-lookup"><span data-stu-id="b0888-146">IsHardware</span></span>

<span data-ttu-id="b0888-147">指定 [ <em>IsHardware</em> 介面卡] 屬性，以決定這是否為硬體配接器。</span><span class="sxs-lookup"><span data-stu-id="b0888-147">Specifies the <em>IsHardware</em> adapter property, which determines whether or not this is a hardware adapter.</span></span> <span data-ttu-id="b0888-148">不是硬體配接器的介面卡是軟體配接器。</span><span class="sxs-lookup"><span data-stu-id="b0888-148">An adapter that's not a hardware adapter is a software adapter.</span></span>

<span data-ttu-id="b0888-149"><em>IsHardware</em>介面卡屬性的類型為<b>bool</b>。</span><span class="sxs-lookup"><span data-stu-id="b0888-149">The <em>IsHardware</em> adapter property has type <b>bool</b>.</span></span>

### <a name="isintegrated"></a><span data-ttu-id="b0888-150">IsIntegrated</span><span class="sxs-lookup"><span data-stu-id="b0888-150">IsIntegrated</span></span>

<span data-ttu-id="b0888-151">指定 [ <em>IsIntegrated</em> 介面卡] 屬性，以決定是否將介面卡報告為整合式圖形處理器， (iGPU) 。</span><span class="sxs-lookup"><span data-stu-id="b0888-151">Specifies the <em>IsIntegrated</em> adapter property, which determines whether the adapter is reported to be an integrated graphics processor (iGPU).</span></span>

<span data-ttu-id="b0888-152"><em>IsIntegrated</em>介面卡屬性的類型為<b>bool</b>。</span><span class="sxs-lookup"><span data-stu-id="b0888-152">The <em>IsIntegrated</em> adapter property has type <b>bool</b>.</span></span>

### <a name="isdetachable"></a><span data-ttu-id="b0888-153">IsDetachable</span><span class="sxs-lookup"><span data-stu-id="b0888-153">IsDetachable</span></span>

<span data-ttu-id="b0888-154">指定 [ <em>IsDetachable</em> 介面卡] 屬性，以判斷介面卡是否已回報為可卸離或卸載。</span><span class="sxs-lookup"><span data-stu-id="b0888-154">Specifies the <em>IsDetachable</em> adapter property, which determines whether the adapter has been reported to be detachable, or removable.</span></span>

<span data-ttu-id="b0888-155"><em>IsDetachable</em>介面卡屬性的類型為<b>bool</b>。</span><span class="sxs-lookup"><span data-stu-id="b0888-155">The <em>IsDetachable</em> adapter property has type <b>bool</b>.</span></span>

<span data-ttu-id="b0888-156"><b>請注意</b>。</span><span class="sxs-lookup"><span data-stu-id="b0888-156"><b>Note</b>.</span></span> <span data-ttu-id="b0888-157">即使 <a href="/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty">IDXCoreAdapter：： GetProperty</a> 指出 `false` 此屬性，介面卡仍具有可回報為已移除的功能，例如發生故障或驅動程式更新。</span><span class="sxs-lookup"><span data-stu-id="b0888-157">Even if <a href="/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty">IDXCoreAdapter::GetProperty</a> indicates `false` for this property, the adapter still has the ability to be reported as removed, such as in the case of malfunction, or driver update.</span></span>

## <a name="see-also"></a><span data-ttu-id="b0888-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0888-158">See also</span></span>

<span data-ttu-id="b0888-159">[IDXCoreAdapter：： GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md)、 [IDXCoreAdapter：： GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="b0888-159">[IDXCoreAdapter::GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md), [IDXCoreAdapter::GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>