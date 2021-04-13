---
title: 執行選取專案和意見反應
description: 執行選取專案和意見反應
ms.assetid: 908114b3-ac0e-4fd5-ad28-137e6af7ffc7
keywords:
- OpenGL，選取範圍
- OpenGL、意見反應
- OpenGL、轉譯
- 選取模式 OpenGL
- 意見反應模式 OpenGL
- 轉譯模式 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be13ae103d33039c996851582823c23c30316731
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300876"
---
# <a name="performing-selection-and-feedback"></a>執行選取專案和意見反應

選取專案、意見反應和轉譯都是作業的互斥模式。 轉譯是一般的預設模式，在此模式中，片段是由光柵產生的。

在選取範圍和意見反應模式中，不會產生任何片段;因此，不會進行畫面格緩衝區修改。 在 [選取] 模式中，您可以決定要將哪些基本專案繪製至視窗的某個區域;在意見反應模式中，會將要進行柵格化之基本專案的相關資訊回送至應用程式。

您可以使用 [**glRenderMode**](glrendermode.md)在這三種模式中進行選取。

-   [選取範圍](selection.md)
-   [意見反應](feedback.md)
-   [選取範圍和意見反應參考](selection-and-feedback-reference.md)

 

 




