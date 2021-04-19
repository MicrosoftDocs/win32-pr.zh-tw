---
description: IDownloadJob 介面會定義下列屬性。
ms.assetid: 50e672d7-0ad6-402d-878c-4ac79b70a036
title: IDownloadJob 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c9bd940b4b091f2eeefbaaa2a60d66306a3e14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981142"
---
# <a name="idownloadjob-properties"></a><span data-ttu-id="9e765-103">IDownloadJob 屬性</span><span class="sxs-lookup"><span data-stu-id="9e765-103">IDownloadJob Properties</span></span>

<span data-ttu-id="9e765-104">[**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob)介面會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="9e765-104">The [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) interface defines the following properties.</span></span>



| <span data-ttu-id="9e765-105">屬性</span><span class="sxs-lookup"><span data-stu-id="9e765-105">Property</span></span>                                        | <span data-ttu-id="9e765-106">描述</span><span class="sxs-lookup"><span data-stu-id="9e765-106">Description</span></span>                                                                                                                                              |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9e765-107">**AsyncState**</span><span class="sxs-lookup"><span data-stu-id="9e765-107">**AsyncState**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_asyncstate)   | <span data-ttu-id="9e765-108">取得傳遞至 [**IUpdateDownloader. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) 方法的呼叫端特定狀態物件。</span><span class="sxs-lookup"><span data-stu-id="9e765-108">Gets the caller-specific state object that is passed to the [**IUpdateDownloader.BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) method.</span></span>           |
| [<span data-ttu-id="9e765-109">**IsCompleted**</span><span class="sxs-lookup"><span data-stu-id="9e765-109">**IsCompleted**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_iscompleted) | <span data-ttu-id="9e765-110">取得設定，指出是否已完全處理對 [**IUpdateDownloader. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="9e765-110">Gets the setting that indicates whether the call to [**IUpdateDownloader.BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) was processed completely.</span></span> |
| [<span data-ttu-id="9e765-111">**更新**</span><span class="sxs-lookup"><span data-stu-id="9e765-111">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_updates)         | <span data-ttu-id="9e765-112">取得介面，其中包含在下載中指定之更新的唯讀集合。</span><span class="sxs-lookup"><span data-stu-id="9e765-112">Gets an interface that contains a read-only collection of the updates that are specified in a download.</span></span>                                                  |



 

 

 



