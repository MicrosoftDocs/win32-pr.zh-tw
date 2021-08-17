---
title: 在瀏覽器中搭配 Windows Media Player 控制項使用薩米文
description: 在瀏覽器中搭配 Windows Media Player 控制項使用薩米文
ms.assetid: 41906e57-adaa-4df7-86ba-19b8a757e216
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
ms.openlocfilehash: d277f2849e6036d85bc8c03940a7dbd59df8b81083ca88240ebd68be768fde9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134341"
---
# <a name="using-sami-with-the-windows-media-player-control-in-a-browser"></a>在瀏覽器中搭配 Windows Media Player 控制項使用薩米文

您可以使用基本腳本和 Windows Media Player 控制項物件模型，在一個檔案中宣告不同的樣式類別，而不是建立每個字型樣式或語言的薩米文檔案。 您可以建立自訂控制項，讓使用者可以在不同的樣式和語言選項之間進行選擇。 此外，您可以完全掌控播放程式介面的設計和每個函式的自訂。

如需在網頁中內嵌 Windows Media Player 控制項的詳細資訊，請參閱[在網頁中編寫腳本的簡單範例](simple-example-of-scripting-in-a-web-page.md)。

下列範例程式碼示範如何使用隱藏式輔助字幕搭配網頁中內嵌的 Windows Media Player 控制項。 它包含的控制項可讓使用者選取字型樣式和語言。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**將隱藏式輔助字幕新增至數位媒體**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




