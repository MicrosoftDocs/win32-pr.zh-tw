---
title: Win32_TSClientSetting 類別
description: 定義與 \_ 連接原則相關的 Win32 終端機類別的設定。
ms.assetid: 438baf22-adc2-410e-bf9b-4b17a05c5ce4
ms.tgt_platform: multiple
keywords:
- Win32_TSClientSetting 類別遠端桌面服務
- Win32_TSClientSetting 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSClientSetting
- Win32_TSClientSetting.Caption
- Win32_TSClientSetting.Description
- Win32_TSClientSetting.InstallDate
- Win32_TSClientSetting.Name
- Win32_TSClientSetting.Status
- Win32_TSClientSetting.TerminalName
- Win32_TSClientSetting.ConnectionPolicy
- Win32_TSClientSetting.ConnectClientDrivesAtLogon
- Win32_TSClientSetting.ConnectPrinterAtLogon
- Win32_TSClientSetting.DefaultToClientPrinter
- Win32_TSClientSetting.PolicySourceDefaultToClientPrinter
- Win32_TSClientSetting.WindowsPrinterMapping
- Win32_TSClientSetting.PolicySourceWindowsPrinterMapping
- Win32_TSClientSetting.LPTPortMapping
- Win32_TSClientSetting.PolicySourceLPTPortMapping
- Win32_TSClientSetting.COMPortMapping
- Win32_TSClientSetting.PolicySourceCOMPortMapping
- Win32_TSClientSetting.DriveMapping
- Win32_TSClientSetting.PolicySourceDriveMapping
- Win32_TSClientSetting.AudioMapping
- Win32_TSClientSetting.PolicySourceAudioMapping
- Win32_TSClientSetting.ClipboardMapping
- Win32_TSClientSetting.PolicySourceClipboardMapping
- Win32_TSClientSetting.ColorDepthPolicy
- Win32_TSClientSetting.PolicySourceColorDepthPolicy
- Win32_TSClientSetting.ColorDepth
- Win32_TSClientSetting.PolicySourceColorDepth
- Win32_TSClientSetting.MaxMonitors
- Win32_TSClientSetting.MaxXResolution
- Win32_TSClientSetting.MaxYResolution
- Win32_TSClientSetting.PolicySourceMaxMonitors
- Win32_TSClientSetting.PolicySourceMaxResolution
- Win32_TSClientSetting.PNPRedirection
- Win32_TSClientSetting.PolicySourcePNPRedirection
- Win32_TSClientSetting.AudioCaptureRedir
- Win32_TSClientSetting.PolicySourceAudioCaptureRedir
- Win32_TSClientSetting.VideoPlaybackRedir
- Win32_TSClientSetting.PolicySourceVideoPlaybackRedir
- Win32_TSClientSetting.AllowDwm
- Win32_TSClientSetting.PolicySourceAllowDwm
- Win32_TSClientSetting.PolicyAdvancedRemoteAppGraphics
- Win32_TSClientSetting.AdvancedRemoteAppGraphics
- Win32_TSClientSetting.RemoteSessionProfile
- Win32_TSClientSetting.PolicySourceRemoteSessionProfile
- Win32_TSClientSetting.AVC444ModePreferred
- Win32_TSClientSetting.PolicySourceAvc444ModePreferred
- Win32_TSClientSetting.EncodeImageQuality
- Win32_TSClientSetting.PolicySourceEncodeImageQuality
- Win32_TSClientSetting.HardwareGraphicsAdapter
- Win32_TSClientSetting.PolicySourceHardwareGraphicsAdapter
- Win32_TSClientSetting.SelectTransport
- Win32_TSClientSetting.PolicySourceSelectTransport
- Win32_TSClientSetting.SelectNetworkDetect
- Win32_TSClientSetting.PolicySourceSelectNetworkDetect
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 204f38570e1e023ca070ed1845e4574d9570b8ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105834"
---
# <a name="win32_tsclientsetting-class"></a><span data-ttu-id="8d873-105">Win32 \_ TSClientSetting 類別</span><span class="sxs-lookup"><span data-stu-id="8d873-105">Win32\_TSClientSetting class</span></span>

<span data-ttu-id="8d873-106">**Win32 \_ TSClientSetting** WMI 類別會定義與連接原則相關的 [**win32 \_ 終端**](win32-terminal.md)機類別的設定。</span><span class="sxs-lookup"><span data-stu-id="8d873-106">The **Win32\_TSClientSetting** WMI class defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class related to connection policy.</span></span>

<span data-ttu-id="8d873-107">下列語法簡化自 MOF 程式碼，並依字母順序包含所有定義和繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8d873-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="8d873-108">如需方法的參考資訊，請參閱本主題稍後的方法表格。</span><span class="sxs-lookup"><span data-stu-id="8d873-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d873-109">語法</span><span class="sxs-lookup"><span data-stu-id="8d873-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSCLIENTSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSClientSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ConnectionPolicy;
  uint32   ConnectClientDrivesAtLogon;
  uint32   ConnectPrinterAtLogon;
  uint32   DefaultToClientPrinter;
  uint32   PolicySourceDefaultToClientPrinter;
  uint32   WindowsPrinterMapping;
  uint32   PolicySourceWindowsPrinterMapping;
  uint32   LPTPortMapping;
  uint32   PolicySourceLPTPortMapping;
  uint32   COMPortMapping;
  uint32   PolicySourceCOMPortMapping;
  uint32   DriveMapping;
  uint32   PolicySourceDriveMapping;
  uint32   AudioMapping;
  uint32   PolicySourceAudioMapping;
  uint32   ClipboardMapping;
  uint32   PolicySourceClipboardMapping;
  uint32   ColorDepthPolicy;
  uint32   PolicySourceColorDepthPolicy;
  uint32   ColorDepth;
  uint32   PolicySourceColorDepth;
  uint32   MaxMonitors;
  uint32   MaxXResolution;
  uint32   MaxYResolution;
  uint32   PolicySourceMaxMonitors;
  uint32   PolicySourceMaxResolution;
  uint32   PNPRedirection;
  uint32   PolicySourcePNPRedirection;
  uint32   AudioCaptureRedir;
  uint32   PolicySourceAudioCaptureRedir;
  uint32   VideoPlaybackRedir;
  uint32   PolicySourceVideoPlaybackRedir;
  uint32   AllowDwm;
  uint32   PolicySourceAllowDwm;
  uint32   PolicyAdvancedRemoteAppGraphics;
  uint32   AdvancedRemoteAppGraphics;
  uint32   RemoteSessionProfile;
  uint32   PolicySourceRemoteSessionProfile;
  uint32   AVC444ModePreferred;
  uint32   PolicySourceAvc444ModePreferred;
  uint32   EncodeImageQuality;
  uint32   PolicySourceEncodeImageQuality;
  uint32   HardwareGraphicsAdapter;
  uint32   PolicySourceHardwareGraphicsAdapter;
  uint32   SelectTransport;
  uint32   PolicySourceSelectTransport;
  uint32   SelectNetworkDetect;
  uint32   PolicySourceSelectNetworkDetect;
};
```

## <a name="members"></a><span data-ttu-id="8d873-110">成員</span><span class="sxs-lookup"><span data-stu-id="8d873-110">Members</span></span>

<span data-ttu-id="8d873-111">**Win32 \_ TSClientSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8d873-111">The **Win32\_TSClientSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="8d873-112">方法</span><span class="sxs-lookup"><span data-stu-id="8d873-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="8d873-113">屬性</span><span class="sxs-lookup"><span data-stu-id="8d873-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8d873-114">方法</span><span class="sxs-lookup"><span data-stu-id="8d873-114">Methods</span></span>

<span data-ttu-id="8d873-115">**Win32 \_ TSClientSetting** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="8d873-115">The **Win32\_TSClientSetting** class has these methods.</span></span>



| <span data-ttu-id="8d873-116">方法</span><span class="sxs-lookup"><span data-stu-id="8d873-116">Method</span></span>                                                                   | <span data-ttu-id="8d873-117">描述</span><span class="sxs-lookup"><span data-stu-id="8d873-117">Description</span></span>                                                                                                                                                  |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d873-118">**ConnectionSettings**</span><span class="sxs-lookup"><span data-stu-id="8d873-118">**ConnectionSettings**</span></span>](win32-tsclientsetting-connectionsettings.md)   | <span data-ttu-id="8d873-119">設定這個類別的 **ConnectClientDrivesAtLogon**、 **ConnectPrinterAtLogon** 和 **DefaultToClientPrinter** 屬性。</span><span class="sxs-lookup"><span data-stu-id="8d873-119">Sets the **ConnectClientDrivesAtLogon**, **ConnectPrinterAtLogon**, and **DefaultToClientPrinter** properties of this class.</span></span><br/>                      |
| [<span data-ttu-id="8d873-120">**SetAllowDwm**</span><span class="sxs-lookup"><span data-stu-id="8d873-120">**SetAllowDwm**</span></span>](setallowdwm-win32-tsclientsetting.md)                 | <span data-ttu-id="8d873-121">不支援。</span><span class="sxs-lookup"><span data-stu-id="8d873-121">Not supported.</span></span><br/> <span data-ttu-id="8d873-122">**Windows 7 和 Windows Server 2008 R2：** 設定 **AllowDwm** 屬性。</span><span class="sxs-lookup"><span data-stu-id="8d873-122">**Windows 7 and Windows Server 2008 R2:** Sets the **AllowDwm** property.</span></span><br/>                                               |
| [<span data-ttu-id="8d873-123">**SetClientProperty**</span><span class="sxs-lookup"><span data-stu-id="8d873-123">**SetClientProperty**</span></span>](win32-tsclientsetting-setclientproperty.md)     | <span data-ttu-id="8d873-124">設定 **LPTPortMapping**、 **COMPortMapping**、 **AudioMapping**、 **ClipboardMapping**、 **DriveMapping** 或 **WindowsPrinterMapping** 屬性。</span><span class="sxs-lookup"><span data-stu-id="8d873-124">Sets the **LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping**, **DriveMapping**, or **WindowsPrinterMapping** property.</span></span><br/> |
| [<span data-ttu-id="8d873-125">**SetColorDepth**</span><span class="sxs-lookup"><span data-stu-id="8d873-125">**SetColorDepth**</span></span>](win32-tsclientsetting-setcolordepth.md)             | <span data-ttu-id="8d873-126">設定 **ColorDepth** 屬性。</span><span class="sxs-lookup"><span data-stu-id="8d873-126">Sets the **ColorDepth** property.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="8d873-127">**SetColorDepthPolicy**</span><span class="sxs-lookup"><span data-stu-id="8d873-127">**SetColorDepthPolicy**</span></span>](win32-tsclientsetting-setcolordepthpolicy.md) | <span data-ttu-id="8d873-128">設定 **ColorDepthPolicy** 屬性。</span><span class="sxs-lookup"><span data-stu-id="8d873-128">Sets the **ColorDepthPolicy** property.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="8d873-129">**SetMaxMonitors**</span><span class="sxs-lookup"><span data-stu-id="8d873-129">**SetMaxMonitors**</span></span>](setmaxmonitors-win32-tsclientsetting.md)           | <span data-ttu-id="8d873-130">設定 **MaxMonitors** 屬性。</span><span class="sxs-lookup"><span data-stu-id="8d873-130">Sets the **MaxMonitors** property.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="8d873-131">**SetMaxXResolution**</span><span class="sxs-lookup"><span data-stu-id="8d873-131">**SetMaxXResolution**</span></span>](setmaxxresolution-win32-tsclientsetting.md)     | <span data-ttu-id="8d873-132">設定 **MaxXResolution** 屬性。</span><span class="sxs-lookup"><span data-stu-id="8d873-132">Sets the **MaxXResolution** property.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="8d873-133">**SetMaxYResolution**</span><span class="sxs-lookup"><span data-stu-id="8d873-133">**SetMaxYResolution**</span></span>](setmaxyresolution-win32-tsclientsetting.md)     | <span data-ttu-id="8d873-134">設定 **MaxYResolution** 屬性。</span><span class="sxs-lookup"><span data-stu-id="8d873-134">Sets the **MaxYResolution** property.</span></span><br/>                                                                                                             |



 

### <a name="properties"></a><span data-ttu-id="8d873-135">屬性</span><span class="sxs-lookup"><span data-stu-id="8d873-135">Properties</span></span>

<span data-ttu-id="8d873-136">**Win32 \_ TSClientSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8d873-136">The **Win32\_TSClientSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8d873-137">**AdvancedRemoteAppGraphics**</span><span class="sxs-lookup"><span data-stu-id="8d873-137">**AdvancedRemoteAppGraphics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-138">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8d873-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8d873-140">指定是否啟用 RemoteApp 的 advanced RemoteFX 圖形。</span><span class="sxs-lookup"><span data-stu-id="8d873-140">Specifies whether to enable advanced RemoteFX graphics for RemoteApp.</span></span>

<span data-ttu-id="8d873-141">**Windows server 2012、Windows 8、Windows server 2008 R2、Windows 7、Windows server 2008 和 Windows Vista：** 在 Windows Server 2012 R2 和 Windows 8.1 之前，無法使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="8d873-141">**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2012 R2 and Windows 8.1.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8d873-142"><span id="FALSE"></span><span id="false"></span>**FALSE** (0) </span><span class="sxs-lookup"><span data-stu-id="8d873-142"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8d873-143">已停用 Advanced graphics。</span><span class="sxs-lookup"><span data-stu-id="8d873-143">Advanced graphics are disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8d873-144"><span id="TRUE"></span><span id="true"></span>**TRUE** (1) </span><span class="sxs-lookup"><span data-stu-id="8d873-144"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8d873-145">已啟用先進的圖形。</span><span class="sxs-lookup"><span data-stu-id="8d873-145">Advanced graphics are enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-146">**AllowDwm**</span><span class="sxs-lookup"><span data-stu-id="8d873-146">**AllowDwm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-147">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-149">無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="8d873-149">This property is not available.</span></span>

<span data-ttu-id="8d873-150">\* \* Windows 7 和 Windows Server 2008 R2： \* \*</span><span class="sxs-lookup"><span data-stu-id="8d873-150">\*\*Windows 7 and Windows Server 2008 R2:  \*\*</span></span>

<span data-ttu-id="8d873-151">指定是否要啟用或停用遠端桌面組合。</span><span class="sxs-lookup"><span data-stu-id="8d873-151">Specifies whether to enable or disable remote desktop composition.</span></span> <span data-ttu-id="8d873-152">零會停用遠端桌面組合，而非零值會啟用它。</span><span class="sxs-lookup"><span data-stu-id="8d873-152">Zero will disable remote desktop composition and a nonzero value will enable it.</span></span>

<span data-ttu-id="8d873-153">您可以使用 [**SetAllowDwm**](setallowdwm-win32-tsclientsetting.md) 方法來修改此屬性。</span><span class="sxs-lookup"><span data-stu-id="8d873-153">Use the [**SetAllowDwm**](setallowdwm-win32-tsclientsetting.md) method to modify this property.</span></span>

</dd> <dt>

<span data-ttu-id="8d873-154">**AudioCaptureRedir**</span><span class="sxs-lookup"><span data-stu-id="8d873-154">**AudioCaptureRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-155">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-157">指定是否允許音訊捕獲重新導向。</span><span class="sxs-lookup"><span data-stu-id="8d873-157">Specifies whether to allow audio capture redirection.</span></span>

<span data-ttu-id="8d873-158">**Windows Server 2008 和 Windows Vista：** 此屬性在 Windows Server 2008 R2 和 Windows 7 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="8d873-158">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8d873-159">**FALSE** (0) </span><span class="sxs-lookup"><span data-stu-id="8d873-159">**FALSE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8d873-160">**TRUE** (1) </span><span class="sxs-lookup"><span data-stu-id="8d873-160">**TRUE** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-161">**AudioMapping**</span><span class="sxs-lookup"><span data-stu-id="8d873-161">**AudioMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-162">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-164">指定是否停用或啟用音訊對應。</span><span class="sxs-lookup"><span data-stu-id="8d873-164">Specifies whether audio mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8d873-165"><span id="FALSE"></span><span id="false"></span>**FALSE** (0) </span><span class="sxs-lookup"><span data-stu-id="8d873-165"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8d873-166">音訊對應已啟用。</span><span class="sxs-lookup"><span data-stu-id="8d873-166">Audio mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8d873-167"><span id="TRUE"></span><span id="true"></span>**TRUE** (1) </span><span class="sxs-lookup"><span data-stu-id="8d873-167"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8d873-168">音訊對應已停用。</span><span class="sxs-lookup"><span data-stu-id="8d873-168">Audio mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-169">**AVC444ModePreferred**</span><span class="sxs-lookup"><span data-stu-id="8d873-169">**AVC444ModePreferred**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-170">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-171">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8d873-171">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8d873-172">指定是否偏好 AVC444 模式。</span><span class="sxs-lookup"><span data-stu-id="8d873-172">Specifies whether AVC444 mode is preferred.</span></span>

<span data-ttu-id="8d873-173">**Windows 8.1、Windows server 2012 r2、Windows 8、Windows server 2012、windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：** 此屬性在 Windows 10 或 Windows Server 2016 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="8d873-173">**Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 10 or Windows Server 2016.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8d873-174">**FALSE** (0) </span><span class="sxs-lookup"><span data-stu-id="8d873-174">**FALSE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8d873-175">**TRUE** (1) </span><span class="sxs-lookup"><span data-stu-id="8d873-175">**TRUE** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-176">**標題**</span><span class="sxs-lookup"><span data-stu-id="8d873-176">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8d873-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d873-179">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="8d873-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8d873-180">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="8d873-180">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="8d873-181">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8d873-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d873-182">**ClipboardMapping**</span><span class="sxs-lookup"><span data-stu-id="8d873-182">**ClipboardMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-183">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-185">指定是否停用或啟用剪貼簿對應。</span><span class="sxs-lookup"><span data-stu-id="8d873-185">Specifies whether clipboard mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8d873-186"><span id="FALSE"></span><span id="false"></span>**FALSE** (0) </span><span class="sxs-lookup"><span data-stu-id="8d873-186"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8d873-187">剪貼簿對應已啟用。</span><span class="sxs-lookup"><span data-stu-id="8d873-187">Clipboard mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8d873-188"><span id="TRUE"></span><span id="true"></span>**TRUE** (1) </span><span class="sxs-lookup"><span data-stu-id="8d873-188"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8d873-189">剪貼簿對應已停用。</span><span class="sxs-lookup"><span data-stu-id="8d873-189">Clipboard mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-190">**ColorDepth**</span><span class="sxs-lookup"><span data-stu-id="8d873-190">**ColorDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-191">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-191">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-193">指定色彩深度。</span><span class="sxs-lookup"><span data-stu-id="8d873-193">Specifies the color depth.</span></span> <span data-ttu-id="8d873-194">如需可能的值，請參閱 [**SetColorDepth**](win32-tsclientsetting-setcolordepth.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="8d873-194">For possible values, see the [**SetColorDepth**](win32-tsclientsetting-setcolordepth.md) method.</span></span>

<dt>

<span id="8_bit"></span><span id="8_BIT"></span>

<span data-ttu-id="8d873-195"><span id="8_bit"></span><span id="8_BIT"></span>**8 位** (1) </span><span class="sxs-lookup"><span data-stu-id="8d873-195"><span id="8_bit"></span><span id="8_BIT"></span>**8 bit** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="15_bit"></span><span id="15_BIT"></span>

<span data-ttu-id="8d873-196"><span id="15_bit"></span><span id="15_BIT"></span>**15 位** (2) </span><span class="sxs-lookup"><span data-stu-id="8d873-196"><span id="15_bit"></span><span id="15_BIT"></span>**15 bit** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="16_bit"></span><span id="16_BIT"></span>

<span data-ttu-id="8d873-197"><span id="16_bit"></span><span id="16_BIT"></span>**16 位** (3) </span><span class="sxs-lookup"><span data-stu-id="8d873-197"><span id="16_bit"></span><span id="16_BIT"></span>**16 bit** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="24_bit"></span><span id="24_BIT"></span>

<span data-ttu-id="8d873-198"><span id="24_bit"></span><span id="24_BIT"></span>**24 位** (4) </span><span class="sxs-lookup"><span data-stu-id="8d873-198"><span id="24_bit"></span><span id="24_BIT"></span>**24 bit** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="32_bit"></span><span id="32_BIT"></span>

<span data-ttu-id="8d873-199"><span id="32_bit"></span><span id="32_BIT"></span>**32 位** (5) </span><span class="sxs-lookup"><span data-stu-id="8d873-199"><span id="32_bit"></span><span id="32_BIT"></span>**32 bit** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-200">**ColorDepthPolicy**</span><span class="sxs-lookup"><span data-stu-id="8d873-200">**ColorDepthPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-201">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-202">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-203">指定是否要覆寫使用者的最大色彩設定。</span><span class="sxs-lookup"><span data-stu-id="8d873-203">Specifies whether to override the user's maximum color setting.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8d873-204"><span id="FALSE"></span><span id="false"></span>**FALSE** (0) </span><span class="sxs-lookup"><span data-stu-id="8d873-204"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8d873-205">請勿覆寫使用者的原則。</span><span class="sxs-lookup"><span data-stu-id="8d873-205">Do not override the user's policy.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8d873-206"><span id="TRUE"></span><span id="true"></span>**TRUE** (1) </span><span class="sxs-lookup"><span data-stu-id="8d873-206"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8d873-207">覆寫使用者的原則。</span><span class="sxs-lookup"><span data-stu-id="8d873-207">Override the user's policy.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-208">**COMPortMapping**</span><span class="sxs-lookup"><span data-stu-id="8d873-208">**COMPortMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-209">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-210">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-211">指定 COM 埠對應是否已停用或啟用。</span><span class="sxs-lookup"><span data-stu-id="8d873-211">Specifies whether COM port mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8d873-212"><span id="FALSE"></span><span id="false"></span>**FALSE** (0) </span><span class="sxs-lookup"><span data-stu-id="8d873-212"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8d873-213">已啟用 COM 埠對應。</span><span class="sxs-lookup"><span data-stu-id="8d873-213">COM port mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8d873-214"><span id="TRUE"></span><span id="true"></span>**TRUE** (1) </span><span class="sxs-lookup"><span data-stu-id="8d873-214"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8d873-215">COM 埠對應已停用。</span><span class="sxs-lookup"><span data-stu-id="8d873-215">COM port mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-216">**ConnectClientDrivesAtLogon**</span><span class="sxs-lookup"><span data-stu-id="8d873-216">**ConnectClientDrivesAtLogon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-217">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-217">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-219">指定在登入程式期間，是否會自動連接用戶端的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="8d873-219">Specifies whether the client's drives will be automatically connected during the logon process.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8d873-220"><span id="FALSE"></span><span id="false"></span>**FALSE** (0) </span><span class="sxs-lookup"><span data-stu-id="8d873-220"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8d873-221">磁片磁碟機將不會自動連線。</span><span class="sxs-lookup"><span data-stu-id="8d873-221">Drives will not be automatically connected.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8d873-222"><span id="TRUE"></span><span id="true"></span>**TRUE** (1) </span><span class="sxs-lookup"><span data-stu-id="8d873-222"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8d873-223">磁片磁碟機將會自動連接。</span><span class="sxs-lookup"><span data-stu-id="8d873-223">Drives will be automatically connected.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-224">**ConnectionPolicy**</span><span class="sxs-lookup"><span data-stu-id="8d873-224">**ConnectionPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-225">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-226">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8d873-226">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8d873-227">伺服器用來取得使用者連接設定的原則。</span><span class="sxs-lookup"><span data-stu-id="8d873-227">The policy the server uses to retrieve the user connection settings.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="8d873-228"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**每位使用者** (0) </span><span class="sxs-lookup"><span data-stu-id="8d873-228"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8d873-229">使用者的連接設定有效。</span><span class="sxs-lookup"><span data-stu-id="8d873-229">The user's connection settings are in effect.</span></span>

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="8d873-230"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**伺服器-覆寫** (1) </span><span class="sxs-lookup"><span data-stu-id="8d873-230"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8d873-231">伺服器會覆寫使用者的連接設定。</span><span class="sxs-lookup"><span data-stu-id="8d873-231">The user's connection settings are overridden by the server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-232">**ConnectPrinterAtLogon**</span><span class="sxs-lookup"><span data-stu-id="8d873-232">**ConnectPrinterAtLogon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-233">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-233">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-234">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-235">指定在登入程式期間，用戶端的所有對應本機印表機是否會自動連接。</span><span class="sxs-lookup"><span data-stu-id="8d873-235">Specifies whether all mapped local printers of the client will be automatically connected during the logon process.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8d873-236"><span id="FALSE"></span><span id="false"></span>**FALSE** (0) </span><span class="sxs-lookup"><span data-stu-id="8d873-236"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8d873-237">本機印表機不會自動連線。</span><span class="sxs-lookup"><span data-stu-id="8d873-237">Local printers will not be automatically connected.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8d873-238"><span id="TRUE"></span><span id="true"></span>**TRUE** (1) </span><span class="sxs-lookup"><span data-stu-id="8d873-238"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8d873-239">本機印表機會自動連接。</span><span class="sxs-lookup"><span data-stu-id="8d873-239">Local printers will be automatically connected.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-240">**DefaultToClientPrinter**</span><span class="sxs-lookup"><span data-stu-id="8d873-240">**DefaultToClientPrinter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-241">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-242">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-243">指定列印工作是否會自動傳送至用戶端的本機印表機。</span><span class="sxs-lookup"><span data-stu-id="8d873-243">Specifies whether print jobs will be automatically sent to the client's local printer.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8d873-244"><span id="FALSE"></span><span id="false"></span>**FALSE** (0) </span><span class="sxs-lookup"><span data-stu-id="8d873-244"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8d873-245">列印工作不會自動傳送至用戶端的本機印表機。</span><span class="sxs-lookup"><span data-stu-id="8d873-245">Print jobs are not to be automatically sent to the client's local printer.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8d873-246"><span id="TRUE"></span><span id="true"></span>**TRUE** (1) </span><span class="sxs-lookup"><span data-stu-id="8d873-246"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8d873-247">列印工作會自動傳送至用戶端的本機印表機。</span><span class="sxs-lookup"><span data-stu-id="8d873-247">Print jobs are to be automatically sent to the client's local printer.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-248">**說明**</span><span class="sxs-lookup"><span data-stu-id="8d873-248">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-249">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8d873-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-250">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-251">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="8d873-251">Description of the object.</span></span>

<span data-ttu-id="8d873-252">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8d873-252">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d873-253">**DriveMapping**</span><span class="sxs-lookup"><span data-stu-id="8d873-253">**DriveMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-254">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-254">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-255">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-256">指定是否停用或啟用磁片磁碟機對應。</span><span class="sxs-lookup"><span data-stu-id="8d873-256">Specifies whether drive mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8d873-257"><span id="FALSE"></span><span id="false"></span>**FALSE** (0) </span><span class="sxs-lookup"><span data-stu-id="8d873-257"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8d873-258">磁片磁碟機對應已啟用。</span><span class="sxs-lookup"><span data-stu-id="8d873-258">Drive mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8d873-259"><span id="TRUE"></span><span id="true"></span>**TRUE** (1) </span><span class="sxs-lookup"><span data-stu-id="8d873-259"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8d873-260">磁片磁碟機對應已停用。</span><span class="sxs-lookup"><span data-stu-id="8d873-260">Drive mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-261">**EncodeImageQuality**</span><span class="sxs-lookup"><span data-stu-id="8d873-261">**EncodeImageQuality**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-262">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-263">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8d873-263">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8d873-264">指定 RDP 體驗的影像品質。</span><span class="sxs-lookup"><span data-stu-id="8d873-264">Specifies the image quality for RDP experience.</span></span>

<span data-ttu-id="8d873-265">**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：** 此屬性在 Windows 8 或 Windows Server 2012 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="8d873-265">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span id="lossless"></span><span id="LOSSLESS"></span>

<span data-ttu-id="8d873-266">無 **失真 (1**) </span><span class="sxs-lookup"><span data-stu-id="8d873-266">**lossless** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="8d873-267">**高** (2) </span><span class="sxs-lookup"><span data-stu-id="8d873-267">**high** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="8d873-268">**中型** (3) </span><span class="sxs-lookup"><span data-stu-id="8d873-268">**medium** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-269">**HardwareGraphicsAdapter**</span><span class="sxs-lookup"><span data-stu-id="8d873-269">**HardwareGraphicsAdapter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-270">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-270">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-271">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8d873-271">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8d873-272">指定 RD 工作階段主機伺服器是否使用硬體圖形轉譯器作為預設介面卡。</span><span class="sxs-lookup"><span data-stu-id="8d873-272">Specifies whether the RD Session Host server uses the hardware graphics renderer as the default adapter.</span></span>

<span data-ttu-id="8d873-273">**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：** 此屬性在 Windows 8 或 Windows Server 2012 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="8d873-273">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8d873-274">**FALSE** (0) </span><span class="sxs-lookup"><span data-stu-id="8d873-274">**FALSE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8d873-275">**TRUE** (1) </span><span class="sxs-lookup"><span data-stu-id="8d873-275">**TRUE** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-276">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8d873-276">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-277">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="8d873-277">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-278">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d873-279">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="8d873-279">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="8d873-280">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="8d873-280">The date the object was installed.</span></span> <span data-ttu-id="8d873-281">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="8d873-281">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8d873-282">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8d873-282">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d873-283">**LPTPortMapping**</span><span class="sxs-lookup"><span data-stu-id="8d873-283">**LPTPortMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-284">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-284">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-285">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-286">指定是否停用或啟用 LPT 埠對應。</span><span class="sxs-lookup"><span data-stu-id="8d873-286">Specifies whether LPT port mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8d873-287"><span id="FALSE"></span><span id="false"></span>**FALSE** (0) </span><span class="sxs-lookup"><span data-stu-id="8d873-287"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8d873-288">啟用了 LPT 埠對應。</span><span class="sxs-lookup"><span data-stu-id="8d873-288">LPT port mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8d873-289"><span id="TRUE"></span><span id="true"></span>**TRUE** (1) </span><span class="sxs-lookup"><span data-stu-id="8d873-289"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8d873-290">已停用 LPT 埠對應。</span><span class="sxs-lookup"><span data-stu-id="8d873-290">LPT port mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-291">**MaxMonitors**</span><span class="sxs-lookup"><span data-stu-id="8d873-291">**MaxMonitors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-292">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-293">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-294">伺服器支援的監視器數目上限。</span><span class="sxs-lookup"><span data-stu-id="8d873-294">The maximum number of monitors supported by the server.</span></span> <span data-ttu-id="8d873-295">您可以使用 [**SetMaxMonitors**](setmaxmonitors-win32-tsclientsetting.md) 方法來修改此屬性。</span><span class="sxs-lookup"><span data-stu-id="8d873-295">Use the [**SetMaxMonitors**](setmaxmonitors-win32-tsclientsetting.md) method to modify this property.</span></span>

<span data-ttu-id="8d873-296">**Windows Server 2008 和 Windows Vista：** 此屬性在 Windows Server 2008 R2 和 Windows 7 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="8d873-296">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="8d873-297">**MaxXResolution**</span><span class="sxs-lookup"><span data-stu-id="8d873-297">**MaxXResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-298">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-298">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-299">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-300">伺服器支援的最大 X 解析度。</span><span class="sxs-lookup"><span data-stu-id="8d873-300">The maximum X resolution supported by the server.</span></span> <span data-ttu-id="8d873-301">您可以使用 [**SetMaxXResolution**](setmaxxresolution-win32-tsclientsetting.md) 方法來修改此屬性。</span><span class="sxs-lookup"><span data-stu-id="8d873-301">Use the [**SetMaxXResolution**](setmaxxresolution-win32-tsclientsetting.md) method to modify this property.</span></span>

<span data-ttu-id="8d873-302">**Windows Server 2008 和 Windows Vista：** 此屬性在 Windows Server 2008 R2 和 Windows 7 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="8d873-302">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="8d873-303">**MaxYResolution**</span><span class="sxs-lookup"><span data-stu-id="8d873-303">**MaxYResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-304">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-304">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-305">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-306">伺服器支援的最大 Y 解析度。</span><span class="sxs-lookup"><span data-stu-id="8d873-306">The maximum Y resolution supported by the server.</span></span> <span data-ttu-id="8d873-307">您可以使用 [**SetMaxYResolution**](setmaxyresolution-win32-tsclientsetting.md) 方法來修改此屬性。</span><span class="sxs-lookup"><span data-stu-id="8d873-307">Use the [**SetMaxYResolution**](setmaxyresolution-win32-tsclientsetting.md) method to modify this property.</span></span>

<span data-ttu-id="8d873-308">**Windows Server 2008 和 Windows Vista：** 此屬性在 Windows Server 2008 R2 和 Windows 7 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="8d873-308">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="8d873-309">**名稱**</span><span class="sxs-lookup"><span data-stu-id="8d873-309">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-310">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8d873-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-311">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-312">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d873-312">The name of the object.</span></span>

<span data-ttu-id="8d873-313">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8d873-313">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d873-314">**PNPRedirection**</span><span class="sxs-lookup"><span data-stu-id="8d873-314">**PNPRedirection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-315">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-316">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-317">指定是否允許隨插即用重新導向。</span><span class="sxs-lookup"><span data-stu-id="8d873-317">Specifies whether to allow Plug and Play redirection.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8d873-318"><span id="FALSE"></span><span id="false"></span>**FALSE** (0) </span><span class="sxs-lookup"><span data-stu-id="8d873-318"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8d873-319">允許隨插即用重新導向。</span><span class="sxs-lookup"><span data-stu-id="8d873-319">Allow Plug and Play redirection.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8d873-320"><span id="TRUE"></span><span id="true"></span>**TRUE** (1) </span><span class="sxs-lookup"><span data-stu-id="8d873-320"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8d873-321">不允許隨插即用重新導向。</span><span class="sxs-lookup"><span data-stu-id="8d873-321">Do not allow Plug and Play redirection.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-322">**PolicyAdvancedRemoteAppGraphics**</span><span class="sxs-lookup"><span data-stu-id="8d873-322">**PolicyAdvancedRemoteAppGraphics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-323">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-323">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-324">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-325">指出是否由伺服器或群組原則設定 **AdvancedRemoteAppGraphics** 屬性。</span><span class="sxs-lookup"><span data-stu-id="8d873-325">Indicates whether the **AdvancedRemoteAppGraphics** property is configured by the server or group policy.</span></span>

<span data-ttu-id="8d873-326">**Windows server 2012、Windows 8、Windows server 2008 R2、Windows 7、Windows server 2008 和 Windows Vista：** 在 Windows Server 2012 R2 和 Windows 8.1 之前，無法使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="8d873-326">**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2012 R2 and Windows 8.1.</span></span>

<dt>

<span data-ttu-id="8d873-327">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="8d873-327">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-328">伺服器</span><span class="sxs-lookup"><span data-stu-id="8d873-328">Server</span></span>

</dd> <dt>

<span data-ttu-id="8d873-329">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="8d873-329">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-330">群組原則</span><span class="sxs-lookup"><span data-stu-id="8d873-330">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-331">**PolicySourceAllowDwm**</span><span class="sxs-lookup"><span data-stu-id="8d873-331">**PolicySourceAllowDwm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-332">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-332">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-333">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-334">無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="8d873-334">This property is not available.</span></span>

<span data-ttu-id="8d873-335">\* \* Windows 7 和 Windows Server 2008 R2： \* \*</span><span class="sxs-lookup"><span data-stu-id="8d873-335">\*\*Windows 7 and Windows Server 2008 R2:  \*\*</span></span>

<span data-ttu-id="8d873-336">指出是否由伺服器或群組原則設定 **AllowDwm** 屬性。</span><span class="sxs-lookup"><span data-stu-id="8d873-336">Indicates whether the **AllowDwm** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="8d873-337">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="8d873-337">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-338">伺服器</span><span class="sxs-lookup"><span data-stu-id="8d873-338">Server</span></span>

</dd> <dt>

<span data-ttu-id="8d873-339">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="8d873-339">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-340">群組原則</span><span class="sxs-lookup"><span data-stu-id="8d873-340">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-341">**PolicySourceAudioCaptureRedir**</span><span class="sxs-lookup"><span data-stu-id="8d873-341">**PolicySourceAudioCaptureRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-342">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-343">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-344">指出是否由伺服器或群組原則設定 **AudioCaptureRedir** 屬性。</span><span class="sxs-lookup"><span data-stu-id="8d873-344">Indicates whether the **AudioCaptureRedir** property is configured by the server or group policy.</span></span>

<span data-ttu-id="8d873-345">**Windows Server 2008 和 Windows Vista：** 此屬性在 Windows Server 2008 R2 和 Windows 7 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="8d873-345">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span data-ttu-id="8d873-346">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="8d873-346">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-347">伺服器</span><span class="sxs-lookup"><span data-stu-id="8d873-347">Server</span></span>

</dd> <dt>

<span data-ttu-id="8d873-348">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="8d873-348">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-349">群組原則</span><span class="sxs-lookup"><span data-stu-id="8d873-349">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-350">**PolicySourceAudioMapping**</span><span class="sxs-lookup"><span data-stu-id="8d873-350">**PolicySourceAudioMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-351">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-351">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-352">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-353">指出 **AudioMapping** 屬性是由伺服器、群組原則或預設設定。</span><span class="sxs-lookup"><span data-stu-id="8d873-353">Indicates whether the **AudioMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8d873-354">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="8d873-354">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-355">伺服器</span><span class="sxs-lookup"><span data-stu-id="8d873-355">Server</span></span>

</dd> <dt>

<span data-ttu-id="8d873-356">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="8d873-356">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-357">群組原則</span><span class="sxs-lookup"><span data-stu-id="8d873-357">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8d873-358">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="8d873-358">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-359">預設</span><span class="sxs-lookup"><span data-stu-id="8d873-359">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-360">**PolicySourceAvc444ModePreferred**</span><span class="sxs-lookup"><span data-stu-id="8d873-360">**PolicySourceAvc444ModePreferred**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-361">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-361">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-362">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-363">指出如何設定 **AVC444ModePreferredis** 屬性。</span><span class="sxs-lookup"><span data-stu-id="8d873-363">Indicates how the **AVC444ModePreferredis** property is configured.</span></span>

<span data-ttu-id="8d873-364">**Windows 8.1、Windows server 2012 r2、Windows 8、Windows server 2012、windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：** 此屬性在 Windows 10 或 Windows Server 2016 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="8d873-364">**Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 10 or Windows Server 2016.</span></span>

<dt>

<span data-ttu-id="8d873-365">0</span><span class="sxs-lookup"><span data-stu-id="8d873-365">0</span></span>
</dt> <dd>

<span data-ttu-id="8d873-366">伺服器</span><span class="sxs-lookup"><span data-stu-id="8d873-366">Server</span></span>

</dd> <dt>

<span data-ttu-id="8d873-367">1</span><span class="sxs-lookup"><span data-stu-id="8d873-367">1</span></span>
</dt> <dd>

<span data-ttu-id="8d873-368">群組原則</span><span class="sxs-lookup"><span data-stu-id="8d873-368">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-369">**PolicySourceClipboardMapping**</span><span class="sxs-lookup"><span data-stu-id="8d873-369">**PolicySourceClipboardMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-370">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-370">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-371">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-372">指出 **ClipboardMapping** 屬性是由伺服器、群組原則或預設設定。</span><span class="sxs-lookup"><span data-stu-id="8d873-372">Indicates whether the **ClipboardMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8d873-373">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="8d873-373">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-374">伺服器</span><span class="sxs-lookup"><span data-stu-id="8d873-374">Server</span></span>

</dd> <dt>

<span data-ttu-id="8d873-375">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="8d873-375">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-376">群組原則</span><span class="sxs-lookup"><span data-stu-id="8d873-376">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8d873-377">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="8d873-377">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-378">預設</span><span class="sxs-lookup"><span data-stu-id="8d873-378">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-379">**PolicySourceColorDepth**</span><span class="sxs-lookup"><span data-stu-id="8d873-379">**PolicySourceColorDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-380">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-381">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-382">指出 **ColorDepth** 屬性是由伺服器、群組原則或預設設定。</span><span class="sxs-lookup"><span data-stu-id="8d873-382">Indicates whether the **ColorDepth** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8d873-383">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="8d873-383">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-384">伺服器</span><span class="sxs-lookup"><span data-stu-id="8d873-384">Server</span></span>

</dd> <dt>

<span data-ttu-id="8d873-385">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="8d873-385">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-386">群組原則</span><span class="sxs-lookup"><span data-stu-id="8d873-386">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8d873-387">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="8d873-387">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-388">預設</span><span class="sxs-lookup"><span data-stu-id="8d873-388">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-389">**PolicySourceColorDepthPolicy**</span><span class="sxs-lookup"><span data-stu-id="8d873-389">**PolicySourceColorDepthPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-390">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-390">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-391">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-392">指出 **ColorDepthPolicy** 屬性是由伺服器、群組原則或預設設定。</span><span class="sxs-lookup"><span data-stu-id="8d873-392">Indicates whether the **ColorDepthPolicy** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8d873-393">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="8d873-393">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-394">伺服器</span><span class="sxs-lookup"><span data-stu-id="8d873-394">Server</span></span>

</dd> <dt>

<span data-ttu-id="8d873-395">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="8d873-395">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-396">群組原則</span><span class="sxs-lookup"><span data-stu-id="8d873-396">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8d873-397">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="8d873-397">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-398">預設</span><span class="sxs-lookup"><span data-stu-id="8d873-398">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-399">**PolicySourceCOMPortMapping**</span><span class="sxs-lookup"><span data-stu-id="8d873-399">**PolicySourceCOMPortMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-400">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-400">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-401">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-401">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-402">指出 **COMPortMapping** 屬性是由伺服器、群組原則或預設設定。</span><span class="sxs-lookup"><span data-stu-id="8d873-402">Indicates whether the **COMPortMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8d873-403">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="8d873-403">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-404">伺服器</span><span class="sxs-lookup"><span data-stu-id="8d873-404">Server</span></span>

</dd> <dt>

<span data-ttu-id="8d873-405">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="8d873-405">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-406">群組原則</span><span class="sxs-lookup"><span data-stu-id="8d873-406">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8d873-407">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="8d873-407">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-408">預設</span><span class="sxs-lookup"><span data-stu-id="8d873-408">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-409">**PolicySourceDefaultToClientPrinter**</span><span class="sxs-lookup"><span data-stu-id="8d873-409">**PolicySourceDefaultToClientPrinter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-410">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-410">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-411">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-412">指出 **DefaultToClientPrinter** 屬性是由伺服器、群組原則或預設設定。</span><span class="sxs-lookup"><span data-stu-id="8d873-412">Indicates whether the **DefaultToClientPrinter** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8d873-413">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="8d873-413">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-414">伺服器</span><span class="sxs-lookup"><span data-stu-id="8d873-414">Server</span></span>

</dd> <dt>

<span data-ttu-id="8d873-415">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="8d873-415">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-416">群組原則</span><span class="sxs-lookup"><span data-stu-id="8d873-416">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8d873-417">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="8d873-417">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-418">預設</span><span class="sxs-lookup"><span data-stu-id="8d873-418">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-419">**PolicySourceDriveMapping**</span><span class="sxs-lookup"><span data-stu-id="8d873-419">**PolicySourceDriveMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-420">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-420">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-421">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-422">指出 **DriveMapping** 屬性是由伺服器、群組原則或預設設定。</span><span class="sxs-lookup"><span data-stu-id="8d873-422">Indicates whether the **DriveMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8d873-423">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="8d873-423">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-424">伺服器</span><span class="sxs-lookup"><span data-stu-id="8d873-424">Server</span></span>

</dd> <dt>

<span data-ttu-id="8d873-425">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="8d873-425">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-426">群組原則</span><span class="sxs-lookup"><span data-stu-id="8d873-426">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8d873-427">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="8d873-427">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-428">預設</span><span class="sxs-lookup"><span data-stu-id="8d873-428">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-429">**PolicySourceEncodeImageQuality**</span><span class="sxs-lookup"><span data-stu-id="8d873-429">**PolicySourceEncodeImageQuality**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-430">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-430">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-431">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-432">指出如何設定 **EncodeImageQualityi** 。</span><span class="sxs-lookup"><span data-stu-id="8d873-432">Indicates how the **EncodeImageQualityi** is configured.</span></span>

<span data-ttu-id="8d873-433">**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：** 此屬性在 Windows 8 或 Windows Server 2012 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="8d873-433">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="8d873-434">0</span><span class="sxs-lookup"><span data-stu-id="8d873-434">0</span></span>
</dt> <dd>

<span data-ttu-id="8d873-435">伺服器</span><span class="sxs-lookup"><span data-stu-id="8d873-435">Server</span></span>

</dd> <dt>

<span data-ttu-id="8d873-436">1</span><span class="sxs-lookup"><span data-stu-id="8d873-436">1</span></span>
</dt> <dd>

<span data-ttu-id="8d873-437">群組原則</span><span class="sxs-lookup"><span data-stu-id="8d873-437">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-438">**PolicySourceHardwareGraphicsAdapter**</span><span class="sxs-lookup"><span data-stu-id="8d873-438">**PolicySourceHardwareGraphicsAdapter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-439">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-439">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-440">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-441">指出如何設定 **HardwareGraphicsAdapter** 。</span><span class="sxs-lookup"><span data-stu-id="8d873-441">Indicates how the **HardwareGraphicsAdapter** is configured.</span></span>

<span data-ttu-id="8d873-442">**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：** 此屬性在 Windows 8 或 Windows Server 2012 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="8d873-442">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="8d873-443">0</span><span class="sxs-lookup"><span data-stu-id="8d873-443">0</span></span>
</dt> <dd>

<span data-ttu-id="8d873-444">伺服器</span><span class="sxs-lookup"><span data-stu-id="8d873-444">Server</span></span>

</dd> <dt>

<span data-ttu-id="8d873-445">1</span><span class="sxs-lookup"><span data-stu-id="8d873-445">1</span></span>
</dt> <dd>

<span data-ttu-id="8d873-446">群組原則</span><span class="sxs-lookup"><span data-stu-id="8d873-446">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-447">**PolicySourceLPTPortMapping**</span><span class="sxs-lookup"><span data-stu-id="8d873-447">**PolicySourceLPTPortMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-448">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-448">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-449">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-450">指出 **LPTPortMapping** 屬性是由伺服器、群組原則或預設設定。</span><span class="sxs-lookup"><span data-stu-id="8d873-450">Indicates whether the **LPTPortMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8d873-451">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="8d873-451">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-452">伺服器</span><span class="sxs-lookup"><span data-stu-id="8d873-452">Server</span></span>

</dd> <dt>

<span data-ttu-id="8d873-453">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="8d873-453">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-454">群組原則</span><span class="sxs-lookup"><span data-stu-id="8d873-454">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8d873-455">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="8d873-455">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-456">預設</span><span class="sxs-lookup"><span data-stu-id="8d873-456">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-457">**PolicySourceMaxMonitors**</span><span class="sxs-lookup"><span data-stu-id="8d873-457">**PolicySourceMaxMonitors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-458">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-458">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-459">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-460">指出 **MaxMonitors** 屬性是由伺服器、群組原則或預設值所設定。</span><span class="sxs-lookup"><span data-stu-id="8d873-460">Indicates whether the **MaxMonitors** property is configured by the server, group policy, or default.</span></span>

<dt>

<span data-ttu-id="8d873-461">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="8d873-461">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-462">伺服器</span><span class="sxs-lookup"><span data-stu-id="8d873-462">Server</span></span>

</dd> <dt>

<span data-ttu-id="8d873-463">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="8d873-463">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-464">群組原則</span><span class="sxs-lookup"><span data-stu-id="8d873-464">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8d873-465">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="8d873-465">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-466">預設</span><span class="sxs-lookup"><span data-stu-id="8d873-466">Default</span></span>

</dd> </dl>

<span data-ttu-id="8d873-467">**Windows Server 2008 和 Windows Vista：** 此屬性在 Windows Server 2008 R2 和 Windows 7 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="8d873-467">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="8d873-468">**PolicySourceMaxResolution**</span><span class="sxs-lookup"><span data-stu-id="8d873-468">**PolicySourceMaxResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-469">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-469">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-470">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-471">指出 **MaxXResolution** 和 **MaxYResolution** 屬性是否由伺服器、群組原則或預設值所設定。</span><span class="sxs-lookup"><span data-stu-id="8d873-471">Indicates whether the **MaxXResolution** and **MaxYResolution** properties are configured by the server, group policy, or default.</span></span>

<span data-ttu-id="8d873-472">**Windows Server 2008 和 Windows Vista：** 此屬性在 Windows Server 2008 R2 和 Windows 7 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="8d873-472">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span data-ttu-id="8d873-473">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="8d873-473">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-474">伺服器</span><span class="sxs-lookup"><span data-stu-id="8d873-474">Server</span></span>

</dd> <dt>

<span data-ttu-id="8d873-475">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="8d873-475">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-476">群組原則</span><span class="sxs-lookup"><span data-stu-id="8d873-476">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8d873-477">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="8d873-477">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-478">預設</span><span class="sxs-lookup"><span data-stu-id="8d873-478">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-479">**PolicySourcePNPRedirection**</span><span class="sxs-lookup"><span data-stu-id="8d873-479">**PolicySourcePNPRedirection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-480">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-480">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-481">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-482">指出 **PNPRedirection** 屬性是由伺服器或群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="8d873-482">Indicates whether the **PNPRedirection** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="8d873-483">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="8d873-483">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-484">伺服器</span><span class="sxs-lookup"><span data-stu-id="8d873-484">Server</span></span>

</dd> <dt>

<span data-ttu-id="8d873-485">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="8d873-485">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-486">群組原則</span><span class="sxs-lookup"><span data-stu-id="8d873-486">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-487">**PolicySourceRemoteSessionProfile**</span><span class="sxs-lookup"><span data-stu-id="8d873-487">**PolicySourceRemoteSessionProfile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-488">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-488">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-489">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-489">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-490">指出如何設定 **RemoteSessionProfile** 。</span><span class="sxs-lookup"><span data-stu-id="8d873-490">Indicates how the **RemoteSessionProfile** is configured.</span></span>

<span data-ttu-id="8d873-491">**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：** 此屬性在 Windows 8 或 Windows Server 2012 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="8d873-491">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is unavailable prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="8d873-492">0</span><span class="sxs-lookup"><span data-stu-id="8d873-492">0</span></span>
</dt> <dd>

<span data-ttu-id="8d873-493">伺服器</span><span class="sxs-lookup"><span data-stu-id="8d873-493">Server</span></span>

</dd> <dt>

<span data-ttu-id="8d873-494">1</span><span class="sxs-lookup"><span data-stu-id="8d873-494">1</span></span>
</dt> <dd>

<span data-ttu-id="8d873-495">群組原則</span><span class="sxs-lookup"><span data-stu-id="8d873-495">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-496">**PolicySourceSelectNetworkDetect**</span><span class="sxs-lookup"><span data-stu-id="8d873-496">**PolicySourceSelectNetworkDetect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-497">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-497">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-498">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-498">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-499">指出屬性 **SelectNetworkDetect** 的設定方式。</span><span class="sxs-lookup"><span data-stu-id="8d873-499">Indicates how the property **SelectNetworkDetect** is configured.</span></span>

<span data-ttu-id="8d873-500">**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：** 此屬性在 Windows 8 或 Windows Server 2012 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="8d873-500">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="8d873-501">0</span><span class="sxs-lookup"><span data-stu-id="8d873-501">0</span></span>
</dt> <dd>

<span data-ttu-id="8d873-502">伺服器</span><span class="sxs-lookup"><span data-stu-id="8d873-502">Server</span></span>

</dd> <dt>

<span data-ttu-id="8d873-503">1</span><span class="sxs-lookup"><span data-stu-id="8d873-503">1</span></span>
</dt> <dd>

<span data-ttu-id="8d873-504">群組原則</span><span class="sxs-lookup"><span data-stu-id="8d873-504">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-505">**PolicySourceSelectTransport**</span><span class="sxs-lookup"><span data-stu-id="8d873-505">**PolicySourceSelectTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-506">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-506">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-507">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-508">指出屬性 **SelectTransport** 的設定方式。</span><span class="sxs-lookup"><span data-stu-id="8d873-508">Indicates how the property **SelectTransport** is configured.</span></span>

<span data-ttu-id="8d873-509">**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：** 此屬性在 Windows 8 或 Windows Server 2012 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="8d873-509">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="8d873-510">0</span><span class="sxs-lookup"><span data-stu-id="8d873-510">0</span></span>
</dt> <dd>

<span data-ttu-id="8d873-511">伺服器</span><span class="sxs-lookup"><span data-stu-id="8d873-511">Server</span></span>

</dd> <dt>

<span data-ttu-id="8d873-512">1</span><span class="sxs-lookup"><span data-stu-id="8d873-512">1</span></span>
</dt> <dd>

<span data-ttu-id="8d873-513">群組原則</span><span class="sxs-lookup"><span data-stu-id="8d873-513">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-514">**PolicySourceVideoPlaybackRedir**</span><span class="sxs-lookup"><span data-stu-id="8d873-514">**PolicySourceVideoPlaybackRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-515">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-515">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-516">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-516">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-517">指出是否由伺服器或群組原則設定 **VideoPlaybackRedir** 屬性。</span><span class="sxs-lookup"><span data-stu-id="8d873-517">Indicates whether the **VideoPlaybackRedir** property is configured by the server or group policy.</span></span>

<span data-ttu-id="8d873-518">**Windows Server 2008 和 Windows Vista：** 此屬性在 Windows Server 2008 R2 和 Windows 7 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="8d873-518">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span data-ttu-id="8d873-519">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="8d873-519">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-520">伺服器</span><span class="sxs-lookup"><span data-stu-id="8d873-520">Server</span></span>

</dd> <dt>

<span data-ttu-id="8d873-521">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="8d873-521">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-522">群組原則</span><span class="sxs-lookup"><span data-stu-id="8d873-522">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-523">**PolicySourceWindowsPrinterMapping**</span><span class="sxs-lookup"><span data-stu-id="8d873-523">**PolicySourceWindowsPrinterMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-524">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-524">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-525">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-525">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-526">指出 **WindowsPrinterMapping** 屬性是由伺服器、群組原則或預設設定。</span><span class="sxs-lookup"><span data-stu-id="8d873-526">Indicates whether the **WindowsPrinterMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8d873-527">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="8d873-527">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-528">伺服器</span><span class="sxs-lookup"><span data-stu-id="8d873-528">Server</span></span>

</dd> <dt>

<span data-ttu-id="8d873-529">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="8d873-529">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-530">群組原則</span><span class="sxs-lookup"><span data-stu-id="8d873-530">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8d873-531">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="8d873-531">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8d873-532">預設</span><span class="sxs-lookup"><span data-stu-id="8d873-532">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-533">**RemoteSessionProfile**</span><span class="sxs-lookup"><span data-stu-id="8d873-533">**RemoteSessionProfile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-534">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-534">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-535">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8d873-535">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8d873-536">指定 RDP 體驗的設定檔。</span><span class="sxs-lookup"><span data-stu-id="8d873-536">Specifies the profile for the RDP experience.</span></span>

<span data-ttu-id="8d873-537">**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：** 此屬性在 Windows 8 或 Windows Server 2012 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="8d873-537">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span id="scale"></span><span id="SCALE"></span>

<span data-ttu-id="8d873-538">**調整** (1) </span><span class="sxs-lookup"><span data-stu-id="8d873-538">**scale** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="experience"></span><span id="EXPERIENCE"></span>

<span data-ttu-id="8d873-539">**體驗** (2) </span><span class="sxs-lookup"><span data-stu-id="8d873-539">**experience** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="bandwidth"></span><span id="BANDWIDTH"></span>

<span data-ttu-id="8d873-540">**頻寬** (3) </span><span class="sxs-lookup"><span data-stu-id="8d873-540">**bandwidth** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-541">**SelectNetworkDetect**</span><span class="sxs-lookup"><span data-stu-id="8d873-541">**SelectNetworkDetect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-542">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-542">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-543">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8d873-543">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8d873-544">指定是否使用網路偵測。</span><span class="sxs-lookup"><span data-stu-id="8d873-544">Specifies whether network detection is used.</span></span>

<span data-ttu-id="8d873-545">**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：** 此屬性在 Windows 8 或 Windows Server 2012 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="8d873-545">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="8d873-546">0</span><span class="sxs-lookup"><span data-stu-id="8d873-546">0</span></span>
</dt> <dd>

<span data-ttu-id="8d873-547">在連線時間和穩定狀態中使用。</span><span class="sxs-lookup"><span data-stu-id="8d873-547">used at connect time and in steady state.</span></span>

</dd> <dt>

<span data-ttu-id="8d873-548">1</span><span class="sxs-lookup"><span data-stu-id="8d873-548">1</span></span>
</dt> <dd>

<span data-ttu-id="8d873-549">在連線時間停用</span><span class="sxs-lookup"><span data-stu-id="8d873-549">disabled at connect time</span></span>

</dd> <dt>

<span data-ttu-id="8d873-550">2</span><span class="sxs-lookup"><span data-stu-id="8d873-550">2</span></span>
</dt> <dd>

<span data-ttu-id="8d873-551">在穩定狀態中停用</span><span class="sxs-lookup"><span data-stu-id="8d873-551">disabled in steady state</span></span>

</dd> <dt>

<span data-ttu-id="8d873-552">3</span><span class="sxs-lookup"><span data-stu-id="8d873-552">3</span></span>
</dt> <dd>

<span data-ttu-id="8d873-553">在連線時間和穩定狀態中停用。</span><span class="sxs-lookup"><span data-stu-id="8d873-553">disabled at connect time and in steady state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-554">**SelectTransport**</span><span class="sxs-lookup"><span data-stu-id="8d873-554">**SelectTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-555">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-555">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-556">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8d873-556">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8d873-557">指定可使用哪些傳輸通訊協定來進行伺服器的 RDP 存取。</span><span class="sxs-lookup"><span data-stu-id="8d873-557">Specifies which transport protocols can be used for RDP access to server.</span></span>

<span data-ttu-id="8d873-558">**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：** 此屬性在 Windows 8 或 Windows Server 2012 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="8d873-558">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="8d873-559">0</span><span class="sxs-lookup"><span data-stu-id="8d873-559">0</span></span>
</dt> <dd>

<span data-ttu-id="8d873-560">使用 UDP 和 TCP。</span><span class="sxs-lookup"><span data-stu-id="8d873-560">Use both UDP and TCP.</span></span>

</dd> <dt>

<span data-ttu-id="8d873-561">1</span><span class="sxs-lookup"><span data-stu-id="8d873-561">1</span></span>
</dt> <dd>

<span data-ttu-id="8d873-562">僅使用 TCP。</span><span class="sxs-lookup"><span data-stu-id="8d873-562">Use only TCP.</span></span>

</dd> <dt>

<span data-ttu-id="8d873-563">2</span><span class="sxs-lookup"><span data-stu-id="8d873-563">2</span></span>
</dt> <dd>

<span data-ttu-id="8d873-564">請使用 UDP 或 TCP。</span><span class="sxs-lookup"><span data-stu-id="8d873-564">Use either UDP or TCP.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-565">**狀態**</span><span class="sxs-lookup"><span data-stu-id="8d873-565">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-566">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8d873-566">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-567">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-567">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d873-568">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="8d873-568">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="8d873-569">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="8d873-569">Current status of the object.</span></span> <span data-ttu-id="8d873-570">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="8d873-570">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="8d873-571">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="8d873-571">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="8d873-572">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="8d873-572">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8d873-573">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="8d873-573">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8d873-574">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="8d873-574">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8d873-575">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8d873-575">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="8d873-576"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="8d873-576">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8d873-577"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="8d873-577">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8d873-578"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="8d873-578">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8d873-579"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="8d873-579">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8d873-580"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="8d873-580">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8d873-581"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="8d873-581">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8d873-582"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="8d873-582">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8d873-583"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="8d873-583">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-584">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="8d873-584">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-585">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8d873-585">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-586">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-586">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-587">終端機的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d873-587">The name of the terminal.</span></span>

<span data-ttu-id="8d873-588">這個屬性繼承自 [**Win32 \_ TerminalSetting**](win32-terminalsetting.md)。</span><span class="sxs-lookup"><span data-stu-id="8d873-588">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d873-589">**VideoPlaybackRedir**</span><span class="sxs-lookup"><span data-stu-id="8d873-589">**VideoPlaybackRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-590">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-590">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-591">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-591">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-592">指定是否允許播放影片重新導向。</span><span class="sxs-lookup"><span data-stu-id="8d873-592">Specifies whether to allow video playback redirection.</span></span>

<span data-ttu-id="8d873-593">**Windows Server 2008 和 Windows Vista：** 此屬性在 Windows Server 2008 R2 和 Windows 7 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="8d873-593">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8d873-594">**FALSE** (0) </span><span class="sxs-lookup"><span data-stu-id="8d873-594">**FALSE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8d873-595">**TRUE** (1) </span><span class="sxs-lookup"><span data-stu-id="8d873-595">**TRUE** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8d873-596">**WindowsPrinterMapping**</span><span class="sxs-lookup"><span data-stu-id="8d873-596">**WindowsPrinterMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d873-597">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d873-597">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d873-598">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8d873-598">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d873-599">指定是否停用或啟用用戶端視窗的印表機對應。</span><span class="sxs-lookup"><span data-stu-id="8d873-599">Specifies whether printer mapping is disabled or enabled for the client's window.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8d873-600"><span id="FALSE"></span><span id="false"></span>**FALSE** (0) </span><span class="sxs-lookup"><span data-stu-id="8d873-600"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8d873-601">印表機對應已啟用。</span><span class="sxs-lookup"><span data-stu-id="8d873-601">Printer mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8d873-602"><span id="TRUE"></span><span id="true"></span>**TRUE** (1) </span><span class="sxs-lookup"><span data-stu-id="8d873-602"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8d873-603">印表機對應已停用。</span><span class="sxs-lookup"><span data-stu-id="8d873-603">Printer mapping is disabled.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8d873-604">備註</span><span class="sxs-lookup"><span data-stu-id="8d873-604">Remarks</span></span>

<span data-ttu-id="8d873-605">請注意，與主控台會話相關聯的視窗工作站無法存取此類別的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="8d873-605">Be aware that a window station associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="8d873-606">如果嘗試將 "Console" 指定為 **TerminalName** 屬性的值，則此物件的方法會傳回 **\_ \_ 不 \_ 支援的 WBEM E**。</span><span class="sxs-lookup"><span data-stu-id="8d873-606">If an attempt is made to do so by specifying "Console" as the value of the **TerminalName** property, methods of this object will return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="8d873-607">如果視窗工作站嘗試呼叫此物件的方法來新增或修改 LocalSystem、LocalService 或 NetworkService 帳戶的安全性屬性，也會傳回此錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8d873-607">This error code is also returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="8d873-608">若要連接到 \\ 根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway 命名空間，驗證層級必須包含封包隱私權。</span><span class="sxs-lookup"><span data-stu-id="8d873-608">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="8d873-609">針對 C/c + + 呼叫，這是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="8d873-609">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="8d873-610">針對 Visual Basic 和腳本呼叫，這是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為六。</span><span class="sxs-lookup"><span data-stu-id="8d873-610">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of six.</span></span>

<span data-ttu-id="8d873-611">下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="8d873-611">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="8d873-612">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="8d873-612">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8d873-613">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="8d873-613">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8d873-614">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="8d873-614">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8d873-615">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="8d873-615">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d873-616">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d873-616">Requirements</span></span>



| <span data-ttu-id="8d873-617">需求</span><span class="sxs-lookup"><span data-stu-id="8d873-617">Requirement</span></span> | <span data-ttu-id="8d873-618">值</span><span class="sxs-lookup"><span data-stu-id="8d873-618">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d873-619">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8d873-619">Minimum supported client</span></span><br/> | <span data-ttu-id="8d873-620">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8d873-620">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8d873-621">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8d873-621">Minimum supported server</span></span><br/> | <span data-ttu-id="8d873-622">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d873-622">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8d873-623">命名空間</span><span class="sxs-lookup"><span data-stu-id="8d873-623">Namespace</span></span><br/>                | <span data-ttu-id="8d873-624">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="8d873-624">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="8d873-625">MOF</span><span class="sxs-lookup"><span data-stu-id="8d873-625">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d873-626"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d873-626"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8d873-627">DLL</span><span class="sxs-lookup"><span data-stu-id="8d873-627">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d873-628"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d873-628"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d873-629">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d873-629">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d873-630">**Win32 \_ 終端機**</span><span class="sxs-lookup"><span data-stu-id="8d873-630">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="8d873-631">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="8d873-631">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dt>

[<span data-ttu-id="8d873-632">**CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="8d873-632">**CIM\_Setting**</span></span>](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

