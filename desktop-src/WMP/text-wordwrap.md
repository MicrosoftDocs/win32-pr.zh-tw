---
title: WordWrap
description: WordWrap 屬性會指定或抓取值，指出是否啟用或停用自動換行。
ms.assetid: 3bb127d8-42f1-4167-986a-d41690cb5647
keywords:
- WordWrap Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.wordWrap
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2b4d030a7e9efdda1bc7503ae3bf8eb5985401
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996025"
---
# <a name="textwordwrap"></a><span data-ttu-id="b1995-104">WordWrap</span><span class="sxs-lookup"><span data-stu-id="b1995-104">TEXT.wordWrap</span></span>

<span data-ttu-id="b1995-105">**WordWrap** 屬性會指定或抓取值，指出是否啟用或停用自動換行。</span><span class="sxs-lookup"><span data-stu-id="b1995-105">The **wordWrap** attribute specifies or retrieves a value indicating whether word wrap is enabled or disabled.</span></span>

``` syntax
        elementID.wordWrap
```

## <a name="possible-values"></a><span data-ttu-id="b1995-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="b1995-106">Possible Values</span></span>

<span data-ttu-id="b1995-107">此屬性是讀取/寫入 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="b1995-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="b1995-108">值</span><span class="sxs-lookup"><span data-stu-id="b1995-108">Value</span></span> | <span data-ttu-id="b1995-109">描述</span><span class="sxs-lookup"><span data-stu-id="b1995-109">Description</span></span>                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1995-110">true</span><span class="sxs-lookup"><span data-stu-id="b1995-110">true</span></span>  | <span data-ttu-id="b1995-111">已啟用自動換行。</span><span class="sxs-lookup"><span data-stu-id="b1995-111">Word wrap is enabled.</span></span>                                                                             |
| <span data-ttu-id="b1995-112">false</span><span class="sxs-lookup"><span data-stu-id="b1995-112">false</span></span> | <span data-ttu-id="b1995-113">預設值。</span><span class="sxs-lookup"><span data-stu-id="b1995-113">Default.</span></span> <span data-ttu-id="b1995-114">已停用自動換行。</span><span class="sxs-lookup"><span data-stu-id="b1995-114">Word wrap is disabled.</span></span> <span data-ttu-id="b1995-115">如果文字無法容納在控制項內，則會裁剪文字。</span><span class="sxs-lookup"><span data-stu-id="b1995-115">If the text does not fit within the control, the text is cropped.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b1995-116">備註</span><span class="sxs-lookup"><span data-stu-id="b1995-116">Remarks</span></span>

<span data-ttu-id="b1995-117">文字控制項不會將單字分開。</span><span class="sxs-lookup"><span data-stu-id="b1995-117">The Text control does not split words apart.</span></span> <span data-ttu-id="b1995-118">如果單字延伸超過控制項的寬度，則會使用自動換行將單字移到下一行。</span><span class="sxs-lookup"><span data-stu-id="b1995-118">If a word extends beyond the width of the control, word wrap is employed to move the word to the next line.</span></span> <span data-ttu-id="b1995-119">如果單一單字的長度超過控制項寬度，則會裁剪該單字，並佔用一行。</span><span class="sxs-lookup"><span data-stu-id="b1995-119">If a single word is longer than the control width, that word is clipped and occupies a single line.</span></span>

<span data-ttu-id="b1995-120">如果未指定 **width** 屬性， **wordWrap** 會被忽略，而文字控制項會調整大小，而不是換行文字。</span><span class="sxs-lookup"><span data-stu-id="b1995-120">If the **width** attribute is not specified, **wordWrap** is ignored and the Text control will resize rather than wrapping the text.</span></span>

<span data-ttu-id="b1995-121">如果特定位置需要換行，必須使用 "& \# 13;" 或 "r" 在值中明確指定 \\ 。</span><span class="sxs-lookup"><span data-stu-id="b1995-121">If line breaks are desired in particular locations, they must be explicitly specified in **value** using "&\#13;" or "\\r".</span></span> <span data-ttu-id="b1995-122">如果直接指定值時使用第二個表單，則字串的前面必須加上 "JScript："，且實際的值必須以單引號括住，如下所示。</span><span class="sxs-lookup"><span data-stu-id="b1995-122">If the latter form is used when specifying the value directly, the string must be prefixed with "JScript:" and the actual value must be surrounded by single quotes, as shown below.</span></span> <span data-ttu-id="b1995-123">如果是從事件處理常式內動態設定值，就不需要這麼做。</span><span class="sxs-lookup"><span data-stu-id="b1995-123">This is not necessary if the value is set dynamically from within an event handler.</span></span>

<span data-ttu-id="b1995-124">如果 [ **wordWrap** ] 設定為 [true]，而且未指定 [ **工具提示** ]，則工具提示會顯示 [ **值** ] 屬性的完整文字。</span><span class="sxs-lookup"><span data-stu-id="b1995-124">If **wordWrap** is set to true and **toolTip** is not specified, the ToolTip will display the full text of the **value** attribute.</span></span> <span data-ttu-id="b1995-125">如果沒有任何需要的工具提示，請將 **tooltip** 設定為 "" (空白字串) 。</span><span class="sxs-lookup"><span data-stu-id="b1995-125">If no ToolTip is desired, set **toolTip** to "" (empty string).</span></span>

## <a name="examples"></a><span data-ttu-id="b1995-126">範例</span><span class="sxs-lookup"><span data-stu-id="b1995-126">Examples</span></span>


```C++
<THEME>
  <VIEW>
    <TEXT
      width = "50"
      height = "200"
      wordWrap = "true"
      backgroundColor = "blue"
      foregroundColor = "white"
      value = "This is a test.&#13;&#13;It is only a test."
    />
    <TEXT
      width = "50"
      height = "200"
      left = "100"
      wordWrap = "true"
      backgroundColor = "green"
      foregroundColor = "white"
      value = "JScript:'This is a test.\r\rIt is only a test.'"
    />
  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="b1995-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1995-127">Requirements</span></span>



| <span data-ttu-id="b1995-128">需求</span><span class="sxs-lookup"><span data-stu-id="b1995-128">Requirement</span></span> | <span data-ttu-id="b1995-129">值</span><span class="sxs-lookup"><span data-stu-id="b1995-129">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b1995-130">版本</span><span class="sxs-lookup"><span data-stu-id="b1995-130">Version</span></span><br/> | <span data-ttu-id="b1995-131">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="b1995-131">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b1995-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1995-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1995-133">**AmbientAttributes 寬度**</span><span class="sxs-lookup"><span data-stu-id="b1995-133">**AmbientAttributes.width**</span></span>](ambientattributes-width.md)
</dt> <dt>

[<span data-ttu-id="b1995-134">**TEXT 元素**</span><span class="sxs-lookup"><span data-stu-id="b1995-134">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="b1995-135">**文字。工具提示**</span><span class="sxs-lookup"><span data-stu-id="b1995-135">**TEXT.toolTip**</span></span>](text-tooltip.md)
</dt> <dt>

[<span data-ttu-id="b1995-136">**TEXT。值**</span><span class="sxs-lookup"><span data-stu-id="b1995-136">**TEXT.value**</span></span>](text-value.md)
</dt> </dl>

 

 





