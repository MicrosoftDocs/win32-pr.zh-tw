---
title: 圖元擁有權測試
description: 圖元擁有權測試會判斷目前的 OpenGL 內容是否擁有畫面格緩衝區中對應至特定片段的圖元。
ms.assetid: aa9428a6-cc05-4df4-ba31-444f999006a8
keywords:
- OpenGL 處理管線，圖元擁有權測試
- 圖元擁有權測試 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12cfefe133b3951fa70d51736f664ec5a7cb9942c4c05f892115dd222013f294
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936247"
---
# <a name="pixel-ownership-test"></a>圖元擁有權測試

圖元擁有權測試會判斷目前的 OpenGL 內容是否擁有畫面格緩衝區中對應至特定片段的圖元。 如果是，則片段會繼續進行下一個測試。 如果不是，則視窗系統會決定是否要捨棄片段，或是否要使用該片段來執行任何進一步的片段作業。 在這項測試中，當 OpenGL 視窗遮蔽時，視窗系統會控制行為。

 

 




