---
description: Win32 \_ PRINTERCONFIGURATION WMI 類別代表印表機裝置的設定。 這包括解析度、色彩、字型和方向等功能。
ms.assetid: b6649da0-ecb0-4ed1-979c-5005837eb474
ms.tgt_platform: multiple
title: Win32_PrinterConfiguration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterConfiguration
- Win32_PrinterConfiguration.Caption
- Win32_PrinterConfiguration.Description
- Win32_PrinterConfiguration.SettingID
- Win32_PrinterConfiguration.BitsPerPel
- Win32_PrinterConfiguration.Collate
- Win32_PrinterConfiguration.Color
- Win32_PrinterConfiguration.Copies
- Win32_PrinterConfiguration.DeviceName
- Win32_PrinterConfiguration.DisplayFlags
- Win32_PrinterConfiguration.DisplayFrequency
- Win32_PrinterConfiguration.DitherType
- Win32_PrinterConfiguration.DriverVersion
- Win32_PrinterConfiguration.Duplex
- Win32_PrinterConfiguration.FormName
- Win32_PrinterConfiguration.HorizontalResolution
- Win32_PrinterConfiguration.ICMIntent
- Win32_PrinterConfiguration.ICMMethod
- Win32_PrinterConfiguration.LogPixels
- Win32_PrinterConfiguration.MediaType
- Win32_PrinterConfiguration.Name
- Win32_PrinterConfiguration.Orientation
- Win32_PrinterConfiguration.PaperLength
- Win32_PrinterConfiguration.PaperSize
- Win32_PrinterConfiguration.PaperWidth
- Win32_PrinterConfiguration.PelsHeight
- Win32_PrinterConfiguration.PelsWidth
- Win32_PrinterConfiguration.PrintQuality
- Win32_PrinterConfiguration.Scale
- Win32_PrinterConfiguration.SpecificationVersion
- Win32_PrinterConfiguration.TTOption
- Win32_PrinterConfiguration.VerticalResolution
- Win32_PrinterConfiguration.XResolution
- Win32_PrinterConfiguration.YResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1927144484dbf427358735fc9d8ed66da56f3d8d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936417"
---
# <a name="win32_printerconfiguration-class"></a><span data-ttu-id="aaf2a-104">Win32 \_ PrinterConfiguration 類別</span><span class="sxs-lookup"><span data-stu-id="aaf2a-104">Win32\_PrinterConfiguration class</span></span>

<span data-ttu-id="aaf2a-105">**Win32 \_ PrinterConfiguration** [WMI 類別](../wmisdk/retrieving-a-class.md)代表印表機裝置的設定。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-105">The **Win32\_PrinterConfiguration** [WMI class](../wmisdk/retrieving-a-class.md) represents the configuration for a printer device.</span></span> <span data-ttu-id="aaf2a-106">這包括解析度、色彩、字型和方向等功能。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-106">This includes capabilities such as resolution, color, fonts, and orientation.</span></span>

<span data-ttu-id="aaf2a-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="aaf2a-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaf2a-109">語法</span><span class="sxs-lookup"><span data-stu-id="aaf2a-109">Syntax</span></span>

``` syntax
class Win32_PrinterConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  uint32  BitsPerPel;
  boolean Collate;
  uint32  Color;
  uint32  Copies;
  string  DeviceName;
  uint32  DisplayFlags;
  uint32  DisplayFrequency;
  uint32  DitherType;
  uint32  DriverVersion;
  boolean Duplex;
  string  FormName;
  uint32  HorizontalResolution;
  uint32  ICMIntent;
  uint32  ICMMethod;
  uint32  LogPixels;
  uint32  MediaType;
  string  Name;
  uint32  Orientation;
  uint32  PaperLength;
  string  PaperSize;
  uint32  PaperWidth;
  uint32  PelsHeight;
  uint32  PelsWidth;
  uint32  PrintQuality;
  uint32  Scale;
  uint32  SpecificationVersion;
  uint32  TTOption;
  uint32  VerticalResolution;
  uint32  XResolution;
  uint32  YResolution;
};
```

## <a name="members"></a><span data-ttu-id="aaf2a-110">成員</span><span class="sxs-lookup"><span data-stu-id="aaf2a-110">Members</span></span>

<span data-ttu-id="aaf2a-111">**Win32 \_ PrinterConfiguration** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="aaf2a-111">The **Win32\_PrinterConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="aaf2a-112">屬性</span><span class="sxs-lookup"><span data-stu-id="aaf2a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aaf2a-113">屬性</span><span class="sxs-lookup"><span data-stu-id="aaf2a-113">Properties</span></span>

<span data-ttu-id="aaf2a-114">**Win32 \_ PrinterConfiguration** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-114">The **Win32\_PrinterConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aaf2a-115">**BitsPerPel**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-115">**BitsPerPel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-116">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-118">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="aaf2a-118">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-119">用來表示此設定中之色彩的位數， (每圖元) 的位數。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-119">Number of bits used to represent the color in this configuration (the bits per pixel).</span></span> <span data-ttu-id="aaf2a-120">這個屬性已經過時。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-120">This property is obsolete.</span></span> <span data-ttu-id="aaf2a-121">相反地，請使用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md)或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) 類別中的屬性來判斷如何表示色彩。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-121">Instead, use properties in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md), or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) classes to determine how color is represented.</span></span>

</dd> <dt>

<span data-ttu-id="aaf2a-122">**標題**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-125">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="aaf2a-125">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-126">目前物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-126">Short textual description of the current object.</span></span>

<span data-ttu-id="aaf2a-127">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-127">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="aaf2a-128">**自動分頁**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-128">**Collate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-129">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-131">若 **為 TRUE**，則應該將列印的頁面分頁。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-131">If **TRUE**, the pages that are printed should be collated.</span></span> <span data-ttu-id="aaf2a-132">若要進行 collate，請在列印下一個複本之前列印出整份檔，而不是列印出檔的每個頁面所需的次數。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-132">To collate is to print out the entire document before printing the next copy, as opposed to printing out each page of the document the required number of times.</span></span>

<span data-ttu-id="aaf2a-133">除非印表機驅動程式表示支援定序，否則會忽略這個屬性。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-133">This property is ignored unless the printer driver indicates support for collation.</span></span>

</dd> <dt>

<span data-ttu-id="aaf2a-134">**色彩**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-134">**Color**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-135">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-137">檔的色彩。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-137">Color of the document.</span></span> <span data-ttu-id="aaf2a-138">有些彩色印表機可以使用 true 黑色來列印，而不是使用青色、洋紅和黃色 (CMY) 的組合。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-138">Some color printers have the capability to print using true black instead of a combination of cyan, magenta, and yellow (CMY).</span></span> <span data-ttu-id="aaf2a-139">這通常會為檔建立深色且更清晰的文字。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-139">This usually creates darker and sharper text for documents.</span></span> <span data-ttu-id="aaf2a-140">此選項僅適用于支援真黑色列印的彩色印表機。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-140">This option is only useful for color printers that support true black printing.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="aaf2a-141"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-141"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="aaf2a-142">單色 (true 黑色) </span><span class="sxs-lookup"><span data-stu-id="aaf2a-142">Monochrome (true black)</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="aaf2a-143"><span id="2"></span>**二級**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-143"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="aaf2a-144">Color</span><span class="sxs-lookup"><span data-stu-id="aaf2a-144">Color</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aaf2a-145">**份數**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-145">**Copies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-146">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-148">要列印的份數。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-148">Number of copies to be printed.</span></span> <span data-ttu-id="aaf2a-149">印表機驅動程式必須支援列印多頁複製。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-149">The printer driver must support printing multi-page copies.</span></span>

<span data-ttu-id="aaf2a-150">範例：2</span><span class="sxs-lookup"><span data-stu-id="aaf2a-150">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="aaf2a-151">**說明**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-154">目前物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-154">Textual description of the current object.</span></span>

<span data-ttu-id="aaf2a-155">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-155">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="aaf2a-156">**DeviceName**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-156">**DeviceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-159">印表機的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-159">Friendly name of the printer.</span></span> <span data-ttu-id="aaf2a-160">此名稱對印表機的類型而言是唯一的，而且可能因為其衍生來源之字串的限制而遭到截斷。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-160">This name is unique to the type of printer and may be truncated because of the limitations of the string from which it is derived.</span></span>

<span data-ttu-id="aaf2a-161">範例： "PCL/HP LaserJet"</span><span class="sxs-lookup"><span data-stu-id="aaf2a-161">Example: "PCL/HP LaserJet"</span></span>

</dd> <dt>

<span data-ttu-id="aaf2a-162">**DisplayFlags**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-162">**DisplayFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-163">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-165">指出顯示裝置為彩色或單色，以及掃描的類型是 noninterlaced 或交錯式。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-165">Indicates whether the display device is color or monochrome and whether the type of scanning is noninterlaced or interlaced.</span></span> <span data-ttu-id="aaf2a-166">這個屬性已經過時。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-166">This property is obsolete.</span></span> <span data-ttu-id="aaf2a-167">相反地，請使用顯示內容，例如 **Win32 \_ DesktopMonitor** 類別的 **DisplayType** 屬性。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-167">Instead, use display properties such as the **DisplayType** property of the **Win32\_DesktopMonitor** class.</span></span>

</dd> <dt>

<span data-ttu-id="aaf2a-168">**DisplayFrequency**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-168">**DisplayFrequency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-169">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-169">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-171">顯示垂直的重新整理頻率。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-171">Displays the vertical refresh rate.</span></span> <span data-ttu-id="aaf2a-172">監視器的重新整理頻率是每秒重繪螢幕 (頻率) 的次數。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-172">The refresh rate for a monitor is the number of times the screen is redrawn per second (frequency).</span></span> <span data-ttu-id="aaf2a-173">這個屬性已經過時。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-173">This property is obsolete.</span></span> <span data-ttu-id="aaf2a-174">請改為使用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md)或 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) 類別中的屬性。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-174">Instead, use properties in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md), or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="aaf2a-175">**DitherType**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-175">**DitherType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-176">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-178">印表機的遞色類型。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-178">Dither type of the printer.</span></span> <span data-ttu-id="aaf2a-179">這個屬性可以假設預先定義的值為1到5，或從6到256的驅動程式定義值。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-179">This property can assume predefined values of 1 to 5, or driver-defined values from 6 to 256.</span></span> <span data-ttu-id="aaf2a-180">線條藝術遞色是一種特殊的遞色方法，可在黑色、白色和灰色 scalings 之間產生定義完善的框線。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-180">Line art dithering is a special dithering method that produces well defined borders between black, white, and gray scalings.</span></span> <span data-ttu-id="aaf2a-181">它不適用於包含濃度和色調（如掃描的相片）中連續 graduations 的影像。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-181">It is not suitable for images that include continuous graduations in intensity and hue, such as scanned photographs.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="aaf2a-182"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-182"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="aaf2a-183">無遞色</span><span class="sxs-lookup"><span data-stu-id="aaf2a-183">No Dithering</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="aaf2a-184"><span id="2"></span>**二級**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-184"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="aaf2a-185">粗略筆刷</span><span class="sxs-lookup"><span data-stu-id="aaf2a-185">Coarse Brush</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="aaf2a-186"><span id="3"></span>**3**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-186"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="aaf2a-187">精細筆刷</span><span class="sxs-lookup"><span data-stu-id="aaf2a-187">Fine Brush</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="aaf2a-188"><span id="4"></span>**億**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-188"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="aaf2a-189">線狀圖</span><span class="sxs-lookup"><span data-stu-id="aaf2a-189">Line Art</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="aaf2a-190"><span id="5"></span>**.5**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-190"><span id="5"></span>**5**</span></span>


</dt> <dd>

<span data-ttu-id="aaf2a-191">灰階</span><span class="sxs-lookup"><span data-stu-id="aaf2a-191">Grayscale</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aaf2a-192">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-192">**DriverVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-193">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-195">以 Windows 為基礎的印表機驅動程式的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-195">Version number of the Windows-based printer driver.</span></span> <span data-ttu-id="aaf2a-196">版本號碼是由驅動程式製造商建立和維護。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-196">The version numbers are created and maintained by the driver manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="aaf2a-197">**雙工**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-197">**Duplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-198">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-200">若 **為 TRUE**，則會在兩端進行列印。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-200">If **TRUE**, printing is done on both sides.</span></span> <span data-ttu-id="aaf2a-201">若 **為 FALSE**，則只會在媒體的一端進行列印。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-201">If **FALSE**, printing is done on only one side of the media.</span></span>

</dd> <dt>

<span data-ttu-id="aaf2a-202">**FormName**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-202">**FormName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-203">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-205">不支援。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-205">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="aaf2a-206">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-206">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-207">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-209">限定詞：每英寸 [**單位**](../wmisdk/standard-qualifiers.md) (每英寸的點數) </span><span class="sxs-lookup"><span data-stu-id="aaf2a-209">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (dots per inch)</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-210">列印工作的 X 軸 (寬度) 的列印解析度以點為單位， (類似于過時的 **XResolution** 屬性) 。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-210">Print resolution in dots per inch along the x-axis (width) of the print job (similar to the obsolete **XResolution** property).</span></span> <span data-ttu-id="aaf2a-211">只有當這個類別的 **PrintQuality** 屬性是正數時，才會設定這個值。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-211">This value is only set when the **PrintQuality** property of this class is positive.</span></span>

</dd> <dt>

<span data-ttu-id="aaf2a-212">**ICMIntent**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-212">**ICMIntent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-213">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-213">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-214">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-215">有三種可能的色彩比對方法的特定值 (稱為意圖) ，預設應該使用。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-215">Specific value of one of the three possible color matching methods (called intents) that should be used by default.</span></span> <span data-ttu-id="aaf2a-216">ICM 應用程式使用 ICM 函數來建立意圖。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-216">ICM applications establish intents by using the ICM functions.</span></span> <span data-ttu-id="aaf2a-217">這個屬性可以假設預先定義的值為1到3，或從4到256的驅動程式定義值。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-217">This property can assume predefined values of 1 to 3, or driver-defined values from 4 to 256.</span></span> <span data-ttu-id="aaf2a-218">非 ICM 應用程式可以使用此值來判斷印表機處理彩色列印工作的方式。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-218">Non-ICM applications can use this value to determine how the printer handles color printing jobs.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="aaf2a-219"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-219"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="aaf2a-220">飽和度</span><span class="sxs-lookup"><span data-stu-id="aaf2a-220">Saturation</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="aaf2a-221"><span id="2"></span>**二級**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-221"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="aaf2a-222">這個</span><span class="sxs-lookup"><span data-stu-id="aaf2a-222">Contrast</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="aaf2a-223"><span id="3"></span>**3**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-223"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="aaf2a-224">確切色彩</span><span class="sxs-lookup"><span data-stu-id="aaf2a-224">Exact Color</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aaf2a-225">**ICMMethod**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-225">**ICMMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-226">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-226">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-227">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-228">處理 ICM 的方式。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-228">How ICM is handled.</span></span> <span data-ttu-id="aaf2a-229">若為非 ICM 應用程式，這個屬性會決定 ICM 是啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-229">For a non-ICM application, this property determines if ICM is enabled or disabled.</span></span> <span data-ttu-id="aaf2a-230">針對 ICM 應用程式，系統會檢查這個屬性，以判斷電腦系統中哪一部分處理 ICM 支援。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-230">For ICM applications, the system examines this property to determine which part of the computer system handles ICM support.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="aaf2a-231"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-231"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="aaf2a-232">Disabled</span><span class="sxs-lookup"><span data-stu-id="aaf2a-232">Disabled</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="aaf2a-233"><span id="2"></span>**二級**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-233"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="aaf2a-234">Windows</span><span class="sxs-lookup"><span data-stu-id="aaf2a-234">Windows</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="aaf2a-235"><span id="3"></span>**3**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-235"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="aaf2a-236">設備磁碟機</span><span class="sxs-lookup"><span data-stu-id="aaf2a-236">Device Driver</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="aaf2a-237"><span id="4"></span>**億**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-237"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="aaf2a-238">裝置</span><span class="sxs-lookup"><span data-stu-id="aaf2a-238">Device</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aaf2a-239">**LogPixels**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-239">**LogPixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-240">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-240">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-241">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-242">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="aaf2a-242">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-243">每個邏輯英寸的圖元數。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-243">Number of pixels per logical inch.</span></span> <span data-ttu-id="aaf2a-244">此過時的屬性僅適用于使用圖元的裝置，這會排除印表機之類的裝置。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-244">This obsolete property is valid only with devices that work with pixels, which excludes devices such as printers.</span></span> <span data-ttu-id="aaf2a-245">沒有適用于印表機的取代值。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-245">There is no replacement value that applies to printers.</span></span>

</dd> <dt>

<span data-ttu-id="aaf2a-246">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-246">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-247">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-247">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-249">印表機列印的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-249">Type of media on which the printer prints.</span></span> <span data-ttu-id="aaf2a-250">屬性可以設定為預先定義的值，或是大於或等於256的驅動程式定義值。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-250">The property can be set to a predefined value or a driver-defined value greater than or equal to 256.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="aaf2a-251"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-251"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="aaf2a-252">標準</span><span class="sxs-lookup"><span data-stu-id="aaf2a-252">Standard</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="aaf2a-253"><span id="2"></span>**二級**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-253"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="aaf2a-254">透明度</span><span class="sxs-lookup"><span data-stu-id="aaf2a-254">Transparency</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="aaf2a-255"><span id="3"></span>**3**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-255"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="aaf2a-256">光澤</span><span class="sxs-lookup"><span data-stu-id="aaf2a-256">Glossy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aaf2a-257">**名稱**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-257">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-258">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-259">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-260">限定詞： [**Key**](../wmisdk/standard-qualifiers.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="aaf2a-260">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-261">與此設定相關聯的印表機名稱。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-261">Name of the printer with which this configuration is associated.</span></span> <span data-ttu-id="aaf2a-262">這個值符合相關聯的 [**Win32 \_ 印表機**](win32-printer.md)實例的 **Name** 屬性。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-262">This value matches the **Name** property of the associated [**Win32\_Printer**](win32-printer.md) instance.</span></span>

</dd> <dt>

<span data-ttu-id="aaf2a-263">**Orientation**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-263">**Orientation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-264">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-265">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-266">列印紙張的方向。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-266">Printing orientation of the paper.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="aaf2a-267"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-267"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="aaf2a-268">直向</span><span class="sxs-lookup"><span data-stu-id="aaf2a-268">Portrait</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="aaf2a-269"><span id="2"></span>**二級**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-269"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="aaf2a-270">橫向</span><span class="sxs-lookup"><span data-stu-id="aaf2a-270">Landscape</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aaf2a-271">**PaperLength**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-271">**PaperLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-272">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-272">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-273">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-274">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) (十分之一毫米) </span><span class="sxs-lookup"><span data-stu-id="aaf2a-274">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (Tenths of a millimeter)</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-275">紙張的長度。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-275">Length of the paper.</span></span> <span data-ttu-id="aaf2a-276">若要以英寸為單位判斷紙張大小，請將此值除以254。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-276">To determine the size of the paper in inches, divide this value by 254.</span></span>

<span data-ttu-id="aaf2a-277">範例：2794</span><span class="sxs-lookup"><span data-stu-id="aaf2a-277">Example: 2794</span></span>

</dd> <dt>

<span data-ttu-id="aaf2a-278">**PaperSize**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-278">**PaperSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-279">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-280">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-281">紙張大小。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-281">Size of the paper.</span></span> <span data-ttu-id="aaf2a-282">可能的大小可在相關聯的 [**Win32 \_ 印表機**](win32-printer.md)類別的 **PaperSizesSupported** 屬性中找到。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-282">The possible sizes are found in the **PaperSizesSupported** property of the associated [**Win32\_Printer**](win32-printer.md) class.</span></span>

<span data-ttu-id="aaf2a-283">範例：「A4 或字母」。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-283">Example: "A4 or Letter".</span></span>

</dd> <dt>

<span data-ttu-id="aaf2a-284">**PaperWidth**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-284">**PaperWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-285">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-286">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-287">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) (十分之一毫米) </span><span class="sxs-lookup"><span data-stu-id="aaf2a-287">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (Tenths of a millimeter)</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-288">紙張的寬度。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-288">Width of the paper.</span></span> <span data-ttu-id="aaf2a-289">若要以英寸為單位判斷紙張大小，請將此值除以254。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-289">To determine the size of the paper in inches, divide this value by 254.</span></span>

<span data-ttu-id="aaf2a-290">範例：2159</span><span class="sxs-lookup"><span data-stu-id="aaf2a-290">Example: 2159</span></span>

</dd> <dt>

<span data-ttu-id="aaf2a-291">**PelsHeight**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-291">**PelsHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-292">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-293">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-294">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="aaf2a-294">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-295">不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-295">This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="aaf2a-296">**PelsWidth**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-296">**PelsWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-297">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-297">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-298">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-299">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="aaf2a-299">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-300">不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-300">This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="aaf2a-301">**PrintQuality**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-301">**PrintQuality**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-302">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-302">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-303">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-304">列印工作的四個品質等級之一。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-304">One of four quality levels of the print job.</span></span> <span data-ttu-id="aaf2a-305">如果指定了正值，則會以每英寸的點來測量品質。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-305">If a positive value is specified, the quality is measured in dots per inch.</span></span>

<dt>

<span id="-1"></span>

<span data-ttu-id="aaf2a-306"><span id="-1"></span>**-1**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-306"><span id="-1"></span>**-1**</span></span>


</dt> <dd>

<span data-ttu-id="aaf2a-307">草稿</span><span class="sxs-lookup"><span data-stu-id="aaf2a-307">Draft</span></span>

</dd> <dt>

<span id="-2"></span>

<span data-ttu-id="aaf2a-308"><span id="-2"></span>**-2.png**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-308"><span id="-2"></span>**-2**</span></span>


</dt> <dd>

<span data-ttu-id="aaf2a-309">低</span><span class="sxs-lookup"><span data-stu-id="aaf2a-309">Low</span></span>

</dd> <dt>

<span id="-3"></span>

<span data-ttu-id="aaf2a-310"><span id="-3"></span>**-3**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-310"><span id="-3"></span>**-3**</span></span>


</dt> <dd>

<span data-ttu-id="aaf2a-311">中</span><span class="sxs-lookup"><span data-stu-id="aaf2a-311">Medium</span></span>

</dd> <dt>

<span id="-4"></span>

<span data-ttu-id="aaf2a-312"><span id="-4"></span>**-4**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-312"><span id="-4"></span>**-4**</span></span>


</dt> <dd>

<span data-ttu-id="aaf2a-313">高</span><span class="sxs-lookup"><span data-stu-id="aaf2a-313">High</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aaf2a-314">**縮放**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-314">**Scale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-315">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-316">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-317">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) (百分比) </span><span class="sxs-lookup"><span data-stu-id="aaf2a-317">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (Percent)</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-318">要調整列印輸出的依據因數。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-318">Factor by which the printed output is to be scaled.</span></span> <span data-ttu-id="aaf2a-319">例如，縮放比例75可將列印輸出縮減為3/4 的原始高度和寬度。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-319">For example, a scale of 75 reduces the print output to 3/4 its original height and width.</span></span>

</dd> <dt>

<span data-ttu-id="aaf2a-320">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-320">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-321">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-322">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-323">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="aaf2a-323">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-324">已知目前物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-324">Identifier by which the current object is known.</span></span>

<span data-ttu-id="aaf2a-325">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-325">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="aaf2a-326">**SpecificationVersion**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-326">**SpecificationVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-327">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-327">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-328">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-329">與以 Windows 為基礎的印表機相關聯之裝置的初始化資料版本號碼。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-329">Version number of the initialization data for the device associated with the Windows-based printer.</span></span>

</dd> <dt>

<span data-ttu-id="aaf2a-330">**TTOption**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-330">**TTOption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-331">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-332">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-333">指出如何列印 TrueType 字型。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-333">Indicates how TrueType fonts should be printed.</span></span>

<dt>

<span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>

<span data-ttu-id="aaf2a-334"><span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>**點陣圖** (1) </span><span class="sxs-lookup"><span data-stu-id="aaf2a-334"><span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>**Bitmap** (1)</span></span>


</dt> <dd>

<span data-ttu-id="aaf2a-335">將 TrueType 字型列印為圖形。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-335">Prints TrueType fonts as graphics.</span></span> <span data-ttu-id="aaf2a-336">這是點陣印表機的預設動作。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-336">This is the default action for dot-matrix printers.</span></span>

</dd> <dt>

<span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>

<span data-ttu-id="aaf2a-337"><span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>**下載** (2) </span><span class="sxs-lookup"><span data-stu-id="aaf2a-337"><span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>**Download** (2)</span></span>


</dt> <dd>

<span data-ttu-id="aaf2a-338">以軟字型下載 TrueType 字型。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-338">Downloads TrueType fonts as soft fonts.</span></span> <span data-ttu-id="aaf2a-339">這是使用印表機控制語言 (PCL) 印表機的預設動作。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-339">This is the default action for printers that use the Printer Control Language (PCL).</span></span>

</dd> <dt>

<span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>

<span data-ttu-id="aaf2a-340"><span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>**替代** (3) </span><span class="sxs-lookup"><span data-stu-id="aaf2a-340"><span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>**Substitute** (3)</span></span>


</dt> <dd>

<span data-ttu-id="aaf2a-341">替代 TrueType 字型的裝置字型。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-341">Substitutes device fonts for TrueType fonts.</span></span> <span data-ttu-id="aaf2a-342">這是 PostScript 印表機的預設動作。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-342">This is the default action for PostScript printers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aaf2a-343">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-343">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-344">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-344">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-345">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-346">限定詞：每英寸 [**單位**](../wmisdk/standard-qualifiers.md) (每英寸的點數) </span><span class="sxs-lookup"><span data-stu-id="aaf2a-346">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (dots per inch)</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-347">沿著 y 軸列印解析度 (列印工作的高度)  (類似于過時的 **YResolution** 屬性) 。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-347">Print resolution along the y-axis (height) of the print job (similar to the obsolete **YResolution** property).</span></span> <span data-ttu-id="aaf2a-348">只有當這個類別的 **PrintQuality** 屬性是正數時，才會設定這個值。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-348">This value is only set when the **PrintQuality** property of this class is positive.</span></span>

</dd> <dt>

<span data-ttu-id="aaf2a-349">**XResolution**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-349">**XResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-350">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-350">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-351">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-352">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="aaf2a-352">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-353">這個屬性已經過時。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-353">This property is obsolete.</span></span> <span data-ttu-id="aaf2a-354">請改用 **HorizontalResolution** 屬性。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-354">Use the **HorizontalResolution** property instead.</span></span>

</dd> <dt>

<span data-ttu-id="aaf2a-355">**YResolution**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-355">**YResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaf2a-356">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-356">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-357">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf2a-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aaf2a-358">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="aaf2a-358">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="aaf2a-359">這個屬性已經過時。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-359">This property is obsolete.</span></span> <span data-ttu-id="aaf2a-360">請改用 **VerticalResolution** 屬性。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-360">Use the **VerticalResolution** property instead.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aaf2a-361">備註</span><span class="sxs-lookup"><span data-stu-id="aaf2a-361">Remarks</span></span>

<span data-ttu-id="aaf2a-362">**Win32 \_ PrinterConfiguration** 類別衍生自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-362">The **Win32\_PrinterConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="aaf2a-363">**概觀**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-363">**Overview**</span></span>

<span data-ttu-id="aaf2a-364">您必須先深入瞭解這些資源，才能判斷如何以最佳方式散發和使用您的列印資源。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-364">Before you can determine how to best distribute and use your printing resources, you must have a detailed knowledge of those resources.</span></span> <span data-ttu-id="aaf2a-365">例如，部門 A 可能只有三個印表機，相較于部門 B 中的五部印表機。但是，如果部門 A 的印表機可以列印每分鐘20頁，而部門 B 中的印表機每分鐘只能列印5個頁面，則部門 A 中的使用者實際上會有更多列印容量。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-365">For example, Department A might have only three printers compared with five printers in Department B. However, if the printers in Department A can print 20 pages per minute and the printers in Department B can print only 5 pages per minute, users in Department A actually have more printing capacity.</span></span> <span data-ttu-id="aaf2a-366">若未知道這些印表機的詳細功能，您可能會誤結論該部門 A 的列印容量很短，因此購買的其他印表機最後將無法使用。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-366">Without knowing the detailed capabilities of these printers, you might erroneously conclude that Department A is short on printing capacity and thus purchase additional printers that end up going unused.</span></span>

<span data-ttu-id="aaf2a-367">WMI 包含兩個類別： [**Win32 \_ 印表機**](win32-printer.md) 和 **win32 \_ PrinterConfiguration**，可用來傳回電腦上所安裝之所有印表機的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-367">WMI includes two classes, [**Win32\_Printer**](win32-printer.md) and **Win32\_PrinterConfiguration**, which can be used to return detailed information about all the printers installed on a computer.</span></span>

## <a name="examples"></a><span data-ttu-id="aaf2a-368">範例</span><span class="sxs-lookup"><span data-stu-id="aaf2a-368">Examples</span></span>

<span data-ttu-id="aaf2a-369">下列程式碼範例會抓取印表機資訊。</span><span class="sxs-lookup"><span data-stu-id="aaf2a-369">The following code sample retrieves printer information.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colInstalledPrinters = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_PrinterConfiguration")
For Each objPrinter in colInstalledPrinters
 Wscript.Echo "Name: " & objPrinter.Name
 Wscript.Echo "Collate: " & objPrinter.Collate
 Wscript.Echo "Copies: " & objPrinter.Copies
 Wscript.Echo "Driver Version: " & objPrinter.DriverVersion
 Wscript.Echo "Duplex: " & objPrinter.Duplex
 Wscript.Echo "Horizontal Resolution: " & _
 objPrinter.HorizontalResolution
 If objPrinter.Orientation = 1 Then
 strOrientation = "Portrait"
 Else
 strOrientation = "Landscape"
 End If
 Wscript.Echo "Orientation : " & strOrientation
 Wscript.Echo "Paper Length: " & objPrinter.PaperLength / 254
 Wscript.Echo "Paper Width: " & objPrinter.PaperWidth / 254
 Wscript.Echo "Print Quality: " & objPrinter.PrintQuality
 Wscript.Echo "Scale: " & objPrinter.Scale
 Wscript.Echo "Specification Version: " & _
 objPrinter.SpecificationVersion
 If objPrinter.TTOption = 1 Then
 strTTOption = "Print TrueType fonts as graphics."
 ElseIf objPrinter.TTOption = 2 Then
 strTTOption = "Download TrueType fonts as soft fonts."
 Else
 strTTOption = "Substitute device fonts for TrueType fonts."
 End If
 Wscript.Echo "True Type Option: " & strTTOption
 Wscript.Echo "Vertical Resolution: " & objPrinter.VerticalResolution
Next
```



## <a name="requirements"></a><span data-ttu-id="aaf2a-370">規格需求</span><span class="sxs-lookup"><span data-stu-id="aaf2a-370">Requirements</span></span>



| <span data-ttu-id="aaf2a-371">需求</span><span class="sxs-lookup"><span data-stu-id="aaf2a-371">Requirement</span></span> | <span data-ttu-id="aaf2a-372">值</span><span class="sxs-lookup"><span data-stu-id="aaf2a-372">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="aaf2a-373">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aaf2a-373">Minimum supported client</span></span><br/> | <span data-ttu-id="aaf2a-374">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aaf2a-374">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="aaf2a-375">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aaf2a-375">Minimum supported server</span></span><br/> | <span data-ttu-id="aaf2a-376">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aaf2a-376">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="aaf2a-377">命名空間</span><span class="sxs-lookup"><span data-stu-id="aaf2a-377">Namespace</span></span><br/>                | <span data-ttu-id="aaf2a-378">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="aaf2a-378">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="aaf2a-379">MOF</span><span class="sxs-lookup"><span data-stu-id="aaf2a-379">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aaf2a-380"><dt>Win32 \_ 印表機。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="aaf2a-380"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="aaf2a-381">DLL</span><span class="sxs-lookup"><span data-stu-id="aaf2a-381">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aaf2a-382"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aaf2a-382"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="aaf2a-383">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aaf2a-383">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaf2a-384">**CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="aaf2a-384">**CIM\_Setting**</span></span>](./cim-setting.md)
</dt> <dt>

[<span data-ttu-id="aaf2a-385">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="aaf2a-385">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
