---
description: IInstallationJob 介面會定義下列方法。
ms.assetid: 4990ef7c-b6cd-46fc-9e7d-8d1d78edc9f2
title: IInstallationJob 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0c1a5850f3d71ad1a6a51046fe890ea9bc7426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113536"
---
# <a name="iinstallationjob-methods"></a><span data-ttu-id="0beda-103">IInstallationJob 方法</span><span class="sxs-lookup"><span data-stu-id="0beda-103">IInstallationJob Methods</span></span>

<span data-ttu-id="0beda-104">[**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob)介面會定義下列方法。</span><span class="sxs-lookup"><span data-stu-id="0beda-104">The [**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) interface defines the following methods.</span></span>



| <span data-ttu-id="0beda-105">方法</span><span class="sxs-lookup"><span data-stu-id="0beda-105">Method</span></span>                                                | <span data-ttu-id="0beda-106">描述</span><span class="sxs-lookup"><span data-stu-id="0beda-106">Description</span></span>                                                                                                                                           |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0beda-107">**清理**</span><span class="sxs-lookup"><span data-stu-id="0beda-107">**CleanUp**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)           | <span data-ttu-id="0beda-108">等候非同步作業完成，然後釋放所有回呼。</span><span class="sxs-lookup"><span data-stu-id="0beda-108">Waits for an asynchronous operation to be completed and then releases all the callbacks.</span></span>                                                              |
| [<span data-ttu-id="0beda-109">**GetProgress**</span><span class="sxs-lookup"><span data-stu-id="0beda-109">**GetProgress**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-getprogress)   | <span data-ttu-id="0beda-110">傳回 [**IInstallationProgress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) 介面，這個介面會描述安裝或卸載的目前進度。</span><span class="sxs-lookup"><span data-stu-id="0beda-110">Returns an [**IInstallationProgress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) interface that describes the current progress of an installation or uninstallation.</span></span> |
| [<span data-ttu-id="0beda-111">**RequestAbort**</span><span class="sxs-lookup"><span data-stu-id="0beda-111">**RequestAbort**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-requestabort) | <span data-ttu-id="0beda-112">提出取消安裝或卸載的要求。</span><span class="sxs-lookup"><span data-stu-id="0beda-112">Makes a request to cancel the installation or uninstallation.</span></span>                                                                                         |



 

 

 



