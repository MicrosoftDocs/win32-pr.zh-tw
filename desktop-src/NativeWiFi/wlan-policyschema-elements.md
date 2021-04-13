---
description: 原生 Wifi 無線區域網路 (WLAN) 原則設定檔是由下列架構元素所組成。
ms.assetid: e3f45b02-6aea-4df3-938e-c13e7c52ca04
title: WLAN_policy 架構元素
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8346aab6aba209933b20790cf3747d5c0944f972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511183"
---
# <a name="wlan_policy-schema-elements"></a><span data-ttu-id="574c5-103">WLAN \_ 原則架構元素</span><span class="sxs-lookup"><span data-stu-id="574c5-103">WLAN\_policy Schema Elements</span></span>

<span data-ttu-id="574c5-104">原生 Wifi 無線區域網路 (WLAN) 原則設定檔是由下列架構元素所組成。</span><span class="sxs-lookup"><span data-stu-id="574c5-104">A Native Wifi wireless LAN (WLAN) policy profile is composed of the following schema elements.</span></span> <span data-ttu-id="574c5-105">所有命名的元素都位於命名空間中 `https://www.microsoft.com/networking/WLAN/policy/v1` 。</span><span class="sxs-lookup"><span data-stu-id="574c5-105">All of the named elements are in the namespace `https://www.microsoft.com/networking/WLAN/policy/v1`.</span></span>

<span data-ttu-id="574c5-106">下列清單以專案在設定檔中出現的順序顯示已定義的元素。</span><span class="sxs-lookup"><span data-stu-id="574c5-106">The following list shows the defined elements in the order in which the elements appear in a profile.</span></span> <span data-ttu-id="574c5-107">強制執行元素的順序。</span><span class="sxs-lookup"><span data-stu-id="574c5-107">The ordering of elements is enforced.</span></span> <span data-ttu-id="574c5-108">並非所有專案都在每個設定檔中，因為有些元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="574c5-108">Not all elements are in every profile, as some elements are optional.</span></span>

<span data-ttu-id="574c5-109">這份清單不會顯示所有可能出現在設定檔中的元素，因為可以在 **xs：任何** 插入點中加入元素。</span><span class="sxs-lookup"><span data-stu-id="574c5-109">This list does not show all possible elements that can appear in a profile, as elements can be added in **xs:any** insertion points.</span></span>

-   [<span data-ttu-id="574c5-110">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="574c5-110">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
    -   [<span data-ttu-id="574c5-111">**WLANPolicy) 名稱 (**</span><span class="sxs-lookup"><span data-stu-id="574c5-111">**name (WLANPolicy)**</span></span>](wlan-policyschema-name-wlanpolicy-element.md)
    -   [<span data-ttu-id="574c5-112">**描述 (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="574c5-112">**description (WLANPolicy)**</span></span>](wlan-policyschema-description-wlanpolicy-element.md)
    -   [<span data-ttu-id="574c5-113">**globalFlags (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="574c5-113">**globalFlags (WLANPolicy)**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
        -   [<span data-ttu-id="574c5-114">**enableAutoConfig (globalFlags)**</span><span class="sxs-lookup"><span data-stu-id="574c5-114">**enableAutoConfig (globalFlags)**</span></span>](wlan-policyschema-enableautoconfig-globalflags-element.md)
        -   [<span data-ttu-id="574c5-115">**showDeniedNetwork (globalFlags)**</span><span class="sxs-lookup"><span data-stu-id="574c5-115">**showDeniedNetwork (globalFlags)**</span></span>](wlan-policyschema-showdeniednetwork-globalflags-element.md)
        -   [<span data-ttu-id="574c5-116">**allowEveryoneToCreateAllUserProfiles (globalFlags)**</span><span class="sxs-lookup"><span data-stu-id="574c5-116">**allowEveryoneToCreateAllUserProfiles (globalFlags)**</span></span>](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md)
    -   [<span data-ttu-id="574c5-117">**networkFilter (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="574c5-117">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
        -   [<span data-ttu-id="574c5-118">**允許清單 (networkFilter)**</span><span class="sxs-lookup"><span data-stu-id="574c5-118">**allowList (networkFilter)**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)
            -   [<span data-ttu-id="574c5-119">**network (允許清單)**</span><span class="sxs-lookup"><span data-stu-id="574c5-119">**network (allowList)**</span></span>](wlan-policyschema-network-allowlist-element.md)
                -   [<span data-ttu-id="574c5-120">**networkName (networkItemType)**</span><span class="sxs-lookup"><span data-stu-id="574c5-120">**networkName (networkItemType)**</span></span>](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [<span data-ttu-id="574c5-121">**networkType (networkItemType)**</span><span class="sxs-lookup"><span data-stu-id="574c5-121">**networkType (networkItemType)**</span></span>](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [<span data-ttu-id="574c5-122">**封鎖清單 (networkFilter)**</span><span class="sxs-lookup"><span data-stu-id="574c5-122">**blockList (networkFilter)**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)
            -   [<span data-ttu-id="574c5-123">**network (封鎖清單)**</span><span class="sxs-lookup"><span data-stu-id="574c5-123">**network (blockList)**</span></span>](wlan-policyschema-network-blocklist-element.md)
                -   [<span data-ttu-id="574c5-124">**networkName (networkItemType)**</span><span class="sxs-lookup"><span data-stu-id="574c5-124">**networkName (networkItemType)**</span></span>](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [<span data-ttu-id="574c5-125">**networkType (networkItemType)**</span><span class="sxs-lookup"><span data-stu-id="574c5-125">**networkType (networkItemType)**</span></span>](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [<span data-ttu-id="574c5-126">**denyAllIBSS (networkFilter)**</span><span class="sxs-lookup"><span data-stu-id="574c5-126">**denyAllIBSS (networkFilter)**</span></span>](wlan-policyschema-denyallibss-networkfilter-element.md)
        -   [<span data-ttu-id="574c5-127">**denyAllESS (networkFilter)**</span><span class="sxs-lookup"><span data-stu-id="574c5-127">**denyAllESS (networkFilter)**</span></span>](wlan-policyschema-denyalless-networkfilter-element.md)
    -   [<span data-ttu-id="574c5-128">**profileList (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="574c5-128">**profileList (WLANPolicy)**</span></span>](wlan-policyschema-profilelist-wlanpolicy-element.md)

 

 



