---
title: 執行模型
description: 執行模型
ms.assetid: 1947eb24-3a55-4d30-924e-93f2eed2c7b6
keywords:
- OpenGL、執行模型
- 執行模型 OpenGL
- OpenGL、用戶端/伺服器模型
- 用戶端/伺服器模型 OpenGL
- OpenGL、網路透明
- framebuffers，執行模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86012912f9bd963da0489b83cc4a5c1e7e1722ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932475"
---
# <a name="execution-model"></a>執行模型

OpenGL 命令的解讀模型是用戶端/伺服器。 應用程式程式碼 (用戶端) 發出命令，這些命令會由 OpenGL (伺服器) 進行解讀和處理。 伺服器不一定會與用戶端在同一部電腦上運作。 就這種情況而言，OpenGL 是網路透明的。 伺服器可以維護數個 OpenGL 內容，每個都是封裝的 OpenGL 狀態。 用戶端可以連接到這些內容的任何一個。 您可以藉由擴充現有的通訊協定 (（例如 X 視窗系統) 或使用獨立的通訊協定）來執行必要的網路通訊協定。 未提供任何 OpenGL 命令來取得使用者輸入。

配置畫面格緩衝區資源的視窗系統最終會控制畫面格緩衝區上 OpenGL 命令的效果。 視窗系統：

-   判斷畫面格緩衝區 OpenGL 的哪些部分可在任何指定時間存取。
-   將這些部分的結構傳達給 OpenGL。

因此，沒有可設定畫面格緩衝區或初始化 OpenGL 的 OpenGL 命令。 框架緩衝區設定是在 OpenGL 之外與視窗系統一起完成;當視窗系統組態 OpenGL 轉譯的視窗時，就會發生 OpenGL 初始化。

 

 




