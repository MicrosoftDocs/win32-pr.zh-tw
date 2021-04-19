---
title: Color 元素
description: 請注意，本節將說明針對線上商店使用而設計的功能。 |Color 元素
ms.assetid: 36fafe16-b708-4dc1-9325-d4f39265069a
keywords:
- Color 元素 Windows Media Player
topic_type:
- apiref
api_name:
- Color Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6c73aa9fe2c7f731e872c4a2e235bf9c0e29ce05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994838"
---
# <a name="color-element"></a><span data-ttu-id="63e44-105">Color 元素</span><span class="sxs-lookup"><span data-stu-id="63e44-105">Color Element</span></span>

> [!Note]  
> <span data-ttu-id="63e44-106">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="63e44-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="63e44-107">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="63e44-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="63e44-108">Color 元素會指定線上商店導覽按鈕、按鈕文字和功能工作列的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="63e44-108">The Color element specifies the background color for online store navigation buttons, button text, and the Features taskbar.</span></span>

``` syntax
<Color
    MediaPlayer = "#FFFFFF"
    MediaPlayerText = "#FFFFFF"
/>
```

## <a name="attributes"></a><span data-ttu-id="63e44-109">屬性</span><span class="sxs-lookup"><span data-stu-id="63e44-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="63e44-110"><span id="MediaPlayer__required_"></span><span id="mediaplayer__required_"></span><span id="MEDIAPLAYER__REQUIRED_"></span>**MediaPlayer** (必要) </span><span class="sxs-lookup"><span data-stu-id="63e44-110"><span id="MediaPlayer__required_"></span><span id="mediaplayer__required_"></span><span id="MEDIAPLAYER__REQUIRED_"></span>**MediaPlayer** (required)</span></span>
</dt> <dd>

<span data-ttu-id="63e44-111">十六進位 RGB 色彩值。</span><span class="sxs-lookup"><span data-stu-id="63e44-111">Hexadecimal RGB color value.</span></span> <span data-ttu-id="63e44-112">指定按鈕與工作列的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="63e44-112">Specifies the background color for buttons and the taskbar.</span></span>

</dd> <dt>

<span data-ttu-id="63e44-113"><span id="MediaPlayerText__required_"></span><span id="mediaplayertext__required_"></span><span id="MEDIAPLAYERTEXT__REQUIRED_"></span>**MediaPlayerText** (必要) </span><span class="sxs-lookup"><span data-stu-id="63e44-113"><span id="MediaPlayerText__required_"></span><span id="mediaplayertext__required_"></span><span id="MEDIAPLAYERTEXT__REQUIRED_"></span>**MediaPlayerText** (required)</span></span>
</dt> <dd>

<span data-ttu-id="63e44-114">十六進位 RGB 色彩值。</span><span class="sxs-lookup"><span data-stu-id="63e44-114">Hexadecimal RGB color value.</span></span> <span data-ttu-id="63e44-115">指定按鈕文字的色彩。</span><span class="sxs-lookup"><span data-stu-id="63e44-115">Specifies the color for the button text.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="63e44-116">父/子項目</span><span class="sxs-lookup"><span data-stu-id="63e44-116">Parent/Child Elements</span></span>



| <span data-ttu-id="63e44-117">階層</span><span class="sxs-lookup"><span data-stu-id="63e44-117">Hierarchy</span></span>       | <span data-ttu-id="63e44-118">元素</span><span class="sxs-lookup"><span data-stu-id="63e44-118">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="63e44-119">父元素</span><span class="sxs-lookup"><span data-stu-id="63e44-119">Parent elements</span></span> | <span data-ttu-id="63e44-120">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="63e44-120">**ServiceInfo**</span></span> |
| <span data-ttu-id="63e44-121">子元素</span><span class="sxs-lookup"><span data-stu-id="63e44-121">Child elements</span></span>  | <span data-ttu-id="63e44-122">無</span><span class="sxs-lookup"><span data-stu-id="63e44-122">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="63e44-123">備註</span><span class="sxs-lookup"><span data-stu-id="63e44-123">Remarks</span></span>

<span data-ttu-id="63e44-124">**MediaPlayer** 的預設值為 \# 7C9AD6。</span><span class="sxs-lookup"><span data-stu-id="63e44-124">The default value for **MediaPlayer** is \#7C9AD6.</span></span> <span data-ttu-id="63e44-125">**MediaPlayerText** 的預設值為 \# FFFFFF。</span><span class="sxs-lookup"><span data-stu-id="63e44-125">The default value for **MediaPlayerText** is \#FFFFFF.</span></span>

<span data-ttu-id="63e44-126">請務必使用可讓使用者更容易閱讀按鈕文字的色彩。</span><span class="sxs-lookup"><span data-stu-id="63e44-126">Be sure to use colors that make it easy for the user to read the button text.</span></span> <span data-ttu-id="63e44-127">例如，您應該避免使用淺色按鈕的白色按鈕文字。</span><span class="sxs-lookup"><span data-stu-id="63e44-127">For example, you should avoid using white button text on light colored buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="63e44-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="63e44-128">Requirements</span></span>



| <span data-ttu-id="63e44-129">需求</span><span class="sxs-lookup"><span data-stu-id="63e44-129">Requirement</span></span> | <span data-ttu-id="63e44-130">值</span><span class="sxs-lookup"><span data-stu-id="63e44-130">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="63e44-131">版本</span><span class="sxs-lookup"><span data-stu-id="63e44-131">Version</span></span><br/> | <span data-ttu-id="63e44-132">Windows Media Player 10 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="63e44-132">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="63e44-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="63e44-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63e44-134">**類型1線上商店的範例 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="63e44-134">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="63e44-135">**Type 2 線上商店的範例 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="63e44-135">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="63e44-136">**ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="63e44-136">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





