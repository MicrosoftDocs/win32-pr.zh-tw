---
description: 定義 802.1 X 設定元素。
ms.assetid: 4755356e-cb4b-4eed-a494-ca0d17f5184f
title: OneX 架構
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9df45ed7981c055e955afe72333a42db99ddb21a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192642"
---
# <a name="onex-schema"></a><span data-ttu-id="87528-103">OneX 架構</span><span class="sxs-lookup"><span data-stu-id="87528-103">OneX Schema</span></span>

<span data-ttu-id="87528-104">OneX 架構會定義 802.1 X 設定元素。</span><span class="sxs-lookup"><span data-stu-id="87528-104">The OneX Schema defines 802.1X configuration elements.</span></span> <span data-ttu-id="87528-105">所有的 OneX 架構元素都適用于有線和無線設定檔。</span><span class="sxs-lookup"><span data-stu-id="87528-105">All OneX schema elements apply to both wired and wireless profiles.</span></span> <span data-ttu-id="87528-106">如需定義的元素清單，請參閱 [OneX Schema elements](onexschema-elements.md)。</span><span class="sxs-lookup"><span data-stu-id="87528-106">For a list of defined elements, see [OneX Schema Elements](onexschema-elements.md).</span></span>

<span data-ttu-id="87528-107">802.1 X 設定檔的根項目是 [**OneX**](onexschema-onex-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="87528-107">The root element of an 802.1X profile is the [**OneX**](onexschema-onex-element.md) element.</span></span> <span data-ttu-id="87528-108">每個設定檔都只會有一個根項目。</span><span class="sxs-lookup"><span data-stu-id="87528-108">Each profile will have exactly one root element.</span></span> <span data-ttu-id="87528-109">**OneX** 元素位於 `https://www.microsoft.com/networking/OneX/v1` 命名空間中。</span><span class="sxs-lookup"><span data-stu-id="87528-109">The **OneX** element is in the `https://www.microsoft.com/networking/OneX/v1` namespace.</span></span>

<span data-ttu-id="87528-110">若要查看包含 802.1 X configuration 元素之無線網路的範例設定檔，請參閱下列設定檔範例：</span><span class="sxs-lookup"><span data-stu-id="87528-110">To view sample profiles for wireless networks that include 802.1X configuration elements, see the following profile samples:</span></span>

-   [<span data-ttu-id="87528-111">啟動程式設定檔範例</span><span class="sxs-lookup"><span data-stu-id="87528-111">Bootstrap Profile Sample</span></span>](bootstrap-profile-sample.md)
-   [<span data-ttu-id="87528-112">FIPS 設定檔範例</span><span class="sxs-lookup"><span data-stu-id="87528-112">FIPS Profile Sample</span></span>](fips-profile-sample.md)
-   [<span data-ttu-id="87528-113">單一 Sign-On 設定檔範例</span><span class="sxs-lookup"><span data-stu-id="87528-113">Single Sign-On Profile Sample</span></span>](single-sign-on-profile-sample.md)
-   [<span data-ttu-id="87528-114">具有 PEAP-MSCHAPv2 設定檔的 WPA-Enterprise 範例</span><span class="sxs-lookup"><span data-stu-id="87528-114">WPA-Enterprise with PEAP-MSCHAPv2 Profile Sample</span></span>](wpa-enterprise-with-peap-mschapv2-profile-sample.md)
-   [<span data-ttu-id="87528-115">具備 TLS 設定檔的 WPA-Enterprise 範例</span><span class="sxs-lookup"><span data-stu-id="87528-115">WPA-Enterprise with TLS Profile Sample</span></span>](wpa-enterprise-with-tls-profile-sample.md)
-   [<span data-ttu-id="87528-116">具有 PEAP-MSCHAPv2 設定檔的 WPA2 Enterprise 範例</span><span class="sxs-lookup"><span data-stu-id="87528-116">WPA2-Enterprise with PEAP-MSCHAPv2 Profile Sample</span></span>](wpa2-enterprise-with-peap-mschapv2-profile-sample.md)
-   [<span data-ttu-id="87528-117">具有 TLS 設定檔的 WPA2 Enterprise 範例</span><span class="sxs-lookup"><span data-stu-id="87528-117">WPA2-Enterprise with TLS Profile Sample</span></span>](wpa2-enterprise-with-tls-profile-sample.md)

<span data-ttu-id="87528-118">若要查看包含 802.1 X 設定元素的有線網路範例設定檔，請參閱下列設定檔範例：</span><span class="sxs-lookup"><span data-stu-id="87528-118">To view sample profiles for wired networks that include 802.1X configuration elements, see the following profile samples:</span></span>

-   [<span data-ttu-id="87528-119">電腦憑證設定檔範例</span><span class="sxs-lookup"><span data-stu-id="87528-119">Machine Certificate Profile Sample</span></span>](machine-certificate-profile-sample.md)
-   [<span data-ttu-id="87528-120">PEAP 設定檔範例</span><span class="sxs-lookup"><span data-stu-id="87528-120">PEAP Profile Sample</span></span>](peap-profile-sample.md)
-   [<span data-ttu-id="87528-121">智慧卡憑證範例設定檔</span><span class="sxs-lookup"><span data-stu-id="87528-121">Smart Card Certificate Sample Profile</span></span>](smart-card-certificate-profile-sample.md)

 

 



