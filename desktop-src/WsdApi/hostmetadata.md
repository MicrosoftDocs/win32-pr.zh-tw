---
description: 定義要執行之裝置的裝載中繼資料。 此元素僅用於 (主機) 的裝置執行。
ms.assetid: ca7bc5ea-8ab2-4233-86d2-5b793021b8ee
title: hostMetadata 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9cf6fa139a2723ed90dfe281fc7b054016386fa
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994795"
---
# <a name="hostmetadata-element"></a><span data-ttu-id="264fe-104">hostMetadata 元素</span><span class="sxs-lookup"><span data-stu-id="264fe-104">hostMetadata element</span></span>

<span data-ttu-id="264fe-105">定義要執行之裝置的裝載中繼資料。</span><span class="sxs-lookup"><span data-stu-id="264fe-105">Defines the hosting metadata for the device to be implemented.</span></span> <span data-ttu-id="264fe-106">此元素僅用於 (主機) 的裝置執行。</span><span class="sxs-lookup"><span data-stu-id="264fe-106">This element is used for device implementations (hosts) only.</span></span>

## <a name="usage"></a><span data-ttu-id="264fe-107">使用方式</span><span class="sxs-lookup"><span data-stu-id="264fe-107">Usage</span></span>

``` syntax
<hostMetadata>
  child elements
</hostMetadata>
```

## <a name="attributes"></a><span data-ttu-id="264fe-108">屬性</span><span class="sxs-lookup"><span data-stu-id="264fe-108">Attributes</span></span>

<span data-ttu-id="264fe-109">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="264fe-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="264fe-110">子元素</span><span class="sxs-lookup"><span data-stu-id="264fe-110">Child elements</span></span>



| <span data-ttu-id="264fe-111">元素</span><span class="sxs-lookup"><span data-stu-id="264fe-111">Element</span></span>                             | <span data-ttu-id="264fe-112">描述</span><span class="sxs-lookup"><span data-stu-id="264fe-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="264fe-113">**主機**</span><span class="sxs-lookup"><span data-stu-id="264fe-113">**host**</span></span>](host.md)<br/>     | <span data-ttu-id="264fe-114">定義服務主機的 ServiceID 和 [**Types**](types.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="264fe-114">Defines the ServiceID and [**Types**](types.md) elements for the service host.</span></span> <span data-ttu-id="264fe-115">如果未明確提供，則 WSDAPI 不會提供任何預設資料來回應中繼資料要求。</span><span class="sxs-lookup"><span data-stu-id="264fe-115">If not provided explicitly, WSDAPI will not supply any default data in response to metadata requests.</span></span><br/> <br/>                                                                                                                                          |
| [<span data-ttu-id="264fe-116">**託管**</span><span class="sxs-lookup"><span data-stu-id="264fe-116">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="264fe-117">定義此服務主機所提供之服務的 [**ServiceID**](serviceid.md) 和 [**Types**](types.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="264fe-117">Defines the [**ServiceID**](serviceid.md) and [**Types**](types.md) elements for the services provided by this service host.</span></span> <span data-ttu-id="264fe-118">這項服務主機提供的每個服務都應該有自己的 [**託管**](hosted.md) 元素資訊，以確保服務在對中繼資料要求的回應中已正確發佈。</span><span class="sxs-lookup"><span data-stu-id="264fe-118">Each service provided by this service host should have its own [**hosted**](hosted.md) element information to ensure that the service is published properly in responses to metadata requests.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="264fe-119">子項目順序</span><span class="sxs-lookup"><span data-stu-id="264fe-119">Child element sequence</span></span>

``` syntax
(
  host?, 
  hosted+
)
```

## <a name="parent-elements"></a><span data-ttu-id="264fe-120">父元素</span><span class="sxs-lookup"><span data-stu-id="264fe-120">Parent elements</span></span>



| <span data-ttu-id="264fe-121">元素</span><span class="sxs-lookup"><span data-stu-id="264fe-121">Element</span></span>                                                         | <span data-ttu-id="264fe-122">描述</span><span class="sxs-lookup"><span data-stu-id="264fe-122">Description</span></span>                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="264fe-123">**relationshipMetadata**</span><span class="sxs-lookup"><span data-stu-id="264fe-123">**relationshipMetadata**</span></span>](relationshipmetadata.md)<br/> | <span data-ttu-id="264fe-124">描述裝置的主機和託管中繼資料。</span><span class="sxs-lookup"><span data-stu-id="264fe-124">Describes the host and hosted metadata for the device.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="264fe-125">備註</span><span class="sxs-lookup"><span data-stu-id="264fe-125">Remarks</span></span>

<span data-ttu-id="264fe-126">裝載中繼資料會顯示在此專案中，類似于裝置設定檔中指定的表單。</span><span class="sxs-lookup"><span data-stu-id="264fe-126">The hosting metadata appears in this element in a form similar to the one specified in the device profile.</span></span> <span data-ttu-id="264fe-127">**hostMetadata** 與裝置設定檔中所述的格式稍有不同，因為它所支援的唯一參考屬性是服務識別碼。</span><span class="sxs-lookup"><span data-stu-id="264fe-127">**hostMetadata** is slightly different from the format described in the device profile in that the only reference property it supports is the service ID.</span></span>

<span data-ttu-id="264fe-128">接著會使用 [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md) 元素來產生包含這項資訊的 C 常數。</span><span class="sxs-lookup"><span data-stu-id="264fe-128">The [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md) element is used subsequently to generate a C constant containing this information.</span></span>

## <a name="element-information"></a><span data-ttu-id="264fe-129">項目資訊</span><span class="sxs-lookup"><span data-stu-id="264fe-129">Element information</span></span>



| <span data-ttu-id="264fe-130">標籤</span><span class="sxs-lookup"><span data-stu-id="264fe-130">Label</span></span> | <span data-ttu-id="264fe-131">值</span><span class="sxs-lookup"><span data-stu-id="264fe-131">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="264fe-132">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="264fe-132">Minimum supported system</span></span><br/> | <span data-ttu-id="264fe-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="264fe-133">Windows Vista</span></span> |
| <span data-ttu-id="264fe-134">可以是空的</span><span class="sxs-lookup"><span data-stu-id="264fe-134">Can be empty</span></span>                        | <span data-ttu-id="264fe-135">否</span><span class="sxs-lookup"><span data-stu-id="264fe-135">No</span></span>            |



 

 




