---
title: 多執行緒 OpenGL 繪圖策略
description: GDI 不支援多個執行緒。
ms.assetid: 3930029d-b2d9-4beb-bad6-4962f952d7ee
keywords:
- Windows、多執行緒繪圖上的 OpenGL
- 多執行緒 OpenGL 繪圖 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05d928a481e4334f97cad2f7009f008c899ad8378f3fd15cf9e117e6b9599393
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937253"
---
# <a name="multithread-opengl-drawing-strategies"></a>多執行緒 OpenGL 繪圖策略

GDI 不支援多個執行緒。 您必須針對每個執行緒使用不同的裝置內容和不同的轉譯內容。 這通常會限制使用多個執行緒搭配執行 OpenGL 應用程式之單一處理器系統的效能優勢。 不過，有一些方法可搭配單一處理器系統使用執行緒，以大幅提升效能。 例如，您可以使用個別的執行緒，將 OpenGL 轉譯呼叫傳遞給專用的立體硬體。

對稱式多重處理 (SMP) 系統可大幅受益于使用多個執行緒。 最簡單的策略是針對每個處理器使用個別的執行緒，以處理個別視窗中的 OpenGL 轉譯。 例如，在飛行模擬應用程式中，您可以使用不同的處理器和執行緒來呈現前端、背面和側邊。

執行緒只能有一個目前的現用轉譯內容。 當您使用多個執行緒和多個轉譯內容時，必須小心同步處理其使用方式。 例如，在所有線程完成繪製之後，只能使用一個執行緒來呼叫 [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) 。

 

 




