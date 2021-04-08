---
title: 關於 Settings 物件
description: 關於 Settings 物件
ms.assetid: 941463e6-7928-438e-824e-e5e281421a4a
keywords:
- Windows Media Player，Settings 物件
- Windows Media Player 物件模型，Settings 物件
- 物件模型，設定物件
- Windows Media Player ActiveX 控制項，Settings 物件
- ActiveX 控制項，Settings 物件
- Windows Media Player 行動 ActiveX 控制項，Settings 物件
- Windows Media Player Mobile，Settings 物件
- Settings 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b20dae51d42e6c67a59ddc23dca19bc7f4180001
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839452"
---
# <a name="about-the-settings-object"></a>關於 Settings 物件

[ **設定** ] 物件控制控制項的設定，例如音量、播放次數、靜音等等。 它只能透過 **Player** 物件的 **Settings** 屬性來存取。 **Settings** 屬性會傳回 **settings** 物件。 建立之後，您只能存取 **設定** 物件的屬性。 例如，若要取得 **Volume** 屬性的值，您必須使用下列程式碼：


```C++
myvolume = player.settings.volume;

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**指令碼語言的播放程式物件模型**](player-object-model-for-scripting-languages.md)
</dt> <dt>

[**Settings 物件**](settings-object.md)
</dt> </dl>

 

 




