---
title: " (UPnP Api) "
description: 包含以字母 S 開頭的 UPnP 相關詞彙。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 94be0f7f-8263-40ad-9d48-35540eaa3a3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9386d7946c51bc02e78aa96c36063d22d75d61d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024442"
---
# <a name="s-upnp-apis"></a><span data-ttu-id="8c5c9-103"> (UPnP Api) </span><span class="sxs-lookup"><span data-stu-id="8c5c9-103">S (UPnP APIs)</span></span>

<span data-ttu-id="8c5c9-104">包含以字母 S 開頭的 UPnP 相關詞彙。</span><span class="sxs-lookup"><span data-stu-id="8c5c9-104">Contains UPnP-related terms that begin with the letter S.</span></span>

<span data-ttu-id="8c5c9-105">[B](a-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F G [H](h-gly.md) I J K L M [N](n-gly.md) O [P](p-gly.md) Q [R](r-gly.md) S T W [](u-gly.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="8c5c9-105">[A](a-gly.md) B [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F G [H](h-gly.md) I J K L M [N](n-gly.md) O [P](p-gly.md) Q [R](r-gly.md) S T [U](u-gly.md) V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="8c5c9-106"><span id="upnp.s_1_gly"></span><span id="UPNP.S_1_GLY"></span>**服務**</span><span class="sxs-lookup"><span data-stu-id="8c5c9-106"><span id="upnp.s_1_gly"></span><span id="UPNP.S_1_GLY"></span>**service**</span></span>
</dt> <dd>

<span data-ttu-id="8c5c9-107">服務是邏輯功能單位。</span><span class="sxs-lookup"><span data-stu-id="8c5c9-107">A service is a logical functional unit.</span></span> <span data-ttu-id="8c5c9-108">服務會使用狀態變數來公開動作，並為實體裝置的部分或所有狀態建立模型。</span><span class="sxs-lookup"><span data-stu-id="8c5c9-108">Services expose actions and model some or all of the states of a physical device using state variables.</span></span>

</dd> <dt>

<span data-ttu-id="8c5c9-109"><span id="upnp.s_2_gly"></span><span id="UPNP.S_2_GLY"></span>**服務描述**</span><span class="sxs-lookup"><span data-stu-id="8c5c9-109"><span id="upnp.s_2_gly"></span><span id="UPNP.S_2_GLY"></span>**service description**</span></span>
</dt> <dd>

<span data-ttu-id="8c5c9-110">服務描述是服務所提供的動作清單，以及與動作相關聯的狀態變數。</span><span class="sxs-lookup"><span data-stu-id="8c5c9-110">A service description is a list of the actions a service provides, and the state variables associated with the actions.</span></span>

</dd> <dt>

<span data-ttu-id="8c5c9-111"><span id="upnp.s_3_gly"></span><span id="UPNP.S_3_GLY"></span>**服務物件**</span><span class="sxs-lookup"><span data-stu-id="8c5c9-111"><span id="upnp.s_3_gly"></span><span id="UPNP.S_3_GLY"></span>**service object**</span></span>
</dt> <dd>

<span data-ttu-id="8c5c9-112">服務物件是服務的控制點 API 標記法。</span><span class="sxs-lookup"><span data-stu-id="8c5c9-112">A service object is the Control Point API representation of a service.</span></span> <span data-ttu-id="8c5c9-113">服務物件會執行 [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) 介面。</span><span class="sxs-lookup"><span data-stu-id="8c5c9-113">A service object implements the [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) interface.</span></span>

</dd> <dt>

<span data-ttu-id="8c5c9-114"><span id="upnp.s_4_gly"></span><span id="UPNP.S_4_GLY"></span>**服務類型**</span><span class="sxs-lookup"><span data-stu-id="8c5c9-114"><span id="upnp.s_4_gly"></span><span id="UPNP.S_4_GLY"></span>**service type**</span></span>
</dt> <dd>

<span data-ttu-id="8c5c9-115">服務類型是用來識別服務的 URN。</span><span class="sxs-lookup"><span data-stu-id="8c5c9-115">A service type is a URN that identifies a service.</span></span> <span data-ttu-id="8c5c9-116">UPnP 服務範本與服務類型之間有一對一的關聯性。</span><span class="sxs-lookup"><span data-stu-id="8c5c9-116">There is a one-to-one relationship between a UPnP service template and a service type.</span></span> <span data-ttu-id="8c5c9-117">UPnP 論壇工作委員會定義了數種標準服務類型。</span><span class="sxs-lookup"><span data-stu-id="8c5c9-117">Several standard service types are defined by the UPnP Forum working committees.</span></span> <span data-ttu-id="8c5c9-118">服務類型的格式為 urn：架構-upnp-org： service： serviceType： version。</span><span class="sxs-lookup"><span data-stu-id="8c5c9-118">The service types are in the form urn:schemas-upnp-org:service:serviceType:version.</span></span> <span data-ttu-id="8c5c9-119">例如，掃描器服務類型可能是 urn：架構-upnp-org： service：掃描器：1。</span><span class="sxs-lookup"><span data-stu-id="8c5c9-119">For example, a scanner service type could be urn:schemas-upnp-org:service:scanner:1.</span></span>

<span data-ttu-id="8c5c9-120">UPnP 廠商可指定額外的服務。</span><span class="sxs-lookup"><span data-stu-id="8c5c9-120">UPnP vendors may specify additional services.</span></span> <span data-ttu-id="8c5c9-121">這類服務是以 urn： domain name： service： serviceType：版本表示，其中的功能變數名稱是向廠商註冊的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="8c5c9-121">Such services are denoted by urn:domain-name:service:serviceType:version where domain-name is a domain name that is registered to the vendor.</span></span>

</dd> <dt>

<span data-ttu-id="8c5c9-122"><span id="upnp.s_5_gly"></span><span id="UPNP.S_5_GLY"></span>**狀態變數**</span><span class="sxs-lookup"><span data-stu-id="8c5c9-122"><span id="upnp.s_5_gly"></span><span id="UPNP.S_5_GLY"></span>**state variable**</span></span>
</dt> <dd>

<span data-ttu-id="8c5c9-123">狀態變數是一段資料，會描述服務狀態的某些部分。</span><span class="sxs-lookup"><span data-stu-id="8c5c9-123">A state variable is a piece of data that describes some part of a service's state.</span></span>

</dd> </dl>

 

 




