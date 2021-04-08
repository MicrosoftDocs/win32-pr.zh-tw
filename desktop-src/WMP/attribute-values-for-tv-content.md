---
title: 電視內容的屬性值
description: 電視內容的屬性值
ms.assetid: 70afb0fc-9eb0-4b94-a32a-f9202db94270
keywords:
- Windows Media Player，媒體專案的屬性
- Windows Media Player 物件模型，媒體專案的屬性
- 物件模型、媒體專案的屬性
- Windows Media Player 行動裝置，媒體專案的屬性
- Windows Media Player ActiveX 控制項、媒體專案的屬性
- Windows Media Player 的行動 ActiveX 控制項、媒體專案的屬性
- ActiveX 控制項、媒體專案的屬性
- Windows Media Player 文件庫、媒體專案的屬性
- 文件庫、媒體專案的屬性
- 屬性、電視內容
- 電視內容屬性值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb63e872edd80944772a320da5f2094e6d8f5757
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022085"
---
# <a name="attribute-values-for-tv-content"></a>電視內容的屬性值

在本主題中， **Player** 物件是以下列方式定義：


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Windows Media Player 10 或更新版本可以組織媒體櫃中的電視內容。 Windows Media Player 將電視內容視為影片內容的子類別。 若要讓影片內容顯示在媒體櫃的電視節點中，請使用 *媒體* 將 **wm/MediaClassPrimaryID** 和 **wm/MediaClassSecondaryID** 屬性設定為下表中的值。**setItemInfo** 方法：



| 屬性                    | 值                                |
|------------------------------|--------------------------------------|
| **WM/MediaClassPrimaryID**   | DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B |
| **WM/MediaClassSecondaryID** | BA7F258A-62F7-47A9-B21F-4651C42A000E |



 

您也可以使用這些值來判斷特定的數位媒體專案是否包含電視內容（使用 *媒體*）。**getItemInfo** 或 *媒體*。**getItemInfoByType** 方法。

當您指定或抓取這些值時，請記得使用 **GUID** 值做為 **字串** 值。

下列 c # 範例程式碼會設定媒體類別屬性，以便將媒體專案識別為電視內容。


```C++
// Initialize the media object.
// This code assumes only 1 item named MyFile.
IWMPMedia3 media = (IWMPMedia3)Player.mediaCollection.getByName("MyFile").item(0);

// Set the primary media-class identifier.
media.setItemInfo("WM/MediaClassPrimaryID", "DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B");

// Set the secondary media-class identifier.
media.setItemInfo("WM/MediaClassSecondaryID", "BA7F258A-62F7-47A9-B21F-4651C42A000E");

```



如需媒體類別屬性可能值的詳細資訊，請參閱 [Windows Media 中繼資料使用指導方針](/previous-versions/ms867702(v=msdn.10))。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**媒體專案屬性**](media-item-attributes.md)
</dt> <dt>

[**程式庫存取**](library-access.md)
</dt> <dt>

[**媒體物件**](media-object.md)
</dt> </dl>

 

 




