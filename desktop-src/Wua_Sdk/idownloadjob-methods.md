---
description: IDownloadJob 介面會定義下列方法。
ms.assetid: b9a6b722-2e32-4177-bcef-514412e132ec
title: IDownloadJob 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f68acd6d7fef37c4ce9309c559a1de1b4d516dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511796"
---
# <a name="idownloadjob-methods"></a><span data-ttu-id="b210b-103">IDownloadJob 方法</span><span class="sxs-lookup"><span data-stu-id="b210b-103">IDownloadJob Methods</span></span>

<span data-ttu-id="b210b-104">[**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob)介面會定義下列方法。</span><span class="sxs-lookup"><span data-stu-id="b210b-104">The [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) interface defines the following methods.</span></span>



| <span data-ttu-id="b210b-105">方法</span><span class="sxs-lookup"><span data-stu-id="b210b-105">Method</span></span>                                            | <span data-ttu-id="b210b-106">描述</span><span class="sxs-lookup"><span data-stu-id="b210b-106">Description</span></span>                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b210b-107">**清理**</span><span class="sxs-lookup"><span data-stu-id="b210b-107">**CleanUp**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup)           | <span data-ttu-id="b210b-108">等候非同步作業完成，並釋放所有回呼。</span><span class="sxs-lookup"><span data-stu-id="b210b-108">Waits for an asynchronous operation to be completed and releases all callbacks.</span></span>                                        |
| [<span data-ttu-id="b210b-109">**GetProgress**</span><span class="sxs-lookup"><span data-stu-id="b210b-109">**GetProgress**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-getprogress)   | <span data-ttu-id="b210b-110">傳回描述下載目前進度的 [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) 介面。</span><span class="sxs-lookup"><span data-stu-id="b210b-110">Returns an [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) interface that describes the current progress of a download.</span></span> |
| [<span data-ttu-id="b210b-111">**RequestAbort**</span><span class="sxs-lookup"><span data-stu-id="b210b-111">**RequestAbort**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-requestabort) | <span data-ttu-id="b210b-112">提出結束非同步下載的要求。</span><span class="sxs-lookup"><span data-stu-id="b210b-112">Makes a request to end an asynchronous download.</span></span>                                                                       |



 

 

 



