---
description: 針對 MFTrace 指定追蹤提供者 (ETW 或 WPP) 。
ms.assetid: 692cce3b-ebf5-4a49-8c37-48c8ef6caee7
title: provider 項目
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ca319b686101766dacd79821ac6d9caf859cf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691627"
---
# <a name="provider-element"></a><span data-ttu-id="47448-103">provider 項目</span><span class="sxs-lookup"><span data-stu-id="47448-103">provider element</span></span>

<span data-ttu-id="47448-104">針對 [MFTrace](mftrace.md)指定追蹤提供者 (ETW 或 WPP) 。</span><span class="sxs-lookup"><span data-stu-id="47448-104">Specifies a trace provider (ETW or WPP) for [MFTrace](mftrace.md).</span></span>

## <a name="usage"></a><span data-ttu-id="47448-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="47448-105">Usage</span></span>

``` syntax
<provider
  ID = "CDATA"
  level = "CDATA">
  child elements
</provider>
```

## <a name="attributes"></a><span data-ttu-id="47448-106">屬性</span><span class="sxs-lookup"><span data-stu-id="47448-106">Attributes</span></span>



| <span data-ttu-id="47448-107">屬性</span><span class="sxs-lookup"><span data-stu-id="47448-107">Attribute</span></span>            | <span data-ttu-id="47448-108">類型</span><span class="sxs-lookup"><span data-stu-id="47448-108">Type</span></span>             | <span data-ttu-id="47448-109">必要</span><span class="sxs-lookup"><span data-stu-id="47448-109">Required</span></span>       | <span data-ttu-id="47448-110">描述</span><span class="sxs-lookup"><span data-stu-id="47448-110">Description</span></span>                                              |
|----------------------|------------------|----------------|----------------------------------------------------------|
| <span data-ttu-id="47448-111">**識別碼**</span><span class="sxs-lookup"><span data-stu-id="47448-111">**ID**</span></span><br/>    | <span data-ttu-id="47448-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="47448-112">CDATA</span></span><br/> | <span data-ttu-id="47448-113">Yes</span><span class="sxs-lookup"><span data-stu-id="47448-113">Yes</span></span><br/> | <span data-ttu-id="47448-114">提供者的名稱或 GUID。</span><span class="sxs-lookup"><span data-stu-id="47448-114">The name or GUID of the provider.</span></span><br/> <br/> |
| <span data-ttu-id="47448-115">**level**</span><span class="sxs-lookup"><span data-stu-id="47448-115">**level**</span></span><br/> | <span data-ttu-id="47448-116">CDATA</span><span class="sxs-lookup"><span data-stu-id="47448-116">CDATA</span></span><br/> | <span data-ttu-id="47448-117">Yes</span><span class="sxs-lookup"><span data-stu-id="47448-117">Yes</span></span><br/> | <span data-ttu-id="47448-118">追蹤層級。</span><span class="sxs-lookup"><span data-stu-id="47448-118">The trace level.</span></span><br/> <br/>                  |



## <a name="child-elements"></a><span data-ttu-id="47448-119">子元素</span><span class="sxs-lookup"><span data-stu-id="47448-119">Child elements</span></span>



| <span data-ttu-id="47448-120">元素</span><span class="sxs-lookup"><span data-stu-id="47448-120">Element</span></span>                               |
|---------------------------------------|
| [<span data-ttu-id="47448-121">**關鍵 字**</span><span class="sxs-lookup"><span data-stu-id="47448-121">**keyword**</span></span>](keyword.md)<br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="47448-122">子項目順序</span><span class="sxs-lookup"><span data-stu-id="47448-122">Child element sequence</span></span>

``` syntax
keyword+
```

## <a name="parent-elements"></a><span data-ttu-id="47448-123">父元素</span><span class="sxs-lookup"><span data-stu-id="47448-123">Parent elements</span></span>



| <span data-ttu-id="47448-124">元素</span><span class="sxs-lookup"><span data-stu-id="47448-124">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="47448-125">**供應商**</span><span class="sxs-lookup"><span data-stu-id="47448-125">**providers**</span></span>](providers.md)<br/> |



## <a name="element-information"></a><span data-ttu-id="47448-126">項目資訊</span><span class="sxs-lookup"><span data-stu-id="47448-126">Element information</span></span>



|              |     |
|--------------|-----|
| <span data-ttu-id="47448-127">可以是空的</span><span class="sxs-lookup"><span data-stu-id="47448-127">Can be empty</span></span> | <span data-ttu-id="47448-128">否</span><span class="sxs-lookup"><span data-stu-id="47448-128">No</span></span>  |



## <a name="see-also"></a><span data-ttu-id="47448-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="47448-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47448-130">MFTrace 設定檔</span><span class="sxs-lookup"><span data-stu-id="47448-130">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




