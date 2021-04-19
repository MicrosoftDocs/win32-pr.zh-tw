---
title: TEXT。值
description: Value 屬性會指定或抓取文字控制項中顯示的文字。
ms.assetid: dbc50be2-ee18-4661-a343-9e906879aba0
keywords:
- TEXT. value Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d87f688f7afffeb588a37ac13ebff4cdc7cc105
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998793"
---
# <a name="textvalue"></a><span data-ttu-id="cbd68-104">TEXT。值</span><span class="sxs-lookup"><span data-stu-id="cbd68-104">TEXT.value</span></span>

<span data-ttu-id="cbd68-105">**Value** 屬性會指定或抓取文字控制項中顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="cbd68-105">The **value** attribute specifies or retrieves the text that is displayed in the Text control.</span></span>

``` syntax
        elementID.value
```

## <a name="possible-values"></a><span data-ttu-id="cbd68-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="cbd68-106">Possible Values</span></span>

<span data-ttu-id="cbd68-107">此屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="cbd68-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbd68-108">備註</span><span class="sxs-lookup"><span data-stu-id="cbd68-108">Remarks</span></span>

<span data-ttu-id="cbd68-109">如果文字控制項的寬度不足以包含提供的文字，則會裁剪文字，並顯示省略號來說明事實。</span><span class="sxs-lookup"><span data-stu-id="cbd68-109">If the width of the Text control is insufficient to contain the text provided, the text is cropped, and an ellipsis is shown to illustrate the fact.</span></span> <span data-ttu-id="cbd68-110">如果尚未設定 **工具提示** 屬性，則在游標停留在控制項上時，完整文字會顯示為工具提示。</span><span class="sxs-lookup"><span data-stu-id="cbd68-110">If the **toolTip** attribute has not been set, the complete text will then appear as a ToolTip when the cursor hovers over the control.</span></span>

<span data-ttu-id="cbd68-111">如果未指定寬度，控制項的預設寬度就是字串的寬度。</span><span class="sxs-lookup"><span data-stu-id="cbd68-111">If a width is not specified, the default width for the control is the width of the string.</span></span>

<span data-ttu-id="cbd68-112">如果未指定控制項的高度，則預設高度為一行。</span><span class="sxs-lookup"><span data-stu-id="cbd68-112">If the height of the control is not specified, the default height is one line.</span></span>

<span data-ttu-id="cbd68-113">如果 [ **wordWrap** ] 屬性設定為 [true]，而且控制項的高度足以容納另一行文字，則文字會換行至後續的行。</span><span class="sxs-lookup"><span data-stu-id="cbd68-113">If the **wordWrap** attribute is set to true and the height of the control is enough to accommodate another line of text, the text wraps to a subsequent line.</span></span> <span data-ttu-id="cbd68-114">只會在文字之間進行換行。</span><span class="sxs-lookup"><span data-stu-id="cbd68-114">Wrapping only occurs between words.</span></span> <span data-ttu-id="cbd68-115">也可以強制換行，如 **wordWrap** 中所述。</span><span class="sxs-lookup"><span data-stu-id="cbd68-115">Line breaks may also be forced, as explained under **wordWrap**.</span></span>

## <a name="examples"></a><span data-ttu-id="cbd68-116">範例</span><span class="sxs-lookup"><span data-stu-id="cbd68-116">Examples</span></span>

<span data-ttu-id="cbd68-117">下列範例是完整的面板定義檔，說明如何使用 **TEXT** 專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="cbd68-117">The following sample is a complete skin definition file that illustrates how the attributes of the **TEXT** element are used.</span></span> <span data-ttu-id="cbd68-118">您可以在與 SDK 一起安裝的範例目錄中找到它。</span><span class="sxs-lookup"><span data-stu-id="cbd68-118">It can be found in the Samples directory that was installed with the SDK.</span></span>


```C++
<THEME>
  <VIEW
    height = "175"
  >
    <TEXT 
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      disabledForegroundColor = "#CCCCCC"
      justification = "Center"
      value = "Play"
      cursor = "hand"
      enabled = "wmpenabled:player.controls.play"
      onClick = "JScript: player.URL='https://proseware.com/laure.wma';"
    />
    <TEXT
      top = "50"
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      disabledForegroundColor = "#CCCCCC"
      justification = "Center"
      value = "Stop"
      cursor = "hand"
      enabled = "wmpenabled:player.controls.stop"
      onClick = "JScript: player.controls.stop();"
    />
    <TEXT
      top = "100"
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "Close"
      cursor = "hand"
      onClick = "JScript: view.close();"
    />
    <TEXT
      top = "30"
      left = "120"
      width = "200"
      fontSize = "20"
      fontStyle = "Underline"
      justification = "Center"
      value = "Volume"
    />
    <TEXT
      top = "60"
      left = "120"
      width = "200"
      fontSize = "40"
      justification = "Center"
      value = "wmpprop:player.settings.volume"
    />
    <TEXT
      top = "65"
      left = "142"
      width = "40"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "-"
      cursor = "hand"
      toolTip = "decrease volume"
      onClick = "player.settings.volume = player.settings.volume - 5"
    />
    <TEXT
      top = "65"
      left = "260"
      width = "40"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "+"
      cursor = "hand"
      toolTip = "increase volume"
      onClick = "player.settings.volume = player.settings.volume + 5"
    />
    <TEXT
      top = "155"
      width = "300"
      height = "30"
      fontFace = "System"
      backgroundColor = "blue"
      foregroundColor = "white"
      justification = "Center"
      scrolling = "true"
      scrollingAmount = "1"
      scrollingDelay = "50"
      value = "wmpprop:player.status"
    />
  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="cbd68-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="cbd68-119">Requirements</span></span>



| <span data-ttu-id="cbd68-120">需求</span><span class="sxs-lookup"><span data-stu-id="cbd68-120">Requirement</span></span> | <span data-ttu-id="cbd68-121">值</span><span class="sxs-lookup"><span data-stu-id="cbd68-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="cbd68-122">版本</span><span class="sxs-lookup"><span data-stu-id="cbd68-122">Version</span></span><br/> | <span data-ttu-id="cbd68-123">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="cbd68-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cbd68-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cbd68-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbd68-125">**TEXT 元素**</span><span class="sxs-lookup"><span data-stu-id="cbd68-125">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="cbd68-126">**文字。工具提示**</span><span class="sxs-lookup"><span data-stu-id="cbd68-126">**TEXT.toolTip**</span></span>](text-tooltip.md)
</dt> <dt>

[<span data-ttu-id="cbd68-127">**WordWrap**</span><span class="sxs-lookup"><span data-stu-id="cbd68-127">**TEXT.wordWrap**</span></span>](text-wordwrap.md)
</dt> </dl>

 

 





