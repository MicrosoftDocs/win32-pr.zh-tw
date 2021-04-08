---
description: 如果您的網路提供者需要支援流覽其網路資源，它應該會執行下列功能。 MPR 會呼叫這些函式來列舉資源。
ms.assetid: 9f7c0e5b-1358-43f8-84e4-26e84a2275ba
title: 列舉函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2670424be1540aad3e46e32c5b0606eb02e04bdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026158"
---
# <a name="enumeration-functions"></a><span data-ttu-id="72bd9-104">列舉函數</span><span class="sxs-lookup"><span data-stu-id="72bd9-104">Enumeration Functions</span></span>

<span data-ttu-id="72bd9-105">如果您的網路提供者需要支援流覽其網路資源，它應該會執行下列功能。</span><span class="sxs-lookup"><span data-stu-id="72bd9-105">If your network provider needs to support browsing of its network resources, it should implement the following functions.</span></span> <span data-ttu-id="72bd9-106">MPR 會呼叫這些函式來列舉資源。</span><span class="sxs-lookup"><span data-stu-id="72bd9-106">MPR calls these functions to enumerate the resources.</span></span>

<span data-ttu-id="72bd9-107">不需要網路提供者來執行任何列舉函數。</span><span class="sxs-lookup"><span data-stu-id="72bd9-107">A network provider is not required to implement any of the enumeration functions.</span></span> <span data-ttu-id="72bd9-108">但是，如果網路提供者執行的是 [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum)、 [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)或 [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum)，則也必須執行其他兩個列舉函數。</span><span class="sxs-lookup"><span data-stu-id="72bd9-108">If, however, a network provider implements either [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum), [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource), or [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum), it must also implement the other two enumeration functions.</span></span>



| <span data-ttu-id="72bd9-109">函式</span><span class="sxs-lookup"><span data-stu-id="72bd9-109">Function</span></span>                                                     | <span data-ttu-id="72bd9-110">描述</span><span class="sxs-lookup"><span data-stu-id="72bd9-110">Description</span></span>                                                                                                                                                         |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72bd9-111">**NPOpenEnum**</span><span class="sxs-lookup"><span data-stu-id="72bd9-111">**NPOpenEnum**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npopenenum)                             | <span data-ttu-id="72bd9-112">開啟網路資源或現有連接的列舉。</span><span class="sxs-lookup"><span data-stu-id="72bd9-112">Opens an enumeration of network resources or existing connections.</span></span>                                                                                                  |
| [<span data-ttu-id="72bd9-113">**NPEnumResource**</span><span class="sxs-lookup"><span data-stu-id="72bd9-113">**NPEnumResource**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npenumresource)                     | <span data-ttu-id="72bd9-114">在 [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum)所傳回的控制碼上執行列舉。</span><span class="sxs-lookup"><span data-stu-id="72bd9-114">Performs an enumeration on a handle returned by [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum).</span></span>                                                                                   |
| [<span data-ttu-id="72bd9-115">**NPCloseEnum**</span><span class="sxs-lookup"><span data-stu-id="72bd9-115">**NPCloseEnum**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npcloseenum)                           | <span data-ttu-id="72bd9-116">關閉列舉。</span><span class="sxs-lookup"><span data-stu-id="72bd9-116">Closes an enumeration.</span></span>                                                                                                                                              |
| [<span data-ttu-id="72bd9-117">**NPGetResourceInformation**</span><span class="sxs-lookup"><span data-stu-id="72bd9-117">**NPGetResourceInformation**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetresourceinformation) | <span data-ttu-id="72bd9-118">判斷提供者是否為回應指定網路資源之要求的正確提供者，並傳回資源類型的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="72bd9-118">Determines whether the provider is the correct provider to respond to a request for a specified network resource and returns information about the resource's type.</span></span> |
| [<span data-ttu-id="72bd9-119">**NPGetResourceParent**</span><span class="sxs-lookup"><span data-stu-id="72bd9-119">**NPGetResourceParent**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetresourceparent)           | <span data-ttu-id="72bd9-120">傳回流覽階層中指定之網路資源的父系。</span><span class="sxs-lookup"><span data-stu-id="72bd9-120">Returns the parent of a specified network resource in the browse hierarchy.</span></span>                                                                                         |



 

 

 



