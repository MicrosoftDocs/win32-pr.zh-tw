---
title: '記錄 (Windows 篩選平台) '
description: Windows 篩選平台 (WFP) 提供封包捨棄和 IKE/AuthIP 失敗的記錄。
ms.assetid: 607b7664-6be4-4ae6-991b-58ac9175405a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27868c76a643a8e1b7b478152c100a2026bfc20
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106994969"
---
# <a name="logging-windows-filtering-platform"></a><span data-ttu-id="cdd6c-103">記錄 (Windows 篩選平台) </span><span class="sxs-lookup"><span data-stu-id="cdd6c-103">Logging (Windows Filtering Platform)</span></span>

<span data-ttu-id="cdd6c-104">Windows 篩選平台 (WFP) 提供封包捨棄和 IKE/AuthIP 失敗的記錄。</span><span class="sxs-lookup"><span data-stu-id="cdd6c-104">The Windows Filtering Platform (WFP) provides logging of packet drops and IKE/AuthIP failures.</span></span>

<span data-ttu-id="cdd6c-105">記錄的事件會定義在 [**FWPM \_ NET \_ 事件 \_ 類型**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_net_event_type) 列舉型別中，如下所示。</span><span class="sxs-lookup"><span data-stu-id="cdd6c-105">The logged events are defined in the [**FWPM\_NET\_EVENT\_TYPE**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_net_event_type) enumerated type and are as follows.</span></span>

-   <span data-ttu-id="cdd6c-106">IKE/AuthIP 主要模式失敗。</span><span class="sxs-lookup"><span data-stu-id="cdd6c-106">IKE/AuthIP main mode failures.</span></span>
-   <span data-ttu-id="cdd6c-107">IKE/AuthIP 快速模式失敗。</span><span class="sxs-lookup"><span data-stu-id="cdd6c-107">IKE/AuthIP quick mode failures.</span></span>
-   <span data-ttu-id="cdd6c-108">AuthIP 延伸模式失敗。</span><span class="sxs-lookup"><span data-stu-id="cdd6c-108">AuthIP extended mode failures.</span></span>
-   <span data-ttu-id="cdd6c-109">分類期間捨棄的封包。</span><span class="sxs-lookup"><span data-stu-id="cdd6c-109">Packets dropped during classification.</span></span>
-   <span data-ttu-id="cdd6c-110">IPsec 丟棄的封包。</span><span class="sxs-lookup"><span data-stu-id="cdd6c-110">Packets dropped by IPsec.</span></span>

<span data-ttu-id="cdd6c-111">根據預設，會針對單播輸入封包和所有輸出封包啟用 WFP 記錄， (單播、多播和廣播) 。</span><span class="sxs-lookup"><span data-stu-id="cdd6c-111">By default, logging for WFP is enabled for unicast inbound packets and for all outbound packets (unicast, multicast, and broadcast).</span></span> <span data-ttu-id="cdd6c-112">您可以透過 [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0) 管理功能，針對其餘的封包啟用記錄，或針對所有封包停用記錄。</span><span class="sxs-lookup"><span data-stu-id="cdd6c-112">Logging can be enabled for the rest of the packets, or disabled for all packets, through the [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0) management function.</span></span> <span data-ttu-id="cdd6c-113">事件設定在重新開機時持續存在。</span><span class="sxs-lookup"><span data-stu-id="cdd6c-113">Event settings persist across reboots.</span></span>

<span data-ttu-id="cdd6c-114">記錄的事件會儲存在迴圈記錄中，也就是當記錄檔到達大小上限時，新的事件會覆寫舊的事件，而且可以使用 WFP 提供的 [事件管理](fwp-mgmt-functions.md) 函式進行分析。</span><span class="sxs-lookup"><span data-stu-id="cdd6c-114">Logged events are stored in a circular log, that is new events override old ones when the log reaches its maximum size, and can be analyzed using the [event management](fwp-mgmt-functions.md) functions provided by WFP.</span></span> <span data-ttu-id="cdd6c-115">事件記錄檔的大小上限為 128 KB，且最多可保存100到150個事件。</span><span class="sxs-lookup"><span data-stu-id="cdd6c-115">The event log has a maximum size of 128 KB and it can hold about 100 to 150 events.</span></span>

<span data-ttu-id="cdd6c-116">一般來說，列舉函數和 [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) / [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1)會在建立列舉控制碼時，取得記錄的快照。</span><span class="sxs-lookup"><span data-stu-id="cdd6c-116">Enumeration functions in general, and [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0)/[**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) in particular, take a snapshot of the log at the time the enumeration handle is created.</span></span> <span data-ttu-id="cdd6c-117">使用相同列舉控制碼的後續呼叫會傳回下一組專案，後面接著最後一個輸出緩衝區中的專案。</span><span class="sxs-lookup"><span data-stu-id="cdd6c-117">Subsequent calls using the same enumeration handle return the next set of items following those in the last output buffer.</span></span>

<span data-ttu-id="cdd6c-118">當應用程式透過呼叫 [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0) 來停用 WFP 記錄 () 所有應用程式都會受到影響。</span><span class="sxs-lookup"><span data-stu-id="cdd6c-118">When an application disables WFP logging (by calling [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)) all applications are affected.</span></span> <span data-ttu-id="cdd6c-119">在應用程式重新啟用 WFP 記錄之前，不會清除事件記錄檔，但在那之前無法查詢事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="cdd6c-119">The event log is not cleaned up until an application re-enables WFP logging, but the event log cannot be queried before then.</span></span>

<span data-ttu-id="cdd6c-120">在重新開機之後，會清空 WFP 事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="cdd6c-120">The WFP event log is emptied after a reboot.</span></span>

 

 




