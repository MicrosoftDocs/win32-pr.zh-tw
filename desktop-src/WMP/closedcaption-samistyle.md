---
title: ClosedCaption.SAMIStyle
description: SAMIStyle 屬性會指定或抓取隱藏式輔助字幕樣式。
ms.assetid: 5535fb31-f1c0-49c4-b758-df74964b1e67
keywords:
- ClosedCaption. SAMIStyle Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIStyle
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ebe81c2c2c4f4504d6167abe538c52ab769550a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990589"
---
# <a name="closedcaptionsamistyle"></a><span data-ttu-id="9c043-104">ClosedCaption.SAMIStyle</span><span class="sxs-lookup"><span data-stu-id="9c043-104">ClosedCaption.SAMIStyle</span></span>

<span data-ttu-id="9c043-105">**SAMIStyle** 屬性會指定或抓取隱藏式輔助字幕樣式。</span><span class="sxs-lookup"><span data-stu-id="9c043-105">The **SAMIStyle** property specifies or retrieves the closed captioning style.</span></span>

``` syntax
player.closedCaption.SAMIStyle
```

## <a name="possible-values"></a><span data-ttu-id="9c043-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="9c043-106">Possible Values</span></span>

<span data-ttu-id="9c043-107">這個屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="9c043-107">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c043-108">備註</span><span class="sxs-lookup"><span data-stu-id="9c043-108">Remarks</span></span>

<span data-ttu-id="9c043-109">薩米文檔案可以包含數個格式樣式定義。</span><span class="sxs-lookup"><span data-stu-id="9c043-109">A SAMI file can contain several format style definitions.</span></span> <span data-ttu-id="9c043-110">薩米文的樣式定義于薩米文檔案的 <STYLE> 和 </STYLE> 標記之間。</span><span class="sxs-lookup"><span data-stu-id="9c043-110">SAMI styles are defined between the <STYLE> and </STYLE> tags in the SAMI file.</span></span> <span data-ttu-id="9c043-111">樣式的定義是以文字字串前面加上 \# 字元。</span><span class="sxs-lookup"><span data-stu-id="9c043-111">A style is defined with a text string preceded by a \# character.</span></span> <span data-ttu-id="9c043-112">例如：</span><span class="sxs-lookup"><span data-stu-id="9c043-112">For example:</span></span>


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}

```



<span data-ttu-id="9c043-113">這會指定產生特定字型的樣式。</span><span class="sxs-lookup"><span data-stu-id="9c043-113">This specifies a style that produces a particular font.</span></span>

<span data-ttu-id="9c043-114">如果未指定薩米體樣式，預設會使用薩米文檔案中所定義的第一個樣式。</span><span class="sxs-lookup"><span data-stu-id="9c043-114">If no SAMI style is specified, the first style defined in the SAMI file is used by default.</span></span>

<span data-ttu-id="9c043-115">**Windows Media Player 10** 行動裝置版：這個屬性是唯讀的，而且一律會傳回空字串。</span><span class="sxs-lookup"><span data-stu-id="9c043-115">**Windows Media Player 10 Mobile:** This property is read only, and always returns an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="9c043-116">範例</span><span class="sxs-lookup"><span data-stu-id="9c043-116">Examples</span></span>

<span data-ttu-id="9c043-117">下列 JScript 範例會建立使用 *closedCaption* 的 HTML SELECT 元素。**SAMIStyle** ，以變更隱藏式輔助字幕文字的外觀。</span><span class="sxs-lookup"><span data-stu-id="9c043-117">The following JScript example creates an HTML SELECT element that uses *closedCaption*.**SAMIStyle** to change the appearance of the closed caption text.</span></span> <span data-ttu-id="9c043-118">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="9c043-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create the SELECT element. -->
<SELECT ID = CCMode  NAME = "CCMode"  LANGUAGE = "JScript"

       /* Change the text style when the SELECT element changes. */
        onChange = "Player.closedCaption.SAMIStyle = CCMode.value;
        ">

       /* Fill the SELECT list with options, set the default to Strong. */
        <OPTION VALUE = "Normal">Normal
        <OPTION VALUE = "Small">Small 
        <OPTION VALUE = "Big Bold Italic" SELECTED>Strong
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="9c043-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c043-119">Requirements</span></span>



| <span data-ttu-id="9c043-120">需求</span><span class="sxs-lookup"><span data-stu-id="9c043-120">Requirement</span></span> | <span data-ttu-id="9c043-121">值</span><span class="sxs-lookup"><span data-stu-id="9c043-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9c043-122">版本</span><span class="sxs-lookup"><span data-stu-id="9c043-122">Version</span></span><br/> | <span data-ttu-id="9c043-123">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="9c043-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9c043-124">DLL</span><span class="sxs-lookup"><span data-stu-id="9c043-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="9c043-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c043-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c043-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9c043-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c043-127">**將隱藏式輔助字幕新增至數位媒體**</span><span class="sxs-lookup"><span data-stu-id="9c043-127">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="9c043-128">**ClosedCaption 物件**</span><span class="sxs-lookup"><span data-stu-id="9c043-128">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> </dl>

 

 





