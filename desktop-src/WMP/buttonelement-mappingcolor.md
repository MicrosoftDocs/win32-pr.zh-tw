---
title: BUTTONELEMENT.mappingColor
description: MappingColor 屬性會指定或抓取在 BUTTONGROUP 中識別此 BUTTONELEMENT 的色彩索引鍵。
ms.assetid: e7b1663c-3263-41d5-9a69-4cf1dcf0fc1f
keywords:
- BUTTONELEMENT. mappingColor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.mappingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7318f01246578fe8ff34118427c95afb7b3bb098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106988668"
---
# <a name="buttonelementmappingcolor"></a><span data-ttu-id="62f6c-104">BUTTONELEMENT.mappingColor</span><span class="sxs-lookup"><span data-stu-id="62f6c-104">BUTTONELEMENT.mappingColor</span></span>

<span data-ttu-id="62f6c-105">**MappingColor** 屬性會指定或抓取在 **BUTTONGROUP** 中識別此 **BUTTONELEMENT** 的色彩索引鍵。</span><span class="sxs-lookup"><span data-stu-id="62f6c-105">The **mappingColor** attribute specifies or retrieves the color key that identifies this **BUTTONELEMENT** in the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.mappingColor
```

## <a name="possible-values"></a><span data-ttu-id="62f6c-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="62f6c-106">Possible Values</span></span>

<span data-ttu-id="62f6c-107">這個屬性是包含任何 Microsoft Internet Explorer 色彩值的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="62f6c-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="62f6c-108">它沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="62f6c-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="62f6c-109">備註</span><span class="sxs-lookup"><span data-stu-id="62f6c-109">Remarks</span></span>

<span data-ttu-id="62f6c-110">這個屬性會指定按鈕群組 **mappingImage** 中對應于這個 button 元素的區域色彩。</span><span class="sxs-lookup"><span data-stu-id="62f6c-110">This attribute specifies the color of the region in the button group **mappingImage** that corresponds to this button element.</span></span> <span data-ttu-id="62f6c-111">此按鈕元素會處理此區域的所有點擊。</span><span class="sxs-lookup"><span data-stu-id="62f6c-111">All clicks on this region are handled by this button element.</span></span>

<span data-ttu-id="62f6c-112">如果指定的色彩無效，則不會啟用 **BUTTONELEMENT** 。</span><span class="sxs-lookup"><span data-stu-id="62f6c-112">If an invalid color is specified, the **BUTTONELEMENT** is not activated.</span></span>

## <a name="examples"></a><span data-ttu-id="62f6c-113">範例</span><span class="sxs-lookup"><span data-stu-id="62f6c-113">Examples</span></span>

<span data-ttu-id="62f6c-114">下列範例是完整的面板定義檔，說明如何使用一些 **BUTTONELEMENT** 屬性。</span><span class="sxs-lookup"><span data-stu-id="62f6c-114">The following sample is a complete skin definition file that illustrates how some of the **BUTTONELEMENT** attributes are used.</span></span> <span data-ttu-id="62f6c-115">您可以在與 SDK 一起安裝的範例目錄中找到它。</span><span class="sxs-lookup"><span data-stu-id="62f6c-115">It can be found in the Samples directory that was installed with the SDK.</span></span>


```
<THEME>
  <VIEW
    backgroundImage = "background.bmp"
    titleBar = "False"
  >
    <PLAYER
      URL = "https://proseware.com/mellow.wma"
    />
    <EFFECTS
      id = "myeffects"
      top = "25"
      left = "88"
      width = "180"
      height = "150"
    />
    <BUTTONGROUP
      mappingImage = "map.bmp"
      hoverImage = "hover.bmp"
    >
      <BUTTONELEMENT
        mappingColor = "#00FF00"
        upToolTip = "Next"
        onClick = "JScript:myeffects.next();"
      />
      <BUTTONELEMENT
        mappingColor = "#FF0000"
        upToolTip = "Previous"
        onClick = "JScript:myeffects.previous();"
      />
    </BUTTONGROUP>
  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="62f6c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="62f6c-116">Requirements</span></span>



| <span data-ttu-id="62f6c-117">需求</span><span class="sxs-lookup"><span data-stu-id="62f6c-117">Requirement</span></span> | <span data-ttu-id="62f6c-118">值</span><span class="sxs-lookup"><span data-stu-id="62f6c-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="62f6c-119">版本</span><span class="sxs-lookup"><span data-stu-id="62f6c-119">Version</span></span><br/> | <span data-ttu-id="62f6c-120">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="62f6c-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="62f6c-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62f6c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62f6c-122">**色彩參考**</span><span class="sxs-lookup"><span data-stu-id="62f6c-122">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="62f6c-123">**BUTTONELEMENT 元素**</span><span class="sxs-lookup"><span data-stu-id="62f6c-123">**BUTTONELEMENT Element**</span></span>](buttonelement-element.md)
</dt> <dt>

[<span data-ttu-id="62f6c-124">**BUTTONGROUP. mappingImage**</span><span class="sxs-lookup"><span data-stu-id="62f6c-124">**BUTTONGROUP.mappingImage**</span></span>](buttongroup-mappingimage.md)
</dt> </dl>

 

 





