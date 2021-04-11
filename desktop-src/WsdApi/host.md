---
description: 定義服務主機的 ServiceID 和 Types 元素。
ms.assetid: 95066c04-5bdc-4c97-98b8-1da9928d9395
title: host 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec073a89cf1911ab363d757d36cd264c85c8a5c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848728"
---
# <a name="host-element"></a><span data-ttu-id="50ac8-103">host 元素</span><span class="sxs-lookup"><span data-stu-id="50ac8-103">host element</span></span>

<span data-ttu-id="50ac8-104">定義服務主機的 [**ServiceID**](serviceid.md) 和 [**Types**](types.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="50ac8-104">Defines the [**ServiceID**](serviceid.md) and [**Types**](types.md) elements for the service host.</span></span>

## <a name="usage"></a><span data-ttu-id="50ac8-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="50ac8-105">Usage</span></span>

``` syntax
<host>
  child elements
</host>
```

## <a name="attributes"></a><span data-ttu-id="50ac8-106">屬性</span><span class="sxs-lookup"><span data-stu-id="50ac8-106">Attributes</span></span>

<span data-ttu-id="50ac8-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="50ac8-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="50ac8-108">子元素</span><span class="sxs-lookup"><span data-stu-id="50ac8-108">Child elements</span></span>



| <span data-ttu-id="50ac8-109">元素</span><span class="sxs-lookup"><span data-stu-id="50ac8-109">Element</span></span>                                   | <span data-ttu-id="50ac8-110">描述</span><span class="sxs-lookup"><span data-stu-id="50ac8-110">Description</span></span>                                                                 |
|-------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="50ac8-111">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="50ac8-111">**ServiceID**</span></span>](serviceid.md)<br/> | <span data-ttu-id="50ac8-112">定義服務主機的服務識別碼。</span><span class="sxs-lookup"><span data-stu-id="50ac8-112">Defines the service identifier for the service host.</span></span><br/> <br/> |
| [<span data-ttu-id="50ac8-113">**類型**</span><span class="sxs-lookup"><span data-stu-id="50ac8-113">**Types**</span></span>](types.md)<br/>         | <span data-ttu-id="50ac8-114">定義 XSD 限定名稱的清單。</span><span class="sxs-lookup"><span data-stu-id="50ac8-114">Defines a list of XSD qualified names.</span></span><br/> <br/>               |



### <a name="child-element-sequence"></a><span data-ttu-id="50ac8-115">子項目順序</span><span class="sxs-lookup"><span data-stu-id="50ac8-115">Child element sequence</span></span>

``` syntax
(
  ServiceID, 
  Types
)
```

## <a name="parent-elements"></a><span data-ttu-id="50ac8-116">父元素</span><span class="sxs-lookup"><span data-stu-id="50ac8-116">Parent elements</span></span>



| <span data-ttu-id="50ac8-117">元素</span><span class="sxs-lookup"><span data-stu-id="50ac8-117">Element</span></span>                                         | <span data-ttu-id="50ac8-118">描述</span><span class="sxs-lookup"><span data-stu-id="50ac8-118">Description</span></span>                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="50ac8-119">**hostMetadata**</span><span class="sxs-lookup"><span data-stu-id="50ac8-119">**hostMetadata**</span></span>](hostmetadata.md)<br/> | <span data-ttu-id="50ac8-120">要執行之裝置的裝載中繼資料。</span><span class="sxs-lookup"><span data-stu-id="50ac8-120">The hosting metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="50ac8-121">項目資訊</span><span class="sxs-lookup"><span data-stu-id="50ac8-121">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="50ac8-122">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="50ac8-122">Minimum supported system</span></span><br/> | <span data-ttu-id="50ac8-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="50ac8-123">Windows Vista</span></span> |
| <span data-ttu-id="50ac8-124">可以是空的</span><span class="sxs-lookup"><span data-stu-id="50ac8-124">Can be empty</span></span>                        | <span data-ttu-id="50ac8-125">否</span><span class="sxs-lookup"><span data-stu-id="50ac8-125">No</span></span>            |



 

 




