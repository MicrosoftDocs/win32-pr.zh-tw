---
description: CIM \_ VideoControllerResolution 類別代表影片控制器可支援的各種影片模式。
ms.assetid: 954ac3fe-9777-460c-8929-853f19379256
ms.tgt_platform: multiple
title: CIM_VideoControllerResolution 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoControllerResolution
- CIM_VideoControllerResolution.Caption
- CIM_VideoControllerResolution.Description
- CIM_VideoControllerResolution.SettingID
- CIM_VideoControllerResolution.HorizontalResolution
- CIM_VideoControllerResolution.MaxRefreshRate
- CIM_VideoControllerResolution.MinRefreshRate
- CIM_VideoControllerResolution.NumberOfColors
- CIM_VideoControllerResolution.RefreshRate
- CIM_VideoControllerResolution.ScanMode
- CIM_VideoControllerResolution.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d448d92d79163bc6a4e1056e88434081c5878159
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847573"
---
# <a name="cim_videocontrollerresolution-class"></a><span data-ttu-id="93ac1-103">CIM \_ VideoControllerResolution 類別</span><span class="sxs-lookup"><span data-stu-id="93ac1-103">CIM\_VideoControllerResolution class</span></span>

<span data-ttu-id="93ac1-104">**CIM \_ VideoControllerResolution** 類別代表影片控制器可支援的各種影片模式。</span><span class="sxs-lookup"><span data-stu-id="93ac1-104">The **CIM\_VideoControllerResolution** class represents the various video modes that a video controller can support.</span></span> <span data-ttu-id="93ac1-105">影片模式是以可能的水準和垂直解析度、重新整理頻率、掃描模式，以及控制器支援的色彩設定數目來定義。</span><span class="sxs-lookup"><span data-stu-id="93ac1-105">Video modes are defined by the possible horizontal and vertical resolutions, refresh rate, scan mode, and number of color settings supported by a controller.</span></span> <span data-ttu-id="93ac1-106">實際使用的解決方式是在 [**CIM \_ VideoController**](cim-videocontroller.md) 物件中指定的值。</span><span class="sxs-lookup"><span data-stu-id="93ac1-106">The actual resolutions in use are the values specified in the [**CIM\_VideoController**](cim-videocontroller.md) object.</span></span>

<span data-ttu-id="93ac1-107">與 Windows 顯示驅動程式模型不相容的硬體 (WDDM) 會傳回這個類別之實例的不正確屬性值。</span><span class="sxs-lookup"><span data-stu-id="93ac1-107">Hardware that is not compatible with Windows Display Driver Model (WDDM) returns inaccurate property values for instances of this class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="93ac1-108">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="93ac1-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="93ac1-109">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="93ac1-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="93ac1-110">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="93ac1-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="93ac1-111">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="93ac1-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="93ac1-112">語法</span><span class="sxs-lookup"><span data-stu-id="93ac1-112">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCEA-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_VideoControllerResolution : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 HorizontalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint64 NumberOfColors;
  uint32 RefreshRate;
  uint16 ScanMode;
  uint32 VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="93ac1-113">成員</span><span class="sxs-lookup"><span data-stu-id="93ac1-113">Members</span></span>

<span data-ttu-id="93ac1-114">**CIM \_ VideoControllerResolution** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="93ac1-114">The **CIM\_VideoControllerResolution** class has these types of members:</span></span>

-   [<span data-ttu-id="93ac1-115">屬性</span><span class="sxs-lookup"><span data-stu-id="93ac1-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="93ac1-116">屬性</span><span class="sxs-lookup"><span data-stu-id="93ac1-116">Properties</span></span>

<span data-ttu-id="93ac1-117">**CIM \_ VideoControllerResolution** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="93ac1-117">The **CIM\_VideoControllerResolution** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="93ac1-118">**標題**</span><span class="sxs-lookup"><span data-stu-id="93ac1-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ac1-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="93ac1-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93ac1-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="93ac1-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ac1-121">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="93ac1-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="93ac1-122">目前物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="93ac1-122">Short textual description of the current object.</span></span>

<span data-ttu-id="93ac1-123">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="93ac1-123">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="93ac1-124">**說明**</span><span class="sxs-lookup"><span data-stu-id="93ac1-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ac1-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="93ac1-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93ac1-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="93ac1-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93ac1-127">目前物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="93ac1-127">Textual description of the current object.</span></span>

<span data-ttu-id="93ac1-128">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="93ac1-128">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="93ac1-129">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="93ac1-129">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ac1-130">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="93ac1-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ac1-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="93ac1-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ac1-132">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentHorizontalResolution**") ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 監視器解析度 \| 002.2 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 圖元 ") </span><span class="sxs-lookup"><span data-stu-id="93ac1-132">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentHorizontalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="93ac1-133">水準解析度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="93ac1-133">Horizontal resolution, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="93ac1-134">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="93ac1-134">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ac1-135">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="93ac1-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ac1-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="93ac1-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ac1-137">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VideoController**](cim-videocontroller.md).**MaxRefreshRate**") ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 監視器解析度 \| 002.7 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 赫茲 ") </span><span class="sxs-lookup"><span data-stu-id="93ac1-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**MaxRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="93ac1-138">在指定的解析度（以赫茲為單位）支援速率範圍時的最大重新整理頻率。</span><span class="sxs-lookup"><span data-stu-id="93ac1-138">Maximum refresh rate when a range of rates is supported at the specified resolutions, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="93ac1-139">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="93ac1-139">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ac1-140">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="93ac1-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ac1-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="93ac1-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ac1-142">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VideoController**](cim-videocontroller.md).**MinRefreshRate**") ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 監視器解析度 \| 002.6 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 赫茲 ") </span><span class="sxs-lookup"><span data-stu-id="93ac1-142">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**MinRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="93ac1-143">在指定的解析度（以赫茲為單位）支援速率範圍時的最小重新整理頻率。</span><span class="sxs-lookup"><span data-stu-id="93ac1-143">Minimum refresh rate when a range of rates is supported at the specified resolutions, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="93ac1-144">**NumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="93ac1-144">**NumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ac1-145">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="93ac1-145">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93ac1-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="93ac1-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ac1-147">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentNumberOfColors**") </span><span class="sxs-lookup"><span data-stu-id="93ac1-147">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentNumberOfColors**")</span></span>
</dt> </dl>

<span data-ttu-id="93ac1-148">目前解析度所支援的色彩數目。</span><span class="sxs-lookup"><span data-stu-id="93ac1-148">Number of colors supported at the current resolution.</span></span>

<span data-ttu-id="93ac1-149">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="93ac1-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="93ac1-150">**RefreshRate**</span><span class="sxs-lookup"><span data-stu-id="93ac1-150">**RefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ac1-151">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="93ac1-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ac1-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="93ac1-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ac1-153">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentRefreshRate**") ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 監視器解析度 \| 002.4 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 赫茲 ") </span><span class="sxs-lookup"><span data-stu-id="93ac1-153">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="93ac1-154">更新頻率（以赫茲為單位）。</span><span class="sxs-lookup"><span data-stu-id="93ac1-154">Refresh rate, in hertz.</span></span> <span data-ttu-id="93ac1-155">如果支援的速率範圍，請使用 **MinRefreshRate** 和 **MaxRefreshRate** 屬性，並將此屬性設定為0。</span><span class="sxs-lookup"><span data-stu-id="93ac1-155">If a range of rates is supported, use the **MinRefreshRate** and **MaxRefreshRate** properties, and set this property to 0.</span></span>

</dd> <dt>

<span data-ttu-id="93ac1-156">**ScanMode**</span><span class="sxs-lookup"><span data-stu-id="93ac1-156">**ScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ac1-157">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="93ac1-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93ac1-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="93ac1-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ac1-159">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentScanMode**") ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 監視器解析度 \| 002.5 ") </span><span class="sxs-lookup"><span data-stu-id="93ac1-159">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentScanMode**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="93ac1-160">控制器操作的掃描模式。</span><span class="sxs-lookup"><span data-stu-id="93ac1-160">Scan mode at which the controller operates.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="93ac1-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="93ac1-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="93ac1-162"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="93ac1-162"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="93ac1-163"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (3) </span><span class="sxs-lookup"><span data-stu-id="93ac1-163"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

<span data-ttu-id="93ac1-164"><span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span> (4) **的非交錯操作**</span><span class="sxs-lookup"><span data-stu-id="93ac1-164"><span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Non-Interlaced Operation** (4)</span></span>


</dt> <dd>

<span data-ttu-id="93ac1-165">Noninterlaced 操作</span><span class="sxs-lookup"><span data-stu-id="93ac1-165">Noninterlaced operation</span></span>

</dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

<span data-ttu-id="93ac1-166"><span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**交錯操作** (5) </span><span class="sxs-lookup"><span data-stu-id="93ac1-166"><span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**Interlaced Operation** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="93ac1-167">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="93ac1-167">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ac1-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="93ac1-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93ac1-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="93ac1-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ac1-170">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SettingID" ) ， [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="93ac1-170">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="93ac1-171">作為目前實例之索引鍵一部分的識別碼。</span><span class="sxs-lookup"><span data-stu-id="93ac1-171">An ID that serves as part of the key for the current instance.</span></span>

</dd> <dt>

<span data-ttu-id="93ac1-172">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="93ac1-172">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ac1-173">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="93ac1-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ac1-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="93ac1-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ac1-175">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentVerticalResolution**") ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 監視器解析度 \| 002.3 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 圖元 ") </span><span class="sxs-lookup"><span data-stu-id="93ac1-175">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentVerticalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="93ac1-176">控制器的垂直解析度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="93ac1-176">Controller's vertical resolution, in pixels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93ac1-177">備註</span><span class="sxs-lookup"><span data-stu-id="93ac1-177">Remarks</span></span>

<span data-ttu-id="93ac1-178">WMI 會實行 **CIM \_ VideoControllerResolution** 類別。</span><span class="sxs-lookup"><span data-stu-id="93ac1-178">WMI implements the **CIM\_VideoControllerResolution** class.</span></span> <span data-ttu-id="93ac1-179">**CIM \_ VideoControllerResolution** 類別是動態類別。</span><span class="sxs-lookup"><span data-stu-id="93ac1-179">The **CIM\_VideoControllerResolution** class is a dynamic class.</span></span>

<span data-ttu-id="93ac1-180">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="93ac1-180">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="93ac1-181">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="93ac1-181">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

<span data-ttu-id="93ac1-182">請注意，這個類別是基類。</span><span class="sxs-lookup"><span data-stu-id="93ac1-182">Note that this class is a base class.</span></span> <span data-ttu-id="93ac1-183">如果您嘗試透過 WMI 存取您的影片控制器，您可能會想要改用 [**Win32 \_ VideoController**](win32-videocontroller.md) 。</span><span class="sxs-lookup"><span data-stu-id="93ac1-183">If you are attempting to access your video controller through WMI, you may wish to use [**Win32\_VideoController**](win32-videocontroller.md) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="93ac1-184">規格需求</span><span class="sxs-lookup"><span data-stu-id="93ac1-184">Requirements</span></span>



| <span data-ttu-id="93ac1-185">需求</span><span class="sxs-lookup"><span data-stu-id="93ac1-185">Requirement</span></span> | <span data-ttu-id="93ac1-186">值</span><span class="sxs-lookup"><span data-stu-id="93ac1-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93ac1-187">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93ac1-187">Minimum supported client</span></span><br/> | <span data-ttu-id="93ac1-188">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93ac1-188">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="93ac1-189">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93ac1-189">Minimum supported server</span></span><br/> | <span data-ttu-id="93ac1-190">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93ac1-190">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="93ac1-191">命名空間</span><span class="sxs-lookup"><span data-stu-id="93ac1-191">Namespace</span></span><br/>                | <span data-ttu-id="93ac1-192">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="93ac1-192">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="93ac1-193">MOF</span><span class="sxs-lookup"><span data-stu-id="93ac1-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93ac1-194"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="93ac1-194"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="93ac1-195">DLL</span><span class="sxs-lookup"><span data-stu-id="93ac1-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93ac1-196"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93ac1-196"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93ac1-197">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93ac1-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93ac1-198">**CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="93ac1-198">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> </dl>

 

