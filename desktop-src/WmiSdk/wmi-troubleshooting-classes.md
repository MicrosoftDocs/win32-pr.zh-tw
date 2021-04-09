---
description: WMI 提供一組疑難排解類別，可讓腳本和應用程式在 WMI 核心和提供者作業期間，用來取得 WMI 內部狀態的相關資訊。
ms.assetid: 631e0cce-0e83-42e5-a381-e96b1f70d6f9
ms.tgt_platform: multiple
title: WMI 疑難排解類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65b3972ba59c80a1495916ab24a72f6e93bef8e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945291"
---
# <a name="wmi-troubleshooting-classes"></a><span data-ttu-id="c8035-103">WMI 疑難排解類別</span><span class="sxs-lookup"><span data-stu-id="c8035-103">WMI Troubleshooting Classes</span></span>

<span data-ttu-id="c8035-104">WMI 提供一組疑難排解類別，可讓腳本和應用程式在 WMI 核心和提供者作業期間，用來取得 WMI 內部狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c8035-104">WMI supplies a set of troubleshooting classes that scripts and applications can use to get information about WMI internal state during WMI core and provider operations.</span></span> <span data-ttu-id="c8035-105">如需 WMI 疑難排解的詳細資訊，請參閱 [Wmi 疑難排解](wmi-troubleshooting.md) 和 [提供者設定和疑難排解類別](provider-configuration-and-troubleshooting-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="c8035-105">For more information about WMI troubleshooting, see [WMI Troubleshooting](wmi-troubleshooting.md) and [Provider Configuration and Troubleshooting Classes](provider-configuration-and-troubleshooting-classes.md).</span></span>

<span data-ttu-id="c8035-106">WMI 有幾個基本的疑難排解類別，適用于 WMI 核心和提供者作業：</span><span class="sxs-lookup"><span data-stu-id="c8035-106">WMI has several basic troubleshooting classes for WMI core and provider operations:</span></span>

-   [<span data-ttu-id="c8035-107">**MSFT \_ 的 wmiprovider \_ 計數器**</span><span class="sxs-lookup"><span data-stu-id="c8035-107">**MSFT\_WmiProvider\_Counters**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-counters)

    <span data-ttu-id="c8035-108">每個電腦系統上只會找到其中一個類別。</span><span class="sxs-lookup"><span data-stu-id="c8035-108">Only one of these classes is found on each computer system.</span></span> <span data-ttu-id="c8035-109">它會提供該系統上各種類型的提供者作業計數。</span><span class="sxs-lookup"><span data-stu-id="c8035-109">It provides counts of various kind of provider operations on that system.</span></span>

-   [<span data-ttu-id="c8035-110">**MSFT \_ WmiSelfEvent**</span><span class="sxs-lookup"><span data-stu-id="c8035-110">**MSFT\_WmiSelfEvent**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent)

    <span data-ttu-id="c8035-111">事件疑難排解類別衍生自 [**MSFT \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent)。</span><span class="sxs-lookup"><span data-stu-id="c8035-111">The event troubleshooting classes derive from [**MSFT\_WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent).</span></span> <span data-ttu-id="c8035-112">此類別的查詢會傳回事件類別的實例，例如 [**msft \_ WmiThreadPoolCreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated) 或 [**msft \_ 的 wmiprovider \_ CreateInstanceEnumAsyncEvent \_ Post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createinstanceenumasyncevent-post)。</span><span class="sxs-lookup"><span data-stu-id="c8035-112">Queries of this class return instances of event classes such as [**MSFT\_WmiThreadPoolCreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated) or [**MSFT\_WmiProvider\_CreateInstanceEnumAsyncEvent\_Post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createinstanceenumasyncevent-post).</span></span>

    <span data-ttu-id="c8035-113">下列清單提供衍生自 [**MSFT \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent)之事件類別的不同類別連結：</span><span class="sxs-lookup"><span data-stu-id="c8035-113">The following list provides links to different categories of event classes derived from [**MSFT\_WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent):</span></span>

    -   [<span data-ttu-id="c8035-114">提供者事件疑難排解類別</span><span class="sxs-lookup"><span data-stu-id="c8035-114">Provider Event Troubleshooting Classes</span></span>](provider-event-troubleshooting-classes.md)
    -   [<span data-ttu-id="c8035-115">ConsumerProvider 疑難排解類別</span><span class="sxs-lookup"><span data-stu-id="c8035-115">ConsumerProvider Troubleshooting Classes</span></span>](consumerprovider-troubleshooting-classes.md)
    -   [<span data-ttu-id="c8035-116">WMI 服務事件疑難排解類別</span><span class="sxs-lookup"><span data-stu-id="c8035-116">WMI Service Event Troubleshooting Classes</span></span>](wmi-service-event-troubleshooting-classes.md)

## <a name="related-topics"></a><span data-ttu-id="c8035-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="c8035-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c8035-118">[WMI 疑難排解](wmi-troubleshooting.md) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="c8035-118">[WMI Troubleshooting](wmi-troubleshooting.md)</span></span>
</dt> <dt>

[<span data-ttu-id="c8035-119">接收 WMI 事件</span><span class="sxs-lookup"><span data-stu-id="c8035-119">Receiving a WMI Event</span></span>](receiving-a-wmi-event.md)
</dt> </dl>

 

 
