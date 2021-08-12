---
title: 變更屬性值
description: 變更屬性值
ms.assetid: c7dd7355-453c-44a5-9932-c41bb3ae2e40
keywords:
- Windows Media Player，媒體專案的屬性
- Windows Media Player 物件模型，媒體專案的屬性
- 物件模型、媒體專案的屬性
- Windows Media Player行動電話，媒體專案的屬性
- Windows Media Player ActiveX 控制項、媒體專案的屬性
- Windows Media Player行動 ActiveX 控制項、媒體專案的屬性
- ActiveX 控制項，媒體專案的屬性
- Windows Media Player 文件庫、媒體專案的屬性
- 文件庫、媒體專案的屬性
- 屬性，變更值
- 變更屬性值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e870d8bfa13012bd79fdd672f1543db4a484ca5d9674ef1a9e48e832119ea1b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118581114"
---
# <a name="changing-attribute-values"></a>變更屬性值

如果您的網頁或應用程式具有程式庫的讀取/寫入權限，而且可以讀取和寫入屬性，則可以變更屬性的值。

您可以變更目前媒體專案的屬性。 若要變更多個媒體專案的屬性，您可以將每個媒體專案依次指派給 *播放* 程式。**currentMedia** 屬性。

在本主題中， **Player** 物件是以下列方式定義：


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



若要變更屬性，請呼叫 *Player*。*currentMedia*。**setItemInfo** 方法，如下列 c # 範例所示。


```C++
IWMPMedia3 media;
// Initialize the Media object
media = Player.currentMedia;
// Set the new genre value
media.setItemInfo("WM/Genre", "My New Genre");

```



建議您呼叫 *媒體*。**isReadOnlyItem** 方法來判斷您是否可以變更特定屬性。

> [!Note]  
> 如果您將控制項內嵌在您的應用程式中，除非使用者執行 Windows Media Player，否則您變更的檔案屬性不會寫入數位媒體檔案。 如果您在以 c + + 撰寫的遠端應用程式中使用控制項，則在進行變更之後，將會立即將您變更的檔案屬性寫入數位媒體檔案。 無論是哪一種情況，您都可以透過程式庫立即使用變更。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**媒體專案屬性**](media-item-attributes.md)
</dt> <dt>

[**程式庫存取**](library-access.md)
</dt> <dt>

[**媒體物件**](media-object.md)
</dt> <dt>

[**讀取屬性值**](reading-attribute-values.md)
</dt> </dl>

 

 




