---
title: 訊息反映
description: 訊息反映
ms.assetid: 26a124d7-6499-4e8f-9001-d2782c1cc290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9191e0e189f8653518aaabb3c31785cde960538b0828d56669096ebf1d63f1e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048046"
---
# <a name="message-reflection"></a>訊息反映

強烈建議 ActiveX 的控制容器支援訊息反映。 這會讓子類別化控制項更有效率地運作。 如果支援訊息反映，則必須支援 MessageReflect 環境屬性，並將值 **設為 TRUE**。 如果容器不會執行訊息反映，則 OLE CDK 會為每個子類別化控制項建立兩個視窗，以代表控制項容器提供訊息反映。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[容器](containers.md)
</dt> </dl>

 

 




