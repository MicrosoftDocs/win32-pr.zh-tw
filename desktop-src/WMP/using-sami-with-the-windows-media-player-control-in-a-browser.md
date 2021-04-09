---
title: 在瀏覽器中搭配 Windows Media Player 控制項使用薩米文
description: 在瀏覽器中搭配 Windows Media Player 控制項使用薩米文
ms.assetid: 41906e57-adaa-4df7-86ba-19b8a757e216
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
ms.openlocfilehash: b651c3af117942d56ffc5334323913d26cdf6f99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932551"
---
# <a name="using-sami-with-the-windows-media-player-control-in-a-browser"></a><span data-ttu-id="ad490-114">在瀏覽器中搭配 Windows Media Player 控制項使用薩米文</span><span class="sxs-lookup"><span data-stu-id="ad490-114">Using SAMI with the Windows Media Player Control in a Browser</span></span>

<span data-ttu-id="ad490-115">您可以使用基本腳本和 Windows Media Player 控制項物件模型，在一個檔案中宣告不同的樣式類別，而不是建立每個字型樣式或語言的薩米文檔案。</span><span class="sxs-lookup"><span data-stu-id="ad490-115">Instead of creating a SAMI file for each font style or language, you can declare different style classes in one file by using basic scripting and the Windows Media Player control object model.</span></span> <span data-ttu-id="ad490-116">您可以建立自訂控制項，讓使用者可以在不同的樣式和語言選項之間進行選擇。</span><span class="sxs-lookup"><span data-stu-id="ad490-116">You can create custom controls that enable the user to choose between the different style and language options.</span></span> <span data-ttu-id="ad490-117">此外，您可以完全掌控播放程式介面的設計和每個函式的自訂。</span><span class="sxs-lookup"><span data-stu-id="ad490-117">Furthermore, you have complete control over the design of the Player interface and the customization of each function.</span></span>

<span data-ttu-id="ad490-118">如需在網頁中內嵌 Windows Media Player 控制項的詳細資訊，請參閱 [在網頁中編寫腳本的簡單範例](simple-example-of-scripting-in-a-web-page.md)。</span><span class="sxs-lookup"><span data-stu-id="ad490-118">For detailed information about embedding the Windows Media Player control in a webpage, see [Simple Example of Scripting in a Web Page](simple-example-of-scripting-in-a-web-page.md).</span></span>

<span data-ttu-id="ad490-119">下列範例程式碼示範如何使用隱藏式輔助字幕搭配網頁中內嵌的 Windows Media Player 控制項。</span><span class="sxs-lookup"><span data-stu-id="ad490-119">The following example code demonstrates how to use closed captions with the Windows Media Player control embedded in a webpage.</span></span> <span data-ttu-id="ad490-120">它包含的控制項可讓使用者選取字型樣式和語言。</span><span class="sxs-lookup"><span data-stu-id="ad490-120">It includes controls to allow the user to select font style and language.</span></span>


```C++
<HTML>
<HEAD>

<SCRIPT>
  // The following variable is used to prevent multiple initialization.
  var initialized = false;
  // The following function populates the select boxes.
  // It is called the first time the media file is opened.
  // Before then, the SAMI settings cannot be retrieved.
  function initialize() {
    var newOption;
    for (var i = 0; i < Player.closedCaption.SAMILangCount; i++) {
      newOption = document.createElement("OPTION");
      newOption.text = Player.closedCaption.getSAMILangName(i);
      newOption.value = newOption.text;
      CCLang.options.add(newOption);
    }
    for (var i = 0; i < Player.closedCaption.SAMIStyleCount; i++) {
      newOption = document.createElement("OPTION");
      newOption.text = Player.closedCaption.getSAMIStyleName(i);
      newOption.value = newOption.text;
      CCStyle.options.add(newOption);
    }
    initialized = true;
  }
</SCRIPT>

<!-- The following script code runs when the page is fully loaded. -->
<SCRIPT for="window" event="onload()">
  Player.closedCaption.captioningID = "captions";
  Player.closedCaption.SAMIFileName = "https://www.proseware.com/Media/seattle.smi";
  // The digital media file will open automatically, after which
  // the OpenStateChange event (handled below) will fire.
  Player.URL = "https://www.proseware.com/Media/seattle.wmv";
</SCRIPT>

<!-- The following script code runs when a media file is opened. -->
<SCRIPT for="Player" event="OpenStateChange(NewState)">
  // The first time this event fires, the Player stops and the 
  // initialize function is called. This allows the user to 
  // select a language and style before viewing the file.
  if (13 == NewState && !initialized) {
    Player.controls.stop();
    initialize();
  }
</SCRIPT>

</HEAD>
<BODY>

<OBJECT 
  ID="Player" 
  classID="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"
  height="200" 
  width="250"
>
</OBJECT>

<TABLE height="100" width="250" border="3" bordercolor="blue">
  <TR align="center">
    <TD bgcolor="white">
      <SELECT ID="CCLang" onClick="Player.closedCaption.SAMILang = value"></SELECT>
      <SELECT ID="CCStyle" onClick="Player.closedCaption.SAMIStyle = value"></SELECT>
    </TD>
  </TR>
  <TR height="75">
    <TD bgcolor="blue">
      <DIV id="captions"></DIV>
    </TD>
  </TR>
</TABLE>

</BODY>
</HTML>

```



## <a name="related-topics"></a><span data-ttu-id="ad490-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="ad490-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad490-122">**將隱藏式輔助字幕新增至數位媒體**</span><span class="sxs-lookup"><span data-stu-id="ad490-122">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




