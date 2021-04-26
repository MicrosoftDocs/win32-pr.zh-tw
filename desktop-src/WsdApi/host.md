---
description: 定義服務主機的 ServiceID 和 Types 元素。
ms.assetid: 95066c04-5bdc-4c97-98b8-1da9928d9395
title: host 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9f051f6665715ecaa519a060e18a3cbf4912210
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993795"
---
# <a name="host-element"></a><span data-ttu-id="bf541-103">host 元素</span><span class="sxs-lookup"><span data-stu-id="bf541-103">host element</span></span>

<span data-ttu-id="bf541-104">定義服務主機的 [**ServiceID**](serviceid.md) 和 [**Types**](types.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="bf541-104">Defines the [**ServiceID**](serviceid.md) and [**Types**](types.md) elements for the service host.</span></span>

## <a name="usage"></a><span data-ttu-id="bf541-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="bf541-105">Usage</span></span>

``` syntax
<host>
  child elements
</host>
```

## <a name="attributes"></a><span data-ttu-id="bf541-106">屬性</span><span class="sxs-lookup"><span data-stu-id="bf541-106">Attributes</span></span>

<span data-ttu-id="bf541-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="bf541-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="bf541-108">子元素</span><span class="sxs-lookup"><span data-stu-id="bf541-108">Child elements</span></span>



| <span data-ttu-id="bf541-109">元素</span><span class="sxs-lookup"><span data-stu-id="bf541-109">Element</span></span>                                   | <span data-ttu-id="bf541-110">描述</span><span class="sxs-lookup"><span data-stu-id="bf541-110">Description</span></span>                                                                 |
|-------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="bf541-111">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="bf541-111">**ServiceID**</span></span>](serviceid.md)<br/> | <span data-ttu-id="bf541-112">定義服務主機的服務識別碼。</span><span class="sxs-lookup"><span data-stu-id="bf541-112">Defines the service identifier for the service host.</span></span><br/> <br/> |
| [<span data-ttu-id="bf541-113">**類型**</span><span class="sxs-lookup"><span data-stu-id="bf541-113">**Types**</span></span>](types.md)<br/>         | <span data-ttu-id="bf541-114">定義 XSD 限定名稱的清單。</span><span class="sxs-lookup"><span data-stu-id="bf541-114">Defines a list of XSD qualified names.</span></span><br/> <br/>               |



### <a name="child-element-sequence"></a><span data-ttu-id="bf541-115">子項目順序</span><span class="sxs-lookup"><span data-stu-id="bf541-115">Child element sequence</span></span>

``` syntax
(
  ServiceID, 
  Types
)
```

## <a name="parent-elements"></a><span data-ttu-id="bf541-116">父元素</span><span class="sxs-lookup"><span data-stu-id="bf541-116">Parent elements</span></span>



| <span data-ttu-id="bf541-117">元素</span><span class="sxs-lookup"><span data-stu-id="bf541-117">Element</span></span>                                         | <span data-ttu-id="bf541-118">描述</span><span class="sxs-lookup"><span data-stu-id="bf541-118">Description</span></span>                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="bf541-119">**hostMetadata**</span><span class="sxs-lookup"><span data-stu-id="bf541-119">**hostMetadata**</span></span>](hostmetadata.md)<br/> | <span data-ttu-id="bf541-120">要執行之裝置的裝載中繼資料。</span><span class="sxs-lookup"><span data-stu-id="bf541-120">The hosting metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="bf541-121">項目資訊</span><span class="sxs-lookup"><span data-stu-id="bf541-121">Element information</span></span>



| <span data-ttu-id="bf541-122">標籤</span><span class="sxs-lookup"><span data-stu-id="bf541-122">Label</span></span> | <span data-ttu-id="bf541-123">值</span><span class="sxs-lookup"><span data-stu-id="bf541-123">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="bf541-124">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="bf541-124">Minimum supported system</span></span><br/> | <span data-ttu-id="bf541-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bf541-125">Windows Vista</span></span> |
| <span data-ttu-id="bf541-126">可以是空的</span><span class="sxs-lookup"><span data-stu-id="bf541-126">Can be empty</span></span>                        | <span data-ttu-id="bf541-127">否</span><span class="sxs-lookup"><span data-stu-id="bf541-127">No</span></span>            |



 

 




