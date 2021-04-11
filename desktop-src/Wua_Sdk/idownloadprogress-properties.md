---
description: IDownloadProgress 介面會定義下列屬性。
ms.assetid: 8f64c702-b2b5-4a5f-9365-bc962e35f499
title: IDownloadProgress 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469246acb59b4aa58efcbf4bb5aa7f04b7e44b6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943484"
---
# <a name="idownloadprogress-properties"></a><span data-ttu-id="22484-103">IDownloadProgress 屬性</span><span class="sxs-lookup"><span data-stu-id="22484-103">IDownloadProgress Properties</span></span>

<span data-ttu-id="22484-104">[**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress)介面會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="22484-104">The [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) interface defines the following properties.</span></span>



| <span data-ttu-id="22484-105">屬性</span><span class="sxs-lookup"><span data-stu-id="22484-105">Property</span></span>                                                                               | <span data-ttu-id="22484-106">描述</span><span class="sxs-lookup"><span data-stu-id="22484-106">Description</span></span>                                                                                                                                      |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22484-107">**CurrentUpdateBytesDownloaded**</span><span class="sxs-lookup"><span data-stu-id="22484-107">**CurrentUpdateBytesDownloaded**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytesdownloaded) | <span data-ttu-id="22484-108">取得字串，這個字串會指定要下載的內容檔案或正在下載之更新檔案的資料量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="22484-108">Gets a string that specifies how much data has been transferred for the content file or files of the update that is being downloaded, in bytes.</span></span>  |
| [<span data-ttu-id="22484-109">**CurrentUpdateBytesToDownload**</span><span class="sxs-lookup"><span data-stu-id="22484-109">**CurrentUpdateBytesToDownload**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytestodownload) | <span data-ttu-id="22484-110">取得字串，這個字串會評估應為所下載之更新內容檔案或檔案所傳送的資料量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="22484-110">Gets a string that estimates how much data should be transferred for the content file or files of the update that is being downloaded, in bytes.</span></span> |
| [<span data-ttu-id="22484-111">**CurrentUpdateDownloadPhase**</span><span class="sxs-lookup"><span data-stu-id="22484-111">**CurrentUpdateDownloadPhase**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatedownloadphase)     | <span data-ttu-id="22484-112">取得 [**DownloadPhase**](/windows/win32/api/wuapi/ne-wuapi-downloadphase) 列舉值，這個值會指定目前進行中之下載的階段。</span><span class="sxs-lookup"><span data-stu-id="22484-112">Gets a [**DownloadPhase**](/windows/win32/api/wuapi/ne-wuapi-downloadphase) enumeration value that specifies the phase of the download that is currently in progress.</span></span>          |
| [<span data-ttu-id="22484-113">**CurrentUpdateIndex**</span><span class="sxs-lookup"><span data-stu-id="22484-113">**CurrentUpdateIndex**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdateindex)                     | <span data-ttu-id="22484-114">取得以零為基底的索引值，這個值會指定在選取多個更新時，目前正在下載的更新。</span><span class="sxs-lookup"><span data-stu-id="22484-114">Gets a zero-based index value that specifies the update that is currently being downloaded when multiple updates have been selected.</span></span>             |
| [<span data-ttu-id="22484-115">**CurrentUpdatePercentComplete**</span><span class="sxs-lookup"><span data-stu-id="22484-115">**CurrentUpdatePercentComplete**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatepercentcomplete) | <span data-ttu-id="22484-116">取得已下載之目前更新百分比的估計值。</span><span class="sxs-lookup"><span data-stu-id="22484-116">Gets an estimate of the percentage of the current update that has been downloaded.</span></span>                                                               |
| [<span data-ttu-id="22484-117">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="22484-117">**PercentComplete**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_percentcomplete)                           | <span data-ttu-id="22484-118">取得已下載的所有更新百分比的估計值。</span><span class="sxs-lookup"><span data-stu-id="22484-118">Gets an estimate of the percentage of all the updates that have been downloaded.</span></span>                                                                 |
| [<span data-ttu-id="22484-119">**TotalBytesDownloaded**</span><span class="sxs-lookup"><span data-stu-id="22484-119">**TotalBytesDownloaded**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytesdownloaded)                 | <span data-ttu-id="22484-120">取得字串，這個字串會指定已下載的總數據量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="22484-120">Gets a string that specifies the total amount of data that has been downloaded, in bytes.</span></span>                                                        |
| [<span data-ttu-id="22484-121">**TotalBytesToDownload**</span><span class="sxs-lookup"><span data-stu-id="22484-121">**TotalBytesToDownload**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytestodownload)                 | <span data-ttu-id="22484-122">取得字串，表示將下載的總數據量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="22484-122">Gets a string that represents the estimate of the total amount of data that will be downloaded, in bytes.</span></span>                                        |



 

 

 



