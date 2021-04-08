---
title: 訊息反映
description: 訊息反映
ms.assetid: 26a124d7-6499-4e8f-9001-d2782c1cc290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96cb563597e5aa92440e1b1434420e983268d9b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020769"
---
# <a name="message-reflection"></a>訊息反映

強烈建議 ActiveX 控制項容器支援訊息反映。 這會讓子類別化控制項更有效率地運作。 如果支援訊息反映，則必須支援 MessageReflect 環境屬性，並將值 **設為 TRUE**。 如果容器不會執行訊息反映，則 OLE CDK 會為每個子類別化控制項建立兩個視窗，以代表控制項容器提供訊息反映。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[容器](containers.md)
</dt> </dl>

 

 




