---
title: 使用 Windows 遠端管理
description: Windows 遠端管理的目的是要改善網路環境中，執行各種不同作業系統的裝置的硬體管理。
ms.assetid: 6ee2b238-5bc2-4274-b7ca-49dbc728d8f1
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0c2934694de5913b467521510179fffdb220b601
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092959"
---
# <a name="using-windows-remote-management"></a><span data-ttu-id="22b44-103">使用 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="22b44-103">Using Windows Remote Management</span></span>

<span data-ttu-id="22b44-104">Windows 遠端管理的目的是要改善網路環境中，執行各種不同作業系統的裝置的硬體管理。</span><span class="sxs-lookup"><span data-stu-id="22b44-104">Windows Remote Management is intended to improve hardware management in a network environment with various devices running a variety of operating systems.</span></span> <span data-ttu-id="22b44-105">服務的整個設計重點在於實作可相互操作的通訊協定標準，以監看和管理遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="22b44-105">The entire design of the service is focused on monitoring and managing remote computers by implementing an interoperable standard protocol.</span></span>

<span data-ttu-id="22b44-106">由於 [Winrm 腳本 api](winrm-scripting-api.md) 和 [Winrm c + + api](winrm-c---api.md) 會執行為 WS-Management 的通訊協定所定義的作業，並將其接收 XML 資料流程以回應要求。</span><span class="sxs-lookup"><span data-stu-id="22b44-106">Because the [WinRM Scripting API](winrm-scripting-api.md) and the [WinRM C++ API](winrm-c---api.md) implement and closely model the operations defined for the WS-Management protocol, scripts and applications receive streams of XML in response to requests.</span></span> <span data-ttu-id="22b44-107">方法呼叫的輸入參數必須以 XML 來建立。</span><span class="sxs-lookup"><span data-stu-id="22b44-107">Input parameters to method calls must be constructed in XML.</span></span> <span data-ttu-id="22b44-108">您可以使用 [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) API 的方法來顯示或建立 XML 字串。</span><span class="sxs-lookup"><span data-stu-id="22b44-108">You can use the methods of the [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) API to display or construct XML strings.</span></span> <span data-ttu-id="22b44-109">如需範例，請參閱 [顯示 WinRM 腳本的 XML 輸出](displaying-xml-output-from-winrm-scripts.md)。</span><span class="sxs-lookup"><span data-stu-id="22b44-109">For an example, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span>

<span data-ttu-id="22b44-110">下列清單包含說明如何使用 WinRM 腳本的主題：</span><span class="sxs-lookup"><span data-stu-id="22b44-110">The following list includes topics that describe how to use WinRM scripting:</span></span>

-   [<span data-ttu-id="22b44-111">偵測遠端電腦是否支援 WS-Management 的通訊協定</span><span class="sxs-lookup"><span data-stu-id="22b44-111">Detecting Whether a Remote Computer Supports WS-Management Protocol</span></span>](detecting-whether-a-remote-computer-supports-ws-management-protocol.md)
-   [<span data-ttu-id="22b44-112">從本機電腦取得資料</span><span class="sxs-lookup"><span data-stu-id="22b44-112">Obtaining Data from the Local Computer</span></span>](obtaining-data-from-the-local-computer.md)
-   [<span data-ttu-id="22b44-113">從遠端電腦取得資料</span><span class="sxs-lookup"><span data-stu-id="22b44-113">Obtaining Data from a Remote Computer</span></span>](obtaining-data-from-a-remote-computer.md)
-   [<span data-ttu-id="22b44-114">列舉或列出資源的所有實例</span><span class="sxs-lookup"><span data-stu-id="22b44-114">Enumerating or Listing All the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
-   [<span data-ttu-id="22b44-115">查詢資源的特定實例</span><span class="sxs-lookup"><span data-stu-id="22b44-115">Querying for Specific Instances of a Resource</span></span>](querying-for-specific-instances-of-a-resource.md)
-   [<span data-ttu-id="22b44-116">顯示 WinRM 腳本的 XML 輸出</span><span class="sxs-lookup"><span data-stu-id="22b44-116">Displaying XML Output from WinRM Scripts</span></span>](displaying-xml-output-from-winrm-scripts.md)

## <a name="tracing-winrm-activity"></a><span data-ttu-id="22b44-117">追蹤 WinRM 活動</span><span class="sxs-lookup"><span data-stu-id="22b44-117">Tracing WinRM Activity</span></span>

<span data-ttu-id="22b44-118">由於 WinRM 會透過 [Windows Management Instrumentation (wmi) ](/windows/desktop/WmiSdk/wmi-start-page)取得資料，因此您可以追蹤 WinRM 訊息所產生的 wmi 活動。</span><span class="sxs-lookup"><span data-stu-id="22b44-118">Because WinRM obtains data through [Windows Management Instrumentation (WMI)](/windows/desktop/WmiSdk/wmi-start-page), you can trace WMI activity that results from WinRM messages.</span></span> <span data-ttu-id="22b44-119">從 Windows Vista 開始，WMI 服務不再使用 [Wmi 記錄](/windows/desktop/WmiSdk/wmi-log-files)檔。</span><span class="sxs-lookup"><span data-stu-id="22b44-119">Starting with Windows Vista, the WMI service no longer uses the [WMI Log Files](/windows/desktop/WmiSdk/wmi-log-files).</span></span> <span data-ttu-id="22b44-120">相反地，它會使用 [事件追蹤](/windows/desktop/ETW/event-tracing-portal) (ETW) ，而事件則是透過 **事件檢視器** UI 或 Evtutil 命令列工具提供。</span><span class="sxs-lookup"><span data-stu-id="22b44-120">Instead it uses [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) and events are available through the **Event Viewer** UI or the Evtutil command line tool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22b44-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="22b44-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22b44-122">Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="22b44-122">Windows Remote Management</span></span>](portal.md)
</dt> <dt>

[<span data-ttu-id="22b44-123">關於 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="22b44-123">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="22b44-124">Windows 遠端管理參考</span><span class="sxs-lookup"><span data-stu-id="22b44-124">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> <dt>

[<span data-ttu-id="22b44-125">Windows 遠端管理中的腳本</span><span class="sxs-lookup"><span data-stu-id="22b44-125">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 