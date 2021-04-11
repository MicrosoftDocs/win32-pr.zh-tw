---
description: Win32 \_ DISPLAYCONTROLLERCONFIGURATION WMI 類別代表執行 Windows 之電腦系統的視訊卡設定資訊。
ms.assetid: 36ebd840-5e8c-411a-828d-38972fe956e2
ms.tgt_platform: multiple
title: Win32_DisplayControllerConfiguration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DisplayControllerConfiguration
- Win32_DisplayControllerConfiguration.Caption
- Win32_DisplayControllerConfiguration.Description
- Win32_DisplayControllerConfiguration.SettingID
- Win32_DisplayControllerConfiguration.BitsPerPixel
- Win32_DisplayControllerConfiguration.ColorPlanes
- Win32_DisplayControllerConfiguration.DeviceEntriesInAColorTable
- Win32_DisplayControllerConfiguration.DeviceSpecificPens
- Win32_DisplayControllerConfiguration.HorizontalResolution
- Win32_DisplayControllerConfiguration.Name
- Win32_DisplayControllerConfiguration.RefreshRate
- Win32_DisplayControllerConfiguration.ReservedSystemPaletteEntries
- Win32_DisplayControllerConfiguration.SystemPaletteEntries
- Win32_DisplayControllerConfiguration.VerticalResolution
- Win32_DisplayControllerConfiguration.VideoMode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8e64f99cb4d4715d9b7a0eb88bd2e7629feed853
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111220"
---
# <a name="win32_displaycontrollerconfiguration-class"></a><span data-ttu-id="7edd5-103">Win32 \_ DisplayControllerConfiguration 類別</span><span class="sxs-lookup"><span data-stu-id="7edd5-103">Win32\_DisplayControllerConfiguration class</span></span>

<span data-ttu-id="7edd5-104">**Win32 \_ DisplayControllerConfiguration** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表執行 Windows 之電腦系統的視訊卡設定資訊。</span><span class="sxs-lookup"><span data-stu-id="7edd5-104">The **Win32\_DisplayControllerConfiguration** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the video adapter configuration information of a computer system running Windows.</span></span>

<span data-ttu-id="7edd5-105">這個類別已經過時。</span><span class="sxs-lookup"><span data-stu-id="7edd5-105">This class is obsolete.</span></span> <span data-ttu-id="7edd5-106">若要取代這個類別，您應該使用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md)和 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) 類別中的屬性。</span><span class="sxs-lookup"><span data-stu-id="7edd5-106">In place of this class, you should use the properties in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md), and [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) classes.</span></span>

<span data-ttu-id="7edd5-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="7edd5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7edd5-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="7edd5-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7edd5-109">語法</span><span class="sxs-lookup"><span data-stu-id="7edd5-109">Syntax</span></span>

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), UUID("{8502C4E5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DisplayControllerConfiguration : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 BitsPerPixel;
  uint32 ColorPlanes;
  uint32 DeviceEntriesInAColorTable;
  uint32 DeviceSpecificPens;
  uint32 HorizontalResolution;
  string Name;
  sint32 RefreshRate;
  uint32 ReservedSystemPaletteEntries;
  uint32 SystemPaletteEntries;
  uint32 VerticalResolution;
  string VideoMode;
};
```

## <a name="members"></a><span data-ttu-id="7edd5-110">成員</span><span class="sxs-lookup"><span data-stu-id="7edd5-110">Members</span></span>

<span data-ttu-id="7edd5-111">**Win32 \_ DisplayControllerConfiguration** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7edd5-111">The **Win32\_DisplayControllerConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="7edd5-112">屬性</span><span class="sxs-lookup"><span data-stu-id="7edd5-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7edd5-113">屬性</span><span class="sxs-lookup"><span data-stu-id="7edd5-113">Properties</span></span>

<span data-ttu-id="7edd5-114">**Win32 \_ DisplayControllerConfiguration** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7edd5-114">The **Win32\_DisplayControllerConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7edd5-115">**BitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="7edd5-115">**BitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7edd5-116">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7edd5-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7edd5-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7edd5-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7edd5-118">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| BITSPIXEL" ) </span><span class="sxs-lookup"><span data-stu-id="7edd5-118">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|BITSPIXEL")</span></span>
</dt> </dl>

<span data-ttu-id="7edd5-119">用來表示此設定中之色彩的位數，或每個圖元中的位數。</span><span class="sxs-lookup"><span data-stu-id="7edd5-119">Either the number of bits used to represent the color in this configuration, or the bits in each pixel.</span></span>

<span data-ttu-id="7edd5-120">範例：8</span><span class="sxs-lookup"><span data-stu-id="7edd5-120">Example: 8</span></span>

</dd> <dt>

<span data-ttu-id="7edd5-121">**標題**</span><span class="sxs-lookup"><span data-stu-id="7edd5-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7edd5-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7edd5-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7edd5-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7edd5-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7edd5-124">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="7edd5-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7edd5-125">目前物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="7edd5-125">Short textual description of the current object.</span></span>

<span data-ttu-id="7edd5-126">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="7edd5-126">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="7edd5-127">**ColorPlanes**</span><span class="sxs-lookup"><span data-stu-id="7edd5-127">**ColorPlanes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7edd5-128">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7edd5-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7edd5-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7edd5-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7edd5-130">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API 裝置內容函式 \| \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| 平面」 ) </span><span class="sxs-lookup"><span data-stu-id="7edd5-130">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|PLANES")</span></span>
</dt> </dl>

<span data-ttu-id="7edd5-131">顯示設定中使用的目前色彩平面數目。</span><span class="sxs-lookup"><span data-stu-id="7edd5-131">Current number of color planes used in the display configuration.</span></span> <span data-ttu-id="7edd5-132">色彩平面是代表圖元色彩的另一種方式。</span><span class="sxs-lookup"><span data-stu-id="7edd5-132">A color plane is another way to represent pixel colors.</span></span> <span data-ttu-id="7edd5-133">色彩平面會將圖形分隔為每個主要色彩元件 (紅色、綠色、藍色) ，並將其儲存在自己的平面中，而不是將單一 RGB 值指派給每個圖元。</span><span class="sxs-lookup"><span data-stu-id="7edd5-133">Instead of assigning a single RGB value to each pixel, color planes separate the graphic into each of the primary color components (red, green, blue), and stores them in their own planes.</span></span> <span data-ttu-id="7edd5-134">這可讓您在8位和16位的影片系統上有更高的色彩深度。</span><span class="sxs-lookup"><span data-stu-id="7edd5-134">This allows for greater color depths on 8-bit and 16-bit video systems.</span></span> <span data-ttu-id="7edd5-135">呈現圖形系統的 bitwidth 夠大，足以儲存色彩深度資訊，也就是說，只需要一個色彩平面。</span><span class="sxs-lookup"><span data-stu-id="7edd5-135">Present graphics systems have the bitwidth large enough to store color depth information, meaning only one color plane is needed.</span></span>

<span data-ttu-id="7edd5-136">範例：1</span><span class="sxs-lookup"><span data-stu-id="7edd5-136">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="7edd5-137">**說明**</span><span class="sxs-lookup"><span data-stu-id="7edd5-137">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7edd5-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7edd5-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7edd5-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7edd5-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7edd5-140">目前物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="7edd5-140">Textual description of the current object.</span></span>

<span data-ttu-id="7edd5-141">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="7edd5-141">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="7edd5-142">**DeviceEntriesInAColorTable**</span><span class="sxs-lookup"><span data-stu-id="7edd5-142">**DeviceEntriesInAColorTable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7edd5-143">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7edd5-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7edd5-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7edd5-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7edd5-145">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| NUMCOLORS" ) </span><span class="sxs-lookup"><span data-stu-id="7edd5-145">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|NUMCOLORS")</span></span>
</dt> </dl>

<span data-ttu-id="7edd5-146">顯示裝置的色彩表中的色彩索引數目 (如果裝置的色彩深度為每圖元) 不超過8位。</span><span class="sxs-lookup"><span data-stu-id="7edd5-146">Number of color indexes in a color table of a display device (if the device has a color depth of no more than 8 bits per pixel).</span></span> <span data-ttu-id="7edd5-147">如果裝置具有較高的色彩深度，則會傳回-1。</span><span class="sxs-lookup"><span data-stu-id="7edd5-147">For devices with greater color depths, -1 is returned.</span></span>

<span data-ttu-id="7edd5-148">範例：256</span><span class="sxs-lookup"><span data-stu-id="7edd5-148">Example: 256</span></span>

</dd> <dt>

<span data-ttu-id="7edd5-149">**DeviceSpecificPens**</span><span class="sxs-lookup"><span data-stu-id="7edd5-149">**DeviceSpecificPens**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7edd5-150">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7edd5-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7edd5-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7edd5-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7edd5-152">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| NUMPENS" ) </span><span class="sxs-lookup"><span data-stu-id="7edd5-152">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|NUMPENS")</span></span>
</dt> </dl>

<span data-ttu-id="7edd5-153">裝置特定畫筆的目前數目。</span><span class="sxs-lookup"><span data-stu-id="7edd5-153">Current number of device-specific pens.</span></span> <span data-ttu-id="7edd5-154">0xFFFFFFFF 的值表示裝置不支援畫筆。</span><span class="sxs-lookup"><span data-stu-id="7edd5-154">A value of 0xFFFFFFFF means the device does not support pens.</span></span> <span data-ttu-id="7edd5-155">畫筆是可由顯示控制器指派以顯示裝置的邏輯屬性，可用來繪製線條、多邊形框線和文字。</span><span class="sxs-lookup"><span data-stu-id="7edd5-155">Pens are logical properties that can be assigned by the display controller to display devices, and are used to draw lines, borders of polygons, and text.</span></span>

<span data-ttu-id="7edd5-156">範例：3</span><span class="sxs-lookup"><span data-stu-id="7edd5-156">Example: 3</span></span>

</dd> <dt>

<span data-ttu-id="7edd5-157">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="7edd5-157">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7edd5-158">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7edd5-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7edd5-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7edd5-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7edd5-160">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| HORZRES" ) ，[**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "圖元" ) </span><span class="sxs-lookup"><span data-stu-id="7edd5-160">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|HORZRES"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="7edd5-161">水準方向的目前圖元數目 (X 軸) 顯示。</span><span class="sxs-lookup"><span data-stu-id="7edd5-161">Current number of pixels in the horizontal direction (x-axis) of the display.</span></span>

<span data-ttu-id="7edd5-162">範例：1024</span><span class="sxs-lookup"><span data-stu-id="7edd5-162">Example: 1024</span></span>

</dd> <dt>

<span data-ttu-id="7edd5-163">**名稱**</span><span class="sxs-lookup"><span data-stu-id="7edd5-163">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7edd5-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7edd5-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7edd5-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7edd5-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7edd5-166">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="7edd5-166">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="7edd5-167">此設定中使用的介面卡名稱。</span><span class="sxs-lookup"><span data-stu-id="7edd5-167">Name of the adapter used in this configuration.</span></span>

</dd> <dt>

<span data-ttu-id="7edd5-168">**RefreshRate**</span><span class="sxs-lookup"><span data-stu-id="7edd5-168">**RefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7edd5-169">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="7edd5-169">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7edd5-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7edd5-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7edd5-171">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| HORZRESVREFRESH" ) ，[**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "赫茲" ) </span><span class="sxs-lookup"><span data-stu-id="7edd5-171">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|HORZRESVREFRESH"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="7edd5-172">視訊卡的更新頻率。</span><span class="sxs-lookup"><span data-stu-id="7edd5-172">Refresh rate of the video adapter.</span></span> <span data-ttu-id="7edd5-173">值為 0 (零) 或 1 (一個) 表示正在使用預設費率。</span><span class="sxs-lookup"><span data-stu-id="7edd5-173">A value of 0 (zero) or 1 (one) indicates a default rate is being used.</span></span> <span data-ttu-id="7edd5-174">-1 值表示使用的是最佳的速率。</span><span class="sxs-lookup"><span data-stu-id="7edd5-174">A value of -1 indicates that an optimal rate is being used.</span></span>

<span data-ttu-id="7edd5-175">範例：72</span><span class="sxs-lookup"><span data-stu-id="7edd5-175">Example: 72</span></span>

</dd> <dt>

<span data-ttu-id="7edd5-176">**ReservedSystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="7edd5-176">**ReservedSystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7edd5-177">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7edd5-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7edd5-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7edd5-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7edd5-179">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| NUMRESERVED" ) </span><span class="sxs-lookup"><span data-stu-id="7edd5-179">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|NUMRESERVED")</span></span>
</dt> </dl>

<span data-ttu-id="7edd5-180">保留供系統使用的目前色彩索引項目數目。</span><span class="sxs-lookup"><span data-stu-id="7edd5-180">Current number of color index entries reserved for system use.</span></span> <span data-ttu-id="7edd5-181">此值僅適用于使用索引調色板的顯示設定。</span><span class="sxs-lookup"><span data-stu-id="7edd5-181">This value is only valid for display settings that use an indexed palette.</span></span> <span data-ttu-id="7edd5-182">索引的調色板不會用於每圖元8位以上的色彩深度。</span><span class="sxs-lookup"><span data-stu-id="7edd5-182">Indexed palettes are not used for color depths greater than 8 bits per pixel.</span></span> <span data-ttu-id="7edd5-183">如果色彩深度超過每圖元8位，此值會設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7edd5-183">If the color depth is more than 8 bits per pixel, this value is set to **NULL**.</span></span>

<span data-ttu-id="7edd5-184">範例：20</span><span class="sxs-lookup"><span data-stu-id="7edd5-184">Example: 20</span></span>

</dd> <dt>

<span data-ttu-id="7edd5-185">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="7edd5-185">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7edd5-186">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7edd5-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7edd5-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7edd5-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7edd5-188">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="7edd5-188">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7edd5-189">已知目前物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7edd5-189">Identifier by which the current object is known.</span></span>

<span data-ttu-id="7edd5-190">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="7edd5-190">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="7edd5-191">**SystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="7edd5-191">**SystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7edd5-192">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7edd5-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7edd5-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7edd5-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7edd5-194">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| NUMRESERVED" ) </span><span class="sxs-lookup"><span data-stu-id="7edd5-194">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|NUMRESERVED")</span></span>
</dt> </dl>

<span data-ttu-id="7edd5-195">保留供系統使用的目前色彩索引項目數目。</span><span class="sxs-lookup"><span data-stu-id="7edd5-195">Current number of color index entries reserved for system use.</span></span> <span data-ttu-id="7edd5-196">此值僅適用于使用索引調色板的顯示設定。</span><span class="sxs-lookup"><span data-stu-id="7edd5-196">This value is only valid for display settings that use an indexed palette.</span></span> <span data-ttu-id="7edd5-197">索引的調色板不會用於每圖元8位以上的色彩深度。</span><span class="sxs-lookup"><span data-stu-id="7edd5-197">Indexed palettes are not used for color depths greater than 8 bits per pixel.</span></span> <span data-ttu-id="7edd5-198">如果色彩深度超過每圖元8位，此值會設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7edd5-198">If the color depth is more than 8 bits per pixel, this value is set to **NULL**.</span></span>

<span data-ttu-id="7edd5-199">範例：20</span><span class="sxs-lookup"><span data-stu-id="7edd5-199">Example: 20</span></span>

</dd> <dt>

<span data-ttu-id="7edd5-200">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="7edd5-200">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7edd5-201">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7edd5-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7edd5-202">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7edd5-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7edd5-203">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Device CoNtext 函數 \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| VERTRES" ) ，[**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "圖元" ) </span><span class="sxs-lookup"><span data-stu-id="7edd5-203">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|VERTRES"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="7edd5-204">垂直方向的目前圖元數 (y 軸) 顯示。</span><span class="sxs-lookup"><span data-stu-id="7edd5-204">Current number of pixels in the vertical direction (y-axis) of the display.</span></span>

<span data-ttu-id="7edd5-205">範例：768</span><span class="sxs-lookup"><span data-stu-id="7edd5-205">Example: 768</span></span>

</dd> <dt>

<span data-ttu-id="7edd5-206">**VideoMode**</span><span class="sxs-lookup"><span data-stu-id="7edd5-206">**VideoMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7edd5-207">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7edd5-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7edd5-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7edd5-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7edd5-209">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="7edd5-209">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="7edd5-210">使用者可讀取的目前螢幕解析度和色彩設定的描述。</span><span class="sxs-lookup"><span data-stu-id="7edd5-210">User-readable description of the current screen resolution and color setting of the display.</span></span>

<span data-ttu-id="7edd5-211">範例： "1024 768 with 256 colors"</span><span class="sxs-lookup"><span data-stu-id="7edd5-211">Example: "1024   768 with 256 colors"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7edd5-212">備註</span><span class="sxs-lookup"><span data-stu-id="7edd5-212">Remarks</span></span>

<span data-ttu-id="7edd5-213">**Win32 \_ DisplayControllerConfiguration** 類別衍生自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="7edd5-213">The **Win32\_DisplayControllerConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7edd5-214">規格需求</span><span class="sxs-lookup"><span data-stu-id="7edd5-214">Requirements</span></span>



| <span data-ttu-id="7edd5-215">需求</span><span class="sxs-lookup"><span data-stu-id="7edd5-215">Requirement</span></span> | <span data-ttu-id="7edd5-216">值</span><span class="sxs-lookup"><span data-stu-id="7edd5-216">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7edd5-217">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7edd5-217">Minimum supported client</span></span><br/> | <span data-ttu-id="7edd5-218">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7edd5-218">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7edd5-219">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7edd5-219">Minimum supported server</span></span><br/> | <span data-ttu-id="7edd5-220">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7edd5-220">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7edd5-221">命名空間</span><span class="sxs-lookup"><span data-stu-id="7edd5-221">Namespace</span></span><br/>                | <span data-ttu-id="7edd5-222">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7edd5-222">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7edd5-223">MOF</span><span class="sxs-lookup"><span data-stu-id="7edd5-223">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7edd5-224"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="7edd5-224"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7edd5-225">DLL</span><span class="sxs-lookup"><span data-stu-id="7edd5-225">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7edd5-226"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7edd5-226"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7edd5-227">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7edd5-227">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7edd5-228">**CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="7edd5-228">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="7edd5-229">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="7edd5-229">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

