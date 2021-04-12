---
title: 混音器架構
description: 混音器架構
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
ms.openlocfilehash: 447b0cdc44a33237aa7e0c726a5eb533b3bc7d0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300771"
---
# <a name="mixer-architecture"></a>混音器架構

混音器架構的基本元素是一 *條音訊*。 音訊行是由一或多個源自單一來源或系統資源的資料通道所組成。 例如，身歷聲音訊線有兩個資料通道，但因為它來自單一來源，所以會被視為單一音訊行。

混音器架構會提供路由服務，以管理電腦上的音訊線。 如果您已安裝足夠的硬體裝置和軟體驅動程式，就可以使用路由服務。 混音器架構可讓數個音訊來源線對應到單一目的地音訊行。

每個音訊線條可以有相關聯的混音器控制項。 混音器控制項可以執行任意數目的函式 (例如控制音量) ，視相關聯音訊行的特性而定。

 

 




