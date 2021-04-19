---
description: 不再支援 WMI 記錄檔。
ms.assetid: 4ba80063-7aa6-42df-a620-1b366b795034
ms.tgt_platform: multiple
title: 記錄 WMI 活動
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ced8645eb7ad9005e6ba751d011ae7f0ccb3dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978230"
---
# <a name="logging-wmi-activity"></a><span data-ttu-id="c8d00-103">記錄 WMI 活動</span><span class="sxs-lookup"><span data-stu-id="c8d00-103">Logging WMI Activity</span></span>

<span data-ttu-id="c8d00-104">不再支援 WMI 記錄檔。</span><span class="sxs-lookup"><span data-stu-id="c8d00-104">The WMI log files are no longer supported.</span></span> <span data-ttu-id="c8d00-105">從 Windows Vista 開始，WMI 會使用 [windows 的事件追蹤 (ETW](/windows/desktop/ETW/event-tracing-portal)) 以及透過 **事件檢視器** UI 或 Wevtutil 命令列工具提供的事件。</span><span class="sxs-lookup"><span data-stu-id="c8d00-105">Starting with Windows Vista, WMI uses [Event Tracing for Windows (ETW](/windows/desktop/ETW/event-tracing-portal)) and events that are available through the **Event Viewer** UI or the Wevtutil command line tool.</span></span> <span data-ttu-id="c8d00-106">如需詳細資訊，請參閱 ETW 提供者和 [Wevutil](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732848(v=ws.11)) 命令列檔。</span><span class="sxs-lookup"><span data-stu-id="c8d00-106">For more information, see the ETW provider and the [Wevutil](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732848(v=ws.11)) command-line documentation.</span></span>

<span data-ttu-id="c8d00-107">本主題將討論下列各節：</span><span class="sxs-lookup"><span data-stu-id="c8d00-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="c8d00-108">Windows Vista 之前的 WMI 記錄檔</span><span class="sxs-lookup"><span data-stu-id="c8d00-108">WMI Log Files Before Windows Vista</span></span>](#wmi-log-files-before-windows-vista)
-   [<span data-ttu-id="c8d00-109">Windows Vista 之前的 WMI 核心元件記錄活動</span><span class="sxs-lookup"><span data-stu-id="c8d00-109">Logging Activities for WMI Core Components Before Windows Vista</span></span>](#logging-activities-for-wmi-core-components-before-windows-vista)
-   [<span data-ttu-id="c8d00-110">Windows Vista 之前的 WMI 提供者元件記錄活動</span><span class="sxs-lookup"><span data-stu-id="c8d00-110">Logging Activities for WMI Provider Components Before Windows Vista</span></span>](#logging-activities-for-wmi-provider-components-before-windows-vista)
-   [<span data-ttu-id="c8d00-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="c8d00-111">Related topics</span></span>](#related-topics)

## <a name="wmi-log-files-before-windows-vista"></a><span data-ttu-id="c8d00-112">Windows Vista 之前的 WMI 記錄檔</span><span class="sxs-lookup"><span data-stu-id="c8d00-112">WMI Log Files Before Windows Vista</span></span>

<span data-ttu-id="c8d00-113">WMI 和各種提供者所建立的記錄檔會記錄：事件、追蹤或診斷資料、錯誤和各種活動。</span><span class="sxs-lookup"><span data-stu-id="c8d00-113">The log files created by WMI and various providers record: events, trace or diagnostic data, errors, and various activities.</span></span> <span data-ttu-id="c8d00-114">只有系統管理員才具有在% windir% \\ system32 wbem 記錄檔中找到之 WMI 記錄檔資料夾的讀取權限 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="c8d00-114">Only administrators have read access to the WMI log folder found at %windir%\\system32\\wbem\\logs.</span></span>

<span data-ttu-id="c8d00-115">只有 WMI 核心元件或 WMI 提供者會寫入記錄檔。</span><span class="sxs-lookup"><span data-stu-id="c8d00-115">Only WMI core components or WMI providers write to log files.</span></span> <span data-ttu-id="c8d00-116">您只能讀取或查看這些記錄檔中的資料，以供診斷之用。</span><span class="sxs-lookup"><span data-stu-id="c8d00-116">You can only read or view the data in these logs for diagnostic purposes.</span></span> <span data-ttu-id="c8d00-117">您可以在 WMI 記錄檔目錄中建立並儲存自己的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="c8d00-117">You can create and store your own log files in the WMI log directory.</span></span>

## <a name="logging-activities-for-wmi-core-components-before-windows-vista"></a><span data-ttu-id="c8d00-118">Windows Vista 之前的 WMI 核心元件記錄活動</span><span class="sxs-lookup"><span data-stu-id="c8d00-118">Logging Activities for WMI Core Components Before Windows Vista</span></span>

<span data-ttu-id="c8d00-119">這些檔案不包含適合以程式設計方式讀取的一致格式。</span><span class="sxs-lookup"><span data-stu-id="c8d00-119">These files do not contain a consistent format that is suitable for reading programmatically.</span></span> <span data-ttu-id="c8d00-120">如需特定記錄檔的詳細資訊，請參閱 [WMI 記錄](wmi-log-files.md)檔。</span><span class="sxs-lookup"><span data-stu-id="c8d00-120">For more information about specific logs, see [WMI Log Files](wmi-log-files.md).</span></span>

<span data-ttu-id="c8d00-121">設定下列登錄機碼時，會發生 WMI 核心元件的記錄活動：</span><span class="sxs-lookup"><span data-stu-id="c8d00-121">Logging activities for WMI core components occurs when the following registry keys are set:</span></span>

-   <span data-ttu-id="c8d00-122">記錄層級</span><span class="sxs-lookup"><span data-stu-id="c8d00-122">Logging level</span></span>

    <span data-ttu-id="c8d00-123">記錄層級登錄值的變更會立即生效。</span><span class="sxs-lookup"><span data-stu-id="c8d00-123">Changes to the logging level registry value take effect immediately.</span></span> <span data-ttu-id="c8d00-124">不需要重新開機 WMI 服務。</span><span class="sxs-lookup"><span data-stu-id="c8d00-124">No restart of the WMI service is necessary.</span></span>

    <span data-ttu-id="c8d00-125">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **記錄**= 2</span><span class="sxs-lookup"><span data-stu-id="c8d00-125">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**Logging** = 2</span></span>

    <span data-ttu-id="c8d00-126">下列清單列出可在登錄中定義的記錄層級。</span><span class="sxs-lookup"><span data-stu-id="c8d00-126">The following list lists the logging levels that can be defined in the registry.</span></span>

    

    | <span data-ttu-id="c8d00-127">記錄層級</span><span class="sxs-lookup"><span data-stu-id="c8d00-127">Logging level</span></span> | <span data-ttu-id="c8d00-128">描述</span><span class="sxs-lookup"><span data-stu-id="c8d00-128">Description</span></span>               |
    |---------------|---------------------------|
    | <span data-ttu-id="c8d00-129">0</span><span class="sxs-lookup"><span data-stu-id="c8d00-129">0</span></span>             | <span data-ttu-id="c8d00-130">無記錄</span><span class="sxs-lookup"><span data-stu-id="c8d00-130">No Logging</span></span>                |
    | <span data-ttu-id="c8d00-131">1</span><span class="sxs-lookup"><span data-stu-id="c8d00-131">1</span></span>             | <span data-ttu-id="c8d00-132">只記錄錯誤</span><span class="sxs-lookup"><span data-stu-id="c8d00-132">Log only errors</span></span>           |
    | <span data-ttu-id="c8d00-133">2</span><span class="sxs-lookup"><span data-stu-id="c8d00-133">2</span></span>             | <span data-ttu-id="c8d00-134">詳細資訊記錄 (預設) </span><span class="sxs-lookup"><span data-stu-id="c8d00-134">Verbose Logging (default)</span></span> |

    

     

-   <span data-ttu-id="c8d00-135">記錄檔位置</span><span class="sxs-lookup"><span data-stu-id="c8d00-135">Log file location</span></span>

    <span data-ttu-id="c8d00-136">若要讓記錄檔位置的變更生效，請重新開機 WMI 服務。</span><span class="sxs-lookup"><span data-stu-id="c8d00-136">For changes to log file location to take effect, restart the WMI service.</span></span>

    <span data-ttu-id="c8d00-137">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **記錄目錄**=% windir% \\ system32 \\ WBEM \\ 記錄</span><span class="sxs-lookup"><span data-stu-id="c8d00-137">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**Logging Directory** = %windir%\\system32\\wbem\\logs</span></span>

-   <span data-ttu-id="c8d00-138">記錄檔大小上限（以位元組為單位）</span><span class="sxs-lookup"><span data-stu-id="c8d00-138">Maximum log file size, in bytes</span></span>

    <span data-ttu-id="c8d00-139">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **記錄檔大小上限**= 65536</span><span class="sxs-lookup"><span data-stu-id="c8d00-139">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**Log File Max Size** = 65536</span></span>

<span data-ttu-id="c8d00-140">您可以透過登錄編輯程式或 Microsoft Management Console 的 WMI 嵌入式管理單元來變更這些登錄機碼值。</span><span class="sxs-lookup"><span data-stu-id="c8d00-140">You can change these registry key values through the Registry Editor or through the WMI snap-in for the Microsoft Management Console.</span></span>

<span data-ttu-id="c8d00-141">**在 Windows Vista 之前設定 WMI 的記錄層級**</span><span class="sxs-lookup"><span data-stu-id="c8d00-141">**To set the logging level for WMI before Windows Vista**</span></span>

1.  <span data-ttu-id="c8d00-142">按一下 **[開始]** ，然後按一下 **[執行]** 。</span><span class="sxs-lookup"><span data-stu-id="c8d00-142">Click **Start**, and then click **Run**.</span></span>
2.  <span data-ttu-id="c8d00-143">輸入 **wmimgmt.msc services.msc**</span><span class="sxs-lookup"><span data-stu-id="c8d00-143">Type **wmimgmt.msc**</span></span>
3.  <span data-ttu-id="c8d00-144">在 [動作] 功能表上，按一下 [內容]。</span><span class="sxs-lookup"><span data-stu-id="c8d00-144">On the **Action** menu, click **Properties**.</span></span>
4.  <span data-ttu-id="c8d00-145">在 [ **記錄** ] 索引標籤上，將記錄層級設定為 **停用**、 **已啟用** 或 **詳細** 資訊。</span><span class="sxs-lookup"><span data-stu-id="c8d00-145">On the **Logging** tab, set the logging level to **Disabled**, **Enabled**, or **Verbose**.</span></span>
5.  <span data-ttu-id="c8d00-146">在 [ **位置：**] 中，輸入記錄檔資料夾的路徑，並以 **大小上限 (位元組) ：**，設定記錄檔的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c8d00-146">In **Location:**, type the path to the log file folder and in **Maximum size (bytes):**, set the maximum size, in bytes, of the log file.</span></span>

<span data-ttu-id="c8d00-147">如需有關設定記錄檔屬性的詳細資訊，請參閱 WMI 控制應用程式的線上說明。</span><span class="sxs-lookup"><span data-stu-id="c8d00-147">For more information about setting the log file properties, see the online Help for the WMI Control application.</span></span>

## <a name="logging-activities-for-wmi-provider-components-before-windows-vista"></a><span data-ttu-id="c8d00-148">Windows Vista 之前的 WMI 提供者元件記錄活動</span><span class="sxs-lookup"><span data-stu-id="c8d00-148">Logging Activities for WMI Provider Components Before Windows Vista</span></span>

<span data-ttu-id="c8d00-149">啟用 WMI 核心元件的記錄時，也會針對具有記錄功能的任何提供者啟用記錄。</span><span class="sxs-lookup"><span data-stu-id="c8d00-149">When logging for WMI core components is enabled, logging is also enabled for any provider with logging capabilities.</span></span>

<span data-ttu-id="c8d00-150">下列清單列出必要的值。</span><span class="sxs-lookup"><span data-stu-id="c8d00-150">The following list lists the required values.</span></span>

<dl> <dt>

<span data-ttu-id="c8d00-151"><span id="File"></span><span id="file"></span><span id="FILE"></span>**檔**</span><span class="sxs-lookup"><span data-stu-id="c8d00-151"><span id="File"></span><span id="file"></span><span id="FILE"></span>**File**</span></span>
</dt> <dd>

<span data-ttu-id="c8d00-152">記錄檔的完整路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="c8d00-152">Full path and file name of the log file.</span></span> <span data-ttu-id="c8d00-153">預設值為% windir% \\ system32 \\ wbem \\ 記錄。</span><span class="sxs-lookup"><span data-stu-id="c8d00-153">The default value is %windir%\\system32\\wbem\\logs.</span></span> <span data-ttu-id="c8d00-154">必須將命名值的 **型** 別設定為 = File，才能使用此命名值。</span><span class="sxs-lookup"><span data-stu-id="c8d00-154">The **Type** named value must be set to = File for this named value to be used.</span></span>

</dd> <dt>

<span data-ttu-id="c8d00-155"><span id="Level"></span><span id="level"></span><span id="LEVEL"></span>**水準**</span><span class="sxs-lookup"><span data-stu-id="c8d00-155"><span id="Level"></span><span id="level"></span><span id="LEVEL"></span>**Level**</span></span>
</dt> <dd>

<span data-ttu-id="c8d00-156">用來定義提供者所產生之偵錯工具輸出型別的32位邏輯遮罩。</span><span class="sxs-lookup"><span data-stu-id="c8d00-156">A 32-bit logical mask that defines the type of debugging output generated by the provider.</span></span> <span data-ttu-id="c8d00-157">此值與提供者相依。</span><span class="sxs-lookup"><span data-stu-id="c8d00-157">This value is provider-dependent.</span></span> <span data-ttu-id="c8d00-158">預設值是 0 (零)。</span><span class="sxs-lookup"><span data-stu-id="c8d00-158">The default value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="c8d00-159"><span id="MaxFileSize"></span><span id="maxfilesize"></span><span id="MAXFILESIZE"></span>**MaxFileSize**</span><span class="sxs-lookup"><span data-stu-id="c8d00-159"><span id="MaxFileSize"></span><span id="maxfilesize"></span><span id="MAXFILESIZE"></span>**MaxFileSize**</span></span>
</dt> <dd>

<span data-ttu-id="c8d00-160">記錄檔的檔案大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c8d00-160">Maximum file size, in bytes, of the log file.</span></span> <span data-ttu-id="c8d00-161">這個整數值的範圍必須介於1024到 2 ^ 32-1 之間。</span><span class="sxs-lookup"><span data-stu-id="c8d00-161">This integer value must be in the range 1024 to 2^32-1.</span></span> <span data-ttu-id="c8d00-162">當檔案大小超過此值時，會將檔案重新命名為 **~ filename** ，並建立新的空白記錄檔。</span><span class="sxs-lookup"><span data-stu-id="c8d00-162">When the file size exceeds this value, the file is renamed to **~filename** and a new, empty log file is created.</span></span> <span data-ttu-id="c8d00-163">記錄檔所需的磁碟空間是 **MaxFileSize** 值的兩倍。</span><span class="sxs-lookup"><span data-stu-id="c8d00-163">The disk space required for the log file is twice the value of **MaxFileSize**.</span></span> <span data-ttu-id="c8d00-164">預設值為65535。</span><span class="sxs-lookup"><span data-stu-id="c8d00-164">The default value is 65,535.</span></span>

</dd> <dt>

<span data-ttu-id="c8d00-165"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**類型**</span><span class="sxs-lookup"><span data-stu-id="c8d00-165"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Type**</span></span>
</dt> <dd>

<span data-ttu-id="c8d00-166">可以設定為 = File 或 = 偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="c8d00-166">Can be set to = File or = Debugger.</span></span> <span data-ttu-id="c8d00-167">如果設定為 = File，則會將追蹤資訊寫入名為的檔案中指定 **的記錄** 檔。</span><span class="sxs-lookup"><span data-stu-id="c8d00-167">If set to = File, the trace information is written to the log file specified in the **File** named value.</span></span> <span data-ttu-id="c8d00-168">預設值為 = File。</span><span class="sxs-lookup"><span data-stu-id="c8d00-168">The default value is = File.</span></span>

</dd> </dl>

<span data-ttu-id="c8d00-169">例如，若要從 View Provider 記錄查詢並取得實例呼叫，請使用下列登錄機碼值。</span><span class="sxs-lookup"><span data-stu-id="c8d00-169">For example, to log query and get instance calls from the View Provider, use the following registry key values.</span></span> <span data-ttu-id="c8d00-170">記錄檔將會位於記錄檔資料夾中，而且將會是預設的檔案大小。</span><span class="sxs-lookup"><span data-stu-id="c8d00-170">The log will be located in the log folder and will be the default file size.</span></span>

<span data-ttu-id="c8d00-171">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **提供者** \\ **記錄** \\ **ViewProvider** 檔 \\  = C： \\ Windows \\ system32 \\ WBEM \\ 記錄 \\ ViewProvider .log</span><span class="sxs-lookup"><span data-stu-id="c8d00-171">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**PROVIDERS**\\**Logging**\\**ViewProvider**\\**File** = C:\\Windows\\system32\\WBEM\\Logs\\ViewProvider.log</span></span>

<span data-ttu-id="c8d00-172">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **提供者** \\ **記錄** \\ **ViewProvider** \\ **層級**= 2</span><span class="sxs-lookup"><span data-stu-id="c8d00-172">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**PROVIDERS**\\**Logging**\\**ViewProvider**\\**Level** = 2</span></span>

<span data-ttu-id="c8d00-173">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **提供者** \\ **記錄** \\ **ViewProvider** \\ **MaxFileSize** = 65535</span><span class="sxs-lookup"><span data-stu-id="c8d00-173">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**PROVIDERS**\\**Logging**\\**ViewProvider**\\**MaxFileSize** = 65535</span></span>

<span data-ttu-id="c8d00-174">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **提供者** \\ **記錄** \\ **ViewProvider** \\ **類型**= 檔案</span><span class="sxs-lookup"><span data-stu-id="c8d00-174">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**PROVIDERS**\\**Logging**\\**ViewProvider**\\**Type** = File</span></span>

> [!Note]  
> <span data-ttu-id="c8d00-175">針對具有記錄功能的您自己的提供者，您需要撰寫必要的登錄機碼和值以啟用記錄。</span><span class="sxs-lookup"><span data-stu-id="c8d00-175">For your own providers with logging capabilities, you need to write the necessary registry keys and values to enable logging.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c8d00-176">相關主題</span><span class="sxs-lookup"><span data-stu-id="c8d00-176">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c8d00-177">[WMI 疑難排解](wmi-troubleshooting.md) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="c8d00-177">[WMI Troubleshooting](wmi-troubleshooting.md)</span></span>
</dt> <dt>

[<span data-ttu-id="c8d00-178">WMI 記錄檔</span><span class="sxs-lookup"><span data-stu-id="c8d00-178">WMI Log Files</span></span>](wmi-log-files.md)
</dt> <dt>

[<span data-ttu-id="c8d00-179">WMI 疑難排解類別</span><span class="sxs-lookup"><span data-stu-id="c8d00-179">WMI Troubleshooting Classes</span></span>](wmi-troubleshooting-classes.md)
</dt> <dt>

[<span data-ttu-id="c8d00-180">追蹤 WMI 活動</span><span class="sxs-lookup"><span data-stu-id="c8d00-180">Tracing WMI Activity</span></span>](tracing-wmi-activity.md)
</dt> </dl>

 

 
