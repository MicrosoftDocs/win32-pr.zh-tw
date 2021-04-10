---
description: IInstallationBehavior 介面會定義下列屬性。
ms.assetid: abb8e247-44c4-491c-b8ea-9f32d7420c45
title: IInstallationBehavior 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 210f495c19c530a6507ffbd0584f647fc952ae46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943481"
---
# <a name="iinstallationbehavior-properties"></a><span data-ttu-id="c9b86-103">IInstallationBehavior 屬性</span><span class="sxs-lookup"><span data-stu-id="c9b86-103">IInstallationBehavior Properties</span></span>

<span data-ttu-id="c9b86-104">[**IInstallationBehavior**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior)介面會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="c9b86-104">The [**IInstallationBehavior**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior) interface defines the following properties.</span></span>



| <span data-ttu-id="c9b86-105">屬性</span><span class="sxs-lookup"><span data-stu-id="c9b86-105">Property</span></span>                                                                                 | <span data-ttu-id="c9b86-106">描述</span><span class="sxs-lookup"><span data-stu-id="c9b86-106">Description</span></span>                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c9b86-107">**CanRequestUserInput**</span><span class="sxs-lookup"><span data-stu-id="c9b86-107">**CanRequestUserInput**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_canrequestuserinput)                 | <span data-ttu-id="c9b86-108">取得布林值，thast 指出安裝或卸載更新是否會提示使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="c9b86-108">Gets a Boolean value thast indicates whether the installation or uninstallation of an update can prompt for user input.</span></span>                                                        |
| [<span data-ttu-id="c9b86-109">**影響**</span><span class="sxs-lookup"><span data-stu-id="c9b86-109">**Impact**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_impact)                                           | <span data-ttu-id="c9b86-110">取得 [**InstallationImpact**](/windows/win32/api/wuapi/ne-wuapi-installationimpact) 列舉，指出更新的安裝或卸載如何影響電腦。</span><span class="sxs-lookup"><span data-stu-id="c9b86-110">Gets an [**InstallationImpact**](/windows/win32/api/wuapi/ne-wuapi-installationimpact) enumeration that indicates how the installation or uninstallation of the update affects the computer.</span></span>                 |
| [<span data-ttu-id="c9b86-111">**RebootBehavior**</span><span class="sxs-lookup"><span data-stu-id="c9b86-111">**RebootBehavior**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_rebootbehavior)                           | <span data-ttu-id="c9b86-112">取得 [**InstallationRebootBehavior**](/windows/win32/api/wuapi/ne-wuapi-installationrebootbehavior) 列舉，這個列舉會指定當您安裝或卸載更新時所發生的重新開機行為。</span><span class="sxs-lookup"><span data-stu-id="c9b86-112">Gets an [**InstallationRebootBehavior**](/windows/win32/api/wuapi/ne-wuapi-installationrebootbehavior) enumeration that specifies the restart behavior that occurs when you install or uninstall the update.</span></span> |
| [<span data-ttu-id="c9b86-113">**RequiresNetworkConnectivity**</span><span class="sxs-lookup"><span data-stu-id="c9b86-113">**RequiresNetworkConnectivity**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_requiresnetworkconnectivity) | <span data-ttu-id="c9b86-114">取得布林值，這個值表示安裝或卸載更新是否需要網路連接。</span><span class="sxs-lookup"><span data-stu-id="c9b86-114">Gets a Boolean value that indicates whether the installation or uninstallation of an update requires network connectivity.</span></span>                                                     |



 

 

 



