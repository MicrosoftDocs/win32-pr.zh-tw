---
description: IUpdateInstaller 介面會定義下列方法。
ms.assetid: 94e2516e-19e1-4e9c-9b9a-fa9a68222b08
title: IUpdateInstaller 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1422c149d2de287c4863078f4012e526212b64ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191473"
---
# <a name="iupdateinstaller-methods"></a><span data-ttu-id="1f623-103">IUpdateInstaller 方法</span><span class="sxs-lookup"><span data-stu-id="1f623-103">IUpdateInstaller Methods</span></span>

<span data-ttu-id="1f623-104">[**IUpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller)介面會定義下列方法。</span><span class="sxs-lookup"><span data-stu-id="1f623-104">The [**IUpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller) interface defines the following methods.</span></span>



| <span data-ttu-id="1f623-105">方法</span><span class="sxs-lookup"><span data-stu-id="1f623-105">Method</span></span>                                                    | <span data-ttu-id="1f623-106">描述</span><span class="sxs-lookup"><span data-stu-id="1f623-106">Description</span></span>                                                                          |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f623-107">**BeginInstall**</span><span class="sxs-lookup"><span data-stu-id="1f623-107">**BeginInstall**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall)     | <span data-ttu-id="1f623-108">開始非同步安裝更新。</span><span class="sxs-lookup"><span data-stu-id="1f623-108">Starts an asynchronous installation of the updates.</span></span>                                  |
| [<span data-ttu-id="1f623-109">**BeginUninstall**</span><span class="sxs-lookup"><span data-stu-id="1f623-109">**BeginUninstall**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) | <span data-ttu-id="1f623-110">開始非同步卸載更新。</span><span class="sxs-lookup"><span data-stu-id="1f623-110">Starts an asynchronous uninstallation of the updates.</span></span>                                |
| [<span data-ttu-id="1f623-111">**EndInstall**</span><span class="sxs-lookup"><span data-stu-id="1f623-111">**EndInstall**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-endinstall)         | <span data-ttu-id="1f623-112">完成更新的非同步安裝。</span><span class="sxs-lookup"><span data-stu-id="1f623-112">Completes an asynchronous installation of the updates.</span></span>                               |
| [<span data-ttu-id="1f623-113">**EndUninstall**</span><span class="sxs-lookup"><span data-stu-id="1f623-113">**EndUninstall**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-enduninstall)     | <span data-ttu-id="1f623-114">完成更新的非同步卸載。</span><span class="sxs-lookup"><span data-stu-id="1f623-114">Completes an asynchronous uninstallation of the updates.</span></span>                             |
| [<span data-ttu-id="1f623-115">**安裝**</span><span class="sxs-lookup"><span data-stu-id="1f623-115">**Install**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-install)               | <span data-ttu-id="1f623-116">啟動更新的同步安裝。</span><span class="sxs-lookup"><span data-stu-id="1f623-116">Starts a synchronous installation of the updates.</span></span>                                    |
| [<span data-ttu-id="1f623-117">**RunWizard**</span><span class="sxs-lookup"><span data-stu-id="1f623-117">**RunWizard**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-runwizard)           | <span data-ttu-id="1f623-118">啟動精靈，引導本機使用者完成安裝更新的步驟。</span><span class="sxs-lookup"><span data-stu-id="1f623-118">Starts a wizard that guides the local user through the steps to install the updates.</span></span> |
| [<span data-ttu-id="1f623-119">**解除安裝**</span><span class="sxs-lookup"><span data-stu-id="1f623-119">**Uninstall**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-uninstall)           | <span data-ttu-id="1f623-120">啟動更新的同步卸載。</span><span class="sxs-lookup"><span data-stu-id="1f623-120">Starts a synchronous uninstallation of the updates.</span></span>                                  |



 

 

 



