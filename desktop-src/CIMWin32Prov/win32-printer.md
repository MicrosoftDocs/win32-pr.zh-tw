---
description: 代表連接到在 Microsoft Windows 作業系統上執行之電腦的裝置，該電腦可在紙張或其他媒體上產生列印的影像或文字。
ms.assetid: 58090e6a-8f13-4859-adb8-a7c6299d3efd
ms.tgt_platform: multiple
title: Win32_Printer 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer
- Win32_Printer.Reset
- Win32_Printer.SetPowerState
- Win32_Printer.Attributes
- Win32_Printer.Availability
- Win32_Printer.AvailableJobSheets
- Win32_Printer.AveragePagesPerMinute
- Win32_Printer.Capabilities
- Win32_Printer.CapabilityDescriptions
- Win32_Printer.Caption
- Win32_Printer.CharSetsSupported
- Win32_Printer.Comment
- Win32_Printer.ConfigManagerErrorCode
- Win32_Printer.ConfigManagerUserConfig
- Win32_Printer.CreationClassName
- Win32_Printer.CurrentCapabilities
- Win32_Printer.CurrentCharSet
- Win32_Printer.CurrentLanguage
- Win32_Printer.CurrentMimeType
- Win32_Printer.CurrentNaturalLanguage
- Win32_Printer.CurrentPaperType
- Win32_Printer.Default
- Win32_Printer.DefaultCapabilities
- Win32_Printer.DefaultCopies
- Win32_Printer.DefaultLanguage
- Win32_Printer.DefaultMimeType
- Win32_Printer.DefaultNumberUp
- Win32_Printer.DefaultPaperType
- Win32_Printer.DefaultPriority
- Win32_Printer.Description
- Win32_Printer.DetectedErrorState
- Win32_Printer.DeviceID
- Win32_Printer.Direct
- Win32_Printer.DoCompleteFirst
- Win32_Printer.DriverName
- Win32_Printer.EnableBIDI
- Win32_Printer.EnableDevQueryPrint
- Win32_Printer.ErrorCleared
- Win32_Printer.ErrorDescription
- Win32_Printer.ErrorInformation
- Win32_Printer.ExtendedDetectedErrorState
- Win32_Printer.ExtendedPrinterStatus
- Win32_Printer.Hidden
- Win32_Printer.HorizontalResolution
- Win32_Printer.InstallDate
- Win32_Printer.JobCountSinceLastReset
- Win32_Printer.KeepPrintedJobs
- Win32_Printer.LanguagesSupported
- Win32_Printer.LastErrorCode
- Win32_Printer.Local
- Win32_Printer.Location
- Win32_Printer.MarkingTechnology
- Win32_Printer.MaxCopies
- Win32_Printer.MaxNumberUp
- Win32_Printer.MaxSizeSupported
- Win32_Printer.MimeTypesSupported
- Win32_Printer.Name
- Win32_Printer.NaturalLanguagesSupported
- Win32_Printer.Network
- Win32_Printer.PaperSizesSupported
- Win32_Printer.PaperTypesAvailable
- Win32_Printer.Parameters
- Win32_Printer.PNPDeviceID
- Win32_Printer.PortName
- Win32_Printer.PowerManagementCapabilities
- Win32_Printer.PowerManagementSupported
- Win32_Printer.PrinterPaperNames
- Win32_Printer.PrinterState
- Win32_Printer.PrinterStatus
- Win32_Printer.PrintJobDataType
- Win32_Printer.PrintProcessor
- Win32_Printer.Priority
- Win32_Printer.Published
- Win32_Printer.Queued
- Win32_Printer.RawOnly
- Win32_Printer.SeparatorFile
- Win32_Printer.ServerName
- Win32_Printer.Shared
- Win32_Printer.ShareName
- Win32_Printer.SpoolEnabled
- Win32_Printer.StartTime
- Win32_Printer.Status
- Win32_Printer.StatusInfo
- Win32_Printer.SystemCreationClassName
- Win32_Printer.SystemName
- Win32_Printer.TimeOfLastReset
- Win32_Printer.UntilTime
- Win32_Printer.VerticalResolution
- Win32_Printer.WorkOffline
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 48fc170cb3e85d44dc3e01140fe2c881a7ec975b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187731"
---
# <a name="win32_printer-class"></a><span data-ttu-id="046b4-103">Win32 \_ 印表機類別</span><span class="sxs-lookup"><span data-stu-id="046b4-103">Win32\_Printer class</span></span>

<span data-ttu-id="046b4-104">**Win32 \_ 印表機** [WMI 類別](../wmisdk/retrieving-a-class.md)代表連接到在 Microsoft Windows 作業系統上執行之電腦的裝置，可在紙張或其他媒體上產生列印的影像或文字。</span><span class="sxs-lookup"><span data-stu-id="046b4-104">The **Win32\_Printer** [WMI class](../wmisdk/retrieving-a-class.md) represents a device connected to a computer running on a Microsoft Windows operating system that can produce a printed image or text on paper or other medium.</span></span>

<span data-ttu-id="046b4-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="046b4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="046b4-106">語法</span><span class="sxs-lookup"><span data-stu-id="046b4-106">Syntax</span></span>

``` syntax
class Win32_Printer : CIM_Printer
{
  uint32   Attributes;
  uint16   Availability;
  string   AvailableJobSheets[];
  uint32   AveragePagesPerMinute;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CharSetsSupported[];
  string   Comment;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint16   CurrentCapabilities[];
  string   CurrentCharSet;
  uint16   CurrentLanguage;
  string   CurrentMimeType;
  string   CurrentNaturalLanguage;
  string   CurrentPaperType;
  boolean  Default;
  uint16   DefaultCapabilities[];
  uint32   DefaultCopies;
  uint16   DefaultLanguage;
  string   DefaultMimeType;
  uint32   DefaultNumberUp;
  string   DefaultPaperType;
  uint32   DefaultPriority;
  string   Description;
  uint16   DetectedErrorState;
  string   DeviceID;
  boolean  Direct;
  boolean  DoCompleteFirst;
  string   DriverName;
  boolean  EnableBIDI;
  boolean  EnableDevQueryPrint;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorInformation[];
  uint16   ExtendedDetectedErrorState;
  uint16   ExtendedPrinterStatus;
  boolean  Hidden;
  uint32   HorizontalResolution;
  datetime InstallDate;
  uint32   JobCountSinceLastReset;
  boolean  KeepPrintedJobs;
  uint16   LanguagesSupported[];
  uint32   LastErrorCode;
  boolean  Local;
  string   Location;
  uint16   MarkingTechnology;
  uint32   MaxCopies;
  uint32   MaxNumberUp;
  uint32   MaxSizeSupported;
  string   MimeTypesSupported[];
  string   Name;
  string   NaturalLanguagesSupported[];
  boolean  Network;
  uint16   PaperSizesSupported[];
  string   PaperTypesAvailable[];
  string   Parameters;
  string   PNPDeviceID;
  string   PortName;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   PrinterPaperNames[];
  uint32   PrinterState;
  uint16   PrinterStatus;
  string   PrintJobDataType;
  string   PrintProcessor;
  uint32   Priority;
  boolean  Published;
  boolean  Queued;
  boolean  RawOnly;
  string   SeparatorFile;
  string   ServerName;
  boolean  Shared;
  string   ShareName;
  boolean  SpoolEnabled;
  datetime StartTime;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
  datetime UntilTime;
  uint32   VerticalResolution;
  boolean  WorkOffline;
};
```

## <a name="members"></a><span data-ttu-id="046b4-107">成員</span><span class="sxs-lookup"><span data-stu-id="046b4-107">Members</span></span>

<span data-ttu-id="046b4-108">**Win32 \_ 印表機** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="046b4-108">The **Win32\_Printer** class has these types of members:</span></span>

-   [<span data-ttu-id="046b4-109">方法</span><span class="sxs-lookup"><span data-stu-id="046b4-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="046b4-110">屬性</span><span class="sxs-lookup"><span data-stu-id="046b4-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="046b4-111">方法</span><span class="sxs-lookup"><span data-stu-id="046b4-111">Methods</span></span>

<span data-ttu-id="046b4-112">**Win32 \_ 印表機** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="046b4-112">The **Win32\_Printer** class has these methods.</span></span>



| <span data-ttu-id="046b4-113">方法</span><span class="sxs-lookup"><span data-stu-id="046b4-113">Method</span></span>                                                                               | <span data-ttu-id="046b4-114">描述</span><span class="sxs-lookup"><span data-stu-id="046b4-114">Description</span></span>                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="046b4-115">**AddPrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="046b4-115">**AddPrinterConnection**</span></span>](addprinterconnection-method-in-class-win32-printer.md)   | <span data-ttu-id="046b4-116">將連接新增至印表機。</span><span class="sxs-lookup"><span data-stu-id="046b4-116">Adds a connection to the printer.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="046b4-117">**CancelAllJobs**</span><span class="sxs-lookup"><span data-stu-id="046b4-117">**CancelAllJobs**</span></span>](cancelalljobs-method-in-class-win32-printer.md)                 | <span data-ttu-id="046b4-118">取消所有作業。</span><span class="sxs-lookup"><span data-stu-id="046b4-118">Cancels all jobs.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="046b4-119">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="046b4-119">**GetSecurityDescriptor**</span></span>](getsecuritydescriptor-method-in-class-win32-printer.md) | <span data-ttu-id="046b4-120">傳回控制印表機存取的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="046b4-120">Returns the security descriptor that controls access to the printer.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="046b4-121">**暫停**</span><span class="sxs-lookup"><span data-stu-id="046b4-121">**Pause**</span></span>](pause-method-in-class-win32-printer.md)                                 | <span data-ttu-id="046b4-122">暫停列印佇列。</span><span class="sxs-lookup"><span data-stu-id="046b4-122">Pauses the print queue.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="046b4-123">**PrintTestPage**</span><span class="sxs-lookup"><span data-stu-id="046b4-123">**PrintTestPage**</span></span>](printtestpage-method-in-class-win32-printer.md)                 | <span data-ttu-id="046b4-124">列印測試頁面。</span><span class="sxs-lookup"><span data-stu-id="046b4-124">Prints a test page.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="046b4-125">**RenamePrinter**</span><span class="sxs-lookup"><span data-stu-id="046b4-125">**RenamePrinter**</span></span>](renameprinter-method-in-class-win32-printer.md)                 | <span data-ttu-id="046b4-126">重新命名印表機。</span><span class="sxs-lookup"><span data-stu-id="046b4-126">Renames a printer.</span></span><br/>                                                                                                                                                                                     |
| <span data-ttu-id="046b4-127">**重設**</span><span class="sxs-lookup"><span data-stu-id="046b4-127">**Reset**</span></span>                                                                            | <span data-ttu-id="046b4-128">未實作。</span><span class="sxs-lookup"><span data-stu-id="046b4-128">Not implemented.</span></span> <span data-ttu-id="046b4-129">如需如何執行此方法的詳細資訊，請參閱 [**CIM \_ 印表機**](cim-printer.md)中的 [**Reset**](reset-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="046b4-129">For more information about how to implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Printer**](cim-printer.md).</span></span><br/>                 |
| [<span data-ttu-id="046b4-130">**繼續**</span><span class="sxs-lookup"><span data-stu-id="046b4-130">**Resume**</span></span>](resume-method-in-class-win32-printer.md)                               | <span data-ttu-id="046b4-131">繼續暫停的列印佇列。</span><span class="sxs-lookup"><span data-stu-id="046b4-131">Resumes paused print queue.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="046b4-132">**SetDefaultPrinter**</span><span class="sxs-lookup"><span data-stu-id="046b4-132">**SetDefaultPrinter**</span></span>](setdefaultprinter-method-in-class-win32-printer.md)         | <span data-ttu-id="046b4-133">設定預設印表機。</span><span class="sxs-lookup"><span data-stu-id="046b4-133">Sets the default printer.</span></span><br/>                                                                                                                                                                              |
| <span data-ttu-id="046b4-134">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="046b4-134">**SetPowerState**</span></span>                                                                    | <span data-ttu-id="046b4-135">未實作。</span><span class="sxs-lookup"><span data-stu-id="046b4-135">Not implemented.</span></span> <span data-ttu-id="046b4-136">如需如何執行此方法的詳細資訊，請參閱 [**CIM \_ 印表機**](cim-printer.md)中的 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="046b4-136">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Printer**](cim-printer.md).</span></span><br/> |
| [<span data-ttu-id="046b4-137">**SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="046b4-137">**SetSecurityDescriptor**</span></span>](setsecuritydescriptor-method-in-class-win32-printer.md) | <span data-ttu-id="046b4-138">寫入控制印表機存取權之安全描述項的更新版本。</span><span class="sxs-lookup"><span data-stu-id="046b4-138">Writes an updated version of the security descriptor that controls access to the printer.</span></span><br/>                                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="046b4-139">屬性</span><span class="sxs-lookup"><span data-stu-id="046b4-139">Properties</span></span>

<span data-ttu-id="046b4-140">**Win32 \_ 印表機** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="046b4-140">The **Win32\_Printer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="046b4-141">**屬性**</span><span class="sxs-lookup"><span data-stu-id="046b4-141">**Attributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-142">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="046b4-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="046b4-144">以 Windows 為基礎之列印裝置的屬性點陣圖。</span><span class="sxs-lookup"><span data-stu-id="046b4-144">Bitmap of attributes for a Windows-based printing device.</span></span>

<dt>

<span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>

<span data-ttu-id="046b4-145"><span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>**印表機 \_屬性已 \_ 排入佇列** (1 (0x1) ) </span><span class="sxs-lookup"><span data-stu-id="046b4-145"><span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>**PRINTER\_ATTRIBUTE\_QUEUED** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="046b4-146">已排入佇列</span><span class="sxs-lookup"><span data-stu-id="046b4-146">Queued</span></span>

<span data-ttu-id="046b4-147">列印工作已緩衝處理並排入佇列。</span><span class="sxs-lookup"><span data-stu-id="046b4-147">Print jobs are buffered and queued.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>

<span data-ttu-id="046b4-148"><span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>**印表機 \_屬性 \_ 直接** (2 (0x2) ) </span><span class="sxs-lookup"><span data-stu-id="046b4-148"><span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>**PRINTER\_ATTRIBUTE\_DIRECT** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="046b4-149">直接</span><span class="sxs-lookup"><span data-stu-id="046b4-149">Direct</span></span>

<span data-ttu-id="046b4-150">要直接傳送到印表機的檔。</span><span class="sxs-lookup"><span data-stu-id="046b4-150">Document to be sent directly to the printer.</span></span> <span data-ttu-id="046b4-151">如果列印工作未正確排入佇列，則會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="046b4-151">This value is used if print jobs are not queued correctly.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>

<span data-ttu-id="046b4-152"><span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>**印表機 \_屬性 \_ 預設** (4 (0x4) ) </span><span class="sxs-lookup"><span data-stu-id="046b4-152"><span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>**PRINTER\_ATTRIBUTE\_DEFAULT** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="046b4-153">預設</span><span class="sxs-lookup"><span data-stu-id="046b4-153">Default</span></span>

<span data-ttu-id="046b4-154">電腦上的預設印表機。</span><span class="sxs-lookup"><span data-stu-id="046b4-154">Default printer on a computer.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>

<span data-ttu-id="046b4-155"><span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>**印表機 \_屬性 \_ 共用** (8 (0x8) ) </span><span class="sxs-lookup"><span data-stu-id="046b4-155"><span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>**PRINTER\_ATTRIBUTE\_SHARED** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="046b4-156">共用</span><span class="sxs-lookup"><span data-stu-id="046b4-156">Shared</span></span>

<span data-ttu-id="046b4-157">可作為共用網路資源。</span><span class="sxs-lookup"><span data-stu-id="046b4-157">Available as a shared network resource.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>

<span data-ttu-id="046b4-158"><span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>**印表機 \_ATTRIBUTE \_ NETWORK** (16 (0x10) ) </span><span class="sxs-lookup"><span data-stu-id="046b4-158"><span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>**PRINTER\_ATTRIBUTE\_NETWORK** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="046b4-159">網路</span><span class="sxs-lookup"><span data-stu-id="046b4-159">Network</span></span>

<span data-ttu-id="046b4-160">附加至網路。</span><span class="sxs-lookup"><span data-stu-id="046b4-160">Attached to a network.</span></span> <span data-ttu-id="046b4-161">如果同時設定了本機和網路位，這就表示網路印表機。</span><span class="sxs-lookup"><span data-stu-id="046b4-161">If both Local and Network bits are set, this indicates a network printer.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>

<span data-ttu-id="046b4-162"><span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>**印表機 \_屬性 \_ 隱藏** (32 (0x20) ) </span><span class="sxs-lookup"><span data-stu-id="046b4-162"><span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>**PRINTER\_ATTRIBUTE\_HIDDEN** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="046b4-163">Hidden</span><span class="sxs-lookup"><span data-stu-id="046b4-163">Hidden</span></span>

<span data-ttu-id="046b4-164">從網路上的某些使用者隱藏。</span><span class="sxs-lookup"><span data-stu-id="046b4-164">Hidden from some users on the network.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>

<span data-ttu-id="046b4-165"><span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>**印表機 \_屬性 \_ LOCAL** (64 (0x40) ) </span><span class="sxs-lookup"><span data-stu-id="046b4-165"><span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>**PRINTER\_ATTRIBUTE\_LOCAL** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="046b4-166">本機</span><span class="sxs-lookup"><span data-stu-id="046b4-166">Local</span></span>

<span data-ttu-id="046b4-167">直接連接到電腦。</span><span class="sxs-lookup"><span data-stu-id="046b4-167">Directly connected to a computer.</span></span> <span data-ttu-id="046b4-168">如果同時設定了本機和網路位，這就表示網路印表機。</span><span class="sxs-lookup"><span data-stu-id="046b4-168">If both Local and Network bits are set, this indicates a network printer.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>

<span data-ttu-id="046b4-169"><span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>**印表機 \_屬性 \_ ENABLEDEVQ** (128 (0x80) ) </span><span class="sxs-lookup"><span data-stu-id="046b4-169"><span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>**PRINTER\_ATTRIBUTE\_ENABLEDEVQ** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="046b4-170">EnableDevQ</span><span class="sxs-lookup"><span data-stu-id="046b4-170">EnableDevQ</span></span>

<span data-ttu-id="046b4-171">啟用印表機上的佇列（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="046b4-171">Enable the queue on the printer if available.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>

<span data-ttu-id="046b4-172"><span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>**印表機 \_屬性 \_ KEEPPRINTEDJOBS** (256 (0x100) ) </span><span class="sxs-lookup"><span data-stu-id="046b4-172"><span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>**PRINTER\_ATTRIBUTE\_KEEPPRINTEDJOBS** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="046b4-173">KeepPrintedJobs</span><span class="sxs-lookup"><span data-stu-id="046b4-173">KeepPrintedJobs</span></span>

<span data-ttu-id="046b4-174">列印多工緩衝處理器不應該在列印檔案之後刪除它們。</span><span class="sxs-lookup"><span data-stu-id="046b4-174">Spooler should not delete documents after they are printed.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>

<span data-ttu-id="046b4-175"><span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>**印表機 \_屬性 \_ \_ \_ 先完成** (512 (0x200) ) </span><span class="sxs-lookup"><span data-stu-id="046b4-175"><span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>**PRINTER\_ATTRIBUTE\_DO\_COMPLETE\_FIRST** (512 (0x200))</span></span>


</dt> <dd>

<span data-ttu-id="046b4-176">DoCompleteFirst</span><span class="sxs-lookup"><span data-stu-id="046b4-176">DoCompleteFirst</span></span>

<span data-ttu-id="046b4-177">啟動先完成幕後處理的作業。</span><span class="sxs-lookup"><span data-stu-id="046b4-177">Start jobs that are finished spooling first.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>

<span data-ttu-id="046b4-178"><span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>**印表機 \_屬性 \_ \_ 離線工作** (1024 (0x400) ) </span><span class="sxs-lookup"><span data-stu-id="046b4-178"><span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>**PRINTER\_ATTRIBUTE\_WORK\_OFFLINE** (1024 (0x400))</span></span>


</dt> <dd>

<span data-ttu-id="046b4-179">WorkOffline</span><span class="sxs-lookup"><span data-stu-id="046b4-179">WorkOffline</span></span>

<span data-ttu-id="046b4-180">無法使用印表機時，將列印工作排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="046b4-180">Queue print jobs when a printer is not available.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>

<span data-ttu-id="046b4-181"><span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>**印表機 \_ATTRIBUTE \_ 啟用 \_ 雙向** (2048 (0x800) ) </span><span class="sxs-lookup"><span data-stu-id="046b4-181"><span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>**PRINTER\_ATTRIBUTE\_ENABLE\_BIDI** (2048 (0x800))</span></span>


</dt> <dd>

<span data-ttu-id="046b4-182">EnableBIDI</span><span class="sxs-lookup"><span data-stu-id="046b4-182">EnableBIDI</span></span>

<span data-ttu-id="046b4-183">啟用雙向列印。</span><span class="sxs-lookup"><span data-stu-id="046b4-183">Enable bidirectional printing.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>

<span data-ttu-id="046b4-184"><span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>**印表機 \_\_ \_ 僅限 RAW 屬性** (4096 (0x1000) ) </span><span class="sxs-lookup"><span data-stu-id="046b4-184"><span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>**PRINTER\_ATTRIBUTE\_RAW\_ONLY** (4096 (0x1000))</span></span>


</dt> <dd>

<span data-ttu-id="046b4-185">只允許對原始資料類型作業進行多工緩衝處理。</span><span class="sxs-lookup"><span data-stu-id="046b4-185">Allow only raw data type jobs to be spooled.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>

<span data-ttu-id="046b4-186"><span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>**印表機 \_屬性 \_ 發行** (8192 (0x2000) ) </span><span class="sxs-lookup"><span data-stu-id="046b4-186"><span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>**PRINTER\_ATTRIBUTE\_PUBLISHED** (8192 (0x2000))</span></span>


</dt> <dd>

<span data-ttu-id="046b4-187">已發行</span><span class="sxs-lookup"><span data-stu-id="046b4-187">Published</span></span>

<span data-ttu-id="046b4-188">發佈于網路目錄服務。</span><span class="sxs-lookup"><span data-stu-id="046b4-188">Published in the network directory service.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="046b4-189">**可用性**</span><span class="sxs-lookup"><span data-stu-id="046b4-189">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-190">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="046b4-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-192">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="046b4-192">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-193">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="046b4-193">Availability and status of the device.</span></span>

<span data-ttu-id="046b4-194">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-194">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="046b4-195"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="046b4-195"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="046b4-196"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="046b4-196"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="046b4-197"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="046b4-197"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-198">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="046b4-198">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="046b4-199"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="046b4-199"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="046b4-200"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="046b4-200"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="046b4-201"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="046b4-201"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="046b4-202"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="046b4-202"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="046b4-203"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="046b4-203"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="046b4-204"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="046b4-204"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="046b4-205"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="046b4-205"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="046b4-206"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="046b4-206"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="046b4-207"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="046b4-207"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="046b4-208"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="046b4-208"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-209">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="046b4-209">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="046b4-210"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="046b4-210"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-211">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="046b4-211">The device is in a power save state but is still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="046b4-212"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="046b4-212"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-213">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="046b4-213">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="046b4-214"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="046b4-214"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="046b4-215"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="046b4-215"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-216">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="046b4-216">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="046b4-217"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="046b4-217"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-218">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="046b4-218">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="046b4-219"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="046b4-219"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-220">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="046b4-220">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="046b4-221"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="046b4-221"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-222">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="046b4-222">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="046b4-223"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="046b4-223"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-224">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="046b4-224">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="046b4-225">**AvailableJobSheets**</span><span class="sxs-lookup"><span data-stu-id="046b4-225">**AvailableJobSheets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-226">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="046b4-226">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="046b4-227">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-228">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "CIM \_ PrintJob. RequiredJobSheets" ) </span><span class="sxs-lookup"><span data-stu-id="046b4-228">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.RequiredJobSheets")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-229">印表機上所有可用工作表的陣列。</span><span class="sxs-lookup"><span data-stu-id="046b4-229">Array of all the job sheets available on a printer.</span></span> <span data-ttu-id="046b4-230">也可以用來描述印表機可能會在每個作業開始時提供的橫幅，或其他使用者指定的選項。</span><span class="sxs-lookup"><span data-stu-id="046b4-230">Can also be used to describe the banner that a printer might provide at the beginning of each job, or other user-specified options.</span></span>

<span data-ttu-id="046b4-231">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-231">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-232">**AveragePagesPerMinute**</span><span class="sxs-lookup"><span data-stu-id="046b4-232">**AveragePagesPerMinute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-233">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="046b4-233">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-234">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="046b4-235">印表機可以產生輸出的列印速率（平均每分鐘頁面數）。</span><span class="sxs-lookup"><span data-stu-id="046b4-235">Printing rate, in average number of pages per minute, that a printer can produce output.</span></span>

</dd> <dt>

<span data-ttu-id="046b4-236">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="046b4-236">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-237">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="046b4-237">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="046b4-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-239">限定詞： [**ArrayType**](../wmisdk/standard-qualifiers.md) ( 「已編制索引」 ) ， [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (」[**CIM \_ 印表機**](cim-printer.md)。CapabilityDescriptions "、" CIM \_ PrintJob. 完成 "、" cim \_ PrintService. 功能 ") </span><span class="sxs-lookup"><span data-stu-id="046b4-239">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).CapabilityDescriptions", "CIM\_PrintJob.Finishing", "CIM\_PrintService.Capabilities")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-240">印表機功能的陣列。</span><span class="sxs-lookup"><span data-stu-id="046b4-240">Array of printer capabilities.</span></span>

<span data-ttu-id="046b4-241">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-241">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="046b4-242"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="046b4-242"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="046b4-243"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="046b4-243"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="046b4-244"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**色彩列印** (2) </span><span class="sxs-lookup"><span data-stu-id="046b4-244"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="046b4-245"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**雙工列印** (3) </span><span class="sxs-lookup"><span data-stu-id="046b4-245"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="046b4-246"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span> (4) **複製**</span><span class="sxs-lookup"><span data-stu-id="046b4-246"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="046b4-247"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>定 **序** (5) </span><span class="sxs-lookup"><span data-stu-id="046b4-247"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="046b4-248"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**裝訂** (6) </span><span class="sxs-lookup"><span data-stu-id="046b4-248"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="046b4-249"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span> (7) 的 **透明列印**</span><span class="sxs-lookup"><span data-stu-id="046b4-249"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="046b4-250"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**打孔** (8) </span><span class="sxs-lookup"><span data-stu-id="046b4-250"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="046b4-251"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**涵蓋** (9) </span><span class="sxs-lookup"><span data-stu-id="046b4-251"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="046b4-252"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>系 **結 (10**) </span><span class="sxs-lookup"><span data-stu-id="046b4-252"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="046b4-253"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**黑白列印** (11) </span><span class="sxs-lookup"><span data-stu-id="046b4-253"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="046b4-254"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**一側** (12) </span><span class="sxs-lookup"><span data-stu-id="046b4-254"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-255">One-Sided</span><span class="sxs-lookup"><span data-stu-id="046b4-255">One-Sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="046b4-256"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**雙側長邊緣** (13) </span><span class="sxs-lookup"><span data-stu-id="046b4-256"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-257">Two-Sided 長邊緣</span><span class="sxs-lookup"><span data-stu-id="046b4-257">Two-Sided Long Edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="046b4-258"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**兩個側邊短邊緣** (14) </span><span class="sxs-lookup"><span data-stu-id="046b4-258"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-259">Two-Sided 短邊緣</span><span class="sxs-lookup"><span data-stu-id="046b4-259">Two-Sided Short Edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="046b4-260"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**縱向** (15) </span><span class="sxs-lookup"><span data-stu-id="046b4-260"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="046b4-261"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**橫向** (16) </span><span class="sxs-lookup"><span data-stu-id="046b4-261"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="046b4-262"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**反向縱向** (17) </span><span class="sxs-lookup"><span data-stu-id="046b4-262"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="046b4-263"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**反向橫向** (18) </span><span class="sxs-lookup"><span data-stu-id="046b4-263"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="046b4-264"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**高品質** (19) </span><span class="sxs-lookup"><span data-stu-id="046b4-264"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="046b4-265"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**高品質標準** (20) </span><span class="sxs-lookup"><span data-stu-id="046b4-265"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="046b4-266"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**品質低** (21) </span><span class="sxs-lookup"><span data-stu-id="046b4-266"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="046b4-267">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="046b4-267">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-268">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="046b4-268">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="046b4-269">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-270">限定詞： [**ArrayType**](../wmisdk/standard-qualifiers.md) ( 「已編制索引」 ) ， [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (」[**CIM \_ 印表機**](cim-printer.md)。**功能**") </span><span class="sxs-lookup"><span data-stu-id="046b4-270">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-271">自由格式字串的陣列，提供 **功能** 陣列中指出之印表機功能的詳細說明。</span><span class="sxs-lookup"><span data-stu-id="046b4-271">Array of free-form strings that provide detailed explanations for the printer features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="046b4-272">這個陣列的每個專案都與位於相同索引的 **功能** 陣列中的專案相關。</span><span class="sxs-lookup"><span data-stu-id="046b4-272">Each entry of this array is related to an entry in the **Capabilities** array that is located in the same index.</span></span>

<span data-ttu-id="046b4-273">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-273">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-274">**標題**</span><span class="sxs-lookup"><span data-stu-id="046b4-274">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-275">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="046b4-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-276">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-277">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="046b4-277">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-278">物件的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="046b4-278">Short description of an object—a one-line string.</span></span>

<span data-ttu-id="046b4-279">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-279">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-280">**CharSetsSupported**</span><span class="sxs-lookup"><span data-stu-id="046b4-280">**CharSetsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-281">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="046b4-281">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="046b4-282">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-283">限定詞： [**ArrayType**](../wmisdk/standard-qualifiers.md) ( "Indexed" ) ， [**MODELCORRESPONDENCE**](../wmisdk/standard-qualifiers.md) ( "CIM \_ PrintJob. 字元集" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIB。IETF \| 印表機-prtLocalizationCharacterSet ") </span><span class="sxs-lookup"><span data-stu-id="046b4-283">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.CharSet"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtLocalizationCharacterSet")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-284">輸出的可用字元集陣列。</span><span class="sxs-lookup"><span data-stu-id="046b4-284">Array of available character sets for output.</span></span> <span data-ttu-id="046b4-285">在此屬性中提供的字串必須符合 RFC 2046 (MIME 第2部分) 中的第4.1.2 節 ( "字元集參數" ) 所指定的語義和語法，並且包含在 IANA 字元集登錄中。</span><span class="sxs-lookup"><span data-stu-id="046b4-285">Strings provided in this property must conform to the semantics and syntax specified by section 4.1.2 ("Charset parameters") in RFC 2046 (MIME Part 2) and contained in the IANA character-set registry.</span></span> <span data-ttu-id="046b4-286">範例包括 "UTF-8"、"us-ASCII" 和 "iso-8859-1"。</span><span class="sxs-lookup"><span data-stu-id="046b4-286">Examples include, "UTF-8", "us-ASCII", and "iso-8859-1".</span></span>

<span data-ttu-id="046b4-287">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-287">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-288">**註解**</span><span class="sxs-lookup"><span data-stu-id="046b4-288">**Comment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-289">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="046b4-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-290">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="046b4-290">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="046b4-291">列印佇列的批註。</span><span class="sxs-lookup"><span data-stu-id="046b4-291">Comment for a print queue.</span></span>

<span data-ttu-id="046b4-292">範例：彩色印表機</span><span class="sxs-lookup"><span data-stu-id="046b4-292">Example: Color printer</span></span>

</dd> <dt>

<span data-ttu-id="046b4-293">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="046b4-293">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-294">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="046b4-294">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-295">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-296">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="046b4-296">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-297">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="046b4-297">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="046b4-298">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="046b4-299"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="046b4-299"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="046b4-300"> (0)</span><span class="sxs-lookup"><span data-stu-id="046b4-300">(0)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-301">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="046b4-301">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="046b4-302"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="046b4-302"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="046b4-303">(1)</span><span class="sxs-lookup"><span data-stu-id="046b4-303">(1)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-304">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="046b4-304">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="046b4-305"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="046b4-305"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="046b4-306">(2)</span><span class="sxs-lookup"><span data-stu-id="046b4-306">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="046b4-307"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="046b4-307"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="046b4-308">(3)</span><span class="sxs-lookup"><span data-stu-id="046b4-308">(3)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-309">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="046b4-309">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="046b4-310"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="046b4-310"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="046b4-311">(4)</span><span class="sxs-lookup"><span data-stu-id="046b4-311">(4)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-312">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="046b4-312">Device is not working properly.</span></span> <span data-ttu-id="046b4-313">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="046b4-313">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="046b4-314"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="046b4-314"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="046b4-315">(5)</span><span class="sxs-lookup"><span data-stu-id="046b4-315">(5)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-316">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="046b4-316">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="046b4-317"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="046b4-317"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="046b4-318">(6)</span><span class="sxs-lookup"><span data-stu-id="046b4-318">(6)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-319">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="046b4-319">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="046b4-320"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="046b4-320"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="046b4-321">(7)</span><span class="sxs-lookup"><span data-stu-id="046b4-321">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="046b4-322"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="046b4-322"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="046b4-323">(8)</span><span class="sxs-lookup"><span data-stu-id="046b4-323">(8)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-324">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="046b4-324">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="046b4-325"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="046b4-325"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="046b4-326">(9)</span><span class="sxs-lookup"><span data-stu-id="046b4-326">(9)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-327">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="046b4-327">Device is not working properly.</span></span> <span data-ttu-id="046b4-328">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="046b4-328">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="046b4-329"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="046b4-329"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="046b4-330">(10)</span><span class="sxs-lookup"><span data-stu-id="046b4-330">(10)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-331">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="046b4-331">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="046b4-332"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="046b4-332"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="046b4-333">(11)</span><span class="sxs-lookup"><span data-stu-id="046b4-333">(11)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-334">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="046b4-334">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="046b4-335"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="046b4-335"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="046b4-336"> (12) </span><span class="sxs-lookup"><span data-stu-id="046b4-336">(12)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-337">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="046b4-337">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="046b4-338"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="046b4-338"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="046b4-339">(13)</span><span class="sxs-lookup"><span data-stu-id="046b4-339">(13)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-340">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="046b4-340">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="046b4-341"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="046b4-341"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="046b4-342">(14)</span><span class="sxs-lookup"><span data-stu-id="046b4-342">(14)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-343">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="046b4-343">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="046b4-344"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="046b4-344"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="046b4-345">(15)</span><span class="sxs-lookup"><span data-stu-id="046b4-345">(15)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-346">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="046b4-346">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="046b4-347"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="046b4-347"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="046b4-348">(16)</span><span class="sxs-lookup"><span data-stu-id="046b4-348">(16)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-349">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="046b4-349">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="046b4-350"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="046b4-350"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="046b4-351">(17)</span><span class="sxs-lookup"><span data-stu-id="046b4-351">(17)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-352">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="046b4-352">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="046b4-353"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="046b4-353"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="046b4-354">(18)</span><span class="sxs-lookup"><span data-stu-id="046b4-354">(18)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-355">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="046b4-355">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="046b4-356"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="046b4-356"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="046b4-357">(19)</span><span class="sxs-lookup"><span data-stu-id="046b4-357">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="046b4-358"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="046b4-358"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="046b4-359">(20)</span><span class="sxs-lookup"><span data-stu-id="046b4-359">(20)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-360">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="046b4-360">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="046b4-361"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="046b4-361"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="046b4-362">(21)</span><span class="sxs-lookup"><span data-stu-id="046b4-362">(21)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-363">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="046b4-363">System failure.</span></span> <span data-ttu-id="046b4-364">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="046b4-364">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="046b4-365">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="046b4-365">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="046b4-366"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="046b4-366"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="046b4-367">(22)</span><span class="sxs-lookup"><span data-stu-id="046b4-367">(22)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-368">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="046b4-368">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="046b4-369"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="046b4-369"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="046b4-370">(23)</span><span class="sxs-lookup"><span data-stu-id="046b4-370">(23)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-371">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="046b4-371">System failure.</span></span> <span data-ttu-id="046b4-372">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="046b4-372">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="046b4-373"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="046b4-373"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="046b4-374">(24)</span><span class="sxs-lookup"><span data-stu-id="046b4-374">(24)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-375">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="046b4-375">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="046b4-376"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="046b4-376"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="046b4-377">(25)</span><span class="sxs-lookup"><span data-stu-id="046b4-377">(25)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-378">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="046b4-378">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="046b4-379"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="046b4-379"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="046b4-380">(26)</span><span class="sxs-lookup"><span data-stu-id="046b4-380">(26)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-381">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="046b4-381">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="046b4-382"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="046b4-382"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="046b4-383">(27)</span><span class="sxs-lookup"><span data-stu-id="046b4-383">(27)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-384">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="046b4-384">Device does not have a valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="046b4-385"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="046b4-385"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="046b4-386">(28)</span><span class="sxs-lookup"><span data-stu-id="046b4-386">(28)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-387">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="046b4-387">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="046b4-388"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="046b4-388"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="046b4-389">(29)</span><span class="sxs-lookup"><span data-stu-id="046b4-389">(29)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-390">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="046b4-390">Device is disabled.</span></span> <span data-ttu-id="046b4-391">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="046b4-391">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="046b4-392"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="046b4-392"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="046b4-393">(30)</span><span class="sxs-lookup"><span data-stu-id="046b4-393">(30)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-394">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="046b4-394">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="046b4-395"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="046b4-395"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="046b4-396"> (31) </span><span class="sxs-lookup"><span data-stu-id="046b4-396">(31)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-397">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="046b4-397">Device is not working properly.</span></span> <span data-ttu-id="046b4-398">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="046b4-398">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="046b4-399">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="046b4-399">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-400">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="046b4-400">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-401">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-401">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-402">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="046b4-402">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-403">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="046b4-403">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="046b4-404">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-404">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-405">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="046b4-405">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-406">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="046b4-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-407">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-408">限定詞： [ **CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="046b4-408">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="046b4-409">第一個實體類別的名稱，這個類別會出現在用來建立實例的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="046b4-409">Name of the first concrete class to appear in the inheritance chain used to create an instance.</span></span> <span data-ttu-id="046b4-410">搭配類別的其他索引鍵屬性使用時，屬性可讓這個類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="046b4-410">When used with other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="046b4-411">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-412">**CurrentCapabilities**</span><span class="sxs-lookup"><span data-stu-id="046b4-412">**CurrentCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-413">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="046b4-413">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="046b4-414">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-415">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 印表機**](cim-printer.md)」。**功能**") </span><span class="sxs-lookup"><span data-stu-id="046b4-415">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-416">目前正在使用的印表機功能陣列。</span><span class="sxs-lookup"><span data-stu-id="046b4-416">Array of printer capabilities that are being used currently.</span></span> <span data-ttu-id="046b4-417">這個屬性中的專案也必須列在 **功能** 陣列中。</span><span class="sxs-lookup"><span data-stu-id="046b4-417">An entry in this property must also be listed in the **Capabilities** array.</span></span>

<span data-ttu-id="046b4-418">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-418">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="046b4-419"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="046b4-419"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="046b4-420"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="046b4-420"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="046b4-421"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**色彩列印** (2) </span><span class="sxs-lookup"><span data-stu-id="046b4-421"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="046b4-422"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**雙工列印** (3) </span><span class="sxs-lookup"><span data-stu-id="046b4-422"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="046b4-423"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span> (4) **複製**</span><span class="sxs-lookup"><span data-stu-id="046b4-423"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="046b4-424"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>定 **序** (5) </span><span class="sxs-lookup"><span data-stu-id="046b4-424"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="046b4-425"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**裝訂** (6) </span><span class="sxs-lookup"><span data-stu-id="046b4-425"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="046b4-426"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span> (7) 的 **透明列印**</span><span class="sxs-lookup"><span data-stu-id="046b4-426"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="046b4-427"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**打孔** (8) </span><span class="sxs-lookup"><span data-stu-id="046b4-427"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="046b4-428"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**涵蓋** (9) </span><span class="sxs-lookup"><span data-stu-id="046b4-428"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="046b4-429"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>系 **結 (10**) </span><span class="sxs-lookup"><span data-stu-id="046b4-429"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="046b4-430"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**黑白列印** (11) </span><span class="sxs-lookup"><span data-stu-id="046b4-430"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="046b4-431"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**一側** (12) </span><span class="sxs-lookup"><span data-stu-id="046b4-431"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-432">One-Sided</span><span class="sxs-lookup"><span data-stu-id="046b4-432">One-Sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="046b4-433"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**雙側長邊緣** (13) </span><span class="sxs-lookup"><span data-stu-id="046b4-433"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-434">Two-Sided 長邊緣</span><span class="sxs-lookup"><span data-stu-id="046b4-434">Two-Sided Long Edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="046b4-435"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**兩個側邊短邊緣** (14) </span><span class="sxs-lookup"><span data-stu-id="046b4-435"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-436">Two-Sided 短邊緣</span><span class="sxs-lookup"><span data-stu-id="046b4-436">Two-Sided Short Edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="046b4-437"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**縱向** (15) </span><span class="sxs-lookup"><span data-stu-id="046b4-437"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="046b4-438"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**橫向** (16) </span><span class="sxs-lookup"><span data-stu-id="046b4-438"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="046b4-439"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**反向縱向** (17) </span><span class="sxs-lookup"><span data-stu-id="046b4-439"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="046b4-440"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**反向橫向** (18) </span><span class="sxs-lookup"><span data-stu-id="046b4-440"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="046b4-441"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**高品質** (19) </span><span class="sxs-lookup"><span data-stu-id="046b4-441"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="046b4-442"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**高品質標準** (20) </span><span class="sxs-lookup"><span data-stu-id="046b4-442"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="046b4-443"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**品質低** (21) </span><span class="sxs-lookup"><span data-stu-id="046b4-443"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="046b4-444">**CurrentCharSet**</span><span class="sxs-lookup"><span data-stu-id="046b4-444">**CurrentCharSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-445">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="046b4-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-446">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-447">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 印表機**](cim-printer.md)」。**CharSetsSupported**") </span><span class="sxs-lookup"><span data-stu-id="046b4-447">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**CharSetsSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-448">目前用於輸出的字元集。</span><span class="sxs-lookup"><span data-stu-id="046b4-448">The character set currently used for output.</span></span> <span data-ttu-id="046b4-449">在此屬性中提供的字串必須符合 RFC 2046 (MIME 第2部分) 中的第4.1.2 節 ( "字元集參數" ) 所指定的語義和語法，並且包含在 IANA 字元集登錄中。</span><span class="sxs-lookup"><span data-stu-id="046b4-449">Strings provided in this property must conform to the semantics and syntax specified by section 4.1.2 ("Charset parameters") in RFC 2046 (MIME Part 2) and contained in the IANA character-set registry.</span></span> <span data-ttu-id="046b4-450">範例包括 "utf-8"、"us-ASCII" 和 iso-8859-1。</span><span class="sxs-lookup"><span data-stu-id="046b4-450">Examples include "utf-8", "us-ASCII", and iso-8859-1.</span></span>

<span data-ttu-id="046b4-451">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-451">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-452">**CurrentLanguage**</span><span class="sxs-lookup"><span data-stu-id="046b4-452">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-453">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="046b4-453">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-454">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-455">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 印表機**](cim-printer.md)」。LanguagesSupported "，"**CIM \_ Printer**.**CurrentMimeType**") </span><span class="sxs-lookup"><span data-stu-id="046b4-455">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).LanguagesSupported", "**CIM\_Printer**.**CurrentMimeType**")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-456">目前使用的印表機語言。</span><span class="sxs-lookup"><span data-stu-id="046b4-456">Printer language currently used.</span></span> <span data-ttu-id="046b4-457">使用的語言必須列在 **LanguagesSupported** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="046b4-457">The language used must be listed in the **LanguagesSupported** property.</span></span>

<span data-ttu-id="046b4-458">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-458">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="046b4-459"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="046b4-459"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="046b4-460"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="046b4-460"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="046b4-461"><span id="PCL"></span><span id="pcl"></span>**PCL** (3) </span><span class="sxs-lookup"><span data-stu-id="046b4-461"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="046b4-462"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4) </span><span class="sxs-lookup"><span data-stu-id="046b4-462"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="046b4-463"><span id="PJL"></span><span id="pjl"></span>**PJL** (5) </span><span class="sxs-lookup"><span data-stu-id="046b4-463"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="046b4-464"><span id="PS"></span><span id="ps"></span>**PS** (6) </span><span class="sxs-lookup"><span data-stu-id="046b4-464"><span id="PS"></span><span id="ps"></span>**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="046b4-465"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7) </span><span class="sxs-lookup"><span data-stu-id="046b4-465"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="046b4-466"><span id="IPDS"></span><span id="ipds"></span>**Ipd** (8) </span><span class="sxs-lookup"><span data-stu-id="046b4-466"><span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="046b4-467"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9) </span><span class="sxs-lookup"><span data-stu-id="046b4-467"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="046b4-468"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10) </span><span class="sxs-lookup"><span data-stu-id="046b4-468"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="046b4-469"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11) </span><span class="sxs-lookup"><span data-stu-id="046b4-469"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="046b4-470"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12) </span><span class="sxs-lookup"><span data-stu-id="046b4-470"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="046b4-471"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13) </span><span class="sxs-lookup"><span data-stu-id="046b4-471"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="046b4-472"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14) </span><span class="sxs-lookup"><span data-stu-id="046b4-472"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="046b4-473"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**行資料** (15) </span><span class="sxs-lookup"><span data-stu-id="046b4-473"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Line Data** (15)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-474">LineData</span><span class="sxs-lookup"><span data-stu-id="046b4-474">LineData</span></span>

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="046b4-475"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16) </span><span class="sxs-lookup"><span data-stu-id="046b4-475"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-476">DODCA</span><span class="sxs-lookup"><span data-stu-id="046b4-476">DODCA</span></span>

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="046b4-477"><span id="REGIS"></span><span id="regis"></span>**REGIS** (17) </span><span class="sxs-lookup"><span data-stu-id="046b4-477"><span id="REGIS"></span><span id="regis"></span>**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="046b4-478"><span id="SCS"></span><span id="scs"></span>**SCS** (18) </span><span class="sxs-lookup"><span data-stu-id="046b4-478"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="046b4-479"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19) </span><span class="sxs-lookup"><span data-stu-id="046b4-479"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="046b4-480"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20) </span><span class="sxs-lookup"><span data-stu-id="046b4-480"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="046b4-481"><span id="PDS"></span><span id="pds"></span>**PDS** (21) </span><span class="sxs-lookup"><span data-stu-id="046b4-481"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="046b4-482"><span id="IGP"></span><span id="igp"></span>**IGP** (22) </span><span class="sxs-lookup"><span data-stu-id="046b4-482"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="046b4-483"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23) </span><span class="sxs-lookup"><span data-stu-id="046b4-483"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="046b4-484"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24) </span><span class="sxs-lookup"><span data-stu-id="046b4-484"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="046b4-485"><span id="WPS"></span><span id="wps"></span>**WPS** (25) </span><span class="sxs-lookup"><span data-stu-id="046b4-485"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="046b4-486"><span id="LN03"></span><span id="ln03"></span>**LN03** (26) </span><span class="sxs-lookup"><span data-stu-id="046b4-486"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="046b4-487"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27) </span><span class="sxs-lookup"><span data-stu-id="046b4-487"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="046b4-488"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28) </span><span class="sxs-lookup"><span data-stu-id="046b4-488"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="046b4-489"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29) </span><span class="sxs-lookup"><span data-stu-id="046b4-489"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="046b4-490"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30) </span><span class="sxs-lookup"><span data-stu-id="046b4-490"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="046b4-491"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**簡單文字** (31) </span><span class="sxs-lookup"><span data-stu-id="046b4-491"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Simple Text** (31)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-492">SimpleText</span><span class="sxs-lookup"><span data-stu-id="046b4-492">SimpleText</span></span>

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="046b4-493"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32) </span><span class="sxs-lookup"><span data-stu-id="046b4-493"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="046b4-494"><span id="DOC"></span><span id="doc"></span>**DOC** (33) </span><span class="sxs-lookup"><span data-stu-id="046b4-494"><span id="DOC"></span><span id="doc"></span>**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="046b4-495"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span> (34) 的 **印象深刻**</span><span class="sxs-lookup"><span data-stu-id="046b4-495"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="046b4-496"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35) </span><span class="sxs-lookup"><span data-stu-id="046b4-496"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="046b4-497"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36) </span><span class="sxs-lookup"><span data-stu-id="046b4-497"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="046b4-498"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37) </span><span class="sxs-lookup"><span data-stu-id="046b4-498"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="046b4-499"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**自動** (38) </span><span class="sxs-lookup"><span data-stu-id="046b4-499"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="046b4-500"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**頁面** (39) </span><span class="sxs-lookup"><span data-stu-id="046b4-500"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="046b4-501"><span id="LIPS"></span><span id="lips"></span>**Lip** (40) </span><span class="sxs-lookup"><span data-stu-id="046b4-501"><span id="LIPS"></span><span id="lips"></span>**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="046b4-502"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41) </span><span class="sxs-lookup"><span data-stu-id="046b4-502"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="046b4-503"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**診斷** (42) </span><span class="sxs-lookup"><span data-stu-id="046b4-503"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="046b4-504"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43) </span><span class="sxs-lookup"><span data-stu-id="046b4-504"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="046b4-505"><span id="EXCL"></span><span id="excl"></span>**排除** (44) </span><span class="sxs-lookup"><span data-stu-id="046b4-505"><span id="EXCL"></span><span id="excl"></span>**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="046b4-506"><span id="LCDS"></span><span id="lcds"></span>**Lcd** (45) </span><span class="sxs-lookup"><span data-stu-id="046b4-506"><span id="LCDS"></span><span id="lcds"></span>**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="046b4-507"><span id="XES"></span><span id="xes"></span>**XES** (46) </span><span class="sxs-lookup"><span data-stu-id="046b4-507"><span id="XES"></span><span id="xes"></span>**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="046b4-508"><span id="MIME"></span><span id="mime"></span>**MIME** (47) </span><span class="sxs-lookup"><span data-stu-id="046b4-508"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span></span>


</dt> <dd></dd> <dt>

<span data-ttu-id="046b4-509">48</span><span class="sxs-lookup"><span data-stu-id="046b4-509">48</span></span>
</dt> <dd>

<span data-ttu-id="046b4-510">XPS</span><span class="sxs-lookup"><span data-stu-id="046b4-510">XPS</span></span>

</dd> <dt>

<span data-ttu-id="046b4-511">49</span><span class="sxs-lookup"><span data-stu-id="046b4-511">49</span></span>
</dt> <dd>

<span data-ttu-id="046b4-512">HPGL2</span><span class="sxs-lookup"><span data-stu-id="046b4-512">HPGL2</span></span>

</dd> <dt>

<span data-ttu-id="046b4-513">50</span><span class="sxs-lookup"><span data-stu-id="046b4-513">50</span></span>
</dt> <dd>

<span data-ttu-id="046b4-514">PCLXL</span><span class="sxs-lookup"><span data-stu-id="046b4-514">PCLXL</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="046b4-515">**CurrentMimeType**</span><span class="sxs-lookup"><span data-stu-id="046b4-515">**CurrentMimeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-516">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="046b4-516">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-517">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-517">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-518">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 印表機**](cim-printer.md)」。**CurrentLanguage**") </span><span class="sxs-lookup"><span data-stu-id="046b4-518">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**CurrentLanguage**")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-519">如果 **CurrentLanguage** 是 mime 類型 (值 = 47) ，目前正在使用 mime 類型。</span><span class="sxs-lookup"><span data-stu-id="046b4-519">MIME type currently being used if the **CurrentLanguage** is a MIME type (value = 47).</span></span>

<span data-ttu-id="046b4-520">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-520">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-521">**CurrentNaturalLanguage**</span><span class="sxs-lookup"><span data-stu-id="046b4-521">**CurrentNaturalLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-522">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="046b4-522">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-523">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-523">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-524">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 印表機**](cim-printer.md)」。**NaturalLanguagesSupported**") </span><span class="sxs-lookup"><span data-stu-id="046b4-524">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**NaturalLanguagesSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-525">印表機目前用來管理的語言。</span><span class="sxs-lookup"><span data-stu-id="046b4-525">Language that the printer is using for management currently.</span></span> <span data-ttu-id="046b4-526">此處所列的語言也必須列在 **NaturalLanguagesSupported** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="046b4-526">The language listed here must also be listed in the **NaturalLanguagesSupported** property.</span></span>

<span data-ttu-id="046b4-527">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-527">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-528">**CurrentPaperType**</span><span class="sxs-lookup"><span data-stu-id="046b4-528">**CurrentPaperType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-529">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="046b4-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-530">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-530">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-531">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 印表機**](cim-printer.md)」。**PaperTypesAvailable**") </span><span class="sxs-lookup"><span data-stu-id="046b4-531">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**PaperTypesAvailable**")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-532">印表機正在使用的紙張類型。</span><span class="sxs-lookup"><span data-stu-id="046b4-532">Type of paper the printer is using.</span></span> <span data-ttu-id="046b4-533">必須以 ISO/IEC 10175 檔列印應用程式所指定的格式來表示 (DPA) ，在 RFC 1759 (印表機 MIB) 的附錄 C 中摘要說明。</span><span class="sxs-lookup"><span data-stu-id="046b4-533">Must be expressed in the form specified by the ISO/IEC 10175 Document Printing Application (DPA), which is summarized in Appendix C of RFC 1759 (Printer MIB).</span></span>

<span data-ttu-id="046b4-534">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-534">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-535">**預設值**</span><span class="sxs-lookup"><span data-stu-id="046b4-535">**Default**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-536">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="046b4-536">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-537">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="046b4-538">若 **為 TRUE**，表示印表機為預設印表機。</span><span class="sxs-lookup"><span data-stu-id="046b4-538">If **TRUE**, the printer is the default printer.</span></span>

</dd> <dt>

<span data-ttu-id="046b4-539">**DefaultCapabilities**</span><span class="sxs-lookup"><span data-stu-id="046b4-539">**DefaultCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-540">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="046b4-540">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="046b4-541">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-541">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-542">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 印表機**](cim-printer.md)」。**功能**") </span><span class="sxs-lookup"><span data-stu-id="046b4-542">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-543">預設使用的印表機功能陣列。</span><span class="sxs-lookup"><span data-stu-id="046b4-543">Array of the printer capabilities used by default.</span></span> <span data-ttu-id="046b4-544">**DefaultCapabilities** 陣列中的每個專案也都必須列在 **功能** 陣列中。</span><span class="sxs-lookup"><span data-stu-id="046b4-544">Each entry in the **DefaultCapabilities** array must also be listed in the **Capabilities** array.</span></span>

<span data-ttu-id="046b4-545">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-545">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="046b4-546"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="046b4-546"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="046b4-547"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="046b4-547"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="046b4-548"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**色彩列印** (2) </span><span class="sxs-lookup"><span data-stu-id="046b4-548"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="046b4-549"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**雙工列印** (3) </span><span class="sxs-lookup"><span data-stu-id="046b4-549"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="046b4-550"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span> (4) **複製**</span><span class="sxs-lookup"><span data-stu-id="046b4-550"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="046b4-551"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>定 **序** (5) </span><span class="sxs-lookup"><span data-stu-id="046b4-551"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="046b4-552"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**裝訂** (6) </span><span class="sxs-lookup"><span data-stu-id="046b4-552"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="046b4-553"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span> (7) 的 **透明列印**</span><span class="sxs-lookup"><span data-stu-id="046b4-553"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="046b4-554"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**打孔** (8) </span><span class="sxs-lookup"><span data-stu-id="046b4-554"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="046b4-555"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**涵蓋** (9) </span><span class="sxs-lookup"><span data-stu-id="046b4-555"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="046b4-556"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>系 **結 (10**) </span><span class="sxs-lookup"><span data-stu-id="046b4-556"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="046b4-557"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**黑白列印** (11) </span><span class="sxs-lookup"><span data-stu-id="046b4-557"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="046b4-558"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**一側** (12) </span><span class="sxs-lookup"><span data-stu-id="046b4-558"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-559">One-Sided</span><span class="sxs-lookup"><span data-stu-id="046b4-559">One-Sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="046b4-560"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**雙側長邊緣** (13) </span><span class="sxs-lookup"><span data-stu-id="046b4-560"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-561">Two-Sided 長邊緣</span><span class="sxs-lookup"><span data-stu-id="046b4-561">Two-Sided Long Edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="046b4-562"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**兩個側邊短邊緣** (14) </span><span class="sxs-lookup"><span data-stu-id="046b4-562"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-563">Two-Sided 短邊緣</span><span class="sxs-lookup"><span data-stu-id="046b4-563">Two-Sided Short Edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="046b4-564"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**縱向** (15) </span><span class="sxs-lookup"><span data-stu-id="046b4-564"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="046b4-565"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**橫向** (16) </span><span class="sxs-lookup"><span data-stu-id="046b4-565"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="046b4-566"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**反向縱向** (17) </span><span class="sxs-lookup"><span data-stu-id="046b4-566"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="046b4-567"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**反向橫向** (18) </span><span class="sxs-lookup"><span data-stu-id="046b4-567"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="046b4-568"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**高品質** (19) </span><span class="sxs-lookup"><span data-stu-id="046b4-568"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="046b4-569"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**高品質標準** (20) </span><span class="sxs-lookup"><span data-stu-id="046b4-569"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="046b4-570"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**品質低** (21) </span><span class="sxs-lookup"><span data-stu-id="046b4-570"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="046b4-571">**DefaultCopies**</span><span class="sxs-lookup"><span data-stu-id="046b4-571">**DefaultCopies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-572">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="046b4-572">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-573">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-573">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="046b4-574">除非另有指定，否則為一個作業產生的複本數目。</span><span class="sxs-lookup"><span data-stu-id="046b4-574">Number of copies produced for one job—unless otherwise specified.</span></span>

<span data-ttu-id="046b4-575">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-575">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-576">**DefaultLanguage**</span><span class="sxs-lookup"><span data-stu-id="046b4-576">**DefaultLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-577">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="046b4-577">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-578">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-578">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-579">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 印表機**](cim-printer.md)」。LanguagesSupported "，"**CIM \_ Printer**.**DefaultMimeType**") </span><span class="sxs-lookup"><span data-stu-id="046b4-579">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).LanguagesSupported", "**CIM\_Printer**.**DefaultMimeType**")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-580">預設印表機語言。</span><span class="sxs-lookup"><span data-stu-id="046b4-580">Default printer language.</span></span> <span data-ttu-id="046b4-581">此處所列的語言也必須列在 **LanguagesSupported** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="046b4-581">The language listed here must also be listed in the **LanguagesSupported** property.</span></span>

<span data-ttu-id="046b4-582">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-582">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="046b4-583"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="046b4-583"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="046b4-584"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="046b4-584"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="046b4-585"><span id="PCL"></span><span id="pcl"></span>**PCL** (3) </span><span class="sxs-lookup"><span data-stu-id="046b4-585"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="046b4-586"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4) </span><span class="sxs-lookup"><span data-stu-id="046b4-586"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="046b4-587"><span id="PJL"></span><span id="pjl"></span>**PJL** (5) </span><span class="sxs-lookup"><span data-stu-id="046b4-587"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="046b4-588"><span id="PS"></span><span id="ps"></span>**PS** (6) </span><span class="sxs-lookup"><span data-stu-id="046b4-588"><span id="PS"></span><span id="ps"></span>**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="046b4-589"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7) </span><span class="sxs-lookup"><span data-stu-id="046b4-589"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="046b4-590"><span id="IPDS"></span><span id="ipds"></span>**Ipd** (8) </span><span class="sxs-lookup"><span data-stu-id="046b4-590"><span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="046b4-591"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9) </span><span class="sxs-lookup"><span data-stu-id="046b4-591"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="046b4-592"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10) </span><span class="sxs-lookup"><span data-stu-id="046b4-592"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="046b4-593"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11) </span><span class="sxs-lookup"><span data-stu-id="046b4-593"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="046b4-594"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12) </span><span class="sxs-lookup"><span data-stu-id="046b4-594"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="046b4-595"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13) </span><span class="sxs-lookup"><span data-stu-id="046b4-595"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="046b4-596"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14) </span><span class="sxs-lookup"><span data-stu-id="046b4-596"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="046b4-597"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**行資料** (15) </span><span class="sxs-lookup"><span data-stu-id="046b4-597"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Line Data** (15)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-598">LineData</span><span class="sxs-lookup"><span data-stu-id="046b4-598">LineData</span></span>

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="046b4-599"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16) </span><span class="sxs-lookup"><span data-stu-id="046b4-599"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-600">DODCA</span><span class="sxs-lookup"><span data-stu-id="046b4-600">DODCA</span></span>

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="046b4-601"><span id="REGIS"></span><span id="regis"></span>**REGIS** (17) </span><span class="sxs-lookup"><span data-stu-id="046b4-601"><span id="REGIS"></span><span id="regis"></span>**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="046b4-602"><span id="SCS"></span><span id="scs"></span>**SCS** (18) </span><span class="sxs-lookup"><span data-stu-id="046b4-602"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="046b4-603"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19) </span><span class="sxs-lookup"><span data-stu-id="046b4-603"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="046b4-604"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20) </span><span class="sxs-lookup"><span data-stu-id="046b4-604"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="046b4-605"><span id="PDS"></span><span id="pds"></span>**PDS** (21) </span><span class="sxs-lookup"><span data-stu-id="046b4-605"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="046b4-606"><span id="IGP"></span><span id="igp"></span>**IGP** (22) </span><span class="sxs-lookup"><span data-stu-id="046b4-606"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="046b4-607"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23) </span><span class="sxs-lookup"><span data-stu-id="046b4-607"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="046b4-608"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24) </span><span class="sxs-lookup"><span data-stu-id="046b4-608"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="046b4-609"><span id="WPS"></span><span id="wps"></span>**WPS** (25) </span><span class="sxs-lookup"><span data-stu-id="046b4-609"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="046b4-610"><span id="LN03"></span><span id="ln03"></span>**LN03** (26) </span><span class="sxs-lookup"><span data-stu-id="046b4-610"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="046b4-611"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27) </span><span class="sxs-lookup"><span data-stu-id="046b4-611"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="046b4-612"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28) </span><span class="sxs-lookup"><span data-stu-id="046b4-612"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="046b4-613"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29) </span><span class="sxs-lookup"><span data-stu-id="046b4-613"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="046b4-614"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30) </span><span class="sxs-lookup"><span data-stu-id="046b4-614"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="046b4-615"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**簡單文字** (31) </span><span class="sxs-lookup"><span data-stu-id="046b4-615"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Simple Text** (31)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-616">SimpleText</span><span class="sxs-lookup"><span data-stu-id="046b4-616">SimpleText</span></span>

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="046b4-617"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32) </span><span class="sxs-lookup"><span data-stu-id="046b4-617"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="046b4-618"><span id="DOC"></span><span id="doc"></span>**DOC** (33) </span><span class="sxs-lookup"><span data-stu-id="046b4-618"><span id="DOC"></span><span id="doc"></span>**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="046b4-619"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span> (34) 的 **印象深刻**</span><span class="sxs-lookup"><span data-stu-id="046b4-619"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="046b4-620"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35) </span><span class="sxs-lookup"><span data-stu-id="046b4-620"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="046b4-621"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36) </span><span class="sxs-lookup"><span data-stu-id="046b4-621"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="046b4-622"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37) </span><span class="sxs-lookup"><span data-stu-id="046b4-622"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="046b4-623"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**自動** (38) </span><span class="sxs-lookup"><span data-stu-id="046b4-623"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="046b4-624"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**頁面** (39) </span><span class="sxs-lookup"><span data-stu-id="046b4-624"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="046b4-625"><span id="LIPS"></span><span id="lips"></span>**Lip** (40) </span><span class="sxs-lookup"><span data-stu-id="046b4-625"><span id="LIPS"></span><span id="lips"></span>**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="046b4-626"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41) </span><span class="sxs-lookup"><span data-stu-id="046b4-626"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="046b4-627"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**診斷** (42) </span><span class="sxs-lookup"><span data-stu-id="046b4-627"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="046b4-628"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43) </span><span class="sxs-lookup"><span data-stu-id="046b4-628"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="046b4-629"><span id="EXCL"></span><span id="excl"></span>**排除** (44) </span><span class="sxs-lookup"><span data-stu-id="046b4-629"><span id="EXCL"></span><span id="excl"></span>**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="046b4-630"><span id="LCDS"></span><span id="lcds"></span>**Lcd** (45) </span><span class="sxs-lookup"><span data-stu-id="046b4-630"><span id="LCDS"></span><span id="lcds"></span>**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="046b4-631"><span id="XES"></span><span id="xes"></span>**XES** (46) </span><span class="sxs-lookup"><span data-stu-id="046b4-631"><span id="XES"></span><span id="xes"></span>**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="046b4-632"><span id="MIME"></span><span id="mime"></span>**MIME** (47) </span><span class="sxs-lookup"><span data-stu-id="046b4-632"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span></span>


</dt> <dd></dd> <dt>

<span data-ttu-id="046b4-633">48</span><span class="sxs-lookup"><span data-stu-id="046b4-633">48</span></span>
</dt> <dd>

<span data-ttu-id="046b4-634">XPS</span><span class="sxs-lookup"><span data-stu-id="046b4-634">XPS</span></span>

</dd> <dt>

<span data-ttu-id="046b4-635">49</span><span class="sxs-lookup"><span data-stu-id="046b4-635">49</span></span>
</dt> <dd>

<span data-ttu-id="046b4-636">HPGL2</span><span class="sxs-lookup"><span data-stu-id="046b4-636">HPGL2</span></span>

</dd> <dt>

<span data-ttu-id="046b4-637">50</span><span class="sxs-lookup"><span data-stu-id="046b4-637">50</span></span>
</dt> <dd>

<span data-ttu-id="046b4-638">PCLXL</span><span class="sxs-lookup"><span data-stu-id="046b4-638">PCLXL</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="046b4-639">**DefaultMimeType**</span><span class="sxs-lookup"><span data-stu-id="046b4-639">**DefaultMimeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-640">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="046b4-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-641">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-641">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-642">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 印表機**](cim-printer.md)」。**DefaultLanguage**") </span><span class="sxs-lookup"><span data-stu-id="046b4-642">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**DefaultLanguage**")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-643">目前使用的 MIME 類型，如果 **DefaultLanguage** 值是 mime 類型 (值 = 47) 。</span><span class="sxs-lookup"><span data-stu-id="046b4-643">MIME type currently being used, if the **DefaultLanguage** value is a MIME type (value = 47).</span></span>

<span data-ttu-id="046b4-644">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-644">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-645">**DefaultNumberUp**</span><span class="sxs-lookup"><span data-stu-id="046b4-645">**DefaultNumberUp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-646">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="046b4-646">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-647">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-647">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="046b4-648">印表機在一個媒體紙上轉譯的列印資料流程頁面數目，除非作業另有指定。</span><span class="sxs-lookup"><span data-stu-id="046b4-648">Number of print-stream pages that the printer renders on one media sheet—unless a job specifies otherwise.</span></span>

<span data-ttu-id="046b4-649">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-649">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-650">**DefaultPaperType**</span><span class="sxs-lookup"><span data-stu-id="046b4-650">**DefaultPaperType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-651">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="046b4-651">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-652">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-652">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-653">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 印表機**](cim-printer.md)」。**PaperTypesAvailable**") </span><span class="sxs-lookup"><span data-stu-id="046b4-653">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**PaperTypesAvailable**")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-654">印表機使用的紙張類型，除非列印工作指定不同的紙張類型。</span><span class="sxs-lookup"><span data-stu-id="046b4-654">Paper type that the printer uses—unless a print job specifies a different paper type.</span></span> <span data-ttu-id="046b4-655">字串必須以 ISO/IEC 1017 檔列印應用程式所指定的格式表示 (DPA) ，在 [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (印表機 MIB) 的附錄 C 中摘要說明。</span><span class="sxs-lookup"><span data-stu-id="046b4-655">The string must be expressed in the form specified by ISO/IEC 1017 Document Printing Application (DPA), which is summarized in Appendix C of [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Printer MIB).</span></span>

<span data-ttu-id="046b4-656">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-656">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-657">**DefaultPriority**</span><span class="sxs-lookup"><span data-stu-id="046b4-657">**DefaultPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-658">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="046b4-658">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-659">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="046b4-659">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="046b4-660">指派給每個列印工作的預設優先權值。</span><span class="sxs-lookup"><span data-stu-id="046b4-660">Default priority value assigned to each print job.</span></span>

</dd> <dt>

<span data-ttu-id="046b4-661">**說明**</span><span class="sxs-lookup"><span data-stu-id="046b4-661">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-662">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="046b4-662">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-663">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-663">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-664">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="046b4-664">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-665">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="046b4-665">Description of an object.</span></span>

<span data-ttu-id="046b4-666">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-666">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-667">**DetectedErrorState**</span><span class="sxs-lookup"><span data-stu-id="046b4-667">**DetectedErrorState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-668">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="046b4-668">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-669">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-669">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-670">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 印表機**](cim-printer.md)」。**ErrorInformation**") ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" MIB。IETF \| 印表機-hrPrinterDetectedErrorState ") </span><span class="sxs-lookup"><span data-stu-id="046b4-670">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**ErrorInformation**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.hrPrinterDetectedErrorState")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-671">印表機錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="046b4-671">Printer error information.</span></span>

<span data-ttu-id="046b4-672">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-672">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="046b4-673">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="046b4-673">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="046b4-674">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="046b4-674">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Error"></span><span id="no_error"></span><span id="NO_ERROR"></span>

<span data-ttu-id="046b4-675">**沒有錯誤** (2) </span><span class="sxs-lookup"><span data-stu-id="046b4-675">**No Error** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Paper"></span><span id="low_paper"></span><span id="LOW_PAPER"></span>

<span data-ttu-id="046b4-676">**低紙** (3) </span><span class="sxs-lookup"><span data-stu-id="046b4-676">**Low Paper** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Paper"></span><span id="no_paper"></span><span id="NO_PAPER"></span>

<span data-ttu-id="046b4-677">**沒有紙張** (4) </span><span class="sxs-lookup"><span data-stu-id="046b4-677">**No Paper** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Toner"></span><span id="low_toner"></span><span id="LOW_TONER"></span>

<span data-ttu-id="046b4-678">**低碳粉** (5) </span><span class="sxs-lookup"><span data-stu-id="046b4-678">**Low Toner** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Toner"></span><span id="no_toner"></span><span id="NO_TONER"></span>

<span data-ttu-id="046b4-679">**沒有碳粉** (6) </span><span class="sxs-lookup"><span data-stu-id="046b4-679">**No Toner** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Door_Open"></span><span id="door_open"></span><span id="DOOR_OPEN"></span>

<span data-ttu-id="046b4-680">**門開啟** (7) </span><span class="sxs-lookup"><span data-stu-id="046b4-680">**Door Open** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Jammed"></span><span id="jammed"></span><span id="JAMMED"></span>

<span data-ttu-id="046b4-681">**卡** (8) </span><span class="sxs-lookup"><span data-stu-id="046b4-681">**Jammed** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="046b4-682">**離線** (9) </span><span class="sxs-lookup"><span data-stu-id="046b4-682">**Offline** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_Requested"></span><span id="service_requested"></span><span id="SERVICE_REQUESTED"></span>

<span data-ttu-id="046b4-683">**要求的服務** (10) </span><span class="sxs-lookup"><span data-stu-id="046b4-683">**Service Requested** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Output_Bin_Full"></span><span id="output_bin_full"></span><span id="OUTPUT_BIN_FULL"></span>

<span data-ttu-id="046b4-684">**輸出 Bin Full** (11) </span><span class="sxs-lookup"><span data-stu-id="046b4-684">**Output Bin Full** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="046b4-685">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="046b4-685">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-686">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="046b4-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-687">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-687">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-688">限定詞： [ **CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="046b4-688">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="046b4-689">系統上印表機的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="046b4-689">Unique identifier of the printer on a system.</span></span>

<span data-ttu-id="046b4-690">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-690">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-691">**直接**</span><span class="sxs-lookup"><span data-stu-id="046b4-691">**Direct**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-692">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="046b4-692">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-693">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="046b4-693">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="046b4-694">若 **為 TRUE**，列印工作會直接傳送至印表機。</span><span class="sxs-lookup"><span data-stu-id="046b4-694">If **TRUE**, the print job is sent directly to the printer.</span></span> <span data-ttu-id="046b4-695">如果 **為 FALSE**，則表示列印工作已進行多工緩衝處理。</span><span class="sxs-lookup"><span data-stu-id="046b4-695">If **FALSE**, the print job is spooled.</span></span>

</dd> <dt>

<span data-ttu-id="046b4-696">**DoCompleteFirst**</span><span class="sxs-lookup"><span data-stu-id="046b4-696">**DoCompleteFirst**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-697">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="046b4-697">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-698">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="046b4-698">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="046b4-699">若 **為 TRUE**，則印表機會啟動已完成幕後處理的工作。</span><span class="sxs-lookup"><span data-stu-id="046b4-699">If **TRUE**, the printer starts jobs that are finished spooling.</span></span> <span data-ttu-id="046b4-700">如果 **為 FALSE**，則印表機會依接收工作的順序啟動作業。</span><span class="sxs-lookup"><span data-stu-id="046b4-700">If **FALSE**, the printer starts jobs in the order that the jobs are received.</span></span>

</dd> <dt>

<span data-ttu-id="046b4-701">**DriverName**</span><span class="sxs-lookup"><span data-stu-id="046b4-701">**DriverName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-702">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="046b4-702">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-703">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="046b4-703">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="046b4-704">Windows 印表機驅動程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="046b4-704">Name of the Windows printer driver.</span></span>

<span data-ttu-id="046b4-705">範例： Windows 傳真驅動程式</span><span class="sxs-lookup"><span data-stu-id="046b4-705">Example: Windows Fax Driver</span></span>

</dd> <dt>

<span data-ttu-id="046b4-706">**EnableBIDI**</span><span class="sxs-lookup"><span data-stu-id="046b4-706">**EnableBIDI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-707">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="046b4-707">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-708">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="046b4-708">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="046b4-709">若 **為 TRUE**，印表機可以列印雙向。</span><span class="sxs-lookup"><span data-stu-id="046b4-709">If **TRUE**, the printer can print bidirectionally.</span></span>

</dd> <dt>

<span data-ttu-id="046b4-710">**EnableDevQueryPrint**</span><span class="sxs-lookup"><span data-stu-id="046b4-710">**EnableDevQueryPrint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-711">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="046b4-711">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-712">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="046b4-712">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="046b4-713">若 **為 TRUE**，當檔和印表機的設置不相符時，印表機會將檔保留在佇列中。</span><span class="sxs-lookup"><span data-stu-id="046b4-713">If **TRUE**, the printer holds documents in the queue when document and printer setups do not match.</span></span>

</dd> <dt>

<span data-ttu-id="046b4-714">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="046b4-714">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-715">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="046b4-715">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-716">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-716">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="046b4-717">若 **為 TRUE**，則會清除 **LastErrorCode** 中回報的錯誤。</span><span class="sxs-lookup"><span data-stu-id="046b4-717">If **TRUE**, the error reported in **LastErrorCode** has been cleared.</span></span>

<span data-ttu-id="046b4-718">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-718">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-719">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="046b4-719">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-720">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="046b4-720">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-721">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-721">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="046b4-722">**LastErrorCode** 中所記錄之錯誤的相關資訊，以及可採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="046b4-722">Information about the error recorded in **LastErrorCode**, and information about corrective actions that can be taken.</span></span>

<span data-ttu-id="046b4-723">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-723">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-724">**ErrorInformation**</span><span class="sxs-lookup"><span data-stu-id="046b4-724">**ErrorInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-725">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="046b4-725">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="046b4-726">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="046b4-726">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="046b4-727">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 印表機**](cim-printer.md)」。**DetectedErrorState**") </span><span class="sxs-lookup"><span data-stu-id="046b4-727">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**DetectedErrorState**")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-728">**DetectedErrorState** 中指出之目前錯誤狀態的補充資訊陣列。</span><span class="sxs-lookup"><span data-stu-id="046b4-728">Array of supplemental information for the current error state indicated in **DetectedErrorState**.</span></span>

<span data-ttu-id="046b4-729">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-729">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-730">**ExtendedDetectedErrorState**</span><span class="sxs-lookup"><span data-stu-id="046b4-730">**ExtendedDetectedErrorState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-731">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="046b4-731">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-732">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-732">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="046b4-733">報告標準錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="046b4-733">Reports standard error information.</span></span> <span data-ttu-id="046b4-734">您應該在 **DetectedErrorState** 中記錄其他資訊。</span><span class="sxs-lookup"><span data-stu-id="046b4-734">Additional information should be recorded in **DetectedErrorState**.</span></span>

<span data-ttu-id="046b4-735">值為：</span><span class="sxs-lookup"><span data-stu-id="046b4-735">Values are:</span></span>

<dt>

<span data-ttu-id="046b4-736">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="046b4-736">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-737">Unknown</span><span class="sxs-lookup"><span data-stu-id="046b4-737">Unknown</span></span>

</dd> <dt>

<span data-ttu-id="046b4-738">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="046b4-738">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-739">其他</span><span class="sxs-lookup"><span data-stu-id="046b4-739">Other</span></span>

</dd> <dt>

<span data-ttu-id="046b4-740">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="046b4-740">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-741">沒有錯誤</span><span class="sxs-lookup"><span data-stu-id="046b4-741">No Error</span></span>

</dd> <dt>

<span data-ttu-id="046b4-742">3 (0x3) </span><span class="sxs-lookup"><span data-stu-id="046b4-742">3 (0x3)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-743">紙張不足</span><span class="sxs-lookup"><span data-stu-id="046b4-743">Low Paper</span></span>

</dd> <dt>

<span data-ttu-id="046b4-744">4 (0x4) </span><span class="sxs-lookup"><span data-stu-id="046b4-744">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-745">沒有紙張</span><span class="sxs-lookup"><span data-stu-id="046b4-745">No Paper</span></span>

</dd> <dt>

<span data-ttu-id="046b4-746">5 (0x5) </span><span class="sxs-lookup"><span data-stu-id="046b4-746">5 (0x5)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-747">碳粉不足</span><span class="sxs-lookup"><span data-stu-id="046b4-747">Low Toner</span></span>

</dd> <dt>

<span data-ttu-id="046b4-748">6 (0x6) </span><span class="sxs-lookup"><span data-stu-id="046b4-748">6 (0x6)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-749">碳粉用完</span><span class="sxs-lookup"><span data-stu-id="046b4-749">No Toner</span></span>

</dd> <dt>

<span data-ttu-id="046b4-750">7 (0x7) </span><span class="sxs-lookup"><span data-stu-id="046b4-750">7 (0x7)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-751">機門開啟</span><span class="sxs-lookup"><span data-stu-id="046b4-751">Door Open</span></span>

</dd> <dt>

<span data-ttu-id="046b4-752">8 (0x8) </span><span class="sxs-lookup"><span data-stu-id="046b4-752">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-753">夾紙</span><span class="sxs-lookup"><span data-stu-id="046b4-753">Jammed</span></span>

</dd> <dt>

<span data-ttu-id="046b4-754">9 (0x9) </span><span class="sxs-lookup"><span data-stu-id="046b4-754">9 (0x9)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-755">要求的服務</span><span class="sxs-lookup"><span data-stu-id="046b4-755">Service Requested</span></span>

</dd> <dt>

<span data-ttu-id="046b4-756">10 (0xA) </span><span class="sxs-lookup"><span data-stu-id="046b4-756">10 (0xA)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-757">輸出紙匣已滿</span><span class="sxs-lookup"><span data-stu-id="046b4-757">Output Bin Full</span></span>

</dd> <dt>

<span data-ttu-id="046b4-758">11 (0xB) </span><span class="sxs-lookup"><span data-stu-id="046b4-758">11 (0xB)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-759">紙張問題</span><span class="sxs-lookup"><span data-stu-id="046b4-759">Paper Problem</span></span>

</dd> <dt>

<span data-ttu-id="046b4-760">12 (0xC) </span><span class="sxs-lookup"><span data-stu-id="046b4-760">12 (0xC)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-761">無法列印頁面</span><span class="sxs-lookup"><span data-stu-id="046b4-761">Cannot Print Page</span></span>

</dd> <dt>

<span data-ttu-id="046b4-762">13 (0xD) </span><span class="sxs-lookup"><span data-stu-id="046b4-762">13 (0xD)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-763">需要使用者介入</span><span class="sxs-lookup"><span data-stu-id="046b4-763">User Intervention Required</span></span>

</dd> <dt>

<span data-ttu-id="046b4-764">14 (0xE) </span><span class="sxs-lookup"><span data-stu-id="046b4-764">14 (0xE)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-765">記憶體不足</span><span class="sxs-lookup"><span data-stu-id="046b4-765">Out of Memory</span></span>

</dd> <dt>

<span data-ttu-id="046b4-766">15 (0xF) </span><span class="sxs-lookup"><span data-stu-id="046b4-766">15 (0xF)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-767">伺服器不明</span><span class="sxs-lookup"><span data-stu-id="046b4-767">Server Unknown</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="046b4-768">**ExtendedPrinterStatus**</span><span class="sxs-lookup"><span data-stu-id="046b4-768">**ExtendedPrinterStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-769">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="046b4-769">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-770">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-770">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="046b4-771">與 **Availability** 屬性中指定之資訊不同的印表機狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="046b4-771">Status information for a printer that is different from information specified in the **Availability** property.</span></span>

<dt>

<span data-ttu-id="046b4-772">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="046b4-772">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-773">其他</span><span class="sxs-lookup"><span data-stu-id="046b4-773">Other</span></span>

</dd> <dt>

<span data-ttu-id="046b4-774">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="046b4-774">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-775">Unknown</span><span class="sxs-lookup"><span data-stu-id="046b4-775">Unknown</span></span>

</dd> <dt>

<span data-ttu-id="046b4-776">3 (0x3) </span><span class="sxs-lookup"><span data-stu-id="046b4-776">3 (0x3)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-777">閒置</span><span class="sxs-lookup"><span data-stu-id="046b4-777">Idle</span></span>

</dd> <dt>

<span data-ttu-id="046b4-778">4 (0x4) </span><span class="sxs-lookup"><span data-stu-id="046b4-778">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-779">列印</span><span class="sxs-lookup"><span data-stu-id="046b4-779">Printing</span></span>

</dd> <dt>

<span data-ttu-id="046b4-780">5 (0x5) </span><span class="sxs-lookup"><span data-stu-id="046b4-780">5 (0x5)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-781">正在準備</span><span class="sxs-lookup"><span data-stu-id="046b4-781">Warming Up</span></span>

</dd> <dt>

<span data-ttu-id="046b4-782">6 (0x6) </span><span class="sxs-lookup"><span data-stu-id="046b4-782">6 (0x6)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-783">停止列印</span><span class="sxs-lookup"><span data-stu-id="046b4-783">Stopped Printing</span></span>

</dd> <dt>

<span data-ttu-id="046b4-784">7</span><span class="sxs-lookup"><span data-stu-id="046b4-784">7</span></span>
</dt> <dd>

<span data-ttu-id="046b4-785">離線</span><span class="sxs-lookup"><span data-stu-id="046b4-785">Offline</span></span>

</dd> <dt>

<span data-ttu-id="046b4-786">8 (0x8) </span><span class="sxs-lookup"><span data-stu-id="046b4-786">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-787">已暫停</span><span class="sxs-lookup"><span data-stu-id="046b4-787">Paused</span></span>

</dd> <dt>

<span data-ttu-id="046b4-788">9 (0x9) </span><span class="sxs-lookup"><span data-stu-id="046b4-788">9 (0x9)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-789">錯誤</span><span class="sxs-lookup"><span data-stu-id="046b4-789">Error</span></span>

</dd> <dt>

<span data-ttu-id="046b4-790">10 (0xA) </span><span class="sxs-lookup"><span data-stu-id="046b4-790">10 (0xA)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-791">忙碌</span><span class="sxs-lookup"><span data-stu-id="046b4-791">Busy</span></span>

</dd> <dt>

<span data-ttu-id="046b4-792">11 (0xB) </span><span class="sxs-lookup"><span data-stu-id="046b4-792">11 (0xB)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-793">無法使用</span><span class="sxs-lookup"><span data-stu-id="046b4-793">Not Available</span></span>

</dd> <dt>

<span data-ttu-id="046b4-794">12 (0xC) </span><span class="sxs-lookup"><span data-stu-id="046b4-794">12 (0xC)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-795">等候中</span><span class="sxs-lookup"><span data-stu-id="046b4-795">Waiting</span></span>

</dd> <dt>

<span data-ttu-id="046b4-796">13 (0xD) </span><span class="sxs-lookup"><span data-stu-id="046b4-796">13 (0xD)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-797">Processing</span><span class="sxs-lookup"><span data-stu-id="046b4-797">Processing</span></span>

</dd> <dt>

<span data-ttu-id="046b4-798">14 (0xE) </span><span class="sxs-lookup"><span data-stu-id="046b4-798">14 (0xE)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-799">初始化</span><span class="sxs-lookup"><span data-stu-id="046b4-799">Initialization</span></span>

</dd> <dt>

<span data-ttu-id="046b4-800">15</span><span class="sxs-lookup"><span data-stu-id="046b4-800">15</span></span>
</dt> <dd>

<span data-ttu-id="046b4-801">省電</span><span class="sxs-lookup"><span data-stu-id="046b4-801">Power Save</span></span>

</dd> <dt>

<span data-ttu-id="046b4-802">16 (0x10) </span><span class="sxs-lookup"><span data-stu-id="046b4-802">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-803">暫止刪除</span><span class="sxs-lookup"><span data-stu-id="046b4-803">Pending Deletion</span></span>

</dd> <dt>

<span data-ttu-id="046b4-804">17 (0x11) </span><span class="sxs-lookup"><span data-stu-id="046b4-804">17 (0x11)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-805">I/o 主動</span><span class="sxs-lookup"><span data-stu-id="046b4-805">I/O Active</span></span>

</dd> <dt>

<span data-ttu-id="046b4-806">18 (0x12) </span><span class="sxs-lookup"><span data-stu-id="046b4-806">18 (0x12)</span></span>
</dt> <dd>

<span data-ttu-id="046b4-807">手動送紙</span><span class="sxs-lookup"><span data-stu-id="046b4-807">Manual Feed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="046b4-808">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="046b4-808">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-809">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="046b4-809">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-810">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="046b4-810">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="046b4-811">若 **為 TRUE**，則會隱藏網路使用者的印表機。</span><span class="sxs-lookup"><span data-stu-id="046b4-811">If **TRUE**, the printer is hidden from network users.</span></span>

</dd> <dt>

<span data-ttu-id="046b4-812">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="046b4-812">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-813">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="046b4-813">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-814">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-814">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-815">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "CIM \_ PrintJob. HorizontalResolution" ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( "圖元/英寸" ) </span><span class="sxs-lookup"><span data-stu-id="046b4-815">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.HorizontalResolution"), [**Units**](../wmisdk/standard-qualifiers.md) ("pixels per inch")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-816">印表機的水準解析度，以每英吋像素為單位。</span><span class="sxs-lookup"><span data-stu-id="046b4-816">Horizontal resolution of the printer—in pixels per inch.</span></span>

<span data-ttu-id="046b4-817">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-817">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-818">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="046b4-818">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-819">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="046b4-819">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-820">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-820">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-821">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="046b4-821">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-822">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="046b4-822">Date and time an object was installed.</span></span> <span data-ttu-id="046b4-823">可能會在沒有將值寫入這個屬性的情況下安裝物件。</span><span class="sxs-lookup"><span data-stu-id="046b4-823">The object may be installed without a value being written to this property.</span></span> <span data-ttu-id="046b4-824">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-824">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-825">**JobCountSinceLastReset**</span><span class="sxs-lookup"><span data-stu-id="046b4-825">**JobCountSinceLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-826">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="046b4-826">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-827">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-827">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-828">限定詞： **計數器**</span><span class="sxs-lookup"><span data-stu-id="046b4-828">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="046b4-829">自上次重設印表機後的列印工作數目。</span><span class="sxs-lookup"><span data-stu-id="046b4-829">Number of print jobs since the printer was last reset.</span></span>

<span data-ttu-id="046b4-830">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-830">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-831">**KeepPrintedJobs**</span><span class="sxs-lookup"><span data-stu-id="046b4-831">**KeepPrintedJobs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-832">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="046b4-832">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-833">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="046b4-833">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="046b4-834">若 **為 TRUE**，列印多工緩衝處理器就不會刪除已完成的作業。</span><span class="sxs-lookup"><span data-stu-id="046b4-834">If **TRUE**, the print spooler does not delete the completed jobs.</span></span>

</dd> <dt>

<span data-ttu-id="046b4-835">**LanguagesSupported**</span><span class="sxs-lookup"><span data-stu-id="046b4-835">**LanguagesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-836">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="046b4-836">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="046b4-837">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-837">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-838">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIB。IETF \| printer-prtInterpreterLangFamily ") ， [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ printer**](cim-printer.md)。MimeTypesSupported "、" CIM \_ PrintJob Language "、" cim \_ PrintService. LanguagesSupported ") </span><span class="sxs-lookup"><span data-stu-id="046b4-838">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtInterpreterLangFamily"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).MimeTypesSupported", "CIM\_PrintJob.Language", "CIM\_PrintService.LanguagesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-839">原生支援的列印語言陣列。</span><span class="sxs-lookup"><span data-stu-id="046b4-839">Array of the print languages natively supported.</span></span>

<span data-ttu-id="046b4-840">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-840">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="046b4-841"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="046b4-841"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="046b4-842"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="046b4-842"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="046b4-843"><span id="PCL"></span><span id="pcl"></span>**PCL** (3) </span><span class="sxs-lookup"><span data-stu-id="046b4-843"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="046b4-844"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4) </span><span class="sxs-lookup"><span data-stu-id="046b4-844"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="046b4-845"><span id="PJL"></span><span id="pjl"></span>**PJL** (5) </span><span class="sxs-lookup"><span data-stu-id="046b4-845"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="046b4-846"><span id="PS"></span><span id="ps"></span>**PS** (6) </span><span class="sxs-lookup"><span data-stu-id="046b4-846"><span id="PS"></span><span id="ps"></span>**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="046b4-847"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7) </span><span class="sxs-lookup"><span data-stu-id="046b4-847"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="046b4-848"><span id="IPDS"></span><span id="ipds"></span>**Ipd** (8) </span><span class="sxs-lookup"><span data-stu-id="046b4-848"><span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="046b4-849"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9) </span><span class="sxs-lookup"><span data-stu-id="046b4-849"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="046b4-850"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10) </span><span class="sxs-lookup"><span data-stu-id="046b4-850"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="046b4-851"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11) </span><span class="sxs-lookup"><span data-stu-id="046b4-851"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="046b4-852"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12) </span><span class="sxs-lookup"><span data-stu-id="046b4-852"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="046b4-853"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13) </span><span class="sxs-lookup"><span data-stu-id="046b4-853"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="046b4-854"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14) </span><span class="sxs-lookup"><span data-stu-id="046b4-854"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="046b4-855"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**行資料** (15) </span><span class="sxs-lookup"><span data-stu-id="046b4-855"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Line Data** (15)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-856">LineData</span><span class="sxs-lookup"><span data-stu-id="046b4-856">LineData</span></span>

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="046b4-857"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16) </span><span class="sxs-lookup"><span data-stu-id="046b4-857"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-858">DODCA</span><span class="sxs-lookup"><span data-stu-id="046b4-858">DODCA</span></span>

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="046b4-859"><span id="REGIS"></span><span id="regis"></span>**REGIS** (17) </span><span class="sxs-lookup"><span data-stu-id="046b4-859"><span id="REGIS"></span><span id="regis"></span>**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="046b4-860"><span id="SCS"></span><span id="scs"></span>**SCS** (18) </span><span class="sxs-lookup"><span data-stu-id="046b4-860"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="046b4-861"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19) </span><span class="sxs-lookup"><span data-stu-id="046b4-861"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="046b4-862"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20) </span><span class="sxs-lookup"><span data-stu-id="046b4-862"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="046b4-863"><span id="PDS"></span><span id="pds"></span>**PDS** (21) </span><span class="sxs-lookup"><span data-stu-id="046b4-863"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="046b4-864"><span id="IGP"></span><span id="igp"></span>**IGP** (22) </span><span class="sxs-lookup"><span data-stu-id="046b4-864"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="046b4-865"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23) </span><span class="sxs-lookup"><span data-stu-id="046b4-865"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="046b4-866"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24) </span><span class="sxs-lookup"><span data-stu-id="046b4-866"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="046b4-867"><span id="WPS"></span><span id="wps"></span>**WPS** (25) </span><span class="sxs-lookup"><span data-stu-id="046b4-867"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="046b4-868"><span id="LN03"></span><span id="ln03"></span>**LN03** (26) </span><span class="sxs-lookup"><span data-stu-id="046b4-868"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="046b4-869"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27) </span><span class="sxs-lookup"><span data-stu-id="046b4-869"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="046b4-870"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28) </span><span class="sxs-lookup"><span data-stu-id="046b4-870"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="046b4-871"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29) </span><span class="sxs-lookup"><span data-stu-id="046b4-871"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="046b4-872"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30) </span><span class="sxs-lookup"><span data-stu-id="046b4-872"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="046b4-873"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**簡單文字** (31) </span><span class="sxs-lookup"><span data-stu-id="046b4-873"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Simple Text** (31)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-874">SimpleText</span><span class="sxs-lookup"><span data-stu-id="046b4-874">SimpleText</span></span>

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="046b4-875"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32) </span><span class="sxs-lookup"><span data-stu-id="046b4-875"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="046b4-876"><span id="DOC"></span><span id="doc"></span>**DOC** (33) </span><span class="sxs-lookup"><span data-stu-id="046b4-876"><span id="DOC"></span><span id="doc"></span>**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="046b4-877"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span> (34) 的 **印象深刻**</span><span class="sxs-lookup"><span data-stu-id="046b4-877"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="046b4-878"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35) </span><span class="sxs-lookup"><span data-stu-id="046b4-878"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="046b4-879"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36) </span><span class="sxs-lookup"><span data-stu-id="046b4-879"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="046b4-880"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37) </span><span class="sxs-lookup"><span data-stu-id="046b4-880"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="046b4-881"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**自動** (38) </span><span class="sxs-lookup"><span data-stu-id="046b4-881"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="046b4-882"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**頁面** (39) </span><span class="sxs-lookup"><span data-stu-id="046b4-882"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="046b4-883"><span id="LIPS"></span><span id="lips"></span>**Lip** (40) </span><span class="sxs-lookup"><span data-stu-id="046b4-883"><span id="LIPS"></span><span id="lips"></span>**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="046b4-884"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41) </span><span class="sxs-lookup"><span data-stu-id="046b4-884"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="046b4-885"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**診斷** (42) </span><span class="sxs-lookup"><span data-stu-id="046b4-885"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="046b4-886"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43) </span><span class="sxs-lookup"><span data-stu-id="046b4-886"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="046b4-887"><span id="EXCL"></span><span id="excl"></span>**排除** (44) </span><span class="sxs-lookup"><span data-stu-id="046b4-887"><span id="EXCL"></span><span id="excl"></span>**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="046b4-888"><span id="LCDS"></span><span id="lcds"></span>**Lcd** (45) </span><span class="sxs-lookup"><span data-stu-id="046b4-888"><span id="LCDS"></span><span id="lcds"></span>**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="046b4-889"><span id="XES"></span><span id="xes"></span>**XES** (46) </span><span class="sxs-lookup"><span data-stu-id="046b4-889"><span id="XES"></span><span id="xes"></span>**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="046b4-890"><span id="MIME"></span><span id="mime"></span>**MIME** (47) </span><span class="sxs-lookup"><span data-stu-id="046b4-890"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="XPS"></span><span id="xps"></span>

<span data-ttu-id="046b4-891"><span id="XPS"></span><span id="xps"></span>**XPS** (48) </span><span class="sxs-lookup"><span data-stu-id="046b4-891"><span id="XPS"></span><span id="xps"></span>**XPS** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL2"></span><span id="hpgl2"></span>

<span data-ttu-id="046b4-892"><span id="HPGL2"></span><span id="hpgl2"></span>**HPGL2** (49) </span><span class="sxs-lookup"><span data-stu-id="046b4-892"><span id="HPGL2"></span><span id="hpgl2"></span>**HPGL2** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCLXL"></span><span id="pclxl"></span>

<span data-ttu-id="046b4-893"><span id="PCLXL"></span><span id="pclxl"></span>**PCLXL** (50) </span><span class="sxs-lookup"><span data-stu-id="046b4-893"><span id="PCLXL"></span><span id="pclxl"></span>**PCLXL** (50)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="046b4-894">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="046b4-894">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-895">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="046b4-895">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-896">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-896">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="046b4-897">邏輯裝置報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="046b4-897">Last error code that the logical device reports.</span></span>

<span data-ttu-id="046b4-898">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-898">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-899">**本機**</span><span class="sxs-lookup"><span data-stu-id="046b4-899">**Local**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-900">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="046b4-900">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-901">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="046b4-901">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="046b4-902">若 **為 TRUE**，表示印表機未連接到網路。</span><span class="sxs-lookup"><span data-stu-id="046b4-902">If **TRUE**, the printer is not attached to a network.</span></span> <span data-ttu-id="046b4-903">如果 [ **本機** ] 和 [ **網路** ] 屬性都設定為 [ **TRUE**]，則印表機為網路印表機。</span><span class="sxs-lookup"><span data-stu-id="046b4-903">If both the **Local** and **Network** properties are set to **TRUE**, then the printer is a network printer.</span></span>

</dd> <dt>

<span data-ttu-id="046b4-904">**位置**</span><span class="sxs-lookup"><span data-stu-id="046b4-904">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-905">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="046b4-905">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-906">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="046b4-906">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="046b4-907">印表機的實體位置。</span><span class="sxs-lookup"><span data-stu-id="046b4-907">Physical location of the printer.</span></span>

<span data-ttu-id="046b4-908">範例： Bldg。</span><span class="sxs-lookup"><span data-stu-id="046b4-908">Example: Bldg.</span></span> <span data-ttu-id="046b4-909">38，房間1164</span><span class="sxs-lookup"><span data-stu-id="046b4-909">38, Room 1164</span></span>

</dd> <dt>

<span data-ttu-id="046b4-910">**MarkingTechnology**</span><span class="sxs-lookup"><span data-stu-id="046b4-910">**MarkingTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-911">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="046b4-911">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-912">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-912">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-913">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIB。IETF \| 印表機-prtMarkerMarkTech ") </span><span class="sxs-lookup"><span data-stu-id="046b4-913">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtMarkerMarkTech")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-914">標示印表機所使用的技術。</span><span class="sxs-lookup"><span data-stu-id="046b4-914">Marking technology the printer uses.</span></span>

<span data-ttu-id="046b4-915">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-915">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="046b4-916">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="046b4-916">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="046b4-917">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="046b4-917">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_LED"></span><span id="electrophotographic_led"></span><span id="ELECTROPHOTOGRAPHIC_LED"></span>

<span data-ttu-id="046b4-918">**ELECTROPHOTOGRAPHIC LED** (3) </span><span class="sxs-lookup"><span data-stu-id="046b4-918">**Electrophotographic LED** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Laser"></span><span id="electrophotographic_laser"></span><span id="ELECTROPHOTOGRAPHIC_LASER"></span>

<span data-ttu-id="046b4-919">**Electrophotographic 鐳射** (4) </span><span class="sxs-lookup"><span data-stu-id="046b4-919">**Electrophotographic Laser** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Other"></span><span id="electrophotographic_other"></span><span id="ELECTROPHOTOGRAPHIC_OTHER"></span>

<span data-ttu-id="046b4-920">**Electrophotographic 其他** (5) </span><span class="sxs-lookup"><span data-stu-id="046b4-920">**Electrophotographic Other** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_9pin"></span><span id="impact_moving_head_dot_matrix_9pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_9PIN"></span>

<span data-ttu-id="046b4-921">**移動頭部點矩陣 9pin** (6) 的影響</span><span class="sxs-lookup"><span data-stu-id="046b4-921">**Impact Moving Head Dot Matrix 9pin** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_24pin"></span><span id="impact_moving_head_dot_matrix_24pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_24PIN"></span>

<span data-ttu-id="046b4-922">**移動頭部點矩陣 24pin** (7) 的影響</span><span class="sxs-lookup"><span data-stu-id="046b4-922">**Impact Moving Head Dot Matrix 24pin** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_Other"></span><span id="impact_moving_head_dot_matrix_other"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_OTHER"></span>

<span data-ttu-id="046b4-923">將 **頭部點矩陣移至其他** (8) 的影響</span><span class="sxs-lookup"><span data-stu-id="046b4-923">**Impact Moving Head Dot Matrix Other** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Fully_Formed"></span><span id="impact_moving_head_fully_formed"></span><span id="IMPACT_MOVING_HEAD_FULLY_FORMED"></span>

<span data-ttu-id="046b4-924">移動前端 (9) 的 **完整格式影響**</span><span class="sxs-lookup"><span data-stu-id="046b4-924">**Impact Moving Head Fully Formed** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Band"></span><span id="impact_band"></span><span id="IMPACT_BAND"></span>

<span data-ttu-id="046b4-925">**影響波段** (10) </span><span class="sxs-lookup"><span data-stu-id="046b4-925">**Impact Band** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Other"></span><span id="impact_other"></span><span id="IMPACT_OTHER"></span>

<span data-ttu-id="046b4-926">**影響其他** (11) </span><span class="sxs-lookup"><span data-stu-id="046b4-926">**Impact Other** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Aqueous"></span><span id="inkjet_aqueous"></span><span id="INKJET_AQUEOUS"></span>

<span data-ttu-id="046b4-927">**噴墨 Aqueous** (12) </span><span class="sxs-lookup"><span data-stu-id="046b4-927">**Inkjet Aqueous** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Solid"></span><span id="inkjet_solid"></span><span id="INKJET_SOLID"></span>

<span data-ttu-id="046b4-928">**噴墨** (13) </span><span class="sxs-lookup"><span data-stu-id="046b4-928">**Inkjet Solid** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Other"></span><span id="inkjet_other"></span><span id="INKJET_OTHER"></span>

<span data-ttu-id="046b4-929">**其他** (14) 的噴墨</span><span class="sxs-lookup"><span data-stu-id="046b4-929">**Inkjet Other** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Pen"></span><span id="pen"></span><span id="PEN"></span>

<span data-ttu-id="046b4-930">**畫筆** (15) </span><span class="sxs-lookup"><span data-stu-id="046b4-930">**Pen** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Transfer"></span><span id="thermal_transfer"></span><span id="THERMAL_TRANSFER"></span>

<span data-ttu-id="046b4-931"> (16) 的 **熱傳輸**</span><span class="sxs-lookup"><span data-stu-id="046b4-931">**Thermal Transfer** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Sensitive"></span><span id="thermal_sensitive"></span><span id="THERMAL_SENSITIVE"></span>

<span data-ttu-id="046b4-932"> (17) 的 **熱機密**</span><span class="sxs-lookup"><span data-stu-id="046b4-932">**Thermal Sensitive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Diffusion"></span><span id="thermal_diffusion"></span><span id="THERMAL_DIFFUSION"></span>

<span data-ttu-id="046b4-933"> (18) 的 **熱擴散**</span><span class="sxs-lookup"><span data-stu-id="046b4-933">**Thermal Diffusion** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Other"></span><span id="thermal_other"></span><span id="THERMAL_OTHER"></span>

<span data-ttu-id="046b4-934">**其他熱** (19) </span><span class="sxs-lookup"><span data-stu-id="046b4-934">**Thermal Other** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Electroerosion"></span><span id="electroerosion"></span><span id="ELECTROEROSION"></span>

<span data-ttu-id="046b4-935">**Electroerosion** (20) </span><span class="sxs-lookup"><span data-stu-id="046b4-935">**Electroerosion** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrostatic"></span><span id="electrostatic"></span><span id="ELECTROSTATIC"></span>

<span data-ttu-id="046b4-936">**靜電** (21) </span><span class="sxs-lookup"><span data-stu-id="046b4-936">**Electrostatic** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Microfiche"></span><span id="photographic_microfiche"></span><span id="PHOTOGRAPHIC_MICROFICHE"></span>

<span data-ttu-id="046b4-937">**攝影縮微膠片** (22) </span><span class="sxs-lookup"><span data-stu-id="046b4-937">**Photographic Microfiche** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Imagesetter"></span><span id="photographic_imagesetter"></span><span id="PHOTOGRAPHIC_IMAGESETTER"></span>

<span data-ttu-id="046b4-938">**攝影照排機** (23) </span><span class="sxs-lookup"><span data-stu-id="046b4-938">**Photographic Imagesetter** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Other"></span><span id="photographic_other"></span><span id="PHOTOGRAPHIC_OTHER"></span>

<span data-ttu-id="046b4-939">**攝影其他** (24) </span><span class="sxs-lookup"><span data-stu-id="046b4-939">**Photographic Other** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Ion_Deposition"></span><span id="ion_deposition"></span><span id="ION_DEPOSITION"></span>

<span data-ttu-id="046b4-940">**離子 Deposition** (25) </span><span class="sxs-lookup"><span data-stu-id="046b4-940">**Ion Deposition** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="eBeam"></span><span id="ebeam"></span><span id="EBEAM"></span>

<span data-ttu-id="046b4-941">**eBeam** (26) </span><span class="sxs-lookup"><span data-stu-id="046b4-941">**eBeam** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Typesetter"></span><span id="typesetter"></span><span id="TYPESETTER"></span>

<span data-ttu-id="046b4-942">**Typesetter** (27) </span><span class="sxs-lookup"><span data-stu-id="046b4-942">**Typesetter** (27)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="046b4-943">**MaxCopies**</span><span class="sxs-lookup"><span data-stu-id="046b4-943">**MaxCopies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-944">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="046b4-944">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-945">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-945">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-946">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「CIM \_ PrintJob」 ) </span><span class="sxs-lookup"><span data-stu-id="046b4-946">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.Copies")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-947">印表機可以為一個工作產生的最大複本數目。</span><span class="sxs-lookup"><span data-stu-id="046b4-947">Maximum number of copies the printer can produce for one job.</span></span>

<span data-ttu-id="046b4-948">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-948">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-949">**MaxNumberUp**</span><span class="sxs-lookup"><span data-stu-id="046b4-949">**MaxNumberUp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-950">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="046b4-950">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-951">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-951">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-952">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "CIM \_ PrintJob. NumberUp" ) </span><span class="sxs-lookup"><span data-stu-id="046b4-952">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.NumberUp")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-953">印表機可以在一張媒體紙上轉譯的列印資料流程頁面數目上限，例如紙張。</span><span class="sxs-lookup"><span data-stu-id="046b4-953">Maximum number of print-stream pages the printer can render on one media sheet, such as paper.</span></span>

<span data-ttu-id="046b4-954">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-954">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-955">**MaxSizeSupported**</span><span class="sxs-lookup"><span data-stu-id="046b4-955">**MaxSizeSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-956">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="046b4-956">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-957">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-957">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-958">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "CIM \_ PrintJob. JobSize" ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( "kb" ) </span><span class="sxs-lookup"><span data-stu-id="046b4-958">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.JobSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-959">最大的作業（以 kb 為單位），可供印表機接受。</span><span class="sxs-lookup"><span data-stu-id="046b4-959">Largest job as a byte stream, in kilobytes, that the printer can accept.</span></span> <span data-ttu-id="046b4-960">值為 0 (零) 表示未設定任何限制。</span><span class="sxs-lookup"><span data-stu-id="046b4-960">A value of 0 (zero) indicates that no limit is set.</span></span>

<span data-ttu-id="046b4-961">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-961">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-962">**MimeTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="046b4-962">**MimeTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-963">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="046b4-963">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="046b4-964">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-964">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-965">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 印表機**](cim-printer.md)」。LanguagesSupported "、" CIM \_ PrintJob. mimetype "、" cim \_ PrintService. MimeTypesSupported ") </span><span class="sxs-lookup"><span data-stu-id="046b4-965">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).LanguagesSupported", "CIM\_PrintJob.MimeTypes", "CIM\_PrintService.MimeTypesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-966">印表機支援的詳細 MIME 類型說明的陣列。</span><span class="sxs-lookup"><span data-stu-id="046b4-966">Array of detailed MIME-type explanations that the printer supports.</span></span> <span data-ttu-id="046b4-967">如果提供了資料，則值 47 ( "MIME" ) 必須包含在 **LanguagesSupported** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="046b4-967">If data is provided, then the value 47 ("MIME") must be included in the **LanguagesSupported** property.</span></span>

<span data-ttu-id="046b4-968">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-968">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-969">**名稱**</span><span class="sxs-lookup"><span data-stu-id="046b4-969">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-970">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="046b4-970">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-971">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-971">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-972">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="046b4-972">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-973">印表機的名稱。</span><span class="sxs-lookup"><span data-stu-id="046b4-973">Name of the printer.</span></span>

<span data-ttu-id="046b4-974">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-974">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-975">**NaturalLanguagesSupported**</span><span class="sxs-lookup"><span data-stu-id="046b4-975">**NaturalLanguagesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-976">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="046b4-976">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="046b4-977">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-977">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-978">限定詞： [**ArrayType**](../wmisdk/standard-qualifiers.md) ( "Indexed" ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "MIB。IETF \| Printer-prtLocalizationLanguage ") ， [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (" CIM \_ PrintJob. NaturalLanguage ") </span><span class="sxs-lookup"><span data-stu-id="046b4-978">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtLocalizationLanguage"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.NaturalLanguage")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-979">印表機用來輸出管理資訊的字串所支援的語言陣列。</span><span class="sxs-lookup"><span data-stu-id="046b4-979">Array of languages supported for strings that the printer uses for output of management information.</span></span> <span data-ttu-id="046b4-980">必須符合 [RFC 1766](https://www.ietf.org/rfc/rfc1766.txt)。</span><span class="sxs-lookup"><span data-stu-id="046b4-980">Must conform to [RFC 1766](https://www.ietf.org/rfc/rfc1766.txt).</span></span> <span data-ttu-id="046b4-981">例如，"en" 用於英文。</span><span class="sxs-lookup"><span data-stu-id="046b4-981">For example, "en" is used for English.</span></span>

<span data-ttu-id="046b4-982">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-982">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-983">**Network**</span><span class="sxs-lookup"><span data-stu-id="046b4-983">**Network**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-984">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="046b4-984">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-985">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="046b4-985">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="046b4-986">若 **為 TRUE**，表示印表機為網路印表機。</span><span class="sxs-lookup"><span data-stu-id="046b4-986">If **TRUE**, the printer is a network printer.</span></span> <span data-ttu-id="046b4-987">如果 [ **本機** ] 和 [ **網路** ] 屬性都設定為 [ **TRUE**]，則印表機為網路印表機。</span><span class="sxs-lookup"><span data-stu-id="046b4-987">If both the **Local** and **Network** properties are set to **TRUE**, then the printer is a network printer.</span></span>

</dd> <dt>

<span data-ttu-id="046b4-988">**PaperSizesSupported**</span><span class="sxs-lookup"><span data-stu-id="046b4-988">**PaperSizesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-989">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="046b4-989">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="046b4-990">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-990">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="046b4-991">印表機支援的紙張類型陣列。</span><span class="sxs-lookup"><span data-stu-id="046b4-991">Array of the paper types that the printer supports.</span></span>

<span data-ttu-id="046b4-992">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-992">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="046b4-993"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="046b4-993"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="046b4-994"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="046b4-994"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="A"></span><span id="a"></span>

<span data-ttu-id="046b4-995"><span id="A"></span><span id="a"></span>**(2**) </span><span class="sxs-lookup"><span data-stu-id="046b4-995"><span id="A"></span><span id="a"></span>**A** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="B"></span><span id="b"></span>

<span data-ttu-id="046b4-996"><span id="B"></span><span id="b"></span>**B** (3) </span><span class="sxs-lookup"><span data-stu-id="046b4-996"><span id="B"></span><span id="b"></span>**B** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="C"></span><span id="c"></span>

<span data-ttu-id="046b4-997"><span id="C"></span><span id="c"></span>**C** (4) </span><span class="sxs-lookup"><span data-stu-id="046b4-997"><span id="C"></span><span id="c"></span>**C** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="D"></span><span id="d"></span>

<span data-ttu-id="046b4-998"><span id="D"></span><span id="d"></span>**D** (5) </span><span class="sxs-lookup"><span data-stu-id="046b4-998"><span id="D"></span><span id="d"></span>**D** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="E"></span><span id="e"></span>

<span data-ttu-id="046b4-999"><span id="E"></span><span id="e"></span>**E** (6) </span><span class="sxs-lookup"><span data-stu-id="046b4-999"><span id="E"></span><span id="e"></span>**E** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>

<span data-ttu-id="046b4-1000"><span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>**字母** (7) </span><span class="sxs-lookup"><span data-stu-id="046b4-1000"><span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>**Letter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>

<span data-ttu-id="046b4-1001"><span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>**合法** (8) </span><span class="sxs-lookup"><span data-stu-id="046b4-1001"><span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>**Legal** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>

<span data-ttu-id="046b4-1002"><span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>**NA-10x13-信封** (9) </span><span class="sxs-lookup"><span data-stu-id="046b4-1002"><span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>**NA-10x13-Envelope** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>

<span data-ttu-id="046b4-1003"><span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>**NA-9x12-信封** (10) </span><span class="sxs-lookup"><span data-stu-id="046b4-1003"><span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>**NA-9x12-Envelope** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>

<span data-ttu-id="046b4-1004"><span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>**NA-數位-10-信封** (11) </span><span class="sxs-lookup"><span data-stu-id="046b4-1004"><span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>**NA-Number-10-Envelope** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>

<span data-ttu-id="046b4-1005"><span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>**NA-7x9-信封** (12) </span><span class="sxs-lookup"><span data-stu-id="046b4-1005"><span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>**NA-7x9-Envelope** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>

<span data-ttu-id="046b4-1006"><span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>**NA-9x11-信封** (13) </span><span class="sxs-lookup"><span data-stu-id="046b4-1006"><span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>**NA-9x11-Envelope** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>

<span data-ttu-id="046b4-1007"><span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>**NA-10x14-信封** (14) </span><span class="sxs-lookup"><span data-stu-id="046b4-1007"><span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>**NA-10x14-Envelope** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>

<span data-ttu-id="046b4-1008"><span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>**NA-數位-9-信封** (15) </span><span class="sxs-lookup"><span data-stu-id="046b4-1008"><span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>**NA-Number-9-Envelope** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>

<span data-ttu-id="046b4-1009"><span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>**NA-6x9-信封** (16) </span><span class="sxs-lookup"><span data-stu-id="046b4-1009"><span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>**NA-6x9-Envelope** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>

<span data-ttu-id="046b4-1010"><span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>**NA-10x15-信封** (17) </span><span class="sxs-lookup"><span data-stu-id="046b4-1010"><span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>**NA-10x15-Envelope** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="A0"></span><span id="a0"></span>

<span data-ttu-id="046b4-1011"><span id="A0"></span><span id="a0"></span>**A0** (18) </span><span class="sxs-lookup"><span data-stu-id="046b4-1011"><span id="A0"></span><span id="a0"></span>**A0** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="A1"></span><span id="a1"></span>

<span data-ttu-id="046b4-1012"><span id="A1"></span><span id="a1"></span>**A1** (19) </span><span class="sxs-lookup"><span data-stu-id="046b4-1012"><span id="A1"></span><span id="a1"></span>**A1** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="A2"></span><span id="a2"></span>

<span data-ttu-id="046b4-1013"><span id="A2"></span><span id="a2"></span>**A2** (20) </span><span class="sxs-lookup"><span data-stu-id="046b4-1013"><span id="A2"></span><span id="a2"></span>**A2** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="A3"></span><span id="a3"></span>

<span data-ttu-id="046b4-1014"><span id="A3"></span><span id="a3"></span>**A3** (21) </span><span class="sxs-lookup"><span data-stu-id="046b4-1014"><span id="A3"></span><span id="a3"></span>**A3** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="A4"></span><span id="a4"></span>

<span data-ttu-id="046b4-1015"><span id="A4"></span><span id="a4"></span>**A4** (22) </span><span class="sxs-lookup"><span data-stu-id="046b4-1015"><span id="A4"></span><span id="a4"></span>**A4** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="A5"></span><span id="a5"></span>

<span data-ttu-id="046b4-1016"><span id="A5"></span><span id="a5"></span>**A5** (23) </span><span class="sxs-lookup"><span data-stu-id="046b4-1016"><span id="A5"></span><span id="a5"></span>**A5** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="A6"></span><span id="a6"></span>

<span data-ttu-id="046b4-1017"><span id="A6"></span><span id="a6"></span>**A6** (24) </span><span class="sxs-lookup"><span data-stu-id="046b4-1017"><span id="A6"></span><span id="a6"></span>**A6** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="A7"></span><span id="a7"></span>

<span data-ttu-id="046b4-1018"><span id="A7"></span><span id="a7"></span>**A7** (25) </span><span class="sxs-lookup"><span data-stu-id="046b4-1018"><span id="A7"></span><span id="a7"></span>**A7** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="A8"></span><span id="a8"></span>

<span data-ttu-id="046b4-1019"><span id="A8"></span><span id="a8"></span>**A8** (26) </span><span class="sxs-lookup"><span data-stu-id="046b4-1019"><span id="A8"></span><span id="a8"></span>**A8** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="A9A10"></span><span id="a9a10"></span>

<span data-ttu-id="046b4-1020"><span id="A9A10"></span><span id="a9a10"></span>**A9A10** (27) </span><span class="sxs-lookup"><span data-stu-id="046b4-1020"><span id="A9A10"></span><span id="a9a10"></span>**A9A10** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="B0"></span><span id="b0"></span>

<span data-ttu-id="046b4-1021"><span id="B0"></span><span id="b0"></span>**B0** (28) </span><span class="sxs-lookup"><span data-stu-id="046b4-1021"><span id="B0"></span><span id="b0"></span>**B0** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="B1"></span><span id="b1"></span>

<span data-ttu-id="046b4-1022"><span id="B1"></span><span id="b1"></span>**B1** (29) </span><span class="sxs-lookup"><span data-stu-id="046b4-1022"><span id="B1"></span><span id="b1"></span>**B1** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="B2"></span><span id="b2"></span>

<span data-ttu-id="046b4-1023"><span id="B2"></span><span id="b2"></span>**B2** (30) </span><span class="sxs-lookup"><span data-stu-id="046b4-1023"><span id="B2"></span><span id="b2"></span>**B2** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="B3"></span><span id="b3"></span>

<span data-ttu-id="046b4-1024"><span id="B3"></span><span id="b3"></span>**B3** (31) </span><span class="sxs-lookup"><span data-stu-id="046b4-1024"><span id="B3"></span><span id="b3"></span>**B3** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="B4"></span><span id="b4"></span>

<span data-ttu-id="046b4-1025"><span id="B4"></span><span id="b4"></span>**B4** (32) </span><span class="sxs-lookup"><span data-stu-id="046b4-1025"><span id="B4"></span><span id="b4"></span>**B4** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="B5"></span><span id="b5"></span>

<span data-ttu-id="046b4-1026"><span id="B5"></span><span id="b5"></span>**B5** (33) </span><span class="sxs-lookup"><span data-stu-id="046b4-1026"><span id="B5"></span><span id="b5"></span>**B5** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="B6"></span><span id="b6"></span>

<span data-ttu-id="046b4-1027"><span id="B6"></span><span id="b6"></span>**B6** (34) </span><span class="sxs-lookup"><span data-stu-id="046b4-1027"><span id="B6"></span><span id="b6"></span>**B6** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="B7"></span><span id="b7"></span>

<span data-ttu-id="046b4-1028"><span id="B7"></span><span id="b7"></span>**B7** (35) </span><span class="sxs-lookup"><span data-stu-id="046b4-1028"><span id="B7"></span><span id="b7"></span>**B7** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="B8"></span><span id="b8"></span>

<span data-ttu-id="046b4-1029"><span id="B8"></span><span id="b8"></span>**B8** (36) </span><span class="sxs-lookup"><span data-stu-id="046b4-1029"><span id="B8"></span><span id="b8"></span>**B8** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="B9"></span><span id="b9"></span>

<span data-ttu-id="046b4-1030"><span id="B9"></span><span id="b9"></span>**B9** (37) </span><span class="sxs-lookup"><span data-stu-id="046b4-1030"><span id="B9"></span><span id="b9"></span>**B9** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="B10"></span><span id="b10"></span>

<span data-ttu-id="046b4-1031"><span id="B10"></span><span id="b10"></span>**B10** (38) </span><span class="sxs-lookup"><span data-stu-id="046b4-1031"><span id="B10"></span><span id="b10"></span>**B10** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="C0"></span><span id="c0"></span>

<span data-ttu-id="046b4-1032"><span id="C0"></span><span id="c0"></span>**C0** (39) </span><span class="sxs-lookup"><span data-stu-id="046b4-1032"><span id="C0"></span><span id="c0"></span>**C0** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="C1"></span><span id="c1"></span>

<span data-ttu-id="046b4-1033"><span id="C1"></span><span id="c1"></span>**C1** (40) </span><span class="sxs-lookup"><span data-stu-id="046b4-1033"><span id="C1"></span><span id="c1"></span>**C1** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="C2C3"></span><span id="c2c3"></span>

<span data-ttu-id="046b4-1034"><span id="C2C3"></span><span id="c2c3"></span>**C2C3** (41) </span><span class="sxs-lookup"><span data-stu-id="046b4-1034"><span id="C2C3"></span><span id="c2c3"></span>**C2C3** (41)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-1035">C2</span><span class="sxs-lookup"><span data-stu-id="046b4-1035">C2</span></span>

</dd> <dt>

<span id="C4"></span><span id="c4"></span>

<span data-ttu-id="046b4-1036"><span id="C4"></span><span id="c4"></span>**C4** (42) </span><span class="sxs-lookup"><span data-stu-id="046b4-1036"><span id="C4"></span><span id="c4"></span>**C4** (42)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-1037">C3</span><span class="sxs-lookup"><span data-stu-id="046b4-1037">C3</span></span>

</dd> <dt>

<span id="C5"></span><span id="c5"></span>

<span data-ttu-id="046b4-1038"><span id="C5"></span><span id="c5"></span>**C5** (43) </span><span class="sxs-lookup"><span data-stu-id="046b4-1038"><span id="C5"></span><span id="c5"></span>**C5** (43)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-1039">C4</span><span class="sxs-lookup"><span data-stu-id="046b4-1039">C4</span></span>

</dd> <dt>

<span id="C6"></span><span id="c6"></span>

<span data-ttu-id="046b4-1040"><span id="C6"></span><span id="c6"></span>**C6** (44) </span><span class="sxs-lookup"><span data-stu-id="046b4-1040"><span id="C6"></span><span id="c6"></span>**C6** (44)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-1041">C5</span><span class="sxs-lookup"><span data-stu-id="046b4-1041">C5</span></span>

</dd> <dt>

<span id="C7"></span><span id="c7"></span>

<span data-ttu-id="046b4-1042"><span id="C7"></span><span id="c7"></span>**C7** (45) </span><span class="sxs-lookup"><span data-stu-id="046b4-1042"><span id="C7"></span><span id="c7"></span>**C7** (45)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-1043">C6</span><span class="sxs-lookup"><span data-stu-id="046b4-1043">C6</span></span>

</dd> <dt>

<span id="C8"></span><span id="c8"></span>

<span data-ttu-id="046b4-1044"><span id="C8"></span><span id="c8"></span>**C8** (46) </span><span class="sxs-lookup"><span data-stu-id="046b4-1044"><span id="C8"></span><span id="c8"></span>**C8** (46)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-1045">C7</span><span class="sxs-lookup"><span data-stu-id="046b4-1045">C7</span></span>

</dd> <dt>

<span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>

<span data-ttu-id="046b4-1046"><span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>**ISO-指定** (47) </span><span class="sxs-lookup"><span data-stu-id="046b4-1046"><span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>**ISO-Designated** (47)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-1047">C8</span><span class="sxs-lookup"><span data-stu-id="046b4-1047">C8</span></span>

</dd> <dt>

<span id="JIS_B0"></span><span id="jis_b0"></span>

<span data-ttu-id="046b4-1048"><span id="JIS_B0"></span><span id="jis_b0"></span>**JIS B0** (48) </span><span class="sxs-lookup"><span data-stu-id="046b4-1048"><span id="JIS_B0"></span><span id="jis_b0"></span>**JIS B0** (48)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-1049">ISO-Designated</span><span class="sxs-lookup"><span data-stu-id="046b4-1049">ISO-Designated</span></span>

</dd> <dt>

<span id="JIS_B1"></span><span id="jis_b1"></span>

<span data-ttu-id="046b4-1050"><span id="JIS_B1"></span><span id="jis_b1"></span>**JIS B1** (49) </span><span class="sxs-lookup"><span data-stu-id="046b4-1050"><span id="JIS_B1"></span><span id="jis_b1"></span>**JIS B1** (49)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-1051">JIS B0</span><span class="sxs-lookup"><span data-stu-id="046b4-1051">JIS B0</span></span>

</dd> <dt>

<span id="JIS_B2"></span><span id="jis_b2"></span>

<span data-ttu-id="046b4-1052"><span id="JIS_B2"></span><span id="jis_b2"></span>**JIS B2** (50) </span><span class="sxs-lookup"><span data-stu-id="046b4-1052"><span id="JIS_B2"></span><span id="jis_b2"></span>**JIS B2** (50)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-1053">JIS B1</span><span class="sxs-lookup"><span data-stu-id="046b4-1053">JIS B1</span></span>

</dd> <dt>

<span id="JIS_B3"></span><span id="jis_b3"></span>

<span data-ttu-id="046b4-1054"><span id="JIS_B3"></span><span id="jis_b3"></span>**JIS B3** (51) </span><span class="sxs-lookup"><span data-stu-id="046b4-1054"><span id="JIS_B3"></span><span id="jis_b3"></span>**JIS B3** (51)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-1055">JIS B2</span><span class="sxs-lookup"><span data-stu-id="046b4-1055">JIS B2</span></span>

</dd> <dt>

<span id="JIS_B4"></span><span id="jis_b4"></span>

<span data-ttu-id="046b4-1056"><span id="JIS_B4"></span><span id="jis_b4"></span>**JIS B4** (52) </span><span class="sxs-lookup"><span data-stu-id="046b4-1056"><span id="JIS_B4"></span><span id="jis_b4"></span>**JIS B4** (52)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-1057">JIS B3</span><span class="sxs-lookup"><span data-stu-id="046b4-1057">JIS B3</span></span>

</dd> <dt>

<span id="JIS_B5"></span><span id="jis_b5"></span>

<span data-ttu-id="046b4-1058"><span id="JIS_B5"></span><span id="jis_b5"></span>**JIS B5** (53) </span><span class="sxs-lookup"><span data-stu-id="046b4-1058"><span id="JIS_B5"></span><span id="jis_b5"></span>**JIS B5** (53)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-1059">JIS B4</span><span class="sxs-lookup"><span data-stu-id="046b4-1059">JIS B4</span></span>

</dd> <dt>

<span id="JIS_B6"></span><span id="jis_b6"></span>

<span data-ttu-id="046b4-1060"><span id="JIS_B6"></span><span id="jis_b6"></span>**JIS B6** (54) </span><span class="sxs-lookup"><span data-stu-id="046b4-1060"><span id="JIS_B6"></span><span id="jis_b6"></span>**JIS B6** (54)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-1061">JIS B5</span><span class="sxs-lookup"><span data-stu-id="046b4-1061">JIS B5</span></span>

</dd> <dt>

<span id="JIS_B7"></span><span id="jis_b7"></span>

<span data-ttu-id="046b4-1062"><span id="JIS_B7"></span><span id="jis_b7"></span>**JIS B7** (55) </span><span class="sxs-lookup"><span data-stu-id="046b4-1062"><span id="JIS_B7"></span><span id="jis_b7"></span>**JIS B7** (55)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-1063">JIS B6</span><span class="sxs-lookup"><span data-stu-id="046b4-1063">JIS B6</span></span>

</dd> <dt>

<span id="JIS_B8"></span><span id="jis_b8"></span>

<span data-ttu-id="046b4-1064"><span id="JIS_B8"></span><span id="jis_b8"></span>**JIS B8** (56) </span><span class="sxs-lookup"><span data-stu-id="046b4-1064"><span id="JIS_B8"></span><span id="jis_b8"></span>**JIS B8** (56)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-1065">JIS B7</span><span class="sxs-lookup"><span data-stu-id="046b4-1065">JIS B7</span></span>

</dd> <dt>

<span id="JIS_B9"></span><span id="jis_b9"></span>

<span data-ttu-id="046b4-1066"><span id="JIS_B9"></span><span id="jis_b9"></span>**JIS B9** (57) </span><span class="sxs-lookup"><span data-stu-id="046b4-1066"><span id="JIS_B9"></span><span id="jis_b9"></span>**JIS B9** (57)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-1067">JIS B8</span><span class="sxs-lookup"><span data-stu-id="046b4-1067">JIS B8</span></span>

</dd> <dt>

<span id="JIS_B10"></span><span id="jis_b10"></span>

<span data-ttu-id="046b4-1068"><span id="JIS_B10"></span><span id="jis_b10"></span>**JIS B10** (58) </span><span class="sxs-lookup"><span data-stu-id="046b4-1068"><span id="JIS_B10"></span><span id="jis_b10"></span>**JIS B10** (58)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-1069">JIS B9</span><span class="sxs-lookup"><span data-stu-id="046b4-1069">JIS B9</span></span>

</dd> <dt>

<span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>

<span data-ttu-id="046b4-1070"><span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>**NA-字母** (59) </span><span class="sxs-lookup"><span data-stu-id="046b4-1070"><span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>**NA-Letter** (59)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-1071">JIS B10</span><span class="sxs-lookup"><span data-stu-id="046b4-1071">JIS B10</span></span>

</dd> <dt>

<span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>

<span data-ttu-id="046b4-1072"><span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>**NA-合法** (60) </span><span class="sxs-lookup"><span data-stu-id="046b4-1072"><span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>**NA-Legal** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>

<span data-ttu-id="046b4-1073"><span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>**B4-信封** (61) </span><span class="sxs-lookup"><span data-stu-id="046b4-1073"><span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>**B4-Envelope** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>

<span data-ttu-id="046b4-1074"><span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>**B5-信封** (62) </span><span class="sxs-lookup"><span data-stu-id="046b4-1074"><span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>**B5-Envelope** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>

<span data-ttu-id="046b4-1075"><span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>**C3-信封** (63) </span><span class="sxs-lookup"><span data-stu-id="046b4-1075"><span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>**C3-Envelope** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>

<span data-ttu-id="046b4-1076"><span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>**C4-信封** (64) </span><span class="sxs-lookup"><span data-stu-id="046b4-1076"><span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>**C4-Envelope** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>

<span data-ttu-id="046b4-1077"><span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>**C5-信封** (65) </span><span class="sxs-lookup"><span data-stu-id="046b4-1077"><span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>**C5-Envelope** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>

<span data-ttu-id="046b4-1078"><span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>**C6-信封** (66) </span><span class="sxs-lookup"><span data-stu-id="046b4-1078"><span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>**C6-Envelope** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>

<span data-ttu-id="046b4-1079"><span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>**指定-長信封** (67) </span><span class="sxs-lookup"><span data-stu-id="046b4-1079"><span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>**Designated-Long-Envelope** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>

<span data-ttu-id="046b4-1080"><span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>**Monarch-信封** (68) </span><span class="sxs-lookup"><span data-stu-id="046b4-1080"><span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>**Monarch-Envelope** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span data-ttu-id="046b4-1081"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (69) </span><span class="sxs-lookup"><span data-stu-id="046b4-1081"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>

<span data-ttu-id="046b4-1082"><span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span> (70) 的 **對開**</span><span class="sxs-lookup"><span data-stu-id="046b4-1082"><span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>**Folio** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>

<span data-ttu-id="046b4-1083"><span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>**發票** (71) </span><span class="sxs-lookup"><span data-stu-id="046b4-1083"><span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>**Invoice** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>

<span data-ttu-id="046b4-1084"><span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>**總帳** (72) </span><span class="sxs-lookup"><span data-stu-id="046b4-1084"><span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>**Ledger** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>

<span data-ttu-id="046b4-1085"><span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>**Quarto** (73) </span><span class="sxs-lookup"><span data-stu-id="046b4-1085"><span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>**Quarto** (73)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="046b4-1086">**PaperTypesAvailable**</span><span class="sxs-lookup"><span data-stu-id="046b4-1086">**PaperTypesAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-1087">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="046b4-1087">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1088">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-1088">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1089">限定詞： [**ArrayType**](../wmisdk/standard-qualifiers.md) ( "Indexed" ) ， [**MODELCORRESPONDENCE**](../wmisdk/standard-qualifiers.md) ( "cim \_ PrintJob. RequiredPaperType"，"cim \_ PrintService. PaperTypesAvailable" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIB。IETF \| 印表機-prtInputMediaName ") </span><span class="sxs-lookup"><span data-stu-id="046b4-1089">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.RequiredPaperType", "CIM\_PrintService.PaperTypesAvailable"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtInputMediaName")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-1090">印表機目前提供的紙張類型陣列。</span><span class="sxs-lookup"><span data-stu-id="046b4-1090">Array of paper types that are currently available on the printer.</span></span> <span data-ttu-id="046b4-1091">每個字串都必須以 ISO/IEC 10175 檔列印應用程式所指定的格式表示 (DPA) ，在 [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (印表機 MIB) 的附錄 C 中摘要說明。</span><span class="sxs-lookup"><span data-stu-id="046b4-1091">Each string must be expressed in the format specified by ISO/IEC 10175 Document Printing Application (DPA), which is summarized in Appendix C of [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Printer MIB).</span></span> <span data-ttu-id="046b4-1092">這個屬性中所識別的任何紙張大小也必須出現在 **PaperSizesSupported** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="046b4-1092">Any paper size identified in this property must also appear in the **PaperSizesSupported** property.</span></span>

<span data-ttu-id="046b4-1093">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-1093">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<span data-ttu-id="046b4-1094">範例： iso-a4-彩色</span><span class="sxs-lookup"><span data-stu-id="046b4-1094">Example: iso-a4-colored</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1095">**參數**</span><span class="sxs-lookup"><span data-stu-id="046b4-1095">**Parameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-1096">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="046b4-1096">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1097">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="046b4-1097">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="046b4-1098">列印處理器的選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="046b4-1098">Optional parameters for the print processor.</span></span>

<span data-ttu-id="046b4-1099">範例： "副本 = 2"</span><span class="sxs-lookup"><span data-stu-id="046b4-1099">Example: "Copies=2"</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1100">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="046b4-1100">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-1101">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="046b4-1101">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1102">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-1102">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1103">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="046b4-1103">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-1104">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="046b4-1104">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="046b4-1105">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-1105">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="046b4-1106">範例： \* PNP030b</span><span class="sxs-lookup"><span data-stu-id="046b4-1106">Example: \*PNP030b</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1107">**PortName**</span><span class="sxs-lookup"><span data-stu-id="046b4-1107">**PortName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-1108">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="046b4-1108">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1109">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="046b4-1109">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="046b4-1110">用來將資料傳輸至印表機的埠。</span><span class="sxs-lookup"><span data-stu-id="046b4-1110">Port that is used to transmit data to a printer.</span></span> <span data-ttu-id="046b4-1111">如果印表機連線到一個以上的埠，每個埠的名稱會以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="046b4-1111">If a printer is connected to more than one port, the names of each port are separated by commas.</span></span>

<span data-ttu-id="046b4-1112">範例： LPT1：、LPT2：、LPT3：</span><span class="sxs-lookup"><span data-stu-id="046b4-1112">Example: LPT1:, LPT2:, LPT3:</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1113">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="046b4-1113">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-1114">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="046b4-1114">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-1115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="046b4-1116">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="046b4-1116">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="046b4-1117">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="046b4-1117">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="046b4-1118"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="046b4-1118"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="046b4-1119"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="046b4-1119"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="046b4-1120"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="046b4-1120"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="046b4-1121"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="046b4-1121"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-1122">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="046b4-1122">The power management features are currently enabled, but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="046b4-1123"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="046b4-1123"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-1124">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="046b4-1124">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="046b4-1125"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="046b4-1125"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-1126">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="046b4-1126">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="046b4-1127">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="046b4-1127">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="046b4-1128">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](../wmisdk/designing-managed-object-format--mof--classes.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-1128">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="046b4-1129"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="046b4-1129"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-1130">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="046b4-1130">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="046b4-1131"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="046b4-1131"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-1132">支援計時 Power-On</span><span class="sxs-lookup"><span data-stu-id="046b4-1132">Timed Power-On Supported</span></span>

<span data-ttu-id="046b4-1133">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="046b4-1133">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="046b4-1134">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="046b4-1134">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-1135">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="046b4-1135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-1136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="046b4-1137">若 **為 TRUE**，則可以管理裝置的電源，這表示它可以放入暫停模式。</span><span class="sxs-lookup"><span data-stu-id="046b4-1137">If **TRUE**, the power of the device can be managed, which means that it can be put into suspend mode.</span></span> <span data-ttu-id="046b4-1138">屬性不會指出電源管理功能是否已啟用，只有邏輯裝置能夠進行電源管理。</span><span class="sxs-lookup"><span data-stu-id="046b4-1138">The property does not indicate that power management features are enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="046b4-1139">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-1139">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1140">**PrinterPaperNames**</span><span class="sxs-lookup"><span data-stu-id="046b4-1140">**PrinterPaperNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-1141">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="046b4-1141">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-1142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="046b4-1143">印表機支援的紙張大小陣列。</span><span class="sxs-lookup"><span data-stu-id="046b4-1143">Array of paper sizes supported by the printer.</span></span> <span data-ttu-id="046b4-1144">印表機指定的名稱是用來表示支援的紙張大小。</span><span class="sxs-lookup"><span data-stu-id="046b4-1144">The printer-specified names are used to represent supported paper sizes.</span></span>

<span data-ttu-id="046b4-1145">範例： B5 (JIS) </span><span class="sxs-lookup"><span data-stu-id="046b4-1145">Example: B5 (JIS)</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1146">**PrinterState**</span><span class="sxs-lookup"><span data-stu-id="046b4-1146">**PrinterState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-1147">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="046b4-1147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-1148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1149">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="046b4-1149">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="046b4-1150">與此印表機相關的可能狀態之一。</span><span class="sxs-lookup"><span data-stu-id="046b4-1150">One of the possible states relating to this printer.</span></span> <span data-ttu-id="046b4-1151">這個屬性已經過時。</span><span class="sxs-lookup"><span data-stu-id="046b4-1151">This property is obsolete.</span></span> <span data-ttu-id="046b4-1152">若要取代這個屬性，請使用 **PrinterStatus**。</span><span class="sxs-lookup"><span data-stu-id="046b4-1152">In place of this property, use **PrinterStatus**.</span></span>

<dt>

<span data-ttu-id="046b4-1153">0</span><span class="sxs-lookup"><span data-stu-id="046b4-1153">0</span></span>
</dt> <dd>

<span data-ttu-id="046b4-1154">閒置-如需詳細資訊，請參閱下面的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="046b4-1154">Idle - for more information, see the Remarks section below.</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1155">1</span><span class="sxs-lookup"><span data-stu-id="046b4-1155">1</span></span>
</dt> <dd>

<span data-ttu-id="046b4-1156">已暫停</span><span class="sxs-lookup"><span data-stu-id="046b4-1156">Paused</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1157">2</span><span class="sxs-lookup"><span data-stu-id="046b4-1157">2</span></span>
</dt> <dd>

<span data-ttu-id="046b4-1158">錯誤</span><span class="sxs-lookup"><span data-stu-id="046b4-1158">Error</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1159">3</span><span class="sxs-lookup"><span data-stu-id="046b4-1159">3</span></span>
</dt> <dd>

<span data-ttu-id="046b4-1160">暫止刪除</span><span class="sxs-lookup"><span data-stu-id="046b4-1160">Pending Deletion</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1161">4</span><span class="sxs-lookup"><span data-stu-id="046b4-1161">4</span></span>
</dt> <dd>

<span data-ttu-id="046b4-1162">紙紙</span><span class="sxs-lookup"><span data-stu-id="046b4-1162">Paper Jam</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1163">5</span><span class="sxs-lookup"><span data-stu-id="046b4-1163">5</span></span>
</dt> <dd>

<span data-ttu-id="046b4-1164">論文</span><span class="sxs-lookup"><span data-stu-id="046b4-1164">Paper Out</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1165">6</span><span class="sxs-lookup"><span data-stu-id="046b4-1165">6</span></span>
</dt> <dd>

<span data-ttu-id="046b4-1166">手動送紙</span><span class="sxs-lookup"><span data-stu-id="046b4-1166">Manual Feed</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1167">7</span><span class="sxs-lookup"><span data-stu-id="046b4-1167">7</span></span>
</dt> <dd>

<span data-ttu-id="046b4-1168">紙張問題</span><span class="sxs-lookup"><span data-stu-id="046b4-1168">Paper Problem</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1169">8</span><span class="sxs-lookup"><span data-stu-id="046b4-1169">8</span></span>
</dt> <dd>

<span data-ttu-id="046b4-1170">離線</span><span class="sxs-lookup"><span data-stu-id="046b4-1170">Offline</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1171">9</span><span class="sxs-lookup"><span data-stu-id="046b4-1171">9</span></span>
</dt> <dd>

<span data-ttu-id="046b4-1172">I/o 主動</span><span class="sxs-lookup"><span data-stu-id="046b4-1172">I/O Active</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1173">10</span><span class="sxs-lookup"><span data-stu-id="046b4-1173">10</span></span>
</dt> <dd>

<span data-ttu-id="046b4-1174">忙碌</span><span class="sxs-lookup"><span data-stu-id="046b4-1174">Busy</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1175">11</span><span class="sxs-lookup"><span data-stu-id="046b4-1175">11</span></span>
</dt> <dd>

<span data-ttu-id="046b4-1176">列印</span><span class="sxs-lookup"><span data-stu-id="046b4-1176">Printing</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1177">12</span><span class="sxs-lookup"><span data-stu-id="046b4-1177">12</span></span>
</dt> <dd>

<span data-ttu-id="046b4-1178">輸出紙匣已滿</span><span class="sxs-lookup"><span data-stu-id="046b4-1178">Output Bin Full</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1179">13</span><span class="sxs-lookup"><span data-stu-id="046b4-1179">13</span></span>
</dt> <dd>

<span data-ttu-id="046b4-1180">無法使用</span><span class="sxs-lookup"><span data-stu-id="046b4-1180">Not Available</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1181">14</span><span class="sxs-lookup"><span data-stu-id="046b4-1181">14</span></span>
</dt> <dd>

<span data-ttu-id="046b4-1182">等候中</span><span class="sxs-lookup"><span data-stu-id="046b4-1182">Waiting</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1183">15</span><span class="sxs-lookup"><span data-stu-id="046b4-1183">15</span></span>
</dt> <dd>

<span data-ttu-id="046b4-1184">Processing</span><span class="sxs-lookup"><span data-stu-id="046b4-1184">Processing</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1185">16</span><span class="sxs-lookup"><span data-stu-id="046b4-1185">16</span></span>
</dt> <dd>

<span data-ttu-id="046b4-1186">初始化</span><span class="sxs-lookup"><span data-stu-id="046b4-1186">Initialization</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1187">17</span><span class="sxs-lookup"><span data-stu-id="046b4-1187">17</span></span>
</dt> <dd>

<span data-ttu-id="046b4-1188">正在準備</span><span class="sxs-lookup"><span data-stu-id="046b4-1188">Warming Up</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1189">18</span><span class="sxs-lookup"><span data-stu-id="046b4-1189">18</span></span>
</dt> <dd>

<span data-ttu-id="046b4-1190">碳粉不足</span><span class="sxs-lookup"><span data-stu-id="046b4-1190">Toner Low</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1191">19</span><span class="sxs-lookup"><span data-stu-id="046b4-1191">19</span></span>
</dt> <dd>

<span data-ttu-id="046b4-1192">碳粉用完</span><span class="sxs-lookup"><span data-stu-id="046b4-1192">No Toner</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1193">20</span><span class="sxs-lookup"><span data-stu-id="046b4-1193">20</span></span>
</dt> <dd>

<span data-ttu-id="046b4-1194">頁面</span><span class="sxs-lookup"><span data-stu-id="046b4-1194">Page Punt</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1195">21</span><span class="sxs-lookup"><span data-stu-id="046b4-1195">21</span></span>
</dt> <dd>

<span data-ttu-id="046b4-1196">需要使用者介入</span><span class="sxs-lookup"><span data-stu-id="046b4-1196">User Intervention Required</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1197">22</span><span class="sxs-lookup"><span data-stu-id="046b4-1197">22</span></span>
</dt> <dd>

<span data-ttu-id="046b4-1198">記憶體不足</span><span class="sxs-lookup"><span data-stu-id="046b4-1198">Out of Memory</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1199">23</span><span class="sxs-lookup"><span data-stu-id="046b4-1199">23</span></span>
</dt> <dd>

<span data-ttu-id="046b4-1200">機門開啟</span><span class="sxs-lookup"><span data-stu-id="046b4-1200">Door Open</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1201">24</span><span class="sxs-lookup"><span data-stu-id="046b4-1201">24</span></span>
</dt> <dd>

<span data-ttu-id="046b4-1202">伺服器 \_ 不明</span><span class="sxs-lookup"><span data-stu-id="046b4-1202">Server\_Unknown</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1203">25</span><span class="sxs-lookup"><span data-stu-id="046b4-1203">25</span></span>
</dt> <dd>

<span data-ttu-id="046b4-1204">省電</span><span class="sxs-lookup"><span data-stu-id="046b4-1204">Power Save</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="046b4-1205">**PrinterStatus**</span><span class="sxs-lookup"><span data-stu-id="046b4-1205">**PrinterStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-1206">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="046b4-1206">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1207">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-1207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1208">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIB。IETF \| 印表機-hrPrinterStatus ") </span><span class="sxs-lookup"><span data-stu-id="046b4-1208">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.hrPrinterStatus")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-1209">印表機的狀態資訊，與 [邏輯裝置 **可用性** ] 屬性中指定的資訊不同。</span><span class="sxs-lookup"><span data-stu-id="046b4-1209">Status information for a printer that is different from information specified in the logical device **Availability** property.</span></span>

<span data-ttu-id="046b4-1210">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-1210">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="046b4-1211"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="046b4-1211"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="046b4-1212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="046b4-1212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span data-ttu-id="046b4-1213"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**閒置** (3) </span><span class="sxs-lookup"><span data-stu-id="046b4-1213"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Idle** (3)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-1214">閒置-如需詳細資訊，請參閱下面的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="046b4-1214">Idle - for more information, see the Remarks section below.</span></span>

</dd> <dt>

<span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>

<span data-ttu-id="046b4-1215"><span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>**列印** (4) </span><span class="sxs-lookup"><span data-stu-id="046b4-1215"><span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>**Printing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>

<span data-ttu-id="046b4-1216"><span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>**預熱** (5) </span><span class="sxs-lookup"><span data-stu-id="046b4-1216"><span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>**Warmup** (5)</span></span>


</dt> <dd>

<span data-ttu-id="046b4-1217">正在準備</span><span class="sxs-lookup"><span data-stu-id="046b4-1217">Warming Up</span></span>

</dd> <dt>

<span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>

<span data-ttu-id="046b4-1218"><span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>**已停止列印** (6) </span><span class="sxs-lookup"><span data-stu-id="046b4-1218"><span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>**Stopped Printing** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="046b4-1219"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**離線** (7) </span><span class="sxs-lookup"><span data-stu-id="046b4-1219"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="046b4-1220">**PrintJobDataType**</span><span class="sxs-lookup"><span data-stu-id="046b4-1220">**PrintJobDataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-1221">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="046b4-1221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1222">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="046b4-1222">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="046b4-1223">等候 Windows 列印裝置之列印工作的資料類型。</span><span class="sxs-lookup"><span data-stu-id="046b4-1223">Data type of a print job waiting for the Windows-based printing device.</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1224">**PrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="046b4-1224">**PrintProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-1225">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="046b4-1225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1226">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="046b4-1226">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="046b4-1227">處理列印工作的列印多工緩衝處理器名稱。</span><span class="sxs-lookup"><span data-stu-id="046b4-1227">Name of the print spooler that handles print jobs.</span></span>

<span data-ttu-id="046b4-1228">範例： SPOOLSS.DLL</span><span class="sxs-lookup"><span data-stu-id="046b4-1228">Example: SPOOLSS.DLL</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1229">**優先順序**</span><span class="sxs-lookup"><span data-stu-id="046b4-1229">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-1230">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="046b4-1230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1231">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="046b4-1231">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="046b4-1232">印表機的優先順序。</span><span class="sxs-lookup"><span data-stu-id="046b4-1232">Priority of the printer.</span></span> <span data-ttu-id="046b4-1233">較高優先順序的印表機上的工作會先排程。</span><span class="sxs-lookup"><span data-stu-id="046b4-1233">Jobs on a higher priority printer are scheduled first.</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1234">**已發行**</span><span class="sxs-lookup"><span data-stu-id="046b4-1234">**Published**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-1235">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="046b4-1235">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1236">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="046b4-1236">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="046b4-1237">若 **為 TRUE**，則會在網路目錄服務中發佈印表機。</span><span class="sxs-lookup"><span data-stu-id="046b4-1237">If **TRUE**, the printer is published in the network directory service.</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1238">**已排入佇列**</span><span class="sxs-lookup"><span data-stu-id="046b4-1238">**Queued**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-1239">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="046b4-1239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1240">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="046b4-1240">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="046b4-1241">若 **為 TRUE**，則印表機會緩衝並將列印工作排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="046b4-1241">If **TRUE**, the printer buffers and queues print jobs.</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1242">**RawOnly**</span><span class="sxs-lookup"><span data-stu-id="046b4-1242">**RawOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-1243">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="046b4-1243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1244">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="046b4-1244">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="046b4-1245">若 **為 TRUE**，則印表機只接受要進行多工緩衝處理的原始資料。</span><span class="sxs-lookup"><span data-stu-id="046b4-1245">If **TRUE**, the printer accepts only raw data to be spooled.</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1246">**SeparatorFile**</span><span class="sxs-lookup"><span data-stu-id="046b4-1246">**SeparatorFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-1247">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="046b4-1247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1248">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="046b4-1248">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="046b4-1249">用來建立分隔符號頁面的檔案名。</span><span class="sxs-lookup"><span data-stu-id="046b4-1249">Name of the file used to create a separator page.</span></span> <span data-ttu-id="046b4-1250">此頁面是用來分隔傳送至印表機的列印工作。</span><span class="sxs-lookup"><span data-stu-id="046b4-1250">This page is used to separate print jobs sent to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1251">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="046b4-1251">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-1252">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="046b4-1252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1253">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-1253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="046b4-1254">控制印表機的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="046b4-1254">Name of the server that controls the printer.</span></span> <span data-ttu-id="046b4-1255">如果這個字串是 **Null**，則會在本機控制印表機。</span><span class="sxs-lookup"><span data-stu-id="046b4-1255">If this string is **NULL**, the printer is controlled locally.</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1256">[共用]</span><span class="sxs-lookup"><span data-stu-id="046b4-1256">**Shared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-1257">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="046b4-1257">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1258">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="046b4-1258">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="046b4-1259">若為 **TRUE**，則會將印表機作為共用網路資源提供。</span><span class="sxs-lookup"><span data-stu-id="046b4-1259">If **TRUE**, the printer is available as a shared network resource.</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1260">**共用**</span><span class="sxs-lookup"><span data-stu-id="046b4-1260">**ShareName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-1261">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="046b4-1261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1262">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="046b4-1262">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="046b4-1263">以 Windows 為基礎的列印裝置的共用名稱。</span><span class="sxs-lookup"><span data-stu-id="046b4-1263">Share name of the Windows-based printing device.</span></span>

<span data-ttu-id="046b4-1264">範例： " \\ \\ PRINTSERVER1 \\ PRINTER2"</span><span class="sxs-lookup"><span data-stu-id="046b4-1264">Example: "\\\\PRINTSERVER1\\PRINTER2"</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1265">**SpoolEnabled**</span><span class="sxs-lookup"><span data-stu-id="046b4-1265">**SpoolEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-1266">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="046b4-1266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1267">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-1267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1268">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="046b4-1268">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="046b4-1269">這個屬性已過時;請勿使用。</span><span class="sxs-lookup"><span data-stu-id="046b4-1269">This property is obsolete; do not use.</span></span> <span data-ttu-id="046b4-1270">若為 **TRUE**，則會啟用印表機的多工緩衝處理。</span><span class="sxs-lookup"><span data-stu-id="046b4-1270">If **TRUE**, spooling is enabled for printer.</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1271">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="046b4-1271">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-1272">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="046b4-1272">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1273">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="046b4-1273">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="046b4-1274">印表機可以開始列印工作的日期和時間—如果印表機受限於在特定時間列印。</span><span class="sxs-lookup"><span data-stu-id="046b4-1274">Date and time that a printer can start to print a job—if the printer is limited to print at specific times.</span></span> <span data-ttu-id="046b4-1275">此值會表示自 12:00 AM GMT 起的經過時間， (格林尼治平均時間) 。</span><span class="sxs-lookup"><span data-stu-id="046b4-1275">This value is expressed as the time elapsed since 12:00 AM GMT (Greenwich Mean Time).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1276">**狀態**</span><span class="sxs-lookup"><span data-stu-id="046b4-1276">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-1277">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="046b4-1277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1278">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-1278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1279">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="046b4-1279">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-1280">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="046b4-1280">Current status of the object.</span></span> <span data-ttu-id="046b4-1281">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="046b4-1281">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="046b4-1282">作業狀態包括： **[確定]、[\*\*\*\*降級**] 和 [ **Pred** ] (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="046b4-1282">Operational statuses include: **OK**, **Degraded**, and **Pred Fail** (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="046b4-1283">Nonoperational 狀態包括： **錯誤**、 **啟動**、 **停止** 及 **服務**。</span><span class="sxs-lookup"><span data-stu-id="046b4-1283">Nonoperational statuses include: **Error**, **Starting**, **Stopping**, and **Service**.</span></span> <span data-ttu-id="046b4-1284">後者可能會在磁片的鏡像重新同步處理期間 **套用，而** 重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="046b4-1284">The latter, **Service**, could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="046b4-1285">並非所有這類工作都在線上，但是受控元素並不是 **正常** 的，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="046b4-1285">Not all such work is online, yet the managed element is neither **OK** nor in one of the other states.</span></span>

<span data-ttu-id="046b4-1286">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-1286">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="046b4-1287">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="046b4-1287">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="046b4-1288">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="046b4-1288">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="046b4-1289">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="046b4-1289">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="046b4-1290">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="046b4-1290">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="046b4-1291">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="046b4-1291">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="046b4-1292">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="046b4-1292">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="046b4-1293">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="046b4-1293">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="046b4-1294">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="046b4-1294">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="046b4-1295">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="046b4-1295">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="046b4-1296">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="046b4-1296">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="046b4-1297">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="046b4-1297">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="046b4-1298">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="046b4-1298">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="046b4-1299">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="046b4-1299">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="046b4-1300">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="046b4-1300">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-1301">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="046b4-1301">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1302">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-1302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1303">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="046b4-1303">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-1304">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="046b4-1304">State of the logical device.</span></span> <span data-ttu-id="046b4-1305">如果此屬性不適用於邏輯裝置，則應該使用值 5 (**不適用**) 。</span><span class="sxs-lookup"><span data-stu-id="046b4-1305">If this property does not apply to the logical device, the value 5 (**Not Applicable**) should be used.</span></span>

<span data-ttu-id="046b4-1306">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-1306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="046b4-1307">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="046b4-1307">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="046b4-1308">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="046b4-1308">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="046b4-1309">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="046b4-1309">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="046b4-1310">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="046b4-1310">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="046b4-1311">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="046b4-1311">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="046b4-1312">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="046b4-1312">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-1313">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="046b4-1313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1314">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-1314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1315">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="046b4-1315">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="046b4-1316">範圍電腦之 **CreationClassName** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="046b4-1316">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="046b4-1317">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-1317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1318">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="046b4-1318">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-1319">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="046b4-1319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1320">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-1320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1321">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="046b4-1321">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="046b4-1322">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="046b4-1322">Name of the scoping system.</span></span>

<span data-ttu-id="046b4-1323">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-1323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1324">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="046b4-1324">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-1325">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="046b4-1325">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1326">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-1326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="046b4-1327">上次重設印表機的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="046b4-1327">Date and time the printer was last reset.</span></span>

<span data-ttu-id="046b4-1328">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-1328">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1329">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="046b4-1329">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-1330">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="046b4-1330">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1331">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="046b4-1331">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="046b4-1332">印表機可以列印最後一個工作的日期和時間—如果印表機受限於在特定時間列印。</span><span class="sxs-lookup"><span data-stu-id="046b4-1332">Date and time that a printer can print the last job—if the printer is limited to print at specific times.</span></span> <span data-ttu-id="046b4-1333">此值會表示自 12:00 AM GMT 起的經過時間， (格林尼治平均時間) 。</span><span class="sxs-lookup"><span data-stu-id="046b4-1333">This value is expressed as the time elapsed since 12:00 AM GMT (Greenwich Mean Time).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1334">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="046b4-1334">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-1335">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="046b4-1335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1336">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="046b4-1336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1337">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "CIM \_ PrintJob. HorizontalResolution" ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( "圖元/英寸" ) </span><span class="sxs-lookup"><span data-stu-id="046b4-1337">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.HorizontalResolution"), [**Units**](../wmisdk/standard-qualifiers.md) ("pixels per inch")</span></span>
</dt> </dl>

<span data-ttu-id="046b4-1338">印表機的垂直解析度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="046b4-1338">Vertical resolution, in pixels-per-inch, of the printer.</span></span>

<span data-ttu-id="046b4-1339">這個屬性繼承自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-1339">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="046b4-1340">**WorkOffline**</span><span class="sxs-lookup"><span data-stu-id="046b4-1340">**WorkOffline**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="046b4-1341">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="046b4-1341">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="046b4-1342">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="046b4-1342">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="046b4-1343">若 **為 TRUE**，您可以在印表機離線時，將電腦上的列印工作排入佇列。</span><span class="sxs-lookup"><span data-stu-id="046b4-1343">If **TRUE**, you can queue print jobs on the computer when the printer is offline.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="046b4-1344">備註</span><span class="sxs-lookup"><span data-stu-id="046b4-1344">Remarks</span></span>

<span data-ttu-id="046b4-1345">**Win32 \_ 印表機** 類別衍生自 [**CIM \_ 印表機**](cim-printer.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-1345">The **Win32\_Printer** class is derived from [**CIM\_Printer**](cim-printer.md).</span></span> <span data-ttu-id="046b4-1346">針對 **Win32 \_ 印表機** 實例呼叫 [**SWbemObject \_ . Put**](../wmisdk/swbemobject-put-.md)或 [**IWbemServices：:P utinstance**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstance)之前，必須啟用 Visual Basic 和) LoadDriver 的 **SeLoadDriverPrivilege** 許可權 (**wbemPrivilegeLoadDriver** 。</span><span class="sxs-lookup"><span data-stu-id="046b4-1346">Before calling [**SWbemObject.Put\_**](../wmisdk/swbemobject-put-.md) or [**IWbemServices::PutInstance**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstance) for a **Win32\_Printer** instance, the **SeLoadDriverPrivilege** privilege (**wbemPrivilegeLoadDriver** for Visual Basic and LoadDriver for scripting monikers) must be enabled.</span></span> <span data-ttu-id="046b4-1347">如需詳細資訊，請參閱 [**許可權常數**](../wmisdk/privilege-constants.md) 和 [執行特殊許可權作業](../wmisdk/executing-privileged-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="046b4-1347">For more information, see [**Privilege Constants**](../wmisdk/privilege-constants.md) and [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span> <span data-ttu-id="046b4-1348">下列 VBScript 程式碼範例顯示如何在腳本中啟用 **SetLoadDriverPrivilege** 許可權。</span><span class="sxs-lookup"><span data-stu-id="046b4-1348">The following VBScript code example shows how to enable the **SetLoadDriverPrivilege** privilege in script.</span></span>

<span data-ttu-id="046b4-1349">如需使用 MSCS 印表機叢集，請使用 prnadmin.dll 元件，或 .NET Framework 的 [System. 列印](/dotnet/api/system.printing) 命名空間。</span><span class="sxs-lookup"><span data-stu-id="046b4-1349">For working with MSCS Printer clusters, use the prnadmin.dll assembly, or else the .NET Framework [System.Printing](/dotnet/api/system.printing) namespace.</span></span>


```VB
Set objPrinter = GetObject("winmgmts:{impersonationLevel=Impersonate,(LoadDriver)}!//./Root/CIMv2:Win32_Printer")
```



<span data-ttu-id="046b4-1350">Windows 使用執行腳本之使用者的認證來判斷可用的印表機。</span><span class="sxs-lookup"><span data-stu-id="046b4-1350">Windows uses the credentials of the user running the script to determine what the available printers are.</span></span> <span data-ttu-id="046b4-1351">因此，如果您是從遠端執行腳本，您只能存取該遠端系統上您的使用者帳戶所能使用的任何印表機。</span><span class="sxs-lookup"><span data-stu-id="046b4-1351">Therefore, if you are running a script remotely, you may only be able to access any printer that is available to your user account on that remote system.</span></span>

<span data-ttu-id="046b4-1352">您無法針對 MSCS 列印叢集上的印表機使用 **Win32 \_ 印表機** 類別。</span><span class="sxs-lookup"><span data-stu-id="046b4-1352">You cannot use the **Win32\_Printer** class for printers on an MSCS print cluster.</span></span> <span data-ttu-id="046b4-1353">相反地，您可能需要使用 PrinterAdmin 工具 (PrnAdmin.dll) 或 .NET Framework [System. 列印](/dotnet/api/system.printing) 命名空間。</span><span class="sxs-lookup"><span data-stu-id="046b4-1353">Instead, you may need to use either the PrinterAdmin tool (PrnAdmin.dll) or the .NET Framework [System.Printing](/dotnet/api/system.printing) namespace.</span></span>

> [!Note]  
> <span data-ttu-id="046b4-1354">如果您要抓取 **PrinterStatus** = 3 或 **PrinterState** = 0，印表機驅動程式可能無法將正確的資訊饋送至 WMI。</span><span class="sxs-lookup"><span data-stu-id="046b4-1354">If you are retrieving **PrinterStatus** = 3 or **PrinterState** = 0, the printer driver may not be feeding accurate information into WMI.</span></span> <span data-ttu-id="046b4-1355">WMI 會從 spoolsv.exe 進程抓取印表機資訊。</span><span class="sxs-lookup"><span data-stu-id="046b4-1355">WMI retrieves the printer information from the spoolsv.exe process.</span></span> <span data-ttu-id="046b4-1356">印表機驅動程式可能不會將其狀態報表給多工緩衝處理器。</span><span class="sxs-lookup"><span data-stu-id="046b4-1356">It is possible the printer driver does not report its status to the spooler.</span></span> <span data-ttu-id="046b4-1357">在此情況下， **Win32 \_ 印表機** 會將印表機報告為 **閒置**。</span><span class="sxs-lookup"><span data-stu-id="046b4-1357">In this case, **Win32\_Printer** reports the printer as **Idle**.</span></span>

 

## <a name="examples"></a><span data-ttu-id="046b4-1358">範例</span><span class="sxs-lookup"><span data-stu-id="046b4-1358">Examples</span></span>

<span data-ttu-id="046b4-1359">PS 在 TechNet 資源庫上 [使用 visio PowerShell 範例建立電腦設定繪圖](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) 使用 **Win32 \_ 印表機** 與 visio automation 模型互動，以建立 visio 繪圖。</span><span class="sxs-lookup"><span data-stu-id="046b4-1359">The [PS Create a Computer Configuration Drawing using Visio](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) PowerShell sample on TechNet Gallery uses **Win32\_Printer** to interact with Visio automation model to create a Visio drawing.</span></span>

<span data-ttu-id="046b4-1360">[Powershell 遠端電腦資訊腳本](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436)會使用許多類別（包括 **Win32 \_ 印表機**）來取得遠端電腦的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="046b4-1360">The [Powershell Remote PC Info Script](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436) uses a number of classes, including **Win32\_Printer**, to retrieve information about a remote computer.</span></span>

<span data-ttu-id="046b4-1361">下列 PowerShell 程式碼範例顯示如何判斷本機電腦的預設印表機。</span><span class="sxs-lookup"><span data-stu-id="046b4-1361">The following PowerShell code sample shows how to determine the default printer of the local computer.</span></span>


```PowerShell
Get-WmiObject win32_printer | %{if ($_.default) {$_}}
```



<span data-ttu-id="046b4-1362">下列 VBScript 程式碼範例說明如何從 **Win32 \_ 印表機** 的實例取出印表機統計資料。</span><span class="sxs-lookup"><span data-stu-id="046b4-1362">The following VBScript code sample describes how to retrieve printer stats from instances of **Win32\_Printer**.</span></span>


```VB
Set PrinterSet = GetObject("winmgmts:").InstancesOf ("Win32_Printer")
If (PrinterSet.Count = 0 ) Then WScript.Echo "No Printers Installed!"
for each Printer in PrinterSet
   if Printer.PrinterStatus = 3 then WScript.Echo Printer.Name & Chr(13) & "Status:  Idle"
   if Printer.PrinterStatus = 4 then WScript.Echo Printer.Name & Chr(13) & "Status:  Printing"
   
next
```



<span data-ttu-id="046b4-1363">下列 Perl 程式碼範例說明如何從 **Win32 \_ 印表機** 的實例取出印表機統計資料。</span><span class="sxs-lookup"><span data-stu-id="046b4-1363">The following Perl code sample describes how to retrieve printer stats from instances of **Win32\_Printer**.</span></span>


```
use strict;
use Win32::OLE;

my $PrinterSet;

eval { $PrinterSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
   InstancesOf ("Win32_Printer"); };
unless($@)
{
   if ($PrinterSet->{Count} == 0) 
   {
      print "No Printers Installed!\n";
   }

   foreach my $PrinterInst (in $PrinterSet)
   {
      if ($PrinterInst->{PrinterStatus} == 3) 
      {
         print "\n$PrinterInst->{Name}\nStatus:  Idle\n";
      }
      if ($PrinterInst->{PrinterStatus} == 4) 
      {
         print "\n$PrinterInst->{Name}\nStatus:  Printing\n";
      }
   }
}
else
{
   print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="046b4-1364">下列 VBScript 程式碼範例顯示如何取得電腦預設印表機的名稱。</span><span class="sxs-lookup"><span data-stu-id="046b4-1364">The following VBScript code example shows how to obtain the name of the default printer for a computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject( "winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colInstalledPrinters =  objWMIService.ExecQuery ("Select * from Win32_Printer")
For Each objPrinter in colInstalledPrinters

    If objPrinter.Default = "True" Then 
      Wscript.Echo "Name: " & objPrinter.Name
    End If
Next
```



## <a name="requirements"></a><span data-ttu-id="046b4-1365">規格需求</span><span class="sxs-lookup"><span data-stu-id="046b4-1365">Requirements</span></span>



| <span data-ttu-id="046b4-1366">需求</span><span class="sxs-lookup"><span data-stu-id="046b4-1366">Requirement</span></span> | <span data-ttu-id="046b4-1367">值</span><span class="sxs-lookup"><span data-stu-id="046b4-1367">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="046b4-1368">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="046b4-1368">Minimum supported client</span></span><br/> | <span data-ttu-id="046b4-1369">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="046b4-1369">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="046b4-1370">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="046b4-1370">Minimum supported server</span></span><br/> | <span data-ttu-id="046b4-1371">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="046b4-1371">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="046b4-1372">命名空間</span><span class="sxs-lookup"><span data-stu-id="046b4-1372">Namespace</span></span><br/>                | <span data-ttu-id="046b4-1373">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="046b4-1373">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="046b4-1374">MOF</span><span class="sxs-lookup"><span data-stu-id="046b4-1374">MOF</span></span><br/>                      | <dl> <span data-ttu-id="046b4-1375"><dt>Win32 \_ 印表機。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="046b4-1375"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="046b4-1376">DLL</span><span class="sxs-lookup"><span data-stu-id="046b4-1376">DLL</span></span><br/>                      | <dl> <span data-ttu-id="046b4-1377"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="046b4-1377"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="046b4-1378">另請參閱</span><span class="sxs-lookup"><span data-stu-id="046b4-1378">See also</span></span>

<dl> <dt>

[<span data-ttu-id="046b4-1379">**CIM \_ 印表機**</span><span class="sxs-lookup"><span data-stu-id="046b4-1379">**CIM\_Printer**</span></span>](cim-printer.md)
</dt> <dt>

[<span data-ttu-id="046b4-1380">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="046b4-1380">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="046b4-1381">WMI 工作：印表機和列印</span><span class="sxs-lookup"><span data-stu-id="046b4-1381">WMI Tasks: Printers and Printing</span></span>](../wmisdk/wmi-tasks--printers-and-printing.md)
</dt> </dl>

 

 
