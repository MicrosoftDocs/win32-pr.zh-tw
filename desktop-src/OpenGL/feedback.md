---
title: 意見反應
description: 在意見反應模式中，每個要進行柵格化的基本物件都會產生一個值區塊，而這些值會複製到意見陣列中。
ms.assetid: 92f14fe2-71f7-4b59-94a5-9669e986fb30
keywords:
- 意見反應模式、OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb5d307b9033a60a03b585cb4df6109293d3b9b0b276bde822ca595eb37fcd19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082448"
---
# <a name="feedback-mode"></a>意見反應模式

在意見反應模式中，每個要進行柵格化的基本物件都會產生一個值區塊，而這些值會複製到意見陣列中。 提供此陣列的 [**glFeedbackBuffer**](glfeedbackbuffer.md)，您必須先呼叫此陣列，才能將 OpenGL 放入意見反應模式。 值的每個區塊都會以表示基本類型的程式碼開頭，後面接著描述基本頂點和相關資料的值。 此外，也會為點陣圖和圖元矩形寫入專案。 在您呼叫 [**glRenderMode**](glrendermode.md) 讓 OpenGL 離開意見反應模式之前，不保證會將值寫入意見陣列中。 您可以使用 [**glPassThrough**](glpassthrough.md) 來提供以意見反應模式傳回的標記，就像是基本的標記一樣。

 

 




