---
description: IWindowsDriverUpdate2 介面會定義下列屬性。
ms.assetid: ed45a833-5c28-4ddc-993c-1237f69ec63f
title: IWindowsDriverUpdate2 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5271e6623db073313c42a7e6dedebbd33e5eb6c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511776"
---
# <a name="iwindowsdriverupdate2-properties"></a><span data-ttu-id="01593-103">IWindowsDriverUpdate2 屬性</span><span class="sxs-lookup"><span data-stu-id="01593-103">IWindowsDriverUpdate2 Properties</span></span>

<span data-ttu-id="01593-104">[**IWindowsDriverUpdate2**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate)介面會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="01593-104">The [**IWindowsDriverUpdate2**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate) interface defines the following properties.</span></span>



| <span data-ttu-id="01593-105">屬性</span><span class="sxs-lookup"><span data-stu-id="01593-105">Property</span></span>                                                       | <span data-ttu-id="01593-106">描述</span><span class="sxs-lookup"><span data-stu-id="01593-106">Description</span></span>                                                                                                             |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01593-107">**CveIDs**</span><span class="sxs-lookup"><span data-stu-id="01593-107">**CveIDs**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate2-get_cveids)                 | <span data-ttu-id="01593-108">包含與更新相關聯 (CVE) 識別碼的常見弱點和漏洞集合。</span><span class="sxs-lookup"><span data-stu-id="01593-108">Contains a collection of the Common Vulnerabilities and Exposures (CVE) identifiers that are associated with an update.</span></span> |
| [<span data-ttu-id="01593-109">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="01593-109">**IsPresent**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate2-get_ispresent)           | <span data-ttu-id="01593-110">取得布林值，這個值表示是否已在電腦上安裝更新。</span><span class="sxs-lookup"><span data-stu-id="01593-110">Gets a Boolean value that indicates whether an update is installed on the computer.</span></span>                                     |
| [<span data-ttu-id="01593-111">**RebootRequired**</span><span class="sxs-lookup"><span data-stu-id="01593-111">**RebootRequired**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate2-get_rebootrequired) | <span data-ttu-id="01593-112">取得布林值，指出是否必須在安裝或卸載更新之後重新開機電腦。</span><span class="sxs-lookup"><span data-stu-id="01593-112">Gets a Boolean value that indicates whether the computer must be restarted after you install or uninstall an update.</span></span>    |



 

<span data-ttu-id="01593-113">如需此介面所繼承之成員的相關資訊，請參閱下列介面。</span><span class="sxs-lookup"><span data-stu-id="01593-113">For information about the members inherited by this interface, see the following interface.</span></span>

-   [<span data-ttu-id="01593-114">**IWindowsDriverUpdate**</span><span class="sxs-lookup"><span data-stu-id="01593-114">**IWindowsDriverUpdate**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate)

 

 



