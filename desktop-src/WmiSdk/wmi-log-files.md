---
description: WMI 使用事件追蹤 (ETW) ，而事件可以透過事件檢視器使用者介面或 Wevtutil 命令列工具取得。 如需詳細資訊，請參閱追蹤 WMI 活動。
ms.assetid: 315b8355-03b9-40f9-a6c1-29a49f5a2cd8
ms.tgt_platform: multiple
title: WMI 記錄檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a51dfe4efbec32e60812980511676f723fd5aee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998088"
---
# <a name="wmi-log-files"></a><span data-ttu-id="8433c-104">WMI 記錄檔</span><span class="sxs-lookup"><span data-stu-id="8433c-104">WMI Log Files</span></span>

<span data-ttu-id="8433c-105">WMI 使用 [事件追蹤](/windows/desktop/ETW/event-tracing-portal) (ETW) ，而事件可以透過 **事件檢視器** 使用者介面或 Wevtutil 命令列工具取得。</span><span class="sxs-lookup"><span data-stu-id="8433c-105">WMI uses [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) and events can be obtained through the **Event Viewer** user interface or the Wevtutil command line tool.</span></span> <span data-ttu-id="8433c-106">如需詳細資訊，請參閱 [追蹤 WMI 活動](tracing-wmi-activity.md)。</span><span class="sxs-lookup"><span data-stu-id="8433c-106">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

-   [<span data-ttu-id="8433c-107">事件追蹤，而不是文字記錄</span><span class="sxs-lookup"><span data-stu-id="8433c-107">Event Tracing Instead of Text Logs</span></span>](#event-tracing-instead-of-text-logs)
-   [<span data-ttu-id="8433c-108">WMI 記錄檔</span><span class="sxs-lookup"><span data-stu-id="8433c-108">WMI Log Files</span></span>](#wmi-log-files)
-   [<span data-ttu-id="8433c-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="8433c-109">Related topics</span></span>](#related-topics)

## <a name="event-tracing-instead-of-text-logs"></a><span data-ttu-id="8433c-110">事件追蹤，而不是文字記錄</span><span class="sxs-lookup"><span data-stu-id="8433c-110">Event Tracing Instead of Text Logs</span></span>

<span data-ttu-id="8433c-111">WMI 服務活動會記錄在 WMITracing 檔案中。</span><span class="sxs-lookup"><span data-stu-id="8433c-111">WMI service activity is recorded in the WMITracing.log file.</span></span> <span data-ttu-id="8433c-112">如需啟用 WMI 事件追蹤和存取 WMITracing 的詳細資訊，請參閱 [追蹤 WMI 活動](tracing-wmi-activity.md)。</span><span class="sxs-lookup"><span data-stu-id="8433c-112">For more information about enabling WMI event tracing and accessing the WMITracing.log file, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span> <span data-ttu-id="8433c-113">Windows Driver Model (WDM) 提供者會繼續登入 Wbemprov .log 檔案。</span><span class="sxs-lookup"><span data-stu-id="8433c-113">Windows Driver Model (WDM) providers continue to log in the Wbemprov.log file.</span></span>

## <a name="wmi-log-files"></a><span data-ttu-id="8433c-114">WMI 記錄檔</span><span class="sxs-lookup"><span data-stu-id="8433c-114">WMI Log Files</span></span>

<span data-ttu-id="8433c-115">WMI 服務和某些提供者會寫入文字記錄檔來記錄事件。</span><span class="sxs-lookup"><span data-stu-id="8433c-115">The WMI service and some providers write text log files to record events.</span></span>

<dl> <dt>

<span data-ttu-id="8433c-116"><span id="WMI_Provider_Log_Files"></span><span id="wmi_provider_log_files"></span><span id="WMI_PROVIDER_LOG_FILES"></span>[WMI 提供者記錄檔](wmi-provider-log-files.md)</span><span class="sxs-lookup"><span data-stu-id="8433c-116"><span id="WMI_Provider_Log_Files"></span><span id="wmi_provider_log_files"></span><span id="WMI_PROVIDER_LOG_FILES"></span>[WMI Provider Log Files](wmi-provider-log-files.md)</span></span>
</dt> <dd>

<span data-ttu-id="8433c-117">WMI 提供者也可以維護記錄。</span><span class="sxs-lookup"><span data-stu-id="8433c-117">WMI providers also may maintain logs.</span></span> <span data-ttu-id="8433c-118">哪些記錄檔會出現在系統上，視安裝的提供者而定。</span><span class="sxs-lookup"><span data-stu-id="8433c-118">Which log files appear on a system depends on which providers are installed.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="8433c-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="8433c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8433c-120">WMI 參考</span><span class="sxs-lookup"><span data-stu-id="8433c-120">WMI Reference</span></span>](wmi-reference.md)
</dt> <dt>

[<span data-ttu-id="8433c-121">追蹤 WMI 活動</span><span class="sxs-lookup"><span data-stu-id="8433c-121">Tracing WMI Activity</span></span>](tracing-wmi-activity.md)
</dt> <dt>

[<span data-ttu-id="8433c-122">記錄 WMI 活動</span><span class="sxs-lookup"><span data-stu-id="8433c-122">Logging WMI Activity</span></span>](logging-wmi-activity.md)
</dt> </dl>

 

 
