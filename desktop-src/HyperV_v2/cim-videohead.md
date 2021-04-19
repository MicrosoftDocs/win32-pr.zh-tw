---
description: 代表 CIM DisplayController 物件的其中一個標頭 \_ 。
ms.assetid: 2bb034d9-d1df-4cc8-a6a8-b6ad7289f582
title: CIM_VideoHead 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoHead
- CIM_VideoHead.CurrentBitsPerPixel
- CIM_VideoHead.CurrentHorizontalResolution
- CIM_VideoHead.CurrentVerticalResolution
- CIM_VideoHead.MaxRefreshRate
- CIM_VideoHead.MinRefreshRate
- CIM_VideoHead.CurrentRefreshRate
- CIM_VideoHead.CurrentScanMode
- CIM_VideoHead.OtherCurrentScanMode
- CIM_VideoHead.CurrentNumberOfRows
- CIM_VideoHead.CurrentNumberOfColumns
- CIM_VideoHead.CurrentNumberOfColors
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 22f8176c9bdbeae460dfa22ca395e7ed8dd8351e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980793"
---
# <a name="cim_videohead-class"></a><span data-ttu-id="a2d5f-103">CIM \_ VideoHead 類別</span><span class="sxs-lookup"><span data-stu-id="a2d5f-103">CIM\_VideoHead class</span></span>

<span data-ttu-id="a2d5f-104">代表 [**CIM \_ DisplayController**](cim-displaycontroller.md) 物件的其中一個標頭。</span><span class="sxs-lookup"><span data-stu-id="a2d5f-104">Represents one head of a [**CIM\_DisplayController**](cim-displaycontroller.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2d5f-105">語法</span><span class="sxs-lookup"><span data-stu-id="a2d5f-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_VideoHead : CIM_LogicalDevice
{
  uint32 CurrentBitsPerPixel;
  uint32 CurrentHorizontalResolution;
  uint32 CurrentVerticalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint32 CurrentRefreshRate;
  uint16 CurrentScanMode;
  string OtherCurrentScanMode;
  uint32 CurrentNumberOfRows;
  uint32 CurrentNumberOfColumns;
  uint64 CurrentNumberOfColors;
};
```

## <a name="members"></a><span data-ttu-id="a2d5f-106">成員</span><span class="sxs-lookup"><span data-stu-id="a2d5f-106">Members</span></span>

<span data-ttu-id="a2d5f-107">**CIM \_ VideoHead** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a2d5f-107">The **CIM\_VideoHead** class has these types of members:</span></span>

-   [<span data-ttu-id="a2d5f-108">屬性</span><span class="sxs-lookup"><span data-stu-id="a2d5f-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a2d5f-109">屬性</span><span class="sxs-lookup"><span data-stu-id="a2d5f-109">Properties</span></span>

<span data-ttu-id="a2d5f-110">**CIM \_ VideoHead** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a2d5f-110">The **CIM\_VideoHead** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a2d5f-111">**CurrentBitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="a2d5f-111">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d5f-112">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a2d5f-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2d5f-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a2d5f-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2d5f-114">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Bits" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 004.12 ") ， **PUnit** (" bit ") </span><span class="sxs-lookup"><span data-stu-id="a2d5f-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.12"), **PUnit** ("bit")</span></span>
</dt> </dl>

<span data-ttu-id="a2d5f-115">用來顯示每個圖元的位數。</span><span class="sxs-lookup"><span data-stu-id="a2d5f-115">The number of bits used to display each pixel.</span></span>

</dd> <dt>

<span data-ttu-id="a2d5f-116">**CurrentHorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="a2d5f-116">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d5f-117">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a2d5f-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2d5f-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a2d5f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2d5f-119">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "圖元" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 004.11 ") ， [**MODELCORRESPONDENCE**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. HorizontalResolution ") ， **PUnit** (" 圖元 ") </span><span class="sxs-lookup"><span data-stu-id="a2d5f-119">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pixels"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.11"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.HorizontalResolution"), **PUnit** ("pixel")</span></span>
</dt> </dl>

<span data-ttu-id="a2d5f-120">目前的水準圖元數目。</span><span class="sxs-lookup"><span data-stu-id="a2d5f-120">The current number of horizontal pixels.</span></span>

</dd> <dt>

<span data-ttu-id="a2d5f-121">**CurrentNumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="a2d5f-121">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d5f-122">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="a2d5f-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a2d5f-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a2d5f-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2d5f-124">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CIM \_ VideoHeadResolution. NumberOfColors" ) </span><span class="sxs-lookup"><span data-stu-id="a2d5f-124">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.NumberOfColors")</span></span>
</dt> </dl>

<span data-ttu-id="a2d5f-125">目前解析度所支援的色彩數目。</span><span class="sxs-lookup"><span data-stu-id="a2d5f-125">The number of colors supported at the current resolution.</span></span>

</dd> <dt>

<span data-ttu-id="a2d5f-126">**CurrentNumberOfColumns**</span><span class="sxs-lookup"><span data-stu-id="a2d5f-126">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d5f-127">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a2d5f-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2d5f-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a2d5f-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2d5f-129">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 004.14 ") </span><span class="sxs-lookup"><span data-stu-id="a2d5f-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.14")</span></span>
</dt> </dl>

<span data-ttu-id="a2d5f-130">如果在字元模式中，則為顯示控制器的欄數;否則為 "0"。</span><span class="sxs-lookup"><span data-stu-id="a2d5f-130">If in character mode, the number of columns for the display controller; otherwise, "0".</span></span>

</dd> <dt>

<span data-ttu-id="a2d5f-131">**CurrentNumberOfRows**</span><span class="sxs-lookup"><span data-stu-id="a2d5f-131">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d5f-132">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a2d5f-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2d5f-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a2d5f-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2d5f-134">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 004.13 ") </span><span class="sxs-lookup"><span data-stu-id="a2d5f-134">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.13")</span></span>
</dt> </dl>

<span data-ttu-id="a2d5f-135">如果在字元模式中，則為顯示控制器的資料列數目;否則為 "0"。</span><span class="sxs-lookup"><span data-stu-id="a2d5f-135">If in character mode, the number of rows for the display controller; otherwise, "0".</span></span>

</dd> <dt>

<span data-ttu-id="a2d5f-136">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="a2d5f-136">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d5f-137">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a2d5f-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2d5f-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a2d5f-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2d5f-139">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "赫茲" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 004.15 ") ， [**MODELCORRESPONDENCE**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. RefreshRate ") ， **PUnit** (" 赫茲 ") </span><span class="sxs-lookup"><span data-stu-id="a2d5f-139">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.15"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.RefreshRate"), **PUnit** ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="a2d5f-140">顯示控制器目前的重新整理速率（以赫茲為單位）。</span><span class="sxs-lookup"><span data-stu-id="a2d5f-140">The current refresh rate of the display controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="a2d5f-141">**CurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="a2d5f-141">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d5f-142">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a2d5f-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a2d5f-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a2d5f-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2d5f-144">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 004.8 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VideoHead**.**OtherCurrentScanMode**，CIM \_ VideoHeadResolution. ScanMode ") </span><span class="sxs-lookup"><span data-stu-id="a2d5f-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoHead**.**OtherCurrentScanMode**, CIM\_VideoHeadResolution.ScanMode")</span></span>
</dt> </dl>

<span data-ttu-id="a2d5f-145">顯示控制器的目前掃描模式。</span><span class="sxs-lookup"><span data-stu-id="a2d5f-145">The current scan mode of the display controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a2d5f-146">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="a2d5f-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a2d5f-147">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="a2d5f-147">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="a2d5f-148">**不支援** (2) </span><span class="sxs-lookup"><span data-stu-id="a2d5f-148">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

<span data-ttu-id="a2d5f-149">**非交錯操作** (3) </span><span class="sxs-lookup"><span data-stu-id="a2d5f-149">**Non-Interlaced Operation** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

<span data-ttu-id="a2d5f-150">**交錯操作** (4) </span><span class="sxs-lookup"><span data-stu-id="a2d5f-150">**Interlaced Operation** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a2d5f-151">**CurrentVerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="a2d5f-151">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d5f-152">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a2d5f-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2d5f-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a2d5f-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2d5f-154">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "圖元" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 004.10 ") ， [**MODELCORRESPONDENCE**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. VerticalResolution ") ， **PUnit** (" 圖元 ") </span><span class="sxs-lookup"><span data-stu-id="a2d5f-154">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pixels"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.10"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.VerticalResolution"), **PUnit** ("pixel")</span></span>
</dt> </dl>

<span data-ttu-id="a2d5f-155">目前的垂直圖元數目。</span><span class="sxs-lookup"><span data-stu-id="a2d5f-155">The current number of vertical pixels.</span></span>

</dd> <dt>

<span data-ttu-id="a2d5f-156">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="a2d5f-156">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d5f-157">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a2d5f-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2d5f-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a2d5f-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2d5f-159">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "赫茲" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 004.5 ") ， [**MODELCORRESPONDENCE**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. MaxRefreshRate ") ， **PUnit** (" 赫茲 ") </span><span class="sxs-lookup"><span data-stu-id="a2d5f-159">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.MaxRefreshRate"), **PUnit** ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="a2d5f-160">顯示控制器的最大重新整理速率（以赫茲為單位）。</span><span class="sxs-lookup"><span data-stu-id="a2d5f-160">The maximum refresh rate of the display controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="a2d5f-161">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="a2d5f-161">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d5f-162">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a2d5f-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2d5f-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a2d5f-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2d5f-164">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "赫茲" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Video \| 004.4 ") ， [**MODELCORRESPONDENCE**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. MinRefreshRate ") ， **PUnit** (" 赫茲 ") </span><span class="sxs-lookup"><span data-stu-id="a2d5f-164">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.MinRefreshRate"), **PUnit** ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="a2d5f-165">顯示控制器的最小重新整理頻率（以赫茲為單位）。</span><span class="sxs-lookup"><span data-stu-id="a2d5f-165">The minimum refresh rate of the display controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="a2d5f-166">**OtherCurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="a2d5f-166">**OtherCurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d5f-167">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2d5f-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2d5f-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a2d5f-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2d5f-169">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ VideoHead**.**CurrentScanMode**，CIM \_ VideoHeadResolution. OtherScanMode ") </span><span class="sxs-lookup"><span data-stu-id="a2d5f-169">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoHead**.**CurrentScanMode**, CIM\_VideoHeadResolution.OtherScanMode")</span></span>
</dt> </dl>

<span data-ttu-id="a2d5f-170">當 **CurrentScanMode** 屬性為 "1" (其他) 時的目前掃描模式描述。</span><span class="sxs-lookup"><span data-stu-id="a2d5f-170">A description of current scan mode when the **CurrentScanMode** property is "1" (other).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a2d5f-171">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2d5f-171">Requirements</span></span>



| <span data-ttu-id="a2d5f-172">需求</span><span class="sxs-lookup"><span data-stu-id="a2d5f-172">Requirement</span></span> | <span data-ttu-id="a2d5f-173">值</span><span class="sxs-lookup"><span data-stu-id="a2d5f-173">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2d5f-174">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a2d5f-174">Minimum supported client</span></span><br/> | <span data-ttu-id="a2d5f-175">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a2d5f-175">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="a2d5f-176">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a2d5f-176">Minimum supported server</span></span><br/> | <span data-ttu-id="a2d5f-177">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a2d5f-177">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="a2d5f-178">命名空間</span><span class="sxs-lookup"><span data-stu-id="a2d5f-178">Namespace</span></span><br/>                | <span data-ttu-id="a2d5f-179">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="a2d5f-179">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a2d5f-180">MOF</span><span class="sxs-lookup"><span data-stu-id="a2d5f-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2d5f-181"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a2d5f-181"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2d5f-182">DLL</span><span class="sxs-lookup"><span data-stu-id="a2d5f-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2d5f-183"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a2d5f-183"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a2d5f-184">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2d5f-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2d5f-185">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="a2d5f-185">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

