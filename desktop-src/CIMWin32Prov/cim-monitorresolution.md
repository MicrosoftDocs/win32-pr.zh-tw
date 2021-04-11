---
description: CIM \_ MonitorResolution 類別代表水準和垂直解析度之間的關聯性，以及桌面監視器的重新整理頻率和掃描模式。 影片控制器物件中指定了值。
ms.assetid: 064620dd-2d92-42d0-9167-35867830a077
ms.tgt_platform: multiple
title: CIM_MonitorResolution 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MonitorResolution
- CIM_MonitorResolution.Caption
- CIM_MonitorResolution.Description
- CIM_MonitorResolution.SettingID
- CIM_MonitorResolution.HorizontalResolution
- CIM_MonitorResolution.MaxRefreshRate
- CIM_MonitorResolution.MinRefreshRate
- CIM_MonitorResolution.RefreshRate
- CIM_MonitorResolution.ScanMode
- CIM_MonitorResolution.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b359a2e7eccf31b32aced8a2ea9f85fb6dc48b7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936380"
---
# <a name="cim_monitorresolution-class"></a><span data-ttu-id="900fb-104">CIM \_ MonitorResolution 類別</span><span class="sxs-lookup"><span data-stu-id="900fb-104">CIM\_MonitorResolution class</span></span>

<span data-ttu-id="900fb-105">**CIM \_ MonitorResolution** 類別代表水準和垂直解析度之間的關聯性，以及桌面監視器的重新整理頻率和掃描模式。</span><span class="sxs-lookup"><span data-stu-id="900fb-105">The **CIM\_MonitorResolution** class represents the relationship between horizontal and vertical resolutions and the refresh rate and scan mode for a desktop monitor.</span></span> <span data-ttu-id="900fb-106">影片控制器物件中指定了值。</span><span class="sxs-lookup"><span data-stu-id="900fb-106">Values are specified in the video controller object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="900fb-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="900fb-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="900fb-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="900fb-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="900fb-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="900fb-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="900fb-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="900fb-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="900fb-111">語法</span><span class="sxs-lookup"><span data-stu-id="900fb-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCEC-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_MonitorResolution : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 HorizontalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint32 RefreshRate;
  uint16 ScanMode;
  uint32 VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="900fb-112">成員</span><span class="sxs-lookup"><span data-stu-id="900fb-112">Members</span></span>

<span data-ttu-id="900fb-113">**CIM \_ MonitorResolution** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="900fb-113">The **CIM\_MonitorResolution** class has these types of members:</span></span>

-   [<span data-ttu-id="900fb-114">屬性</span><span class="sxs-lookup"><span data-stu-id="900fb-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="900fb-115">屬性</span><span class="sxs-lookup"><span data-stu-id="900fb-115">Properties</span></span>

<span data-ttu-id="900fb-116">**CIM \_ MonitorResolution** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="900fb-116">The **CIM\_MonitorResolution** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="900fb-117">**標題**</span><span class="sxs-lookup"><span data-stu-id="900fb-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="900fb-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="900fb-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="900fb-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="900fb-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="900fb-120">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="900fb-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="900fb-121">目前物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="900fb-121">Short textual description of the current object.</span></span>

<span data-ttu-id="900fb-122">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="900fb-122">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="900fb-123">**說明**</span><span class="sxs-lookup"><span data-stu-id="900fb-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="900fb-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="900fb-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="900fb-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="900fb-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="900fb-126">目前物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="900fb-126">Textual description of the current object.</span></span>

<span data-ttu-id="900fb-127">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="900fb-127">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="900fb-128">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="900fb-128">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="900fb-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="900fb-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="900fb-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="900fb-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="900fb-131">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentHorizontalResolution**") ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 監視器解析度 \| 002.2 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 圖元 ") </span><span class="sxs-lookup"><span data-stu-id="900fb-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentHorizontalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="900fb-132">監視器的水準解析度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="900fb-132">Monitor's horizontal resolution, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="900fb-133">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="900fb-133">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="900fb-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="900fb-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="900fb-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="900fb-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="900fb-136">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VideoController**](cim-videocontroller.md).**MaxRefreshRate**") ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 監視器解析度 \| 002.7 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 赫茲 ") </span><span class="sxs-lookup"><span data-stu-id="900fb-136">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**MaxRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="900fb-137">監視器的最大重新整理速率（以赫茲為單位），可在指定的解析度支援速率範圍時使用。</span><span class="sxs-lookup"><span data-stu-id="900fb-137">Monitor's maximum refresh rate, in hertz, when a range of rates is supported at the specified resolutions.</span></span>

</dd> <dt>

<span data-ttu-id="900fb-138">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="900fb-138">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="900fb-139">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="900fb-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="900fb-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="900fb-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="900fb-141">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VideoController**](cim-videocontroller.md).**MinRefreshRate**") ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 監視器解析度 \| 002.6 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 赫茲 ") </span><span class="sxs-lookup"><span data-stu-id="900fb-141">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**MinRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="900fb-142">監視器的最小重新整理速率（以赫茲為單位），可在指定的解析度支援速率範圍時使用。</span><span class="sxs-lookup"><span data-stu-id="900fb-142">Monitor's minimum refresh rate, in hertz, when a range of rates is supported at the specified resolutions.</span></span>

</dd> <dt>

<span data-ttu-id="900fb-143">**RefreshRate**</span><span class="sxs-lookup"><span data-stu-id="900fb-143">**RefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="900fb-144">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="900fb-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="900fb-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="900fb-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="900fb-146">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentRefreshRate**") ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 監視器解析度 \| 002.4 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 赫茲 ") </span><span class="sxs-lookup"><span data-stu-id="900fb-146">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="900fb-147">監視的重新整理頻率（以赫茲為單位）。</span><span class="sxs-lookup"><span data-stu-id="900fb-147">Monitor's refresh rate, in hertz.</span></span> <span data-ttu-id="900fb-148">如果支援的速率範圍，請使用 **MinRefreshRate** 和 **MaxRefreshRate** 屬性，並將此屬性設定為0。</span><span class="sxs-lookup"><span data-stu-id="900fb-148">If a range of rates is supported, use the **MinRefreshRate** and **MaxRefreshRate** properties, and set this property to 0.</span></span>

</dd> <dt>

<span data-ttu-id="900fb-149">**ScanMode**</span><span class="sxs-lookup"><span data-stu-id="900fb-149">**ScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="900fb-150">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="900fb-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="900fb-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="900fb-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="900fb-152">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentScanMode**") ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 監視器解析度 \| 002.5 ") </span><span class="sxs-lookup"><span data-stu-id="900fb-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentScanMode**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="900fb-153">監視器使用的掃描模式。</span><span class="sxs-lookup"><span data-stu-id="900fb-153">Scan mode that the monitor uses.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="900fb-154">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="900fb-154">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="900fb-155">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="900fb-155">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="900fb-156">**不支援** (3) </span><span class="sxs-lookup"><span data-stu-id="900fb-156">**Not Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

<span data-ttu-id="900fb-157"> (4) **的非交錯操作**</span><span class="sxs-lookup"><span data-stu-id="900fb-157">**Non-Interlaced Operation** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

<span data-ttu-id="900fb-158">**交錯操作** (5) </span><span class="sxs-lookup"><span data-stu-id="900fb-158">**Interlaced Operation** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="900fb-159">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="900fb-159">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="900fb-160">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="900fb-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="900fb-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="900fb-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="900fb-162">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SettingID" ) ， [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="900fb-162">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="900fb-163">作為目前實例之索引鍵的一部分。</span><span class="sxs-lookup"><span data-stu-id="900fb-163">Serves as part of the key for the current instance.</span></span>

</dd> <dt>

<span data-ttu-id="900fb-164">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="900fb-164">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="900fb-165">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="900fb-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="900fb-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="900fb-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="900fb-167">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentVerticalResolution**") ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 監視器解析度 \| 002.3 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 圖元 ") </span><span class="sxs-lookup"><span data-stu-id="900fb-167">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentVerticalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="900fb-168">監視器的垂直解析度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="900fb-168">Monitor's vertical resolution in pixels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="900fb-169">備註</span><span class="sxs-lookup"><span data-stu-id="900fb-169">Remarks</span></span>

<span data-ttu-id="900fb-170">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="900fb-170">WMI does not implement this class.</span></span>

<span data-ttu-id="900fb-171">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="900fb-171">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="900fb-172">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="900fb-172">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="900fb-173">規格需求</span><span class="sxs-lookup"><span data-stu-id="900fb-173">Requirements</span></span>



| <span data-ttu-id="900fb-174">需求</span><span class="sxs-lookup"><span data-stu-id="900fb-174">Requirement</span></span> | <span data-ttu-id="900fb-175">值</span><span class="sxs-lookup"><span data-stu-id="900fb-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="900fb-176">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="900fb-176">Minimum supported client</span></span><br/> | <span data-ttu-id="900fb-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="900fb-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="900fb-178">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="900fb-178">Minimum supported server</span></span><br/> | <span data-ttu-id="900fb-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="900fb-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="900fb-180">命名空間</span><span class="sxs-lookup"><span data-stu-id="900fb-180">Namespace</span></span><br/>                | <span data-ttu-id="900fb-181">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="900fb-181">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="900fb-182">MOF</span><span class="sxs-lookup"><span data-stu-id="900fb-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="900fb-183"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="900fb-183"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="900fb-184">DLL</span><span class="sxs-lookup"><span data-stu-id="900fb-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="900fb-185"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="900fb-185"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="900fb-186">另請參閱</span><span class="sxs-lookup"><span data-stu-id="900fb-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="900fb-187">**CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="900fb-187">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> </dl>

 

