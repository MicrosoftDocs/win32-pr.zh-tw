---
description: 指定制造商名稱的當地語系化版本。
ms.assetid: e87de50f-60ec-4c18-b21c-81f7b6928752
title: manufacturerLS 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d24950355c5439d9a99c4ef451f1330772f3459
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993675"
---
# <a name="manufacturerls-element"></a><span data-ttu-id="3d91a-103">manufacturerLS 元素</span><span class="sxs-lookup"><span data-stu-id="3d91a-103">manufacturerLS element</span></span>

<span data-ttu-id="3d91a-104">指定制造商名稱的當地語系化版本。</span><span class="sxs-lookup"><span data-stu-id="3d91a-104">Specifies a localized version of the manufacturer name.</span></span>

## <a name="usage"></a><span data-ttu-id="3d91a-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="3d91a-105">Usage</span></span>

``` syntax
<manufacturerLS
  Language = "language identifier string"
  Data = "localized manufacturer name string"/>
```

## <a name="attributes"></a><span data-ttu-id="3d91a-106">屬性</span><span class="sxs-lookup"><span data-stu-id="3d91a-106">Attributes</span></span>



| <span data-ttu-id="3d91a-107">屬性</span><span class="sxs-lookup"><span data-stu-id="3d91a-107">Attribute</span></span>               | <span data-ttu-id="3d91a-108">類型</span><span class="sxs-lookup"><span data-stu-id="3d91a-108">Type</span></span>                                          | <span data-ttu-id="3d91a-109">必要</span><span class="sxs-lookup"><span data-stu-id="3d91a-109">Required</span></span>       | <span data-ttu-id="3d91a-110">描述</span><span class="sxs-lookup"><span data-stu-id="3d91a-110">Description</span></span>                                                             |
|-------------------------|-----------------------------------------------|----------------|-------------------------------------------------------------------------|
| <span data-ttu-id="3d91a-111">**資料**</span><span class="sxs-lookup"><span data-stu-id="3d91a-111">**Data**</span></span><br/>     | <span data-ttu-id="3d91a-112">當地語系化的製造商名稱字串</span><span class="sxs-lookup"><span data-stu-id="3d91a-112">localized manufacturer name string</span></span><br/> | <span data-ttu-id="3d91a-113">Yes</span><span class="sxs-lookup"><span data-stu-id="3d91a-113">Yes</span></span><br/> | <span data-ttu-id="3d91a-114">當地語系化的製造商名稱。</span><span class="sxs-lookup"><span data-stu-id="3d91a-114">The localized manufacturer name.</span></span><br/> <br/>                 |
| <span data-ttu-id="3d91a-115">**Language**</span><span class="sxs-lookup"><span data-stu-id="3d91a-115">**Language**</span></span><br/> | <span data-ttu-id="3d91a-116">語言識別項字串</span><span class="sxs-lookup"><span data-stu-id="3d91a-116">language identifier string</span></span><br/>         | <span data-ttu-id="3d91a-117">Yes</span><span class="sxs-lookup"><span data-stu-id="3d91a-117">Yes</span></span><br/> | <span data-ttu-id="3d91a-118">當地語系化製造商名稱的語言。</span><span class="sxs-lookup"><span data-stu-id="3d91a-118">The language of the localized manufacturer name.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="3d91a-119">子元素</span><span class="sxs-lookup"><span data-stu-id="3d91a-119">Child elements</span></span>

<span data-ttu-id="3d91a-120">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="3d91a-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="3d91a-121">父元素</span><span class="sxs-lookup"><span data-stu-id="3d91a-121">Parent elements</span></span>



| <span data-ttu-id="3d91a-122">元素</span><span class="sxs-lookup"><span data-stu-id="3d91a-122">Element</span></span>                                                   | <span data-ttu-id="3d91a-123">描述</span><span class="sxs-lookup"><span data-stu-id="3d91a-123">Description</span></span>                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3d91a-124">**thisModelMetadata**</span><span class="sxs-lookup"><span data-stu-id="3d91a-124">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/> | <span data-ttu-id="3d91a-125">定義要執行之裝置的製造商和型號中繼資料。</span><span class="sxs-lookup"><span data-stu-id="3d91a-125">Defines the manufacturer and model metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="3d91a-126">項目資訊</span><span class="sxs-lookup"><span data-stu-id="3d91a-126">Element information</span></span>



| <span data-ttu-id="3d91a-127">標籤</span><span class="sxs-lookup"><span data-stu-id="3d91a-127">Label</span></span> | <span data-ttu-id="3d91a-128">值</span><span class="sxs-lookup"><span data-stu-id="3d91a-128">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="3d91a-129">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="3d91a-129">Minimum supported system</span></span><br/> | <span data-ttu-id="3d91a-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d91a-130">Windows Vista</span></span> |
| <span data-ttu-id="3d91a-131">可以是空的</span><span class="sxs-lookup"><span data-stu-id="3d91a-131">Can be empty</span></span>                        | <span data-ttu-id="3d91a-132">是</span><span class="sxs-lookup"><span data-stu-id="3d91a-132">Yes</span></span>           |



 

 




