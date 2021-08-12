---
title: 關於設定物件
description: 關於設定物件
ms.assetid: 941463e6-7928-438e-824e-e5e281421a4a
keywords:
- Windows Media Player，設定物件
- Windows Media Player 物件模型，設定物件
- 物件模型，設定物件
- Windows Media Player ActiveX 控制項，設定物件
- ActiveX 控制項，設定物件
- Windows Media PlayerMobile ActiveX control、設定物件
- Windows Media Player行動設定物件
- 設定物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b74b8bd9db946a2915486647fa5831158198bef6115a34b6bb9fb81177f433de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583670"
---
# <a name="about-the-settings-object"></a>關於設定物件

**設定** 物件控制了控制項的設定，例如音量、播放次數、靜音等等。 它只能透過 **Player** 物件的 **設定** 屬性來存取。 **設定** 屬性會傳回 **設定** 物件。 您只能在建立 **設定** 物件的屬性之後，才能存取該物件的屬性。 例如，若要取得 **Volume** 屬性的值，您必須使用下列程式碼：


```C++
myvolume = player.settings.volume;

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**指令碼語言的播放程式物件模型**](player-object-model-for-scripting-languages.md)
</dt> <dt>

[**設定物件**](settings-object.md)
</dt> </dl>

 

 




