---
title: '在 Windows Media 下載套件中使用框線 (已淘汰) '
description: '在 Windows Media 下載套件中使用框線 (已淘汰) '
ms.assetid: d3961c5f-8cce-439d-9a13-41be2f45d92c
keywords:
- Windows Media 中繼檔，Windows Media 下載套件
- Windows Media Player，Windows Media 下載套件
- 中繼檔，Windows Media 下載套件
- Windows Media、Windows Media 下載套件
- 框線，關於
- Windows Media 下載套件、框線
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 87f7d0fec341bb79bfe9b8dd739b63a9ba3a66ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372279"
---
# <a name="using-borders-in-windows-media-download-packages-deprecated"></a>在 Windows Media 下載套件中使用框線 (已淘汰) 

本頁記載了未來版本的 Windows Media Player 和 Windows Media Player SDK 可能無法使用的功能。

框線可讓您為已封裝的內容建立自訂的圖形化使用者介面。 框線可以包含影像、互動式控制項和網站的連結等元素。 如果您想要在已封裝的內容中新增額外的值（例如商標或廣告），您可以使用框線。 當使用者下載並開啟您的 Windows Media 下載套件之後，Windows Media Player 會在播放封裝的內容時自動顯示您的自訂框線。

不同于能讓使用者完全取代 Windows Media Player 使用者介面的面板，只會在完整模式播放程式的 [ **現正播放** ] 窗格中顯示框線。 不過，您用來建立面板的相同工具和技術也會用來建立框線。 下圖顯示框線。

![顯示的框線 windows media player 10](images/border-v10.png)

在嘗試建立框線之前，請務必瞭解建立面板的基本技巧。 您可以使用兩種程式設計語言來完成框執行緒序設計：可延伸標記語言 (XML)  (XML) 和 Microsoft JScript。 XML 是用來定義介面元素，例如按鈕、滑杆和文字方塊。 您不需要瞭解 XML 的所有詳細資料，因為您不需要撰寫新的 XML 程式碼元素;您可以直接使用 Windows Media Player 所提供的專案。 雖然建立框線不需要 JScript，但它可以用來提供額外的功能。

副檔名為 wmz 的壓縮框線檔包含具有 wms 副檔名的框線定義檔，以及框線內使用的所有影像檔案。

若要在 Windows Media 下載套件中包含框線，只要建立框線，並在 Windows Media 中繼檔播放清單中參考該框線即可。 當播放程式剖析中繼檔並解讀參考框線的 **外觀** 專案之後，就會將 border 檔案載入 Windows Media Player 中。 面板 **元素僅** 用於框線，而面板元素的 HREF 屬性只能參考每個套件的一個外觀。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Windows Media Player (已淘汰) 的框線**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**(淘汰的 Windows Media 下載套件)**](windows-media-download-packages--deprecated.md)
</dt> <dt>

[**Windows Media Player 的外觀**](windows-media-player-skins.md)
</dt> </dl>

 

 




