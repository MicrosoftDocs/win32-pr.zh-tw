---
title: 使用自然變化
description: 使用自然變化
ms.assetid: 5d5750e4-cf30-43dc-9419-7e6bbdb9aa5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fd2d35afeb168dc8839ba259f0079434b487c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092233"
---
# <a name="use-natural-variation"></a>使用自然變化

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

雖然應用程式的傳統介面（例如功能表和對話方塊）中的簡報一致性可讓介面更容易預測，但是會改變字元介面中的動畫和讀出的輸出。 適當地改變字元的回應可提供更自然的介面。 如果字元一律以相同的方式處理使用者;例如，一律說出相同的單字，使用者很可能會將人物視為乏味、disinterested 或甚至是。 人們通訊很少牽涉到精確的重複作業。 即使在類似的情況下重複某項功能，我們也可能變更用語、手勢或臉部運算式。

Microsoft 代理程式可讓您針對某個字元建立某種變化。 定義字元的動畫時，您可以在任何動畫框架上使用分支機率，以在動畫播放時變更動畫。 您也可以將多個動畫指派給每個狀態。 Microsoft Agent 會在每次啟動狀態時隨機播放其中一個指派的動畫。 針對語音輸出，您也可以在輸出文字中包含分隔號字元，以自動改變說出的文字。 例如，在處理此文字作為 [**說話**](speak-method.md) 方法的一部分時，Microsoft Agent 會隨機選取下列其中一個語句：

「我可以這麼說。 \|我可以說， \|我可以說其他東西」。

 

 




