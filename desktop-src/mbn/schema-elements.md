---
description: 行動寬頻 v1 設定檔是由下列元素所組成。
ms.assetid: 234dd206-7306-4598-bfbb-b0cd9d726ace
title: Mobile 寬頻設定檔架構 v1 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4b92e9b1fd9daf3cf843e769a0782f5f1ce1848
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972649"
---
# <a name="mobile-broadband-profile-schema-v1-elements"></a><span data-ttu-id="a2779-103">Mobile 寬頻設定檔架構 v1 元素</span><span class="sxs-lookup"><span data-stu-id="a2779-103">Mobile Broadband Profile Schema v1 Elements</span></span>

<span data-ttu-id="a2779-104">行動寬頻 v1 設定檔是由下列元素所組成。</span><span class="sxs-lookup"><span data-stu-id="a2779-104">A Mobile Broadband v1 Profile is comprised of the following elements.</span></span> <span data-ttu-id="a2779-105">所有命名的元素都位於命名空間中 `https://www.microsoft.com/networking/WWAN/profile/v1` 。</span><span class="sxs-lookup"><span data-stu-id="a2779-105">All of the named elements are in the namespace `https://www.microsoft.com/networking/WWAN/profile/v1`.</span></span>

-   [<span data-ttu-id="a2779-106">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="a2779-106">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
    -   [<span data-ttu-id="a2779-107">**AutoConnectOnInternet (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="a2779-107">**AutoConnectOnInternet (MBNProfile)**</span></span>](schema-autoconnectoninternet-mbnprofile-element.md)
    -   [<span data-ttu-id="a2779-108">**ConnectionMode (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="a2779-108">**ConnectionMode (MBNProfile)**</span></span>](schema-connectionmode-mbnprofile-element.md)
    -   [<span data-ttu-id="a2779-109">**MBNProfile) 內容 (**</span><span class="sxs-lookup"><span data-stu-id="a2779-109">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
        -   [<span data-ttu-id="a2779-110">**AccessString (coNtextType)**</span><span class="sxs-lookup"><span data-stu-id="a2779-110">**AccessString (contextType)**</span></span>](schema-accessstring-contexttype-element.md)
        -   [<span data-ttu-id="a2779-111">**AuthProtocol (coNtextType)**</span><span class="sxs-lookup"><span data-stu-id="a2779-111">**AuthProtocol (contextType)**</span></span>](schema-authprotocol-contexttype-element.md)
        -   [<span data-ttu-id="a2779-112">**壓縮 (coNtextType)**</span><span class="sxs-lookup"><span data-stu-id="a2779-112">**Compression (contextType)**</span></span>](schema-compression-contexttype-element.md)
        -   [<span data-ttu-id="a2779-113">**UserLogonCred (coNtextType)**</span><span class="sxs-lookup"><span data-stu-id="a2779-113">**UserLogonCred (contextType)**</span></span>](schema-userlogoncred-contexttype-element.md)
            -   [<span data-ttu-id="a2779-114">**IgnorePassword (UserLogonCred)**</span><span class="sxs-lookup"><span data-stu-id="a2779-114">**IgnorePassword (UserLogonCred)**</span></span>](schema-ignorepassword-userlogoncred-element.md)
            -   [<span data-ttu-id="a2779-115">**密碼 (UserLogonCred)**</span><span class="sxs-lookup"><span data-stu-id="a2779-115">**Password (UserLogonCred)**</span></span>](schema-password-userlogoncred-element.md)
            -   [<span data-ttu-id="a2779-116">**UserName (UserLogonCred)**</span><span class="sxs-lookup"><span data-stu-id="a2779-116">**UserName (UserLogonCred)**</span></span>](schema-username-userlogoncred-element.md)
    -   [<span data-ttu-id="a2779-117">**DataRoamingPartners (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="a2779-117">**DataRoamingPartners (MBNProfile)**</span></span>](schema-dataroamingpartners-mbnprofile-element.md)
        -   [<span data-ttu-id="a2779-118">**提供者 (DataRoamingPartners)**</span><span class="sxs-lookup"><span data-stu-id="a2779-118">**Provider (DataRoamingPartners)**</span></span>](schema-provider-dataroamingpartners-element.md)
            -   [<span data-ttu-id="a2779-119">**ProviderID (providerType)**</span><span class="sxs-lookup"><span data-stu-id="a2779-119">**ProviderID (providerType)**</span></span>](schema-providerid-providertype-element.md)
            -   [<span data-ttu-id="a2779-120">**ProviderName (providerType)**</span><span class="sxs-lookup"><span data-stu-id="a2779-120">**ProviderName (providerType)**</span></span>](schema-providername-providertype-element.md)
    -   [<span data-ttu-id="a2779-121">**描述 (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="a2779-121">**Description (MBNProfile)**</span></span>](schema-description-mbnprofile-element.md)
    -   [<span data-ttu-id="a2779-122">**HomeProviderName (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="a2779-122">**HomeProviderName (MBNProfile)**</span></span>](schema-homeprovidername-mbnprofile-element.md)
    -   [<span data-ttu-id="a2779-123">**ICONFilePath (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="a2779-123">**ICONFilePath (MBNProfile)**</span></span>](schema-iconfilepath-mbnprofile-element.md)
    -   [<span data-ttu-id="a2779-124">**IsDefault (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="a2779-124">**IsDefault (MBNProfile)**</span></span>](schema-isdefault-mbnprofile-element.md)
    -   [<span data-ttu-id="a2779-125">**MBNProfile) 名稱 (**</span><span class="sxs-lookup"><span data-stu-id="a2779-125">**Name (MBNProfile)**</span></span>](schema-name-mbnprofile-element.md)
    -   [<span data-ttu-id="a2779-126">**ProfileCreationType (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="a2779-126">**ProfileCreationType (MBNProfile)**</span></span>](schema-profilecreationtype-mbnprofile-element.md)
    -   [<span data-ttu-id="a2779-127">**SimIccID (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="a2779-127">**SimIccID (MBNProfile)**</span></span>](schema-simiccid-mbnprofile-element.md)
    -   [<span data-ttu-id="a2779-128">**SubscriberID (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="a2779-128">**SubscriberID (MBNProfile)**</span></span>](schema-subscriberid-mbnprofile-element.md)

 

 



