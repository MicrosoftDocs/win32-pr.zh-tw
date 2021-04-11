---
description: Win32 \_ DesktopWMI 類別代表使用者桌面的一般特性。 使用者可以修改這個類別的屬性，以自訂桌面。
ms.assetid: 9615a443-7611-4c30-9693-ea71b09b013b
ms.tgt_platform: multiple
title: Win32_Desktop 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Desktop
- Win32_Desktop.Caption
- Win32_Desktop.Description
- Win32_Desktop.SettingID
- Win32_Desktop.BorderWidth
- Win32_Desktop.CoolSwitch
- Win32_Desktop.CursorBlinkRate
- Win32_Desktop.DragFullWindows
- Win32_Desktop.GridGranularity
- Win32_Desktop.IconSpacing
- Win32_Desktop.IconTitleFaceName
- Win32_Desktop.IconTitleSize
- Win32_Desktop.IconTitleWrap
- Win32_Desktop.Name
- Win32_Desktop.Pattern
- Win32_Desktop.ScreenSaverActive
- Win32_Desktop.ScreenSaverExecutable
- Win32_Desktop.ScreenSaverSecure
- Win32_Desktop.ScreenSaverTimeout
- Win32_Desktop.Wallpaper
- Win32_Desktop.WallpaperStretched
- Win32_Desktop.WallpaperTiled
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1d005104cb663a680bac080b7ff9b6529fd9b7a1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847591"
---
# <a name="win32_desktop-class"></a><span data-ttu-id="bf450-104">Win32 \_ Desktop 類別</span><span class="sxs-lookup"><span data-stu-id="bf450-104">Win32\_Desktop class</span></span>

<span data-ttu-id="bf450-105">**Win32 \_ Desktop**[WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表使用者桌面的一般特性。</span><span class="sxs-lookup"><span data-stu-id="bf450-105">The **Win32\_Desktop**[WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the common characteristics of a user's desktop.</span></span> <span data-ttu-id="bf450-106">使用者可以修改這個類別的屬性，以自訂桌面。</span><span class="sxs-lookup"><span data-stu-id="bf450-106">The properties of this class can be modified by the user to customize the desktop.</span></span>

<span data-ttu-id="bf450-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="bf450-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="bf450-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="bf450-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf450-109">語法</span><span class="sxs-lookup"><span data-stu-id="bf450-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4E3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Desktop : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  uint32  BorderWidth;
  boolean CoolSwitch;
  uint32  CursorBlinkRate;
  boolean DragFullWindows;
  uint32  GridGranularity;
  uint32  IconSpacing;
  string  IconTitleFaceName;
  uint32  IconTitleSize;
  boolean IconTitleWrap;
  string  Name;
  string  Pattern;
  boolean ScreenSaverActive;
  string  ScreenSaverExecutable;
  boolean ScreenSaverSecure;
  uint32  ScreenSaverTimeout;
  string  Wallpaper;
  boolean WallpaperStretched;
  boolean WallpaperTiled;
};
```

## <a name="members"></a><span data-ttu-id="bf450-110">成員</span><span class="sxs-lookup"><span data-stu-id="bf450-110">Members</span></span>

<span data-ttu-id="bf450-111">**Win32 \_ Desktop** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bf450-111">The **Win32\_Desktop** class has these types of members:</span></span>

-   [<span data-ttu-id="bf450-112">屬性</span><span class="sxs-lookup"><span data-stu-id="bf450-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bf450-113">屬性</span><span class="sxs-lookup"><span data-stu-id="bf450-113">Properties</span></span>

<span data-ttu-id="bf450-114">**Win32 \_ Desktop** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="bf450-114">The **Win32\_Desktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bf450-115">**BorderWidth**</span><span class="sxs-lookup"><span data-stu-id="bf450-115">**BorderWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf450-116">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="bf450-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf450-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bf450-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf450-118">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 。DEFAULT \\ \\ 主控台 \\ \\ Desktop \\ \\ WindowMetrics \| BorderWidth ") </span><span class="sxs-lookup"><span data-stu-id="bf450-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\\\\WindowMetrics\|BorderWidth")</span></span>
</dt> </dl>

<span data-ttu-id="bf450-119">所有具有可調整框線之視窗周圍的框線寬度。</span><span class="sxs-lookup"><span data-stu-id="bf450-119">Width of the borders around all windows with adjustable borders.</span></span>

<span data-ttu-id="bf450-120">範例：3</span><span class="sxs-lookup"><span data-stu-id="bf450-120">Example: 3</span></span>

</dd> <dt>

<span data-ttu-id="bf450-121">**標題**</span><span class="sxs-lookup"><span data-stu-id="bf450-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf450-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bf450-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf450-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bf450-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf450-124">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="bf450-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="bf450-125">目前物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="bf450-125">Short textual description of the current object.</span></span>

<span data-ttu-id="bf450-126">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="bf450-126">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf450-127">**CoolSwitch**</span><span class="sxs-lookup"><span data-stu-id="bf450-127">**CoolSwitch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf450-128">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="bf450-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bf450-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bf450-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf450-130">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 主控台 \\ \\ Desktop \| CoolSwitch" ) </span><span class="sxs-lookup"><span data-stu-id="bf450-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|Control Panel\\\\Desktop\|CoolSwitch")</span></span>
</dt> </dl>

<span data-ttu-id="bf450-131">開啟快速工作切換。</span><span class="sxs-lookup"><span data-stu-id="bf450-131">Fast task switching is turned on.</span></span> <span data-ttu-id="bf450-132">快速工作切換可讓使用者使用 **ALT + TAB 鍵** 的鍵盤組合在視窗之間切換。</span><span class="sxs-lookup"><span data-stu-id="bf450-132">Fast task switching allows the user to switch between windows using the **ALT+TAB** keyboard combination.</span></span>

</dd> <dt>

<span data-ttu-id="bf450-133">**CursorBlinkRate**</span><span class="sxs-lookup"><span data-stu-id="bf450-133">**CursorBlinkRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf450-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="bf450-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf450-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bf450-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf450-136">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 主控台 \\ \\ Desktop \| CursorBlinkRate" ) ，[**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫秒" ) </span><span class="sxs-lookup"><span data-stu-id="bf450-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|Control Panel\\\\Desktop\|CursorBlinkRate"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="bf450-137">連續資料指標閃爍之間的時間長度。</span><span class="sxs-lookup"><span data-stu-id="bf450-137">Length of time between successive cursor blinks.</span></span>

<span data-ttu-id="bf450-138">範例：530</span><span class="sxs-lookup"><span data-stu-id="bf450-138">Example: 530</span></span>

</dd> <dt>

<span data-ttu-id="bf450-139">**說明**</span><span class="sxs-lookup"><span data-stu-id="bf450-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf450-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bf450-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf450-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bf450-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf450-142">目前物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="bf450-142">Textual description of the current object.</span></span>

<span data-ttu-id="bf450-143">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="bf450-143">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf450-144">**DragFullWindows**</span><span class="sxs-lookup"><span data-stu-id="bf450-144">**DragFullWindows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf450-145">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="bf450-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bf450-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bf450-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf450-147">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 主控台 \\ \\ Desktop \| DragFullWindows" ) </span><span class="sxs-lookup"><span data-stu-id="bf450-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|Control Panel\\\\Desktop\|DragFullWindows")</span></span>
</dt> </dl>

<span data-ttu-id="bf450-148">當使用者移動視窗時，會顯示視窗的內容。</span><span class="sxs-lookup"><span data-stu-id="bf450-148">Contents of a window are shown when a user moves the window.</span></span>

</dd> <dt>

<span data-ttu-id="bf450-149">**GridGranularity**</span><span class="sxs-lookup"><span data-stu-id="bf450-149">**GridGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf450-150">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="bf450-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf450-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bf450-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf450-152">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 主控台 \\ \\ Desktop \| GridGranularity" ) ，[**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "8 圖元" ) </span><span class="sxs-lookup"><span data-stu-id="bf450-152">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|Control Panel\\\\Desktop\|GridGranularity"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("8 pixels")</span></span>
</dt> </dl>

<span data-ttu-id="bf450-153">視窗在桌面上系結的格線間距。</span><span class="sxs-lookup"><span data-stu-id="bf450-153">Spacing of the grid that windows are bound to on the desktop.</span></span> <span data-ttu-id="bf450-154">這樣可讓您更輕鬆地整理 windows。</span><span class="sxs-lookup"><span data-stu-id="bf450-154">This makes organizing windows easier.</span></span> <span data-ttu-id="bf450-155">間距通常足以讓使用者不會注意到。</span><span class="sxs-lookup"><span data-stu-id="bf450-155">The spacing is usually fine enough that the user does not notice it.</span></span>

<span data-ttu-id="bf450-156">範例：1</span><span class="sxs-lookup"><span data-stu-id="bf450-156">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="bf450-157">**IconSpacing**</span><span class="sxs-lookup"><span data-stu-id="bf450-157">**IconSpacing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf450-158">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="bf450-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf450-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bf450-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf450-160">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 。預設 \\ \\ 主控台 \\ \\ Desktop \\ \\ WindowMetrics \| IconSpacing ") ，[**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 圖元 ") </span><span class="sxs-lookup"><span data-stu-id="bf450-160">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\\\\WindowMetrics\|IconSpacing"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="bf450-161">圖示之間的間距。</span><span class="sxs-lookup"><span data-stu-id="bf450-161">Spacing between icons.</span></span>

<span data-ttu-id="bf450-162">範例：75</span><span class="sxs-lookup"><span data-stu-id="bf450-162">Example: 75</span></span>

</dd> <dt>

<span data-ttu-id="bf450-163">**IconTitleFaceName**</span><span class="sxs-lookup"><span data-stu-id="bf450-163">**IconTitleFaceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf450-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bf450-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf450-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bf450-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf450-166">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 。DEFAULT \\ \\ 主控台 \\ \\ Desktop \\ \\ WindowMetrics \| IconFont ") </span><span class="sxs-lookup"><span data-stu-id="bf450-166">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\\\\WindowMetrics\|IconFont")</span></span>
</dt> </dl>

<span data-ttu-id="bf450-167">圖示名稱所使用的字型。</span><span class="sxs-lookup"><span data-stu-id="bf450-167">Font used for the names of the icons.</span></span>

<span data-ttu-id="bf450-168">範例： "MS San Serif"</span><span class="sxs-lookup"><span data-stu-id="bf450-168">Example: "MS San Serif"</span></span>

</dd> <dt>

<span data-ttu-id="bf450-169">**IconTitleSize**</span><span class="sxs-lookup"><span data-stu-id="bf450-169">**IconTitleSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf450-170">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="bf450-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf450-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bf450-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf450-172">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| 字型 and Text 結構 \| [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) \| lfHeight" ) ，[**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "point" ) </span><span class="sxs-lookup"><span data-stu-id="bf450-172">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Font and Text Structures\|[**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta)\|lfHeight"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("point")</span></span>
</dt> </dl>

<span data-ttu-id="bf450-173">圖示的字型大小。</span><span class="sxs-lookup"><span data-stu-id="bf450-173">Icon font size.</span></span>

<span data-ttu-id="bf450-174">範例：9</span><span class="sxs-lookup"><span data-stu-id="bf450-174">Example: 9</span></span>

</dd> <dt>

<span data-ttu-id="bf450-175">**IconTitleWrap**</span><span class="sxs-lookup"><span data-stu-id="bf450-175">**IconTitleWrap**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf450-176">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="bf450-176">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bf450-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bf450-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf450-178">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 。DEFAULT \\ \\ 主控台 \\ \\ Desktop \\ \\ WindowMetrics \| IconTitleWrap ") </span><span class="sxs-lookup"><span data-stu-id="bf450-178">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\\\\WindowMetrics\|IconTitleWrap")</span></span>
</dt> </dl>

<span data-ttu-id="bf450-179">圖示的標題文字會換行至下一行。</span><span class="sxs-lookup"><span data-stu-id="bf450-179">Icon's title text wraps to the next line.</span></span>

</dd> <dt>

<span data-ttu-id="bf450-180">**名稱**</span><span class="sxs-lookup"><span data-stu-id="bf450-180">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf450-181">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bf450-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf450-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bf450-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf450-183">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="bf450-183">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="bf450-184">識別目前桌面設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf450-184">Name that identifies the current desktop profile.</span></span>

<span data-ttu-id="bf450-185">範例： "MainProf"</span><span class="sxs-lookup"><span data-stu-id="bf450-185">Example: "MainProf"</span></span>

</dd> <dt>

<span data-ttu-id="bf450-186">**模式**</span><span class="sxs-lookup"><span data-stu-id="bf450-186">**Pattern**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf450-187">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bf450-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf450-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bf450-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf450-189">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 。預設 \\ \\ 主控台 \\ \\ 桌面 \| 模式」 ) </span><span class="sxs-lookup"><span data-stu-id="bf450-189">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|Pattern")</span></span>
</dt> </dl>

<span data-ttu-id="bf450-190">用來做為桌面背景的模式名稱。</span><span class="sxs-lookup"><span data-stu-id="bf450-190">Name of the pattern used as the background for the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="bf450-191">**ScreenSaverActive**</span><span class="sxs-lookup"><span data-stu-id="bf450-191">**ScreenSaverActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf450-192">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="bf450-192">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bf450-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bf450-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf450-194">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 。預設 \\ \\ 主控台 \\ \\ Desktop \| ScreenSaveActive ") </span><span class="sxs-lookup"><span data-stu-id="bf450-194">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|ScreenSaveActive")</span></span>
</dt> </dl>

<span data-ttu-id="bf450-195">螢幕保護裝置正在使用中。</span><span class="sxs-lookup"><span data-stu-id="bf450-195">Screen saver is active.</span></span>

</dd> <dt>

<span data-ttu-id="bf450-196">**ScreenSaverExecutable**</span><span class="sxs-lookup"><span data-stu-id="bf450-196">**ScreenSaverExecutable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf450-197">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bf450-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf450-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bf450-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf450-199">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 。預設 \\ \\ 主控台 \\ \\ 桌面 \|SCRNSAVE.EXE」 ) </span><span class="sxs-lookup"><span data-stu-id="bf450-199">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|SCRNSAVE.EXE")</span></span>
</dt> </dl>

<span data-ttu-id="bf450-200">目前螢幕保護裝置可執行檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf450-200">Name of the current screen saver executable file.</span></span>

<span data-ttu-id="bf450-201">範例：「登入。.SCR</span><span class="sxs-lookup"><span data-stu-id="bf450-201">Example: "LOGON.SCR"</span></span>

</dd> <dt>

<span data-ttu-id="bf450-202">**ScreenSaverSecure**</span><span class="sxs-lookup"><span data-stu-id="bf450-202">**ScreenSaverSecure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf450-203">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="bf450-203">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bf450-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bf450-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf450-205">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 。預設 \\ \\ 主控台 \\ \\ Desktop \| ScreenSaverIsSecure ") </span><span class="sxs-lookup"><span data-stu-id="bf450-205">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|ScreenSaverIsSecure")</span></span>
</dt> </dl>

<span data-ttu-id="bf450-206">啟用螢幕保護裝置的密碼。</span><span class="sxs-lookup"><span data-stu-id="bf450-206">Password is enabled for the screen saver.</span></span>

</dd> <dt>

<span data-ttu-id="bf450-207">**ScreenSaverTimeout**</span><span class="sxs-lookup"><span data-stu-id="bf450-207">**ScreenSaverTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf450-208">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="bf450-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf450-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bf450-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf450-210">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 。預設 \\ \\ 主控台 \\ \\ Desktop \| ScreenSaveTimeOut ") ，[**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" seconds ") </span><span class="sxs-lookup"><span data-stu-id="bf450-210">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|ScreenSaveTimeOut"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="bf450-211">螢幕保護裝置啟動前經過的時間量。</span><span class="sxs-lookup"><span data-stu-id="bf450-211">Amount of time that passes before the screen saver starts.</span></span>

</dd> <dt>

<span data-ttu-id="bf450-212">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="bf450-212">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf450-213">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bf450-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf450-214">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bf450-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf450-215">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="bf450-215">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="bf450-216">已知目前物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bf450-216">Identifier by which the current object is known.</span></span>

<span data-ttu-id="bf450-217">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="bf450-217">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf450-218">**桌布**</span><span class="sxs-lookup"><span data-stu-id="bf450-218">**Wallpaper**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf450-219">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bf450-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf450-220">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bf450-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf450-221">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 。預設 \\ \\ 主控台 \\ \\ 桌面 \| 壁紙」 ) </span><span class="sxs-lookup"><span data-stu-id="bf450-221">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|Wallpaper")</span></span>
</dt> </dl>

<span data-ttu-id="bf450-222">桌面背景上的壁紙設計檔案名。</span><span class="sxs-lookup"><span data-stu-id="bf450-222">File name for the wallpaper design on the background of the desktop.</span></span>

<span data-ttu-id="bf450-223">範例： "WINNT.BMP"</span><span class="sxs-lookup"><span data-stu-id="bf450-223">Example: "WINNT.BMP"</span></span>

</dd> <dt>

<span data-ttu-id="bf450-224">**WallpaperStretched**</span><span class="sxs-lookup"><span data-stu-id="bf450-224">**WallpaperStretched**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf450-225">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="bf450-225">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bf450-226">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bf450-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf450-227">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 。預設 \\ \\ 主控台 \\ \\ Desktop \| WallpaperStyle ") </span><span class="sxs-lookup"><span data-stu-id="bf450-227">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|WallpaperStyle")</span></span>
</dt> </dl>

<span data-ttu-id="bf450-228">背景圖樣會伸展以填滿整個畫面。</span><span class="sxs-lookup"><span data-stu-id="bf450-228">Wallpaper is stretched to fill the entire screen.</span></span> <span data-ttu-id="bf450-229">Microsoft Plus</span><span class="sxs-lookup"><span data-stu-id="bf450-229">Microsoft Plus!</span></span> <span data-ttu-id="bf450-230">必須先安裝，才能使用此選項。</span><span class="sxs-lookup"><span data-stu-id="bf450-230">must be installed before this option is available.</span></span> <span data-ttu-id="bf450-231">如果 **為 FALSE**，則壁紙會在桌面背景保留其原始尺寸。</span><span class="sxs-lookup"><span data-stu-id="bf450-231">If **FALSE**, the wallpaper retains its original dimensions on the desktop background.</span></span>

</dd> <dt>

<span data-ttu-id="bf450-232">**WallpaperTiled**</span><span class="sxs-lookup"><span data-stu-id="bf450-232">**WallpaperTiled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf450-233">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="bf450-233">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bf450-234">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bf450-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf450-235">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| 。預設 \\ \\ 主控台 \\ \\ Desktop \| TileWallpaper ") </span><span class="sxs-lookup"><span data-stu-id="bf450-235">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|TileWallpaper")</span></span>
</dt> </dl>

<span data-ttu-id="bf450-236">背景圖樣或置中對齊。</span><span class="sxs-lookup"><span data-stu-id="bf450-236">Wallpaper is tiled or centered.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bf450-237">備註</span><span class="sxs-lookup"><span data-stu-id="bf450-237">Remarks</span></span>

<span data-ttu-id="bf450-238">**Win32 \_ Desktop** 類別衍生自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="bf450-238">The **Win32\_Desktop** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="bf450-239">使用這個類別的呼叫進程必須在登錄所在的電腦上具有「 **SE \_ 還原 \_ 名稱** 」許可權。</span><span class="sxs-lookup"><span data-stu-id="bf450-239">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="bf450-240">例如，如果您在本機電腦上列舉此類別，您的應用程式執行所在的帳戶必須具有此許可權。</span><span class="sxs-lookup"><span data-stu-id="bf450-240">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="bf450-241">如需詳細資訊，請參閱 [執行特殊許可權作業](/windows/desktop/WmiSdk/executing-privileged-operations)。</span><span class="sxs-lookup"><span data-stu-id="bf450-241">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="bf450-242">範例</span><span class="sxs-lookup"><span data-stu-id="bf450-242">Examples</span></span>

<span data-ttu-id="bf450-243">下列程式碼範例說明如何取出桌面資訊。</span><span class="sxs-lookup"><span data-stu-id="bf450-243">The following code sample describes how to retrieve desktop information.</span></span>


```PowerShell
$desktops = Get-WmiObject win32_desktop

"This system has {0} desktop objects" -f $desktops.length
Foreach ($dt in $desktops) {
"Desktop {0}" -f $i++
"  BorderWidth           : {0}" -f $dt.BorderWidth 
"  Caption               : {0}" -f $dt.Caption
"  CoolSwitch            : {0}" -f $dt.CoolSwitch
"  CursorBlinkRate       : {0}" -f $dt.CursorBlinkRate
"  Description           : {0}" -f $dt.Description 
"  DragFullWindows       : {0}" -f $dt.DragFullWindows
"  GridGranularity       : {0}" -f $dt.GridGranularity 
"  IconSpacing           : {0}" -f $dt.IconSpacing
"  IconTitleFaceName     : {0}" -f $dt.IconTitleFaceName
"  IconTitleSize         : {0}" -f $dt.IconTitleSize
"  IconTitleWrap         : {0}" -f $dt.conTitleWrap
"  Name                  : {0}" -f $dt.Name
"  Pattern               : {0}" -f $dt.Pattern 
"  ScreenSaverActive     : {0}" -f $dt.ScreenSaverActive
"  ScreenSaverExecutable : {0}" -f $dt.ScreenSaverExecutable
"  ScreenSaverSecure     : {0}" -f $dt.creenSaverSecure
"  ScreenSaverTimeout    : {0}" -f $dt.ScreenSaverTimeout
"  SettingID             : {0}" -f $dt.SettingID
"  Wallpaper             : {0}" -f $dt.Wallpaper
"  WallpaperStretched    : {0}" -f $dt.WallpaperStretched
"  WallpaperTiled        : {0}" -f $dt.WallpaperTiled
""
}
```



## <a name="requirements"></a><span data-ttu-id="bf450-244">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf450-244">Requirements</span></span>



| <span data-ttu-id="bf450-245">需求</span><span class="sxs-lookup"><span data-stu-id="bf450-245">Requirement</span></span> | <span data-ttu-id="bf450-246">值</span><span class="sxs-lookup"><span data-stu-id="bf450-246">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf450-247">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bf450-247">Minimum supported client</span></span><br/> | <span data-ttu-id="bf450-248">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bf450-248">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bf450-249">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bf450-249">Minimum supported server</span></span><br/> | <span data-ttu-id="bf450-250">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf450-250">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bf450-251">命名空間</span><span class="sxs-lookup"><span data-stu-id="bf450-251">Namespace</span></span><br/>                | <span data-ttu-id="bf450-252">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="bf450-252">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bf450-253">MOF</span><span class="sxs-lookup"><span data-stu-id="bf450-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf450-254"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf450-254"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf450-255">DLL</span><span class="sxs-lookup"><span data-stu-id="bf450-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf450-256"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf450-256"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf450-257">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf450-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf450-258">**CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="bf450-258">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

<span data-ttu-id="bf450-259">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bf450-259">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

