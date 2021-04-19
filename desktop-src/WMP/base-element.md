---
title: 基底元素
description: 基底元素會定義附加至傳送給 Windows Media Player 的 Url 前面的 URL 字串。
ms.assetid: 887cf860-d06e-44a1-b729-28a285f6c7d3
keywords:
- 基底元素 Windows Media Player
topic_type:
- apiref
api_name:
- BASE Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44b62a24f73ed6cf78820efe1ca76e0eccd3fb59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999444"
---
# <a name="base-element"></a><span data-ttu-id="0383d-104">基底元素</span><span class="sxs-lookup"><span data-stu-id="0383d-104">BASE Element</span></span>

<span data-ttu-id="0383d-105">**基底** 元素會定義附加至傳送給 Windows Media Player 的 url 前面的 url 字串。</span><span class="sxs-lookup"><span data-stu-id="0383d-105">The **BASE** element defines a URL string appended to the front of URLs sent to Windows Media Player.</span></span>

``` syntax
<BASE
   HREF = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="0383d-106">屬性</span><span class="sxs-lookup"><span data-stu-id="0383d-106">Attributes</span></span>

<span data-ttu-id="0383d-107">需要) **HREF** (</span><span class="sxs-lookup"><span data-stu-id="0383d-107">**HREF** (required)</span></span>

<span data-ttu-id="0383d-108">附加至傳送給 Windows Media Player 之 Url 前面的字串。</span><span class="sxs-lookup"><span data-stu-id="0383d-108">The string appended to the front to URLs sent to Windows Media Player.</span></span> <span data-ttu-id="0383d-109">預設值為 null 字串 ( "" ) 。</span><span class="sxs-lookup"><span data-stu-id="0383d-109">The default value is the null string ("").</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="0383d-110">父/子項目</span><span class="sxs-lookup"><span data-stu-id="0383d-110">Parent/Child Elements</span></span>



| <span data-ttu-id="0383d-111">階層</span><span class="sxs-lookup"><span data-stu-id="0383d-111">Hierarchy</span></span>       | <span data-ttu-id="0383d-112">元素</span><span class="sxs-lookup"><span data-stu-id="0383d-112">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="0383d-113">父元素</span><span class="sxs-lookup"><span data-stu-id="0383d-113">Parent elements</span></span> | <span data-ttu-id="0383d-114">**ASX**， **進入**</span><span class="sxs-lookup"><span data-stu-id="0383d-114">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="0383d-115">子元素</span><span class="sxs-lookup"><span data-stu-id="0383d-115">Child elements</span></span>  | <span data-ttu-id="0383d-116">無</span><span class="sxs-lookup"><span data-stu-id="0383d-116">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="0383d-117">備註</span><span class="sxs-lookup"><span data-stu-id="0383d-117">Remarks</span></span>

<span data-ttu-id="0383d-118">此元素會定義 URL 字串，並附加至傳送至 Windows Media Player 的 URL 反向 Url 前面。</span><span class="sxs-lookup"><span data-stu-id="0383d-118">This element defines a URL string appended to the front of URL-flip URLs sent to Windows Media Player.</span></span> <span data-ttu-id="0383d-119">URL 翻轉是一種腳本機制，可讓 Windows Media Player 在瀏覽器或瀏覽器框架收到指令碼命令時，開啟新的 URL。</span><span class="sxs-lookup"><span data-stu-id="0383d-119">URL-flipping is a scripting mechanism that causes Windows Media Player to open a new URL in a browser or browser frame when it receives a script command.</span></span>

<span data-ttu-id="0383d-120">**基底** 元素類似于相對連結的主目錄。</span><span class="sxs-lookup"><span data-stu-id="0383d-120">The **BASE** element is similar to a home directory for relative links.</span></span> <span data-ttu-id="0383d-121">它只會影響使用指令碼命令傳送的 Url，做為 Windows Media Player 中播放之內容資料流程的一部分。</span><span class="sxs-lookup"><span data-stu-id="0383d-121">It only affects URLs sent using script commands as part of the content stream that is playing in Windows Media Player.</span></span>

<span data-ttu-id="0383d-122">定義為 **ASX** 元素子系的 **基底** 元素會變成整個中繼檔的預設值。</span><span class="sxs-lookup"><span data-stu-id="0383d-122">A **BASE** element defined as the child of an **ASX** element becomes the default for the entire metafile.</span></span> <span data-ttu-id="0383d-123">**專案專案** 中所定義的 **基底** 元素，會覆寫父 **ASX** 元素中的任何 **基底** 元素， (僅) 該 **entry 專案**。</span><span class="sxs-lookup"><span data-stu-id="0383d-123">A **BASE** element defined in an **ENTRY** element overrides any **BASE** element in the parent **ASX** element (for that **ENTRY** element only).</span></span>

> [!Note]  
> <span data-ttu-id="0383d-124">如果 **HREF** 屬性不是以/字元結尾，Windows Media Player 會將其中一個字元附加至字串結尾。</span><span class="sxs-lookup"><span data-stu-id="0383d-124">If the **HREF** attribute does not end with a / character, Windows Media Player appends one to the end of the string.</span></span>

 

## <a name="examples"></a><span data-ttu-id="0383d-125">範例</span><span class="sxs-lookup"><span data-stu-id="0383d-125">Examples</span></span>


```XML
<BASE HREF="https://msdn.microsoft.com/" />

```



## <a name="requirements"></a><span data-ttu-id="0383d-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="0383d-126">Requirements</span></span>



| <span data-ttu-id="0383d-127">需求</span><span class="sxs-lookup"><span data-stu-id="0383d-127">Requirement</span></span> | <span data-ttu-id="0383d-128">值</span><span class="sxs-lookup"><span data-stu-id="0383d-128">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="0383d-129">版本</span><span class="sxs-lookup"><span data-stu-id="0383d-129">Version</span></span><br/> | <span data-ttu-id="0383d-130">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="0383d-130">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0383d-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0383d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0383d-132">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="0383d-132">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="0383d-133">**Windows Media 中繼檔參考**</span><span class="sxs-lookup"><span data-stu-id="0383d-133">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





