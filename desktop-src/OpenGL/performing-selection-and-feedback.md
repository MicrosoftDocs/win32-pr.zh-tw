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
ms.openlocfilehash: 95efe3f07e86056cd0364daaed1e6a9c0ef402afc18b14d74cca313c9835479f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936283"
---
# <a name="performing-selection-and-feedback"></a>執行選取專案和意見反應

選取專案、意見反應和轉譯都是作業的互斥模式。 轉譯是一般的預設模式，在此模式中，片段是由光柵產生的。

在選取範圍和意見反應模式中，不會產生任何片段;因此，不會進行畫面格緩衝區修改。 在 [選取] 模式中，您可以決定要將哪些基本專案繪製至視窗的某個區域;在意見反應模式中，會將要進行柵格化之基本專案的相關資訊回送至應用程式。

您可以使用 [**glRenderMode**](glrendermode.md)在這三種模式中進行選取。

-   [選取範圍](selection.md)
-   [意見反應](feedback.md)
-   [選取範圍和意見反應參考](selection-and-feedback-reference.md)

 

 




