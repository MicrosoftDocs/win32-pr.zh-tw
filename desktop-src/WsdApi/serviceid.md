---
description: 表示服務識別碼的 URI。
ms.assetid: ef676f02-56a7-4b3a-9ca3-e7fa3c494ec7
title: ServiceID 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305e97250b0b33d276dced4b5d454aec9298387c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991929"
---
# <a name="serviceid-element"></a><span data-ttu-id="9bbf2-103">ServiceID 元素</span><span class="sxs-lookup"><span data-stu-id="9bbf2-103">ServiceID element</span></span>

<span data-ttu-id="9bbf2-104">表示服務識別碼的 URI。</span><span class="sxs-lookup"><span data-stu-id="9bbf2-104">A URI that represents the service identifier.</span></span>

## <a name="usage"></a><span data-ttu-id="9bbf2-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="9bbf2-105">Usage</span></span>

``` syntax
<ServiceID/>
```

## <a name="attributes"></a><span data-ttu-id="9bbf2-106">屬性</span><span class="sxs-lookup"><span data-stu-id="9bbf2-106">Attributes</span></span>

<span data-ttu-id="9bbf2-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="9bbf2-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9bbf2-108">子元素</span><span class="sxs-lookup"><span data-stu-id="9bbf2-108">Child elements</span></span>

<span data-ttu-id="9bbf2-109">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="9bbf2-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="9bbf2-110">父元素</span><span class="sxs-lookup"><span data-stu-id="9bbf2-110">Parent elements</span></span>



| <span data-ttu-id="9bbf2-111">元素</span><span class="sxs-lookup"><span data-stu-id="9bbf2-111">Element</span></span>                             | <span data-ttu-id="9bbf2-112">描述</span><span class="sxs-lookup"><span data-stu-id="9bbf2-112">Description</span></span>                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9bbf2-113">**主機**</span><span class="sxs-lookup"><span data-stu-id="9bbf2-113">**host**</span></span>](host.md)<br/>     | <span data-ttu-id="9bbf2-114">定義服務主機的 **ServiceID** 和 [**Types**](types.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="9bbf2-114">Defines the **ServiceID** and [**Types**](types.md) elements for the service host.</span></span> <span data-ttu-id="9bbf2-115">如果未明確提供，則 WSDAPI 不會提供任何預設資料來回應中繼資料要求。</span><span class="sxs-lookup"><span data-stu-id="9bbf2-115">If not provided explicitly, WSDAPI will not supply any default data in response to metadata requests.</span></span><br/> <br/>                                                                                                                     |
| [<span data-ttu-id="9bbf2-116">**託管**</span><span class="sxs-lookup"><span data-stu-id="9bbf2-116">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="9bbf2-117">定義此服務主機所提供之服務的 **ServiceID** 和 [**Types**](types.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="9bbf2-117">Defines the **ServiceID** and [**Types**](types.md) elements for the services provided by this service host.</span></span> <span data-ttu-id="9bbf2-118">這項服務主機提供的每個服務都應該有自己的 [**託管**](hosted.md) 元素資訊，以確保服務在對中繼資料要求的回應中已正確發佈。</span><span class="sxs-lookup"><span data-stu-id="9bbf2-118">Each service provided by this service host should have its own [**hosted**](hosted.md) element information to ensure that the service is published properly in responses to metadata requests.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="9bbf2-119">項目資訊</span><span class="sxs-lookup"><span data-stu-id="9bbf2-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="9bbf2-120">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="9bbf2-120">Minimum supported system</span></span><br/> | <span data-ttu-id="9bbf2-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9bbf2-121">Windows Vista</span></span> |
| <span data-ttu-id="9bbf2-122">可以是空的</span><span class="sxs-lookup"><span data-stu-id="9bbf2-122">Can be empty</span></span>                        | <span data-ttu-id="9bbf2-123">是</span><span class="sxs-lookup"><span data-stu-id="9bbf2-123">Yes</span></span>           |



 

 




