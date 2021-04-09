---
description: IInstallationJob 介面會定義下列屬性。
ms.assetid: 74087098-bef0-41f8-8d7b-bbca1d000df8
title: IInstallationJob 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b0083acd90b174349c105525676741c762aa05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690724"
---
# <a name="iinstallationjob-properties"></a><span data-ttu-id="fe9e9-103">IInstallationJob 屬性</span><span class="sxs-lookup"><span data-stu-id="fe9e9-103">IInstallationJob Properties</span></span>

<span data-ttu-id="fe9e9-104">[**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob)介面會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="fe9e9-104">The [**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) interface defines the following properties.</span></span>



| <span data-ttu-id="fe9e9-105">屬性</span><span class="sxs-lookup"><span data-stu-id="fe9e9-105">Property</span></span>                                            | <span data-ttu-id="fe9e9-106">描述</span><span class="sxs-lookup"><span data-stu-id="fe9e9-106">Description</span></span>                                                                                                                                                                                                                            |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fe9e9-107">**AsyncState**</span><span class="sxs-lookup"><span data-stu-id="fe9e9-107">**AsyncState**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_asyncstate)   | <span data-ttu-id="fe9e9-108">取得傳遞至 [**IUpdateInstaller. BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) 或 [**IUpdateInstaller. BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) 方法的呼叫端特定狀態物件。</span><span class="sxs-lookup"><span data-stu-id="fe9e9-108">Gets the caller-specific state object that is passed to the [**IUpdateInstaller.BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) or [**IUpdateInstaller.BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) method.</span></span>               |
| [<span data-ttu-id="fe9e9-109">**IsCompleted**</span><span class="sxs-lookup"><span data-stu-id="fe9e9-109">**IsCompleted**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_iscompleted) | <span data-ttu-id="fe9e9-110">取得值，這個值會指出是否已完整處理 [**IUpdateInstaller. BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) 或 [**IUpdateInstaller. BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) 方法的呼叫。</span><span class="sxs-lookup"><span data-stu-id="fe9e9-110">Gets a value that indicates whether a call to the [**IUpdateInstaller.BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) or [**IUpdateInstaller.BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) method is completely processed.</span></span> |
| [<span data-ttu-id="fe9e9-111">**更新**</span><span class="sxs-lookup"><span data-stu-id="fe9e9-111">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_updates)         | <span data-ttu-id="fe9e9-112">取得介面，其中包含安裝或卸載中指定之更新的唯讀集合。</span><span class="sxs-lookup"><span data-stu-id="fe9e9-112">Gets an interface that contains a read-only collection of the updates that are specified in the installation or uninstallation.</span></span>                                                                                                        |



 

 

 



