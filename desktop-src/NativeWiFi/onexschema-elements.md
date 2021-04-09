---
description: 802.1 X 設定檔包含下列架構元素。
ms.assetid: be3f1986-d0c2-47f6-b4dd-8defb89bd03a
title: OneX 架構元素
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b7f3e7bac256b915d0e134720fc63b3519b21e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692947"
---
# <a name="onex-schema-elements"></a><span data-ttu-id="85993-103">OneX 架構元素</span><span class="sxs-lookup"><span data-stu-id="85993-103">OneX Schema Elements</span></span>

<span data-ttu-id="85993-104">802.1 X 設定檔包含下列架構元素。</span><span class="sxs-lookup"><span data-stu-id="85993-104">An 802.1X profile contains the following schema elements.</span></span> <span data-ttu-id="85993-105">所有的 OneX 架構元素都適用于有線和無線設定檔。</span><span class="sxs-lookup"><span data-stu-id="85993-105">All OneX schema elements apply to both wired and wireless profiles.</span></span> <span data-ttu-id="85993-106">`https://www.microsoft.com/networking/OneX/v1`除了命名空間中的 [**EAPConfig (OneX)**](onexschema-eapconfig-onex-element.md)之外，大部分的命名元素都位於命名空間中 `https://www.microsoft.com/provisioning/EapHostConfig` 。</span><span class="sxs-lookup"><span data-stu-id="85993-106">Most of the named elements are in the namespace `https://www.microsoft.com/networking/OneX/v1`, except for [**EAPConfig (OneX)**](onexschema-eapconfig-onex-element.md) which is in the namespace `https://www.microsoft.com/provisioning/EapHostConfig`.</span></span>

<span data-ttu-id="85993-107">下列清單以專案在設定檔中出現的順序顯示已定義的元素。</span><span class="sxs-lookup"><span data-stu-id="85993-107">The following list shows the defined elements in the order in which the elements appear in a profile.</span></span> <span data-ttu-id="85993-108">強制執行元素的順序。</span><span class="sxs-lookup"><span data-stu-id="85993-108">The ordering of elements is enforced.</span></span> <span data-ttu-id="85993-109">並非所有專案都在每個設定檔中，因為有些元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="85993-109">Not all elements are in every profile, as some elements are optional.</span></span>

<span data-ttu-id="85993-110">這份清單不會顯示所有可能出現在設定檔中的元素，因為可以在 **xs：任何** 插入點中加入元素。</span><span class="sxs-lookup"><span data-stu-id="85993-110">This list does not show all possible elements that can appear in a profile, as elements can be added in **xs:any** insertion points.</span></span>

-   [<span data-ttu-id="85993-111">**OneX**</span><span class="sxs-lookup"><span data-stu-id="85993-111">**OneX**</span></span>](onexschema-onex-element.md)
    -   [<span data-ttu-id="85993-112">**cacheUserData (OneX)**</span><span class="sxs-lookup"><span data-stu-id="85993-112">**cacheUserData (OneX)**</span></span>](onexschema-cacheuserdata-onex-element.md)
    -   [<span data-ttu-id="85993-113">**heldPeriod (OneX)**</span><span class="sxs-lookup"><span data-stu-id="85993-113">**heldPeriod (OneX)**</span></span>](onexschema-heldperiod-onex-element.md)
    -   [<span data-ttu-id="85993-114">**authPeriod (OneX)**</span><span class="sxs-lookup"><span data-stu-id="85993-114">**authPeriod (OneX)**</span></span>](onexschema-authperiod-onex-element.md)
    -   [<span data-ttu-id="85993-115">**startPeriod (OneX)**</span><span class="sxs-lookup"><span data-stu-id="85993-115">**startPeriod (OneX)**</span></span>](onexschema-startperiod-onex-element.md)
    -   [<span data-ttu-id="85993-116">**maxStart (OneX)**</span><span class="sxs-lookup"><span data-stu-id="85993-116">**maxStart (OneX)**</span></span>](onexschema-maxstart-onex-element.md)
    -   [<span data-ttu-id="85993-117">**maxAuthFailures (OneX)**</span><span class="sxs-lookup"><span data-stu-id="85993-117">**maxAuthFailures (OneX)**</span></span>](onexschema-maxauthfailures-onex-element.md)
    -   [<span data-ttu-id="85993-118">**supplicantMode (OneX)**</span><span class="sxs-lookup"><span data-stu-id="85993-118">**supplicantMode (OneX)**</span></span>](onexschema-supplicantmode-onex-element.md)
    -   [<span data-ttu-id="85993-119">**authMode (OneX)**</span><span class="sxs-lookup"><span data-stu-id="85993-119">**authMode (OneX)**</span></span>](onexschema-authmode-onex-element.md)
    -   [<span data-ttu-id="85993-120">**singleSignOn (OneX)**</span><span class="sxs-lookup"><span data-stu-id="85993-120">**singleSignOn (OneX)**</span></span>](onexschema-singlesignon-onex-element.md)
        -   [<span data-ttu-id="85993-121">**輸入 (singleSignOn)**</span><span class="sxs-lookup"><span data-stu-id="85993-121">**type (singleSignOn)**</span></span>](onexschema-type-singlesignon-element.md)
        -   [<span data-ttu-id="85993-122">**maxDelay (singleSignOn)**</span><span class="sxs-lookup"><span data-stu-id="85993-122">**maxDelay (singleSignOn)**</span></span>](onexschema-maxdelay-singlesignon-element.md)
        -   [<span data-ttu-id="85993-123">**userBasedVirtualLan (singleSignOn)**</span><span class="sxs-lookup"><span data-stu-id="85993-123">**userBasedVirtualLan (singleSignOn)**</span></span>](onexschema-userbasedvirtuallan-singlesignon-element.md)
    -   [<span data-ttu-id="85993-124">**EAPConfig (OneX)**</span><span class="sxs-lookup"><span data-stu-id="85993-124">**EAPConfig (OneX)**</span></span>](onexschema-eapconfig-onex-element.md)

 

 



