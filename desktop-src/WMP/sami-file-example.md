---
title: 薩米文檔案範例
description: 薩米文檔案範例
ms.assetid: 52b566f1-0d87-4bf2-87b3-3821e69a5699
keywords:
- 'Windows Media Player，可同步的可存取媒體交換 (薩米文) '
- 'Windows Media Player 物件模型、已同步處理的可存取媒體交換 (薩米文) '
- '物件模型、同步的可存取媒體交換 (薩米) '
- 'Windows Media Player行動裝置、已同步處理的可存取媒體交換 (薩米) '
- 'Windows Media Player ActiveX 控制項、同步可存取媒體交換 (薩米文) '
- 'Windows Media PlayerMobile ActiveX control、可同步存取的媒體交換 (薩米文) '
- 'ActiveX control、可同步存取的媒體交換 (薩米文) '
- 已同步處理的可存取媒體交換 (薩米) ，檔案
- 薩米文 (同步處理的可存取媒體交換) 、檔案
- 已同步處理的可存取媒體交換 (薩米) ，範例程式碼
- " (同步處理的可存取媒體交換) ，範例程式碼"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d4e2ab5189f99118afae3fb2dae7374323cc8c16605bb458a04bd31810ed91a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569804"
---
# <a name="sami-file-example"></a>薩米文檔案範例

下列範例程式碼是一個完整的薩米文檔案，其中包含一組隱藏式輔助字幕文字，以及數個適用于文字樣式和標題語言的類別宣告。


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



在薩米文檔案內定義的樣式符合元素、類別和識別碼的標準 CSS 選取器語法。 在 BODY 元素中，所有 P 元素都具有針對 STYLE 專案中 P 元素選取器定義的樣式。 專案的 class 屬性（attribute）會指定該專案的語言，如 () 中的選取器開頭的樣式元素中的類別選取器所定義。 類別選取器指定的語言名稱可以是任何字串。 已指定 ID 屬性的專案會套用額外的樣式，如同 STYLE 專案中的識別碼選取器所示， (前面加上字元) 的選取器 \# 。

搭配 Windows Media Player 物件模型使用時，類別選取器會對應至 *ClosedCaption*。**SAMILang** 屬性，可用來指定標題的語言。 識別碼選取器會對應至 *ClosedCaption*。**SAMIStyle** 屬性，可用來指定要在其中顯示標題的樣式。

如需建立薩米文檔案的詳細資訊，請參閱 [Microsoft 網站](/documentation/)上的瞭解薩米文1.0。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**將隱藏式輔助字幕新增至數位媒體**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 