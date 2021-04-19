---
description: WMI 原則提供者會透過類別提供群組原則的擴充功能，以允許在原則的應用程式中進行調整。
ms.assetid: 5d4d4fd2-ecd0-4546-b919-1e75199a403c
ms.tgt_platform: multiple
title: 原則提供者類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f2e2a142cf677c8f0b14b41ceb5119e71bcfebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974344"
---
# <a name="policy-provider-classes"></a><span data-ttu-id="321a9-103">原則提供者類別</span><span class="sxs-lookup"><span data-stu-id="321a9-103">Policy Provider Classes</span></span>

<span data-ttu-id="321a9-104">WMI 原則提供者會透過類別提供群組原則的擴充功能，以允許在原則的應用程式中進行調整。</span><span class="sxs-lookup"><span data-stu-id="321a9-104">The WMI policy provider provides extensions to group policy through classes, permitting refinements in the application of policy.</span></span> <span data-ttu-id="321a9-105">原則是使用 WMI 查詢語言 (WQL) 所設定，並位於 Active Directory 以方便部署。</span><span class="sxs-lookup"><span data-stu-id="321a9-105">Policy is set using the WMI Query Language (WQL) and resides in the Active Directory for easy deployment.</span></span>

<span data-ttu-id="321a9-106">下表列出 WMI 原則提供者的類別。</span><span class="sxs-lookup"><span data-stu-id="321a9-106">The following table lists the classes for the WMI policy provider.</span></span>



| <span data-ttu-id="321a9-107">類別</span><span class="sxs-lookup"><span data-stu-id="321a9-107">Class</span></span>                                               | <span data-ttu-id="321a9-108">描述</span><span class="sxs-lookup"><span data-stu-id="321a9-108">Description</span></span>                                                       |
|-----------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="321a9-109">**MSFT \_ 提供者**</span><span class="sxs-lookup"><span data-stu-id="321a9-109">**MSFT\_Providers**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-providers) | <span data-ttu-id="321a9-110">公開與提供者實例相關的設定。</span><span class="sxs-lookup"><span data-stu-id="321a9-110">Exposes configuration relating to provider instances.</span></span>             |
| [<span data-ttu-id="321a9-111">**MSFT \_ 規則**</span><span class="sxs-lookup"><span data-stu-id="321a9-111">**MSFT\_Rule**</span></span>](/previous-versions/windows/desktop/policmanprov/msft-rule)                | <span data-ttu-id="321a9-112">定義管理範圍 (SOM) 內的單一規則。</span><span class="sxs-lookup"><span data-stu-id="321a9-112">Defines a single rule within a Scope of Management (SOM).</span></span>         |
| [<span data-ttu-id="321a9-113">**MSFT \_ SomFilter**</span><span class="sxs-lookup"><span data-stu-id="321a9-113">**MSFT\_SomFilter**</span></span>](/previous-versions/windows/desktop/policmanprov/msft-somfilter)      | <span data-ttu-id="321a9-114">提供在目的電腦上評估的規則清單。</span><span class="sxs-lookup"><span data-stu-id="321a9-114">Provides a list of rules which are evaluated on a target machine.</span></span> |



 

 

 
