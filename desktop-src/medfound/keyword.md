---
description: 指定 MFTrace 提供者的關鍵字字。
ms.assetid: 1ce4a5ee-c053-4d31-a984-dc11acebbf2a
title: 關鍵字元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b11632a257e7d51378ddb816124e51548746a178
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983855"
---
# <a name="keyword-element"></a><span data-ttu-id="58517-103">關鍵字元素</span><span class="sxs-lookup"><span data-stu-id="58517-103">keyword element</span></span>

<span data-ttu-id="58517-104">指定 [MFTrace](mftrace.md) 提供者的關鍵字字。</span><span class="sxs-lookup"><span data-stu-id="58517-104">Specifies a key word for an [MFTrace](mftrace.md) provider.</span></span>

## <a name="usage"></a><span data-ttu-id="58517-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="58517-105">Usage</span></span>

``` syntax
<keyword
  ID = "CDATA"/>
```

## <a name="attributes"></a><span data-ttu-id="58517-106">屬性</span><span class="sxs-lookup"><span data-stu-id="58517-106">Attributes</span></span>



| <span data-ttu-id="58517-107">屬性</span><span class="sxs-lookup"><span data-stu-id="58517-107">Attribute</span></span>         | <span data-ttu-id="58517-108">類型</span><span class="sxs-lookup"><span data-stu-id="58517-108">Type</span></span>             | <span data-ttu-id="58517-109">必要</span><span class="sxs-lookup"><span data-stu-id="58517-109">Required</span></span>       | <span data-ttu-id="58517-110">描述</span><span class="sxs-lookup"><span data-stu-id="58517-110">Description</span></span>                                             |
|-------------------|------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="58517-111">**識別碼**</span><span class="sxs-lookup"><span data-stu-id="58517-111">**ID**</span></span><br/> | <span data-ttu-id="58517-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="58517-112">CDATA</span></span><br/> | <span data-ttu-id="58517-113">Yes</span><span class="sxs-lookup"><span data-stu-id="58517-113">Yes</span></span><br/> | <span data-ttu-id="58517-114">關鍵字組的名稱或遮罩</span><span class="sxs-lookup"><span data-stu-id="58517-114">The name or mask of the key word</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="58517-115">子元素</span><span class="sxs-lookup"><span data-stu-id="58517-115">Child elements</span></span>

<span data-ttu-id="58517-116">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="58517-116">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="58517-117">父元素</span><span class="sxs-lookup"><span data-stu-id="58517-117">Parent elements</span></span>



| <span data-ttu-id="58517-118">元素</span><span class="sxs-lookup"><span data-stu-id="58517-118">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="58517-119">**mfdetours**</span><span class="sxs-lookup"><span data-stu-id="58517-119">**mfdetours**</span></span>](mfdetours.md)<br/> |
| [<span data-ttu-id="58517-120">**供應商**</span><span class="sxs-lookup"><span data-stu-id="58517-120">**provider**</span></span>](provider.md)<br/>   |



## <a name="remarks"></a><span data-ttu-id="58517-121">備註</span><span class="sxs-lookup"><span data-stu-id="58517-121">Remarks</span></span>

<span data-ttu-id="58517-122">針對 [**mfdetours**](mfdetours.md) 元素，有效的關鍵字會列在主題 [MFTrace 關鍵字](mftrace-keywords.md)中。</span><span class="sxs-lookup"><span data-stu-id="58517-122">For the [**mfdetours**](mfdetours.md) element, the valid key words are listed in the topic [MFTrace Keywords](mftrace-keywords.md).</span></span>

<span data-ttu-id="58517-123">針對 [**提供者**](provider.md) 專案，關鍵字組相依于事件提供者。</span><span class="sxs-lookup"><span data-stu-id="58517-123">For the [**provider**](provider.md) element, the key words depend on the event provider.</span></span> <span data-ttu-id="58517-124">您可以使用 Wevtutil.exe 公用程式來列出指定提供者的關鍵字。</span><span class="sxs-lookup"><span data-stu-id="58517-124">You can use the Wevtutil.exe utility to list the key words for a given provider.</span></span>

## <a name="element-information"></a><span data-ttu-id="58517-125">項目資訊</span><span class="sxs-lookup"><span data-stu-id="58517-125">Element information</span></span>



|              |     |
|--------------|-----|
| <span data-ttu-id="58517-126">可以是空的</span><span class="sxs-lookup"><span data-stu-id="58517-126">Can be empty</span></span> | <span data-ttu-id="58517-127">Yes</span><span class="sxs-lookup"><span data-stu-id="58517-127">Yes</span></span> |



## <a name="see-also"></a><span data-ttu-id="58517-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58517-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58517-129">MFTrace 設定檔</span><span class="sxs-lookup"><span data-stu-id="58517-129">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> <dt>

[<span data-ttu-id="58517-130">MFTrace 關鍵字</span><span class="sxs-lookup"><span data-stu-id="58517-130">MFTrace Keywords</span></span>](mftrace-keywords.md)
</dt> </dl>

 

 




