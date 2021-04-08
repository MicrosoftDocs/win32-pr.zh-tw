---
title: 關於薩米文的檔案
description: 關於薩米文的檔案
ms.assetid: 39b1e8a8-bbeb-4376-89d9-03a147f4c4fd
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
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d310ab3eb3016937f148ebb26e810dd9e6e6b6b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840151"
---
# <a name="about-sami-files"></a>關於薩米文的檔案

薩米文檔案是副檔名為或薩米文的文字檔。 它們包含用於同步處理之隱藏式輔助字幕、字幕和音訊描述的文字字串。 它們也會指定 Windows Media Player 控制項用來同步處理隱藏式輔助字幕文字與音訊或影片內容的計時參數。 當數位媒體檔案到達薩米文檔案中指定的時間時，文字就會隨著網頁的隱藏式輔助字幕顯示區域而變更。

除了簡單的文字編輯器 (例如 Microsoft 記事本) 之外，不需要特殊的軟體就能建立薩米文的檔案。 薩米文和 HTML 共用通用元素，例如 <HEAD> 和 <BODY> 標記。 在 HTML 中，以薩米文的檔案使用的標記必須一律成對使用。 例如，BODY 元素的開頭是 <BODY> 標記，且一律以標記結尾 </BODY> 。

基本的薩米文檔案需要三個基本標記： <SAMI> 、 <HEAD> 和 <BODY> 。

<SAMI>標記會將檔識別為薩米文的檔，讓其他應用程式可以辨識其檔案格式。

在 <HEAD> 和 </HEAD> 標記之間，您可以定義基本指導方針和其他薩米文檔的格式資訊，例如檔標題、一般資訊，以及隱藏式輔助字幕的樣式屬性。 就像 HTML 一樣，標頭專案內宣告的內容不會顯示為輸出。

<BODY>和</BODY>標記之間定義的專案和屬性會顯示使用者看到的內容。 在薩米文中，BODY 元素包含用於同步處理的參數，以及用於隱藏式輔助字幕的文字字串。

在標頭專案內定義，STYLE 元素可提供薩米文中的新增功能。 在 <STYLE> 和 </STYLE> 標記之間，您可以針對樣式和配置，定義多個級聯樣式表 (CSS) 選取器。 您可以自訂字型、大小和對齊等樣式屬性，以提供豐富的使用者體驗，同時也能提升存取範圍。 例如，定義大型文字字型樣式類別可以改善難以讀取小文字的使用者可讀性。 此外，藉由定義數種不同的語言類別，您可以協助國際使用者更加瞭解數位媒體內容。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**將隱藏式輔助字幕新增至數位媒體**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




