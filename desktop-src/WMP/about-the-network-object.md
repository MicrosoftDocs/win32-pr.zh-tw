---
title: 關於 Network 物件
description: 關於 Network 物件
ms.assetid: 367a51d4-2db8-4c9e-82b7-85b2b631c721
keywords:
- Windows Media Player、Network 物件
- Windows Media Player 物件模型、Network 物件
- 物件模型，網路物件
- Windows Media Player ActiveX 控制項、Network 物件
- ActiveX 控制項、Network 物件
- Windows Media Player 的行動 ActiveX 控制項、Network 物件
- Windows Media Player Mobile、Network 物件
- Network 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a1f3ff892a4d5b078956c9d126d0efaa844031d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671400"
---
# <a name="about-the-network-object"></a>關於 Network 物件

**Network** 物件管理的屬性可讓您決定內容透過網路進行串流的程度。 例如，您可以找出封包是否遺失，並採取適當的動作。 只有透過 **Player** 物件的 **network** 屬性才能存取 **network** 物件。 **Network** 屬性會傳回 **network** 物件。 您只能在建立 **網路** 物件的屬性之後，才存取這些屬性。 例如，若要使用 **頻寬** 屬性，您必須使用下列程式碼：


```C++
mybandwidth = player.network.bandwidth;

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Network 物件**](network-object.md)
</dt> <dt>

[**指令碼語言的播放程式物件模型**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




