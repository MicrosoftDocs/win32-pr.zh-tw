---
title: 使用自動播放清單來組織文件庫中的內容
description: 使用自動播放清單來組織文件庫中的內容
ms.assetid: 118d4357-044f-4986-af51-0c344470e891
keywords:
- Windows Media Player 線上商店、自動播放清單
- 線上商店、自動播放清單
- 輸入1個線上商店、自動播放清單
- 輸入2個線上商店、自動播放清單
- Windows Media Player 線上商店、組織文件庫內容
- 線上商店、組織文件庫內容
- 輸入1個線上商店、組織文件庫內容
- 輸入2個線上商店、組織文件庫內容
- Windows Media Player 線上商店、文件庫內容組織
- 線上商店、文件庫內容組織
- 輸入1個線上商店、文件庫內容組織
- 輸入2個線上商店、文件庫內容組織
- 程式庫，組織內容
- 組織文件庫內容
- 自動播放清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e32d0f95093d9550c71643330267d59a57f56db7e0d666274a492ac29b2c58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507168"
---
# <a name="using-auto-playlists-to-organize-content-in-the-library"></a>使用自動播放清單來組織文件庫中的內容

您可以使用自動播放清單來組織您所提供的 premium 內容。 例如，您可以使用 Windows Media Player 建立自動播放清單，其中只包含您所提供的內容，且使用者至少有四顆星的評等。 然後，您可以在 Windows Media Player 中將自動播放清單新增至媒體櫃，使其顯示在 [內容散發者] 節點下的 [已購買的音樂] 節點中。

若要這樣做，請遵循下列步驟：

1.  建立自動播放清單。
2.  使用 Windows 檔案總管，流覽至自動播放清單並取出 .wpl 檔案。
3.  使用 Windows Media Player 物件模型，將自動播放清單新增至程式庫。
4.  將播放清單的 **WM/ContentDistributor** 屬性設定為內容轉銷商金鑰名稱。
5.  將播放清單的 [ **>synconly** ] 屬性設定為 [true]。

下列 JScript 程式碼範例所示範的函式會將名為「我的最愛點擊次數」的自動播放清單新增至程式庫中的 Proseware 節點：


```C++
function AddWPL()
{
    var pl = Player.mediaCollection.add("c:\\media\\Favorite Hits.wpl");
    pl.setItemInfo("WM/ContentDistributor", "Proseware");
    pl.setItemInfo("SyncOnly", true);
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於程式庫整合](download-manager-overview.md)
</dt> <dt>

[**Type 1 和 Type 2 線上商店的一般資訊**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**MediaCollection 新增**](mediacollection-add.md)
</dt> <dt>

[**播放清單。 setItemInfo**](playlist-setiteminfo.md)
</dt> <dt>

[**靜態和自動播放清單**](static-and-auto-playlists.md)
</dt> <dt>

[**>synconly 屬性**](synconly-attribute.md)
</dt> <dt>

[**WM/ContentDistributor 屬性**](wm-contentdistributor-attribute.md)
</dt> <dt>

[**使用程式庫**](working-with-the-library.md)
</dt> </dl>

 

 




