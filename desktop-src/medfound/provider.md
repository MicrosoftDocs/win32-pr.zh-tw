---
description: 針對 MFTrace 指定追蹤提供者 (ETW 或 WPP) 。
ms.assetid: 692cce3b-ebf5-4a49-8c37-48c8ef6caee7
title: provider 項目
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d96b3015dddbcff74c09f77a1b6245d052fe034
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118443"
---
# <a name="provider-element"></a><span data-ttu-id="e3de8-103">provider 項目</span><span class="sxs-lookup"><span data-stu-id="e3de8-103">provider element</span></span>

<span data-ttu-id="e3de8-104">針對 [MFTrace](mftrace.md)指定追蹤提供者 (ETW 或 WPP) 。</span><span class="sxs-lookup"><span data-stu-id="e3de8-104">Specifies a trace provider (ETW or WPP) for [MFTrace](mftrace.md).</span></span>

## <a name="usage"></a><span data-ttu-id="e3de8-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="e3de8-105">Usage</span></span>

``` syntax
<provider
  ID = "CDATA"
  level = "CDATA">
  child elements
</provider>
```

## <a name="attributes"></a><span data-ttu-id="e3de8-106">屬性</span><span class="sxs-lookup"><span data-stu-id="e3de8-106">Attributes</span></span>



| <span data-ttu-id="e3de8-107">屬性</span><span class="sxs-lookup"><span data-stu-id="e3de8-107">Attribute</span></span>            | <span data-ttu-id="e3de8-108">類型</span><span class="sxs-lookup"><span data-stu-id="e3de8-108">Type</span></span>             | <span data-ttu-id="e3de8-109">必要</span><span class="sxs-lookup"><span data-stu-id="e3de8-109">Required</span></span>       | <span data-ttu-id="e3de8-110">描述</span><span class="sxs-lookup"><span data-stu-id="e3de8-110">Description</span></span>                                              |
|----------------------|------------------|----------------|----------------------------------------------------------|
| <span data-ttu-id="e3de8-111">**識別碼**</span><span class="sxs-lookup"><span data-stu-id="e3de8-111">**ID**</span></span><br/>    | <span data-ttu-id="e3de8-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="e3de8-112">CDATA</span></span><br/> | <span data-ttu-id="e3de8-113">是</span><span class="sxs-lookup"><span data-stu-id="e3de8-113">Yes</span></span><br/> | <span data-ttu-id="e3de8-114">提供者的名稱或 GUID。</span><span class="sxs-lookup"><span data-stu-id="e3de8-114">The name or GUID of the provider.</span></span><br/> <br/> |
| <span data-ttu-id="e3de8-115">**level**</span><span class="sxs-lookup"><span data-stu-id="e3de8-115">**level**</span></span><br/> | <span data-ttu-id="e3de8-116">CDATA</span><span class="sxs-lookup"><span data-stu-id="e3de8-116">CDATA</span></span><br/> | <span data-ttu-id="e3de8-117">是</span><span class="sxs-lookup"><span data-stu-id="e3de8-117">Yes</span></span><br/> | <span data-ttu-id="e3de8-118">追蹤層級。</span><span class="sxs-lookup"><span data-stu-id="e3de8-118">The trace level.</span></span><br/> <br/>                  |



## <a name="child-elements"></a><span data-ttu-id="e3de8-119">子元素</span><span class="sxs-lookup"><span data-stu-id="e3de8-119">Child elements</span></span>



| <span data-ttu-id="e3de8-120">元素</span><span class="sxs-lookup"><span data-stu-id="e3de8-120">Element</span></span>                               |
|---------------------------------------|
| [<span data-ttu-id="e3de8-121">**關鍵 字**</span><span class="sxs-lookup"><span data-stu-id="e3de8-121">**keyword**</span></span>](keyword.md)<br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="e3de8-122">子項目順序</span><span class="sxs-lookup"><span data-stu-id="e3de8-122">Child element sequence</span></span>

``` syntax
keyword+
```

## <a name="parent-elements"></a><span data-ttu-id="e3de8-123">父元素</span><span class="sxs-lookup"><span data-stu-id="e3de8-123">Parent elements</span></span>



| <span data-ttu-id="e3de8-124">元素</span><span class="sxs-lookup"><span data-stu-id="e3de8-124">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="e3de8-125">**供應商**</span><span class="sxs-lookup"><span data-stu-id="e3de8-125">**providers**</span></span>](providers.md)<br/> |



## <a name="element-information"></a><span data-ttu-id="e3de8-126">項目資訊</span><span class="sxs-lookup"><span data-stu-id="e3de8-126">Element information</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="e3de8-127">可以是空的</span><span class="sxs-lookup"><span data-stu-id="e3de8-127">Can be empty</span></span>
    :::column-end:::
    :::column span="2":::
        <span data-ttu-id="e3de8-128">否</span><span class="sxs-lookup"><span data-stu-id="e3de8-128">No</span></span>
    :::column-end:::
:::row-end:::

## <a name="see-also"></a><span data-ttu-id="e3de8-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3de8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3de8-130">MFTrace 設定檔</span><span class="sxs-lookup"><span data-stu-id="e3de8-130">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




