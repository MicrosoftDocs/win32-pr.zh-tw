---
description: IUpdateDownloader 介面會定義下列屬性。
ms.assetid: b6a30356-f97d-408f-becd-a467e9f8e79f
title: IUpdateDownloader 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c16aa762bcc14dc1919ef91d162752652c327e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690719"
---
# <a name="iupdatedownloader-properties"></a><span data-ttu-id="2f1b5-103">IUpdateDownloader 屬性</span><span class="sxs-lookup"><span data-stu-id="2f1b5-103">IUpdateDownloader Properties</span></span>

<span data-ttu-id="2f1b5-104">[**IUpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader)介面會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="2f1b5-104">The [**IUpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader) interface defines the following properties.</span></span>



| <span data-ttu-id="2f1b5-105">屬性</span><span class="sxs-lookup"><span data-stu-id="2f1b5-105">Property</span></span>                                                             | <span data-ttu-id="2f1b5-106">描述</span><span class="sxs-lookup"><span data-stu-id="2f1b5-106">Description</span></span>                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f1b5-107">**ClientApplicationID**</span><span class="sxs-lookup"><span data-stu-id="2f1b5-107">**ClientApplicationID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_clientapplicationid) | <span data-ttu-id="2f1b5-108">取得和設定目前的用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="2f1b5-108">Gets and sets the current client application.</span></span>                                                                                                                              |
| [<span data-ttu-id="2f1b5-109">**IsForced**</span><span class="sxs-lookup"><span data-stu-id="2f1b5-109">**IsForced**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_isforced)                       | <span data-ttu-id="2f1b5-110">取得和設定布林值，指出 Windows Update 代理程式 (WUA) 是否會強制下載已安裝或無法安裝的更新。</span><span class="sxs-lookup"><span data-stu-id="2f1b5-110">Gets and sets a Boolean value that indicates whether the Windows Update Agent (WUA) forces the download of updates that are already installed or that cannot be installed.</span></span> |
| [<span data-ttu-id="2f1b5-111">**優先順序**</span><span class="sxs-lookup"><span data-stu-id="2f1b5-111">**Priority**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_priority)                       | <span data-ttu-id="2f1b5-112">取得和設定下載的優先權層級。</span><span class="sxs-lookup"><span data-stu-id="2f1b5-112">Gets and sets the priority level of the download.</span></span>                                                                                                                          |
| [<span data-ttu-id="2f1b5-113">**更新**</span><span class="sxs-lookup"><span data-stu-id="2f1b5-113">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_updates)                         | <span data-ttu-id="2f1b5-114">取得和設定介面，其中包含指定要下載之更新的唯讀集合。</span><span class="sxs-lookup"><span data-stu-id="2f1b5-114">Gets and sets an interface that contains a read-only collection of the updates that are specified for download.</span></span>                                                            |



 

 

 



