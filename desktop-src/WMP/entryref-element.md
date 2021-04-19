---
title: ENTRYREF 元素
description: ENTRYREF 元素指向外部中繼檔中的專案專案。
ms.assetid: ba39db39-fa90-455b-b278-ca866ce0b69c
keywords:
- ENTRYREF 元素 Windows Media Player
topic_type:
- apiref
api_name:
- ENTRYREF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 520a4262baf17badb136b55e7b2e216bf89d7edf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997636"
---
# <a name="entryref-element"></a><span data-ttu-id="5d716-104">ENTRYREF 元素</span><span class="sxs-lookup"><span data-stu-id="5d716-104">ENTRYREF Element</span></span>

<span data-ttu-id="5d716-105">**ENTRYREF** 元素指向外部中繼檔中的 **專案專案**。</span><span class="sxs-lookup"><span data-stu-id="5d716-105">The **ENTRYREF** element points to the **ENTRY** elements in an external metafile.</span></span>

``` syntax
<ENTRYREF
   HREF = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="5d716-106">屬性</span><span class="sxs-lookup"><span data-stu-id="5d716-106">Attributes</span></span>

<span data-ttu-id="5d716-107">需要) **HREF** (</span><span class="sxs-lookup"><span data-stu-id="5d716-107">**HREF** (required)</span></span>

<span data-ttu-id="5d716-108">參考之中繼檔的 URL。</span><span class="sxs-lookup"><span data-stu-id="5d716-108">URL to a referenced metafile.</span></span>

<span data-ttu-id="5d716-109">**CLIENTBIND**</span><span class="sxs-lookup"><span data-stu-id="5d716-109">**CLIENTBIND**</span></span>

<span data-ttu-id="5d716-110">已不再支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="5d716-110">This attribute is no longer supported.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="5d716-111">父/子項目</span><span class="sxs-lookup"><span data-stu-id="5d716-111">Parent/Child Elements</span></span>



| <span data-ttu-id="5d716-112">階層</span><span class="sxs-lookup"><span data-stu-id="5d716-112">Hierarchy</span></span>       | <span data-ttu-id="5d716-113">元素</span><span class="sxs-lookup"><span data-stu-id="5d716-113">Elements</span></span>                       |
|-----------------|--------------------------------|
| <span data-ttu-id="5d716-114">父元素</span><span class="sxs-lookup"><span data-stu-id="5d716-114">Parent elements</span></span> | <span data-ttu-id="5d716-115">**ASX**、 **事件**、 **重複**</span><span class="sxs-lookup"><span data-stu-id="5d716-115">**ASX**, **EVENT**, **REPEAT**</span></span> |
| <span data-ttu-id="5d716-116">子元素</span><span class="sxs-lookup"><span data-stu-id="5d716-116">Child elements</span></span>  | <span data-ttu-id="5d716-117">無</span><span class="sxs-lookup"><span data-stu-id="5d716-117">None</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="5d716-118">備註</span><span class="sxs-lookup"><span data-stu-id="5d716-118">Remarks</span></span>

<span data-ttu-id="5d716-119">這個元素指向外部中繼檔的內容。</span><span class="sxs-lookup"><span data-stu-id="5d716-119">This element points to the contents of an external metafile.</span></span> <span data-ttu-id="5d716-120">Windows Media Player 處理參考之中繼檔的 **專案專案** ，就如同它們是包含在 **ENTRYREF** 元素位置的主要中繼檔中一樣。</span><span class="sxs-lookup"><span data-stu-id="5d716-120">Windows Media Player processes the **ENTRY** elements of the referenced metafile as if they were included in the primary metafile at the position of the **ENTRYREF** element.</span></span> <span data-ttu-id="5d716-121">但是，它會略過參考的中繼檔中，將 **SKIPIFREF** 屬性設定為 YES 的任何 **專案專案**。</span><span class="sxs-lookup"><span data-stu-id="5d716-121">However, it skips any **ENTRY** elements in the referenced metafile that have the **SKIPIFREF** attribute set to YES.</span></span>

<span data-ttu-id="5d716-122">適用于 Windows XP 的 Windows Media Player 7.0、7.1 和 Windows Media Player 會忽略參考的中繼檔中的任何 **ENTRYREF** 元素。</span><span class="sxs-lookup"><span data-stu-id="5d716-122">Windows Media Player 7.0, 7.1, and Windows Media Player for Windows XP ignore any **ENTRYREF** elements in the referenced metafile.</span></span> <span data-ttu-id="5d716-123">因此，在使用這些版本的播放程式時，中繼檔只能以一層級進行深度嵌套。</span><span class="sxs-lookup"><span data-stu-id="5d716-123">Thus, metafiles can only be nested one level deep when using these versions of the Player.</span></span> <span data-ttu-id="5d716-124">Windows Media Player 也會忽略參考檔案中的 **ASX** 元素及其屬性。</span><span class="sxs-lookup"><span data-stu-id="5d716-124">Windows Media Player also ignores the **ASX** element in the referenced file along with its attributes.</span></span> <span data-ttu-id="5d716-125">Windows Media Player 9 系列或更新版本支援嵌套最多五個層級的中繼檔。</span><span class="sxs-lookup"><span data-stu-id="5d716-125">Windows Media Player 9 Series or later supports nesting metafiles up to five levels deep.</span></span>

<span data-ttu-id="5d716-126">**HREF** 屬性中指定的 url 會成為外部中繼檔中任何相對 url 的基底 url。</span><span class="sxs-lookup"><span data-stu-id="5d716-126">The URL specified in the **HREF** attribute becomes the base URL for any relative URLs in the external metafile.</span></span> <span data-ttu-id="5d716-127">當外部中繼檔的專案現正播放，且使用者將它新增至程式庫時，會使用此 URL。</span><span class="sxs-lookup"><span data-stu-id="5d716-127">This URL is used when an entry from the external metafile is playing and the user adds it to the library.</span></span>

## <a name="examples"></a><span data-ttu-id="5d716-128">範例</span><span class="sxs-lookup"><span data-stu-id="5d716-128">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <TITLE>Example of Using EntryRef</TITLE>
   <ENTRYREF HREF="https://sample.microsoft.com/metafile.asx" />
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="5d716-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d716-129">Requirements</span></span>



| <span data-ttu-id="5d716-130">需求</span><span class="sxs-lookup"><span data-stu-id="5d716-130">Requirement</span></span> | <span data-ttu-id="5d716-131">值</span><span class="sxs-lookup"><span data-stu-id="5d716-131">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="5d716-132">版本</span><span class="sxs-lookup"><span data-stu-id="5d716-132">Version</span></span><br/> | <span data-ttu-id="5d716-133">Windows Media Player 70 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="5d716-133">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5d716-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d716-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d716-135">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="5d716-135">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="5d716-136">**Windows Media 中繼檔參考**</span><span class="sxs-lookup"><span data-stu-id="5d716-136">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





