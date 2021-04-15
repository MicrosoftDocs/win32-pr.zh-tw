---
description: IUpdateServiceManager 介面會定義下列方法。
ms.assetid: b2ae49bc-3fb6-4cb9-82ce-387409096159
title: IUpdateServiceManager 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 464b0b6e48d074dbc43f370f267fe7a526e8269b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510957"
---
# <a name="iupdateservicemanager-methods"></a><span data-ttu-id="3cc55-103">IUpdateServiceManager 方法</span><span class="sxs-lookup"><span data-stu-id="3cc55-103">IUpdateServiceManager Methods</span></span>

<span data-ttu-id="3cc55-104">[**IUpdateServiceManager**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager)介面會定義下列方法。</span><span class="sxs-lookup"><span data-stu-id="3cc55-104">The [**IUpdateServiceManager**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager) interface defines the following methods.</span></span>



| <span data-ttu-id="3cc55-105">方法</span><span class="sxs-lookup"><span data-stu-id="3cc55-105">Method</span></span>                                                                           | <span data-ttu-id="3cc55-106">描述</span><span class="sxs-lookup"><span data-stu-id="3cc55-106">Description</span></span>                                                                                                                                      |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3cc55-107">**AddScanPackageService**</span><span class="sxs-lookup"><span data-stu-id="3cc55-107">**AddScanPackageService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice)     | <span data-ttu-id="3cc55-108">使用 Windows Update 代理程式 (WUA) 註冊掃描封裝即服務，然後傳回 [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) 介面。</span><span class="sxs-lookup"><span data-stu-id="3cc55-108">Registers a scan package as a service with Windows Update Agent (WUA) and then returns an [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) interface.</span></span>    |
| [<span data-ttu-id="3cc55-109">**AddService**</span><span class="sxs-lookup"><span data-stu-id="3cc55-109">**AddService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addservice)                           | <span data-ttu-id="3cc55-110">向 WUA 註冊服務。</span><span class="sxs-lookup"><span data-stu-id="3cc55-110">Registers a service with WUA.</span></span>                                                                                                                    |
| [<span data-ttu-id="3cc55-111">**RegisterServiceWithAU**</span><span class="sxs-lookup"><span data-stu-id="3cc55-111">**RegisterServiceWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau)     | <span data-ttu-id="3cc55-112">使用自動更新註冊服務。</span><span class="sxs-lookup"><span data-stu-id="3cc55-112">Registers a service with Automatic Updates.</span></span>                                                                                                      |
| [<span data-ttu-id="3cc55-113">**RemoveService**</span><span class="sxs-lookup"><span data-stu-id="3cc55-113">**RemoveService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-removeservice)                     | <span data-ttu-id="3cc55-114">從 WUA 移除服務註冊。</span><span class="sxs-lookup"><span data-stu-id="3cc55-114">Removes a service registration from WUA.</span></span>                                                                                                         |
| [<span data-ttu-id="3cc55-115">**SetOption**</span><span class="sxs-lookup"><span data-stu-id="3cc55-115">**SetOption**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-setoption)                             | <span data-ttu-id="3cc55-116">設定指定服務識別碼之物件的選項，以及在變更自動更新的註冊時是否顯示警告。</span><span class="sxs-lookup"><span data-stu-id="3cc55-116">Sets options for the object that specifies the service ID, and whether to display a warning when changing the registration of Automatic Updates.</span></span> |
| [<span data-ttu-id="3cc55-117">**UnregisterServiceWithAU**</span><span class="sxs-lookup"><span data-stu-id="3cc55-117">**UnregisterServiceWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-unregisterservicewithau) | <span data-ttu-id="3cc55-118">使用自動更新取消註冊服務。</span><span class="sxs-lookup"><span data-stu-id="3cc55-118">Unregisters a service with Automatic Updates.</span></span>                                                                                                    |



 

 

 



