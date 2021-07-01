---
description: 指定 Microsoft 媒體基礎繞道提供者，此提供者會追蹤媒體基礎的 API 呼叫。
ms.assetid: 7c9abda9-7968-463c-b4a9-19b54012ef56
title: mfdetours 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cd03711c74c21a9a6ff33d2cc2560e4b6d6e0a3
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119333"
---
# <a name="mfdetours-element"></a><span data-ttu-id="8f167-103">mfdetours 元素</span><span class="sxs-lookup"><span data-stu-id="8f167-103">mfdetours element</span></span>

<span data-ttu-id="8f167-104">指定 Microsoft 媒體基礎繞道提供者，此提供者會追蹤媒體基礎的 API 呼叫。</span><span class="sxs-lookup"><span data-stu-id="8f167-104">Specifies the Microsoft Media Foundation Detours provider, which traces Media Foundation API calls.</span></span>

## <a name="usage"></a><span data-ttu-id="8f167-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="8f167-105">Usage</span></span>

``` syntax
<mfdetours
  level = "CDATA">
  child elements
</mfdetours>
```

## <a name="attributes"></a><span data-ttu-id="8f167-106">屬性</span><span class="sxs-lookup"><span data-stu-id="8f167-106">Attributes</span></span>



| <span data-ttu-id="8f167-107">屬性</span><span class="sxs-lookup"><span data-stu-id="8f167-107">Attribute</span></span>            | <span data-ttu-id="8f167-108">類型</span><span class="sxs-lookup"><span data-stu-id="8f167-108">Type</span></span>             | <span data-ttu-id="8f167-109">必要</span><span class="sxs-lookup"><span data-stu-id="8f167-109">Required</span></span>       | <span data-ttu-id="8f167-110">描述</span><span class="sxs-lookup"><span data-stu-id="8f167-110">Description</span></span>                             |
|----------------------|------------------|----------------|-----------------------------------------|
| <span data-ttu-id="8f167-111">**level**</span><span class="sxs-lookup"><span data-stu-id="8f167-111">**level**</span></span><br/> | <span data-ttu-id="8f167-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="8f167-112">CDATA</span></span><br/> | <span data-ttu-id="8f167-113">是</span><span class="sxs-lookup"><span data-stu-id="8f167-113">Yes</span></span><br/> | <span data-ttu-id="8f167-114">追蹤層級。</span><span class="sxs-lookup"><span data-stu-id="8f167-114">The trace level.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="8f167-115">子元素</span><span class="sxs-lookup"><span data-stu-id="8f167-115">Child elements</span></span>



| <span data-ttu-id="8f167-116">元素</span><span class="sxs-lookup"><span data-stu-id="8f167-116">Element</span></span>                               |
|---------------------------------------|
| [<span data-ttu-id="8f167-117">**關鍵 字**</span><span class="sxs-lookup"><span data-stu-id="8f167-117">**keyword**</span></span>](keyword.md)<br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="8f167-118">子項目順序</span><span class="sxs-lookup"><span data-stu-id="8f167-118">Child element sequence</span></span>

``` syntax
keyword+
```

## <a name="parent-elements"></a><span data-ttu-id="8f167-119">父元素</span><span class="sxs-lookup"><span data-stu-id="8f167-119">Parent elements</span></span>

| <span data-ttu-id="8f167-120">元素</span><span class="sxs-lookup"><span data-stu-id="8f167-120">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="8f167-121">**供應商**</span><span class="sxs-lookup"><span data-stu-id="8f167-121">**providers**</span></span>](providers.md)<br/> |



## <a name="element-information"></a><span data-ttu-id="8f167-122">項目資訊</span><span class="sxs-lookup"><span data-stu-id="8f167-122">Element information</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="8f167-123">可以是空的</span><span class="sxs-lookup"><span data-stu-id="8f167-123">Can be empty</span></span>
    :::column-end:::
    :::column span="2":::
        <span data-ttu-id="8f167-124">否</span><span class="sxs-lookup"><span data-stu-id="8f167-124">No</span></span>
    :::column-end:::
:::row-end:::

## <a name="see-also"></a><span data-ttu-id="8f167-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f167-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f167-126">MFTrace 設定檔</span><span class="sxs-lookup"><span data-stu-id="8f167-126">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




