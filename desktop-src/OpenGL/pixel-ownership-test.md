---
title: 圖元擁有權測試
description: 圖元擁有權測試會判斷目前的 OpenGL 內容是否擁有畫面格緩衝區中對應至特定片段的圖元。
ms.assetid: aa9428a6-cc05-4df4-ba31-444f999006a8
keywords:
- OpenGL 處理管線，圖元擁有權測試
- 圖元擁有權測試 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ad5ae57dbbff9f3551ecc222cd0a628193c97f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301175"
---
# <a name="pixel-ownership-test"></a>圖元擁有權測試

圖元擁有權測試會判斷目前的 OpenGL 內容是否擁有畫面格緩衝區中對應至特定片段的圖元。 如果是，則片段會繼續進行下一個測試。 如果不是，則視窗系統會決定是否要捨棄片段，或是否要使用該片段來執行任何進一步的片段作業。 在這項測試中，當 OpenGL 視窗遮蔽時，視窗系統會控制行為。

 

 




