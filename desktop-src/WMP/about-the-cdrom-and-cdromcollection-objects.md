---
title: 關於 Cdrom 和 CdromCollection 物件
description: 關於 Cdrom 和 CdromCollection 物件
ms.assetid: b764806b-d9e1-4c36-b86b-24613501c926
keywords:
- Windows Media Player、Cdrom 物件
- Windows Media Player 物件模型、Cdrom 物件
- 物件模型、Cdrom 物件
- Windows Media Player ActiveX 控制項、Cdrom 物件
- ActiveX 控制項、Cdrom 物件
- Windows Media Player Mobile ActiveX 控制項、Cdrom 物件
- Windows Media Player Mobile、Cdrom 物件
- Cdrom 物件
- Windows Media Player，CdromCollection 物件
- Windows Media Player 物件模型，CdromCollection 物件
- 物件模型，CdromCollection 物件
- Windows Media Player ActiveX 控制項，CdromCollection 物件
- ActiveX 控制項，CdromCollection 物件
- Windows Media Player 行動 ActiveX 控制項，CdromCollection 物件
- Windows Media Player Mobile，CdromCollection 物件
- CdromCollection 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8fca9f7097f67226e31173670ca2935969704a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673800"
---
# <a name="about-the-cdrom-and-cdromcollection-objects"></a>關於 Cdrom 和 CdromCollection 物件

**Cdrom** 和 **CdromCollection** 物件會管理電腦上的 cd 光碟機介面，以供讀取和播放 cd 之用。

**CdromCollection** 物件只能透過 **Player** 物件的 **CdromCollection** 屬性來存取。 **CdromCollection** 屬性會傳回 **cdromCollection** 物件。 您只能在建立 **CdromCollection** 物件之後，存取其屬性。 例如，若要使用 **count** 屬性，您必須使用下列程式碼：


```C++
mycount = player.cdromcollection.count;
```



您只能透過 **CdromCollection** 物件存取 **Cdrom** 物件。 例如，若要使用 **退出** 方法來退出 CD，您必須先建立集合物件，然後建立物件中的專案。 若要退出 CD，請使用下列程式碼：


```C++
player.cdromcollection.item(0).eject();
```



在這兩種情況下，您會先建立集合物件 (**CdromCollection**) 然後取得該集合的特定物件。 物件是集合中的第一個專案，也就是對應到第一個 CD 光碟機的 **專案** (0) 。 然後，您可以在該專案上呼叫方法 **退出**。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Cdrom 物件**](cdrom-object.md)
</dt> <dt>

[**CdromCollection 物件**](cdromcollection-object.md)
</dt> <dt>

[**指令碼語言的播放程式物件模型**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




