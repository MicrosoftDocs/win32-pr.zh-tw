---
title: SystemMonitor 事件
description: SystemMonitor 類別具有下列事件
ms.assetid: 64d9befd-5ea0-4888-b0fb-cff889f1d188
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 94247cf81fcaf57f373c731cd4eaf06a3ca897ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968206"
---
# <a name="systemmonitor-events"></a><span data-ttu-id="00165-103">SystemMonitor 事件</span><span class="sxs-lookup"><span data-stu-id="00165-103">SystemMonitor Events</span></span>

<span data-ttu-id="00165-104">[**SystemMonitor**](systemmonitor.md)類別具有下列事件：</span><span class="sxs-lookup"><span data-stu-id="00165-104">The [**SystemMonitor**](systemmonitor.md) class has the following events:</span></span>

-   [<span data-ttu-id="00165-105">**OnCounterAdded**</span><span class="sxs-lookup"><span data-stu-id="00165-105">**OnCounterAdded**</span></span>](systemmonitor-oncounteradded.md)
-   [<span data-ttu-id="00165-106">**OnCounterDeleted**</span><span class="sxs-lookup"><span data-stu-id="00165-106">**OnCounterDeleted**</span></span>](-systemmonitor-oncounterdeleted.md)
-   [<span data-ttu-id="00165-107">**OnCounterSelected**</span><span class="sxs-lookup"><span data-stu-id="00165-107">**OnCounterSelected**</span></span>](-systemmonitor-oncounterselected.md)
-   [<span data-ttu-id="00165-108">**OnDblClick**</span><span class="sxs-lookup"><span data-stu-id="00165-108">**OnDblClick**</span></span>](-systemmonitor-ondblclick.md)
-   [<span data-ttu-id="00165-109">**OnSampleCollected**</span><span class="sxs-lookup"><span data-stu-id="00165-109">**OnSampleCollected**</span></span>](-systemmonitor-onsamplecollected.md)

> [!Note]  
> <span data-ttu-id="00165-110">[**更新間隔**](systemmonitor-updateinterval.md)到期之前，您必須從事件處理常式傳回：否則，SYSMON 會顯示訊息方塊，指出使用者無法針對先前的更新間隔進行計數器值的取樣。</span><span class="sxs-lookup"><span data-stu-id="00165-110">You must return from the event handler before the [**update interval**](systemmonitor-updateinterval.md) expires; otherwise, SYSMON displays a message box indicating to the user that it was unable to sample counter values for the previous update interval.</span></span>

 

 

 




