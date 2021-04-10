---
description: IAutomaticUpdatesSettings 介面會定義下列方法。
ms.assetid: 2c6df896-bb59-4d77-acde-64e36ecb7d75
title: IAutomaticUpdatesSettings 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a9ecfc43539f70b9373a6db298acc6c688e83a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848605"
---
# <a name="iautomaticupdatessettings-methods"></a><span data-ttu-id="9b3f7-103">IAutomaticUpdatesSettings 方法</span><span class="sxs-lookup"><span data-stu-id="9b3f7-103">IAutomaticUpdatesSettings Methods</span></span>

<span data-ttu-id="9b3f7-104">[**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings)介面會定義下列方法。</span><span class="sxs-lookup"><span data-stu-id="9b3f7-104">The [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) interface defines the following methods.</span></span>



| <span data-ttu-id="9b3f7-105">方法</span><span class="sxs-lookup"><span data-stu-id="9b3f7-105">Method</span></span>                                               | <span data-ttu-id="9b3f7-106">描述</span><span class="sxs-lookup"><span data-stu-id="9b3f7-106">Description</span></span>                                      |
|------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="9b3f7-107">**重新整理**</span><span class="sxs-lookup"><span data-stu-id="9b3f7-107">**Refresh**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-refresh) | <span data-ttu-id="9b3f7-108">抓取最新的自動更新設定。</span><span class="sxs-lookup"><span data-stu-id="9b3f7-108">Retrieves the latest Automatic Updates settings.</span></span> |
| [<span data-ttu-id="9b3f7-109">**儲存**</span><span class="sxs-lookup"><span data-stu-id="9b3f7-109">**Save**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)       | <span data-ttu-id="9b3f7-110">套用目前的自動更新設定。</span><span class="sxs-lookup"><span data-stu-id="9b3f7-110">Applies the current Automatic Updates settings.</span></span>  |



 

> [!Note]  
> <span data-ttu-id="9b3f7-111">在 Windows RT 上，您將無法再使用 [**IAutomaticUpdatesSettings：： Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save) 方法以程式設計方式設定 Windows Update 設定。</span><span class="sxs-lookup"><span data-stu-id="9b3f7-111">On Windows RT, you can no longer use the [**IAutomaticUpdatesSettings::Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save) method to configure Windows Update settings programmatically.</span></span> <span data-ttu-id="9b3f7-112">如果您使用 [ **儲存** ] 來設定 4 ([**aunlScheduledInstallation**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel)) 以外的任何值，則設定作業會失敗。</span><span class="sxs-lookup"><span data-stu-id="9b3f7-112">The configuration operation fails if you use **Save** to set any value other than 4 ([**aunlScheduledInstallation**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel)).</span></span>

 

 

 



