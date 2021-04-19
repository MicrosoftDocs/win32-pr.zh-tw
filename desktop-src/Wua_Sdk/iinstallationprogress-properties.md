---
description: IInstallationProgress 介面會定義下列屬性。
ms.assetid: f16c682f-3e9f-4767-8f26-d7af0a14d720
title: IInstallationProgress 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcbcdb162c544c81b96326ec7b2b7657d81538a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989920"
---
# <a name="iinstallationprogress-properties"></a><span data-ttu-id="e556d-103">IInstallationProgress 屬性</span><span class="sxs-lookup"><span data-stu-id="e556d-103">IInstallationProgress Properties</span></span>

<span data-ttu-id="e556d-104">[**IInstallationProgress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress)介面會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="e556d-104">The [**IInstallationProgress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) interface defines the following properties.</span></span>



| <span data-ttu-id="e556d-105">屬性</span><span class="sxs-lookup"><span data-stu-id="e556d-105">Property</span></span>                                                                                   | <span data-ttu-id="e556d-106">描述</span><span class="sxs-lookup"><span data-stu-id="e556d-106">Description</span></span>                                                                                                                                        |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e556d-107">**CurrentUpdateIndex**</span><span class="sxs-lookup"><span data-stu-id="e556d-107">**CurrentUpdateIndex**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_currentupdateindex)                     | <span data-ttu-id="e556d-108">取得以零為基底的索引值，這個值會指定在選取多個更新時，目前正在安裝或卸載的更新。</span><span class="sxs-lookup"><span data-stu-id="e556d-108">Gets a zero-based index value that specifies the update that is currently being installed or uninstalled when multiple updates have been selected.</span></span> |
| [<span data-ttu-id="e556d-109">**CurrentUpdatePercentComplete**</span><span class="sxs-lookup"><span data-stu-id="e556d-109">**CurrentUpdatePercentComplete**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_currentupdatepercentcomplete) | <span data-ttu-id="e556d-110">取得目前更新之安裝或卸載程式的進度（以百分比表示）。</span><span class="sxs-lookup"><span data-stu-id="e556d-110">Gets how far the installation or uninstallation process for the current update has progressed, as a percentage.</span></span>                                    |
| [<span data-ttu-id="e556d-111">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="e556d-111">**PercentComplete**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_percentcomplete)                           | <span data-ttu-id="e556d-112">取得整體安裝或卸載進程的進度（以百分比表示）。</span><span class="sxs-lookup"><span data-stu-id="e556d-112">Gets how far the overall installation or uninstallation process has progressed, as a percentage.</span></span>                                                   |



 

 

 



