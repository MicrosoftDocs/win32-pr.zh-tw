---
description: 下列 COM 介面是用來開發監視器。
ms.assetid: 619991f5-1db1-400a-bf18-d4a6dd6999a8
title: 監視介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66bb06e6153d18c7b0a4291df1c7520380a29844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966738"
---
# <a name="monitor-interfaces"></a><span data-ttu-id="98630-103">監視介面</span><span class="sxs-lookup"><span data-stu-id="98630-103">Monitor Interfaces</span></span>

<span data-ttu-id="98630-104">下列 COM 介面是用來開發監視器。</span><span class="sxs-lookup"><span data-stu-id="98630-104">The following COM interfaces are used to develop monitors.</span></span>



| <span data-ttu-id="98630-105">介面</span><span class="sxs-lookup"><span data-stu-id="98630-105">Interface</span></span>                              | <span data-ttu-id="98630-106">描述</span><span class="sxs-lookup"><span data-stu-id="98630-106">Description</span></span>                                                                                                                                             |
|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98630-107">IMonitor</span><span class="sxs-lookup"><span data-stu-id="98630-107">IMonitor</span></span>](imonitor.md)               | <span data-ttu-id="98630-108">提供控制監視操作的方法。</span><span class="sxs-lookup"><span data-stu-id="98630-108">Provides methods that control monitor operation.</span></span> <span data-ttu-id="98630-109">此介面必須由監視器所執行。</span><span class="sxs-lookup"><span data-stu-id="98630-109">This interface must be implemented by the monitor.</span></span>                                                     |
| [<span data-ttu-id="98630-110">IMonitorEventer</span><span class="sxs-lookup"><span data-stu-id="98630-110">IMonitorEventer</span></span>](imonitoreventer.md) | <span data-ttu-id="98630-111">提供用來傳送事件的方法。</span><span class="sxs-lookup"><span data-stu-id="98630-111">Provides methods used to send events.</span></span> <span data-ttu-id="98630-112">此介面是由 [*監視器控制服務*](m.md) (MCSVC) 所提供。</span><span class="sxs-lookup"><span data-stu-id="98630-112">This interface is provided by the [*Monitor Control Service*](m.md) (MCSVC).</span></span> |



 

 

 



