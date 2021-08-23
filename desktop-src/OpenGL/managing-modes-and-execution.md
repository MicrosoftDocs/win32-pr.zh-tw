---
title: 管理模式和執行
description: 管理模式和執行
ms.assetid: 6a1ecc42-194a-4d8f-94f6-fd59696d87cf
keywords:
- OpenGL、模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec448fa94c8ed0983be68f8aa1dbbef0974d2e040c4f68b002b026b300406981
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553978"
---
# <a name="managing-modes-and-execution"></a>管理模式和執行

許多 OpenGL 函數的作用取決於特定模式是否有效。 [**GlEnable**](glenable.md)和 [**glDisable**](gldisable.md)函數會設定這類模式;[**glIsEnabled**](glisenabled.md)會判斷是否已設定特定模式。

您可以使用 [**glFinish**](glfinish.md)來控制先前發行之 OpenGL 函式的執行，這會強制所有這類函式完成或 [**glFlush**](glflush.md)，以確保所有這類函式會在有限的時間內完成。

在特定的 OpenGL 執行中，您可以使用 [**glHint**](glhint.md)來控制提示的特定行為。 這類行為是色彩和材質座標插補的品質;霧化計算的精確度;以及反鋸齒點、線條或多邊形的取樣品質。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[模式和執行參考](modes-and-execution-reference.md)
</dt> </dl>

 

 




