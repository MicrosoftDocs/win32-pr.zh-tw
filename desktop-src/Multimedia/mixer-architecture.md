---
title: Mixer建築
description: Mixer建築
ms.assetid: 11d650bf-c258-4818-88b7-9fdc71a8d859
keywords:
- 多媒體音訊，混音器架構
- 音訊、混音器架構
- 音訊 mixers，架構
- 音訊 mixers，音訊行
- 音訊行
- 音訊 mixers，控制項
- 多媒體音訊、混音器控制項
- 音訊、混音器控制項
- mixers，音訊行
- mixers，架構
- mixers，控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3f435396dd2a8d5983f596628711dfd01afe7111e75af1dc2060f5c6c4ef0a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065608"
---
# <a name="mixer-architecture"></a>Mixer建築

混音器架構的基本元素是一 *條音訊*。 音訊行是由一或多個源自單一來源或系統資源的資料通道所組成。 例如，身歷聲音訊線有兩個資料通道，但因為它來自單一來源，所以會被視為單一音訊行。

混音器架構會提供路由服務，以管理電腦上的音訊線。 如果您已安裝足夠的硬體裝置和軟體驅動程式，就可以使用路由服務。 混音器架構可讓數個音訊來源線對應到單一目的地音訊行。

每個音訊線條可以有相關聯的混音器控制項。 混音器控制項可以執行任意數目的函式 (例如控制音量) ，視相關聯音訊行的特性而定。

 

 




