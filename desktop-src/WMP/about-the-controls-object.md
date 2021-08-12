---
title: 關於控制項物件
description: 關於控制項物件
ms.assetid: 1678c931-af47-42c9-a8a5-b6b775aebda8
keywords:
- Windows Media Player，控制項物件
- Windows Media Player 物件模型，控制項物件
- 物件模型、控制項物件
- Windows Media Player ActiveX 控制項、控制項物件
- ActiveX 控制項，控制項物件
- Windows Media PlayerMobile ActiveX 控制項，控制項物件
- Windows Media PlayerMobile、Controls 物件
- Controls 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea914234ce4458d296a27efe7cf3a392b45b09f05e81f35bef5a355a4e12eab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583895"
---
# <a name="about-the-controls-object"></a>關於控制項物件

**Controls** 物件使用像是 **播放** 和 **停止** 的方法，透過控制項來控制數字媒體內容的傳輸。 它只能透過 **Player** 物件的 **Controls** 屬性來存取。 **Controls** 屬性會傳回 **controls** 物件。 您只能在建立 **控制項** 物件之後，才存取這些屬性。 例如，若要使用 **Play** 方法，您必須使用下列程式碼：


```C++
player.controls.play();

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Controls 物件**](controls-object.md)
</dt> <dt>

[**指令碼語言的播放程式物件模型**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




