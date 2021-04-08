---
description: 從在行動電腦上執行的程式監視系統事件通知，以判斷網路連接頻寬和延遲。 撰寫適用于行動計算和高延遲 Lan 的優化應用程式。
ms.assetid: a27386c5-1ab3-448a-88d9-8c9a18599e59
title: 系統事件通知服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3238441f82c26a33370c37fe09b3e4007639f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944943"
---
# <a name="system-event-notification-service"></a><span data-ttu-id="47f89-104">系統事件通知服務</span><span class="sxs-lookup"><span data-stu-id="47f89-104">System Event Notification Service</span></span>

## <a name="purpose"></a><span data-ttu-id="47f89-105">目的</span><span class="sxs-lookup"><span data-stu-id="47f89-105">Purpose</span></span>

<span data-ttu-id="47f89-106">專為行動使用者所設計的應用程式需要一組獨特的連接功能和通知。</span><span class="sxs-lookup"><span data-stu-id="47f89-106">Applications designed for use by mobile users require a unique set of connectivity functions and notifications.</span></span> <span data-ttu-id="47f89-107">在過去，這些個別的應用程式必須在內部執行這些功能。</span><span class="sxs-lookup"><span data-stu-id="47f89-107">In the past these individual applications were required to implement these features internally.</span></span> <span data-ttu-id="47f89-108">系統事件通知服務 (SENS) 現在會在作業系統中提供這些功能，為應用程式建立統一的連線和通知介面。</span><span class="sxs-lookup"><span data-stu-id="47f89-108">The System Event Notification Service (SENS) now provides these capabilities in the operating system, creating a uniform connectivity and notification interface for applications.</span></span> <span data-ttu-id="47f89-109">使用 SENS 開發人員可以從應用程式內判斷連接頻寬和延遲資訊，並根據這些條件將應用程式的作業優化。</span><span class="sxs-lookup"><span data-stu-id="47f89-109">Using SENS developers can determine connection bandwidth and latency information from within their application and optimize the application's operation based on those conditions.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="47f89-110">適用時</span><span class="sxs-lookup"><span data-stu-id="47f89-110">Where applicable</span></span>

<span data-ttu-id="47f89-111">SENS 的連線能力和通知適用于為行動電腦或連接到高延遲區域網路的電腦所撰寫的應用程式。</span><span class="sxs-lookup"><span data-stu-id="47f89-111">The connectivity functions and notifications of SENS are useful for applications written for mobile computers or computers connected to high latency local area networks.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="47f89-112">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="47f89-112">Developer audience</span></span>

<span data-ttu-id="47f89-113">本檔適用于開發行動電腦運算和高延遲區域網路應用程式的軟體發展人員。</span><span class="sxs-lookup"><span data-stu-id="47f89-113">This document is intended for software developers who develop applications for mobile computing and high latency local area networks.</span></span> <span data-ttu-id="47f89-114">本檔提供系統事件通知服務的所有部分的完整參考，包括 SENS 物件和支援的方法。</span><span class="sxs-lookup"><span data-stu-id="47f89-114">This document provides a complete reference of all parts of the System Event Notification Service including the SENS object and supporting methods.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="47f89-115">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="47f89-115">Run-time requirements</span></span>

<span data-ttu-id="47f89-116">需要 Microsoft Windows XP 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="47f89-116">Requires Microsoft Windows XP or later.</span></span> <span data-ttu-id="47f89-117">如需哪些作業系統需要哪些作業系統才能使用特定介面或功能的相關資訊，請參閱檔的需求一節。</span><span class="sxs-lookup"><span data-stu-id="47f89-117">For information about which operating systems are required to use a particular interface or function, see the Requirements section of the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="47f89-118">本節內容</span><span class="sxs-lookup"><span data-stu-id="47f89-118">In this section</span></span>



| <span data-ttu-id="47f89-119">主題</span><span class="sxs-lookup"><span data-stu-id="47f89-119">Topic</span></span>                                                              | <span data-ttu-id="47f89-120">描述</span><span class="sxs-lookup"><span data-stu-id="47f89-120">Description</span></span>                                                                           |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="47f89-121">概觀</span><span class="sxs-lookup"><span data-stu-id="47f89-121">Overview</span></span>](about-system-event-notification-service.md)<br/> | <span data-ttu-id="47f89-122">關於系統事件通知服務的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="47f89-122">General information about System Event Notification Service.</span></span><br/>               |
| [<span data-ttu-id="47f89-123">參考</span><span class="sxs-lookup"><span data-stu-id="47f89-123">Reference</span></span>](sens-reference.md)<br/>                         | <span data-ttu-id="47f89-124">系統事件通知服務方法和介面的檔。</span><span class="sxs-lookup"><span data-stu-id="47f89-124">Documentation of System Event Notification Service methods and interfaces.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="47f89-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="47f89-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47f89-126">**IEventSubscription**</span><span class="sxs-lookup"><span data-stu-id="47f89-126">**IEventSubscription**</span></span>](/windows/win32/api/eventsys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 
