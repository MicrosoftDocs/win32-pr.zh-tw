---
description: 監視的設計目的是要使用 Windows Management Instrumentation (WMI) 來將事件引發至本機或遠端電腦。
ms.assetid: b20746dd-d8d9-49b6-95b7-5151ee02901d
title: 監視事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98241081d8a59c33ab173447eaedd903e72eb09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469160"
---
# <a name="monitor-events"></a><span data-ttu-id="29343-103">監視事件</span><span class="sxs-lookup"><span data-stu-id="29343-103">Monitor Events</span></span>

<span data-ttu-id="29343-104">監視的設計目的是要使用 [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI) 來將事件引發至本機或遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="29343-104">Monitors are designed to use [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI) to fire events to local or remote computers.</span></span>

> [!Note]  
> <span data-ttu-id="29343-105">因為監視器會使用即時捕獲，所以只能在本機電腦上捕獲資料。</span><span class="sxs-lookup"><span data-stu-id="29343-105">Because monitors use a real-time capture they can only capture data at the local computer.</span></span> <span data-ttu-id="29343-106">這是網路封包提供者之 **IRTC** 介面的限制。</span><span class="sxs-lookup"><span data-stu-id="29343-106">This is a limitation of the network packet provider's **IRTC** interface.</span></span> <span data-ttu-id="29343-107">不過，藉由使用 WMI 事件，可以在本機檢查捕捉的資料，而將事件傳送到本機或遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="29343-107">However, by using WMI events, the captured data can be examined locally while events can be sent to local or remote computers.</span></span>

 

<span data-ttu-id="29343-108">監視器不會直接與 WMI 通訊。</span><span class="sxs-lookup"><span data-stu-id="29343-108">Monitors do not communicate directly with WMI.</span></span> <span data-ttu-id="29343-109">[*監視器控制服務*](m.md) (MCSVC) 會提供一個稱為 [IMonitorEventer](imonitoreventer.md)) 的介面，此 (介面可讓監視用來取得事件資料結構，並將相關資訊填入其中。</span><span class="sxs-lookup"><span data-stu-id="29343-109">The [*Monitor Control Service*](m.md) (MCSVC) provides an interface (called [IMonitorEventer](imonitoreventer.md)), which the monitor can use to obtain an event data structure and fill it with the relevant information.</span></span> <span data-ttu-id="29343-110">然後，MCSVC 會將事件資料結構傳送至 WMI，進而引發事件。</span><span class="sxs-lookup"><span data-stu-id="29343-110">The MCSVC can then send the event data structure to WMI, which in turn fires the event.</span></span>

 

 
