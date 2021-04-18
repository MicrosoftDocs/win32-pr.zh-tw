---
description: 表示顯示控制器。
ms.assetid: 14598ae6-58e2-46ca-8653-b57e5833a224
title: CIM_DisplayController 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DisplayController
- CIM_DisplayController.Description
- CIM_DisplayController.VideoProcessor
- CIM_DisplayController.VideoMemoryType
- CIM_DisplayController.OtherVideoMemoryType
- CIM_DisplayController.NumberOfVideoPages
- CIM_DisplayController.MaxMemorySupported
- CIM_DisplayController.AcceleratorCapabilities
- CIM_DisplayController.CapabilityDescriptions
- CIM_DisplayController.OtherVideoArchitecture
- CIM_DisplayController.VideoArchitecture
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 59db37a89ce1f57e01a6a9a27fb9c24177221b00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983341"
---
# <a name="cim_displaycontroller-class"></a><span data-ttu-id="c7c36-103">CIM \_ DisplayController 類別</span><span class="sxs-lookup"><span data-stu-id="c7c36-103">CIM\_DisplayController class</span></span>

<span data-ttu-id="c7c36-104">表示顯示控制器。</span><span class="sxs-lookup"><span data-stu-id="c7c36-104">Represents a display controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7c36-105">語法</span><span class="sxs-lookup"><span data-stu-id="c7c36-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.25.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_DisplayController : CIM_Controller
{
  string Description;
  string VideoProcessor;
  uint16 VideoMemoryType;
  string OtherVideoMemoryType;
  uint32 NumberOfVideoPages;
  uint32 MaxMemorySupported;
  uint16 AcceleratorCapabilities[];
  string CapabilityDescriptions[];
  string OtherVideoArchitecture;
  uint16 VideoArchitecture;
};
```

## <a name="members"></a><span data-ttu-id="c7c36-106">成員</span><span class="sxs-lookup"><span data-stu-id="c7c36-106">Members</span></span>

<span data-ttu-id="c7c36-107">**CIM \_ DisplayController** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c7c36-107">The **CIM\_DisplayController** class has these types of members:</span></span>

-   [<span data-ttu-id="c7c36-108">屬性</span><span class="sxs-lookup"><span data-stu-id="c7c36-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c7c36-109">屬性</span><span class="sxs-lookup"><span data-stu-id="c7c36-109">Properties</span></span>

<span data-ttu-id="c7c36-110">**CIM \_ DisplayController** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c7c36-110">The **CIM\_DisplayController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c7c36-111">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c7c36-111">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c36-112">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="c7c36-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c7c36-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7c36-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c36-114">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ DisplayController**。**CapabilityDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="c7c36-114">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="c7c36-115">顯示控制器的圖形和3D 功能。</span><span class="sxs-lookup"><span data-stu-id="c7c36-115">The graphics and 3D capabilities of the display controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7c36-116">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="c7c36-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c7c36-117">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c7c36-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span data-ttu-id="c7c36-118">**圖形加速器** (2) </span><span class="sxs-lookup"><span data-stu-id="c7c36-118">**Graphics Accelerator** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span data-ttu-id="c7c36-119">**3D 加速器** (3) </span><span class="sxs-lookup"><span data-stu-id="c7c36-119">**3D Accelerator** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_Fast_Write"></span><span id="pci_fast_write"></span><span id="PCI_FAST_WRITE"></span>

<span data-ttu-id="c7c36-120">**PCI Fast Write** (4) </span><span class="sxs-lookup"><span data-stu-id="c7c36-120">**PCI Fast Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiMonitor_Support"></span><span id="multimonitor_support"></span><span id="MULTIMONITOR_SUPPORT"></span>

<span data-ttu-id="c7c36-121">**MultiMonitor 支援** (5) </span><span class="sxs-lookup"><span data-stu-id="c7c36-121">**MultiMonitor Support** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_Mastering"></span><span id="pci_mastering"></span><span id="PCI_MASTERING"></span>

<span data-ttu-id="c7c36-122">**PCI 主控** (6) </span><span class="sxs-lookup"><span data-stu-id="c7c36-122">**PCI Mastering** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Second_Monochrome_Adapter_Support"></span><span id="second_monochrome_adapter_support"></span><span id="SECOND_MONOCHROME_ADAPTER_SUPPORT"></span>

<span data-ttu-id="c7c36-123">**第二種單色介面卡支援** (7) </span><span class="sxs-lookup"><span data-stu-id="c7c36-123">**Second Monochrome Adapter Support** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Large_Memory_Address_Support"></span><span id="large_memory_address_support"></span><span id="LARGE_MEMORY_ADDRESS_SUPPORT"></span>

<span data-ttu-id="c7c36-124"> (8) 的 **大型記憶體位址支援**</span><span class="sxs-lookup"><span data-stu-id="c7c36-124">**Large Memory Address Support** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c7c36-125">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c7c36-125">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c36-126">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="c7c36-126">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c7c36-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7c36-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c36-128">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ DisplayController**。**AcceleratorCapabilities**") </span><span class="sxs-lookup"><span data-stu-id="c7c36-128">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**AcceleratorCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="c7c36-129">**AcceleratorCapabilities** 陣列的影片加速器功能詳細說明。</span><span class="sxs-lookup"><span data-stu-id="c7c36-129">Detailed explanations for video accelerator features of the **AcceleratorCapabilities** array.</span></span> <span data-ttu-id="c7c36-130">這個陣列中的專案會對應到 **AcceleratorCapabilities** 中的陣列專案。</span><span class="sxs-lookup"><span data-stu-id="c7c36-130">The items in this array correspond to the array items in **AcceleratorCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="c7c36-131">**說明**</span><span class="sxs-lookup"><span data-stu-id="c7c36-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c36-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c7c36-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7c36-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7c36-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c36-134">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 004.18 ") </span><span class="sxs-lookup"><span data-stu-id="c7c36-134">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.18")</span></span>
</dt> </dl>

<span data-ttu-id="c7c36-135">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="c7c36-135">A text description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="c7c36-136">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="c7c36-136">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c36-137">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c7c36-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7c36-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7c36-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c36-139">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Bytes" ) ， **PUnit** ( "byte" ) </span><span class="sxs-lookup"><span data-stu-id="c7c36-139">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="c7c36-140">支援的最大記憶體數量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c7c36-140">The maximum amount of memory supported, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c7c36-141">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="c7c36-141">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c36-142">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c7c36-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7c36-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7c36-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7c36-144">提供目前的解析度和可用記憶體所支援的影片頁面數目。</span><span class="sxs-lookup"><span data-stu-id="c7c36-144">The number of video pages supported given the current resolutions and available memory.</span></span>

</dd> <dt>

<span data-ttu-id="c7c36-145">**OtherVideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="c7c36-145">**OtherVideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c36-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c7c36-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7c36-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7c36-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c36-148">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ DisplayController**.**VideoArchitecture**") </span><span class="sxs-lookup"><span data-stu-id="c7c36-148">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**VideoArchitecture**")</span></span>
</dt> </dl>

<span data-ttu-id="c7c36-149">**VideoArchitecture** 屬性包含 "1" (其他) 的影片架構類型描述。</span><span class="sxs-lookup"><span data-stu-id="c7c36-149">A description of the video architecture type when the **VideoArchitecture** property contains "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="c7c36-150">**OtherVideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="c7c36-150">**OtherVideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c36-151">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c7c36-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7c36-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7c36-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c36-153">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ DisplayController**.**VideoMemoryType**") </span><span class="sxs-lookup"><span data-stu-id="c7c36-153">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**VideoMemoryType**")</span></span>
</dt> </dl>

<span data-ttu-id="c7c36-154">**VideoMemoryType** 屬性為 "1" (其他) 的視訊記憶體類型。</span><span class="sxs-lookup"><span data-stu-id="c7c36-154">The video memory type when the **VideoMemoryType** property is "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="c7c36-155">**VideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="c7c36-155">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c36-156">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c7c36-156">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7c36-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7c36-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7c36-158">用來產生視訊訊號的顯示器控制器影片架構。</span><span class="sxs-lookup"><span data-stu-id="c7c36-158">The display controllers video architecture used to generate the video signal.</span></span> <span data-ttu-id="c7c36-159">通常，專用的視頻處理器會根據指定的架構產生影片信號。</span><span class="sxs-lookup"><span data-stu-id="c7c36-159">Usually, a dedicated video processor generates the video signal in accordance with the specified architecture.</span></span> <span data-ttu-id="c7c36-160">架構會指出顯示控制器的最大解析功能。</span><span class="sxs-lookup"><span data-stu-id="c7c36-160">The architecture indicates of the maximum resolution capability of the display controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7c36-161">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="c7c36-161">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c7c36-162">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c7c36-162">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="CGA"></span><span id="cga"></span>

<span data-ttu-id="c7c36-163">**CGA** (2) </span><span class="sxs-lookup"><span data-stu-id="c7c36-163">**CGA** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EGA"></span><span id="ega"></span>

<span data-ttu-id="c7c36-164">**EGA** (3) </span><span class="sxs-lookup"><span data-stu-id="c7c36-164">**EGA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VGA"></span><span id="vga"></span>

<span data-ttu-id="c7c36-165">**VGA** (4) </span><span class="sxs-lookup"><span data-stu-id="c7c36-165">**VGA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SVGA"></span><span id="svga"></span>

<span data-ttu-id="c7c36-166">**SVGA** (5) </span><span class="sxs-lookup"><span data-stu-id="c7c36-166">**SVGA** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="MDA"></span><span id="mda"></span>

<span data-ttu-id="c7c36-167">**MDA** (6) </span><span class="sxs-lookup"><span data-stu-id="c7c36-167">**MDA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="HGC"></span><span id="hgc"></span>

<span data-ttu-id="c7c36-168">**HGC** (7) </span><span class="sxs-lookup"><span data-stu-id="c7c36-168">**HGC** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="MCGA"></span><span id="mcga"></span>

<span data-ttu-id="c7c36-169">**MCGA** (8) </span><span class="sxs-lookup"><span data-stu-id="c7c36-169">**MCGA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="8514A"></span><span id="8514a"></span>

<span data-ttu-id="c7c36-170">**8514A** (9) </span><span class="sxs-lookup"><span data-stu-id="c7c36-170">**8514A** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="XGA"></span><span id="xga"></span>

<span data-ttu-id="c7c36-171">**XGA** (10) </span><span class="sxs-lookup"><span data-stu-id="c7c36-171">**XGA** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>

<span data-ttu-id="c7c36-172">**線性框架緩衝區** (11) </span><span class="sxs-lookup"><span data-stu-id="c7c36-172">**Linear Frame Buffer** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="c7c36-173">**PC-98** (160) </span><span class="sxs-lookup"><span data-stu-id="c7c36-173">**PC-98** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="c7c36-174">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="c7c36-174">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="c7c36-175">**廠商保留** (0x8000。) </span><span class="sxs-lookup"><span data-stu-id="c7c36-175">**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c7c36-176">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="c7c36-176">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c36-177">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c7c36-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7c36-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7c36-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c36-179">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 004.6 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DisplayController**.**OtherVideoMemoryType**") </span><span class="sxs-lookup"><span data-stu-id="c7c36-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.6"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**OtherVideoMemoryType**")</span></span>
</dt> </dl>

<span data-ttu-id="c7c36-180">視訊記憶體的類型。</span><span class="sxs-lookup"><span data-stu-id="c7c36-180">The type of video memory.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7c36-181">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="c7c36-181">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c7c36-182">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c7c36-182">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="c7c36-183">**VRAM** (2) </span><span class="sxs-lookup"><span data-stu-id="c7c36-183">**VRAM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="c7c36-184">**DRAM** (3) </span><span class="sxs-lookup"><span data-stu-id="c7c36-184">**DRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="c7c36-185">**SRAM** (4) </span><span class="sxs-lookup"><span data-stu-id="c7c36-185">**SRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

<span data-ttu-id="c7c36-186">**WRAM** (5) </span><span class="sxs-lookup"><span data-stu-id="c7c36-186">**WRAM** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

<span data-ttu-id="c7c36-187">**EDO RAM** (6) </span><span class="sxs-lookup"><span data-stu-id="c7c36-187">**EDO RAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="c7c36-188">高載 **同步 DRAM** (7) </span><span class="sxs-lookup"><span data-stu-id="c7c36-188">**Burst Synchronous DRAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

<span data-ttu-id="c7c36-189">**管線** 高載 SRAM (8) </span><span class="sxs-lookup"><span data-stu-id="c7c36-189">**Pipelined Burst SRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="c7c36-190">**CDRAM** (9) </span><span class="sxs-lookup"><span data-stu-id="c7c36-190">**CDRAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="c7c36-191">**3DRAM** (10) </span><span class="sxs-lookup"><span data-stu-id="c7c36-191">**3DRAM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="c7c36-192">**SDRAM** (11) </span><span class="sxs-lookup"><span data-stu-id="c7c36-192">**SDRAM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="c7c36-193">**SGRAM** (12) </span><span class="sxs-lookup"><span data-stu-id="c7c36-193">**SGRAM** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c7c36-194">**VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="c7c36-194">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c36-195">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c7c36-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7c36-196">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7c36-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7c36-197">影片處理器/控制器的文字描述。</span><span class="sxs-lookup"><span data-stu-id="c7c36-197">A text description of the video processor/controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7c36-198">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7c36-198">Requirements</span></span>



| <span data-ttu-id="c7c36-199">需求</span><span class="sxs-lookup"><span data-stu-id="c7c36-199">Requirement</span></span> | <span data-ttu-id="c7c36-200">值</span><span class="sxs-lookup"><span data-stu-id="c7c36-200">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7c36-201">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c7c36-201">Minimum supported client</span></span><br/> | <span data-ttu-id="c7c36-202">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c7c36-202">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="c7c36-203">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c7c36-203">Minimum supported server</span></span><br/> | <span data-ttu-id="c7c36-204">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c7c36-204">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="c7c36-205">命名空間</span><span class="sxs-lookup"><span data-stu-id="c7c36-205">Namespace</span></span><br/>                | <span data-ttu-id="c7c36-206">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="c7c36-206">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c7c36-207">MOF</span><span class="sxs-lookup"><span data-stu-id="c7c36-207">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7c36-208"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="c7c36-208"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7c36-209">DLL</span><span class="sxs-lookup"><span data-stu-id="c7c36-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7c36-210"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c7c36-210"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c7c36-211">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7c36-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7c36-212">**CIM \_ 控制器**</span><span class="sxs-lookup"><span data-stu-id="c7c36-212">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

