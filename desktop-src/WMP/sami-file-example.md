---
title: 薩米文檔案範例
description: 薩米文檔案範例
ms.assetid: 52b566f1-0d87-4bf2-87b3-3821e69a5699
keywords:
- 'Windows Media Player，可同步的可存取媒體交換 (薩米文) '
- 'Windows Media Player 物件模型、已同步處理的可存取媒體交換 (薩米文) '
- '物件模型、同步的可存取媒體交換 (薩米) '
- 'Windows Media Player 行動裝置、已同步處理的可存取媒體交換 (薩米文) '
- 'Windows Media Player ActiveX 控制項、同步存取媒體交換 (薩米文) '
- 'Windows Media Player 的行動 ActiveX 控制項、已同步處理的可存取媒體交換 (薩米文) '
- 'ActiveX 控制項、同步的可存取媒體交換 (薩米) '
- 已同步處理的可存取媒體交換 (薩米) ，檔案
- 薩米文 (同步處理的可存取媒體交換) 、檔案
- 已同步處理的可存取媒體交換 (薩米) ，範例程式碼
- " (同步處理的可存取媒體交換) ，範例程式碼"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9634de52f71b4ca1db151bdf9104c3891c8ce5d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "103853271"
---
# <a name="sami-file-example"></a><span data-ttu-id="40b41-114">薩米文檔案範例</span><span class="sxs-lookup"><span data-stu-id="40b41-114">SAMI File Example</span></span>

<span data-ttu-id="40b41-115">下列範例程式碼是一個完整的薩米文檔案，其中包含一組隱藏式輔助字幕文字，以及數個適用于文字樣式和標題語言的類別宣告。</span><span class="sxs-lookup"><span data-stu-id="40b41-115">The following example code is a complete SAMI file with one set of closed caption text and several class declarations for text style and caption language.</span></span>


```C++
<SAMI>
<HEAD>
   <STYLE TYPE = "text/css">
   <!--
   /* P defines the basic style selector for closed caption paragraph text */
   P {font-family:sans-serif; color:white;}
   /* Source, Small, and Big define additional ID selectors for closed caption text */
   #Source {color: orange; font-family: arial; font-size: 12pt;}
   #Small {Name: SmallTxt; font-size: 8pt; color: yellow;}
   #Big {Name: BigTxt; font-size: 12pt; color: magenta;}
   /* ENUSCC and FRFRCC define language class selectors for closed caption text */
   .ENUSCC {Name: 'English Captions'; lang: en-US; SAMIType: CC;}
   .FRFRCC {Name: 'French Captions'; lang: fr-FR; SAMIType: CC;}
   -->
   </STYLE>
</HEAD>
<BODY>
   <!<entity type="mdash"/>- The closed caption text displays at 1000 milliseconds. -->
   <SYNC Start = 1000>
      <!-- English closed captions -->
      <P Class = ENUSCC ID = Source>Narrator
      <P Class = ENUSCC>Great reason to visit Seattle, brought to you by two out-of-staters.
      <!-- French closed captions -->
      <P Class = FRFRCC ID = Source>Narrateur
      <P Class = FRFRCC>Deux personnes ne venant la r&eacute;gion vous donnent de bonnes raisons de visiter Seattle.
</BODY>
</SAMI>

```



<span data-ttu-id="40b41-116">在薩米文檔案內定義的樣式符合元素、類別和識別碼的標準 CSS 選取器語法。</span><span class="sxs-lookup"><span data-stu-id="40b41-116">Styles defined within a SAMI file conform to standard CSS selector syntax for elements, classes, and IDs.</span></span> <span data-ttu-id="40b41-117">在 BODY 元素中，所有 P 元素都具有針對 STYLE 專案中 P 元素選取器定義的樣式。</span><span class="sxs-lookup"><span data-stu-id="40b41-117">In the BODY element, all P elements have the style defined for the P element selector in the STYLE element.</span></span> <span data-ttu-id="40b41-118">專案的 class 屬性（attribute）會指定該專案的語言，如 () 中的選取器開頭的樣式元素中的類別選取器所定義。</span><span class="sxs-lookup"><span data-stu-id="40b41-118">The class attribute of an element specifies the language of that element as defined by the class selectors in the STYLE element (the selectors beginning with periods).</span></span> <span data-ttu-id="40b41-119">類別選取器指定的語言名稱可以是任何字串。</span><span class="sxs-lookup"><span data-stu-id="40b41-119">The language names specified by the class selectors can be any string.</span></span> <span data-ttu-id="40b41-120">已指定 ID 屬性的專案會套用額外的樣式，如同 STYLE 專案中的識別碼選取器所示， (前面加上字元) 的選取器 \# 。</span><span class="sxs-lookup"><span data-stu-id="40b41-120">Elements with the ID attribute specified have additional styling applied as indicated by the ID selectors in the STYLE element (the selectors prefixed with \# characters).</span></span>

<span data-ttu-id="40b41-121">搭配 Windows Media Player 物件模型使用時，類別選取器會對應至 *ClosedCaption*。**SAMILang** 屬性，可用來指定標題的語言。</span><span class="sxs-lookup"><span data-stu-id="40b41-121">When used in conjunction with the Windows Media Player object model, the class selectors correspond to the *ClosedCaption*.**SAMILang** property, which can be used to specify the language of the captions.</span></span> <span data-ttu-id="40b41-122">識別碼選取器會對應至 *ClosedCaption*。**SAMIStyle** 屬性，可用來指定要在其中顯示標題的樣式。</span><span class="sxs-lookup"><span data-stu-id="40b41-122">The ID selectors correspond to the *ClosedCaption*.**SAMIStyle** property, which can be used to specify the style the captions will appear in.</span></span>

<span data-ttu-id="40b41-123">如需建立薩米文檔案的詳細資訊，請參閱 [Microsoft 網站](/documentation/)上的瞭解薩米文1.0。</span><span class="sxs-lookup"><span data-stu-id="40b41-123">For more information about creating SAMI files, see Understanding SAMI 1.0 at the [Microsoft website](/documentation/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="40b41-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="40b41-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40b41-125">**將隱藏式輔助字幕新增至數位媒體**</span><span class="sxs-lookup"><span data-stu-id="40b41-125">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 