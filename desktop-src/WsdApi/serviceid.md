---
description: 表示服務識別碼的 URI。
ms.assetid: ef676f02-56a7-4b3a-9ca3-e7fa3c494ec7
title: ServiceID 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4c8b02fa8ecfa936aa658a1f18242e4f14eb0dd
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995105"
---
# <a name="serviceid-element"></a><span data-ttu-id="ad9a5-103">ServiceID 元素</span><span class="sxs-lookup"><span data-stu-id="ad9a5-103">ServiceID element</span></span>

<span data-ttu-id="ad9a5-104">表示服務識別碼的 URI。</span><span class="sxs-lookup"><span data-stu-id="ad9a5-104">A URI that represents the service identifier.</span></span>

## <a name="usage"></a><span data-ttu-id="ad9a5-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="ad9a5-105">Usage</span></span>

``` syntax
<ServiceID/>
```

## <a name="attributes"></a><span data-ttu-id="ad9a5-106">屬性</span><span class="sxs-lookup"><span data-stu-id="ad9a5-106">Attributes</span></span>

<span data-ttu-id="ad9a5-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="ad9a5-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ad9a5-108">子元素</span><span class="sxs-lookup"><span data-stu-id="ad9a5-108">Child elements</span></span>

<span data-ttu-id="ad9a5-109">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="ad9a5-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="ad9a5-110">父元素</span><span class="sxs-lookup"><span data-stu-id="ad9a5-110">Parent elements</span></span>



| <span data-ttu-id="ad9a5-111">元素</span><span class="sxs-lookup"><span data-stu-id="ad9a5-111">Element</span></span>                             | <span data-ttu-id="ad9a5-112">描述</span><span class="sxs-lookup"><span data-stu-id="ad9a5-112">Description</span></span>                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ad9a5-113">**主機**</span><span class="sxs-lookup"><span data-stu-id="ad9a5-113">**host**</span></span>](host.md)<br/>     | <span data-ttu-id="ad9a5-114">定義服務主機的 **ServiceID** 和 [**Types**](types.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="ad9a5-114">Defines the **ServiceID** and [**Types**](types.md) elements for the service host.</span></span> <span data-ttu-id="ad9a5-115">如果未明確提供，則 WSDAPI 不會提供任何預設資料來回應中繼資料要求。</span><span class="sxs-lookup"><span data-stu-id="ad9a5-115">If not provided explicitly, WSDAPI will not supply any default data in response to metadata requests.</span></span><br/> <br/>                                                                                                                     |
| [<span data-ttu-id="ad9a5-116">**託管**</span><span class="sxs-lookup"><span data-stu-id="ad9a5-116">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="ad9a5-117">定義此服務主機所提供之服務的 **ServiceID** 和 [**Types**](types.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="ad9a5-117">Defines the **ServiceID** and [**Types**](types.md) elements for the services provided by this service host.</span></span> <span data-ttu-id="ad9a5-118">這項服務主機提供的每個服務都應該有自己的 [**託管**](hosted.md) 元素資訊，以確保服務在對中繼資料要求的回應中已正確發佈。</span><span class="sxs-lookup"><span data-stu-id="ad9a5-118">Each service provided by this service host should have its own [**hosted**](hosted.md) element information to ensure that the service is published properly in responses to metadata requests.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="ad9a5-119">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ad9a5-119">Element information</span></span>



| <span data-ttu-id="ad9a5-120">標籤</span><span class="sxs-lookup"><span data-stu-id="ad9a5-120">Label</span></span> | <span data-ttu-id="ad9a5-121">值</span><span class="sxs-lookup"><span data-stu-id="ad9a5-121">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="ad9a5-122">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="ad9a5-122">Minimum supported system</span></span><br/> | <span data-ttu-id="ad9a5-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ad9a5-123">Windows Vista</span></span> |
| <span data-ttu-id="ad9a5-124">可以是空的</span><span class="sxs-lookup"><span data-stu-id="ad9a5-124">Can be empty</span></span>                        | <span data-ttu-id="ad9a5-125">是</span><span class="sxs-lookup"><span data-stu-id="ad9a5-125">Yes</span></span>           |



 

 




