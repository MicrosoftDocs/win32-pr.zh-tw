---
description: 指定裝置名稱的當地語系化版本。
ms.assetid: 67ebbca0-bdb2-4a6e-98d8-3d8d1029884f
title: modelNameLS 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e47d2f83d1b636efc30e98dff8c46600bcee555d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995495"
---
# <a name="modelnamels-element"></a><span data-ttu-id="eadf3-103">modelNameLS 元素</span><span class="sxs-lookup"><span data-stu-id="eadf3-103">modelNameLS element</span></span>

<span data-ttu-id="eadf3-104">指定裝置名稱的當地語系化版本。</span><span class="sxs-lookup"><span data-stu-id="eadf3-104">Specifies a localized version of the device name.</span></span>

## <a name="usage"></a><span data-ttu-id="eadf3-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="eadf3-105">Usage</span></span>

``` syntax
<modelNameLS
  Language = "language identifier string"
  Data = "localized model name string"/>
```

## <a name="attributes"></a><span data-ttu-id="eadf3-106">屬性</span><span class="sxs-lookup"><span data-stu-id="eadf3-106">Attributes</span></span>



| <span data-ttu-id="eadf3-107">屬性</span><span class="sxs-lookup"><span data-stu-id="eadf3-107">Attribute</span></span>               | <span data-ttu-id="eadf3-108">類型</span><span class="sxs-lookup"><span data-stu-id="eadf3-108">Type</span></span>                                   | <span data-ttu-id="eadf3-109">必要</span><span class="sxs-lookup"><span data-stu-id="eadf3-109">Required</span></span>       | <span data-ttu-id="eadf3-110">描述</span><span class="sxs-lookup"><span data-stu-id="eadf3-110">Description</span></span>                                                      |
|-------------------------|----------------------------------------|----------------|------------------------------------------------------------------|
| <span data-ttu-id="eadf3-111">**資料**</span><span class="sxs-lookup"><span data-stu-id="eadf3-111">**Data**</span></span><br/>     | <span data-ttu-id="eadf3-112">當地語系化的模型名稱字串</span><span class="sxs-lookup"><span data-stu-id="eadf3-112">localized model name string</span></span><br/> | <span data-ttu-id="eadf3-113">Yes</span><span class="sxs-lookup"><span data-stu-id="eadf3-113">Yes</span></span><br/> | <span data-ttu-id="eadf3-114">當地語系化的模型名稱。</span><span class="sxs-lookup"><span data-stu-id="eadf3-114">The localized model name.</span></span><br/> <br/>                 |
| <span data-ttu-id="eadf3-115">**Language**</span><span class="sxs-lookup"><span data-stu-id="eadf3-115">**Language**</span></span><br/> | <span data-ttu-id="eadf3-116">語言識別項字串</span><span class="sxs-lookup"><span data-stu-id="eadf3-116">language identifier string</span></span><br/>  | <span data-ttu-id="eadf3-117">Yes</span><span class="sxs-lookup"><span data-stu-id="eadf3-117">Yes</span></span><br/> | <span data-ttu-id="eadf3-118">當地語系化模型名稱的語言。</span><span class="sxs-lookup"><span data-stu-id="eadf3-118">The language of the localized model name.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="eadf3-119">子元素</span><span class="sxs-lookup"><span data-stu-id="eadf3-119">Child elements</span></span>

<span data-ttu-id="eadf3-120">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="eadf3-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="eadf3-121">父元素</span><span class="sxs-lookup"><span data-stu-id="eadf3-121">Parent elements</span></span>



| <span data-ttu-id="eadf3-122">元素</span><span class="sxs-lookup"><span data-stu-id="eadf3-122">Element</span></span>                                                   | <span data-ttu-id="eadf3-123">描述</span><span class="sxs-lookup"><span data-stu-id="eadf3-123">Description</span></span>                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eadf3-124">**thisModelMetadata**</span><span class="sxs-lookup"><span data-stu-id="eadf3-124">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/> | <span data-ttu-id="eadf3-125">定義要執行之裝置的製造商和型號中繼資料。</span><span class="sxs-lookup"><span data-stu-id="eadf3-125">Defines the manufacturer and model metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="eadf3-126">項目資訊</span><span class="sxs-lookup"><span data-stu-id="eadf3-126">Element information</span></span>



| <span data-ttu-id="eadf3-127">標籤</span><span class="sxs-lookup"><span data-stu-id="eadf3-127">Label</span></span> | <span data-ttu-id="eadf3-128">值</span><span class="sxs-lookup"><span data-stu-id="eadf3-128">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="eadf3-129">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="eadf3-129">Minimum supported system</span></span><br/> | <span data-ttu-id="eadf3-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eadf3-130">Windows Vista</span></span> |
| <span data-ttu-id="eadf3-131">可以是空的</span><span class="sxs-lookup"><span data-stu-id="eadf3-131">Can be empty</span></span>                        | <span data-ttu-id="eadf3-132">是</span><span class="sxs-lookup"><span data-stu-id="eadf3-132">Yes</span></span>           |



 

 




