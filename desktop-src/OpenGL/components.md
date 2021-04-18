---
title: 元件
description: 單元
ms.assetid: 9fbd957d-ee6b-475f-8a04-51effa206ad5
keywords:
- Windows 上的 OpenGL、元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c1294745938e245deda8296f2ce4d1df386b9f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969059"
---
# <a name="components"></a>單元

Microsoft 在 Windows 中執行 OpenGL 的功能包括下列元件：

-   目前的 OpenGL 命令的完整集合

    OpenGL 包含3D 圖形作業的核心功能程式庫。 這些基本函式是用來管理物件圖形描述、矩陣轉換、光源、著色、材質、剪切、點陣圖、霧化和消除鋸齒功能。 這些核心函數的名稱具有 "gl" 前置詞。

    許多 OpenGL 命令都有數種變化，其參數的數目和類型不同。 計算所有的變異數，有300個以上的 OpenGL 命令。

-   OpenGL 公用程式 (X.GLU 隊) 程式庫

    這是輔助函式的程式庫，能補充核心 OpenGL 函式的功能。 這些命令會管理材質支援、座標轉換、多邊形鑲嵌、呈現球體、圓柱和磁片、NURBS (非統一的有理 B 曲線) 曲線和表面，以及錯誤處理。

-   OpenGL 程式設計指南輔助程式庫

    這是與平臺無關的簡易函式程式庫，可用於管理 windows、處理輸入事件、繪製傳統立體物件、管理背景進程，以及執行程式。 視窗管理和輸入常式提供基本層級的功能，可讓您快速開始在 OpenGL 中進行程式設計。

    不過，請勿在生產應用程式中使用它們。 以下是此警告的一些原因：

    -   訊息迴圈是在程式庫程式碼中。
    -   沒有任何方法可新增其他 WM 訊息的處理常式 \* 。
    -   邏輯調色板的支援很少。

    此程式庫會在 *OpenGL 程式設計指南* 中說明和使用。

-   WGL 函式

    這組函式會將 OpenGL 連接至 Windows 視窗化系統。 這些函式會管理轉譯內容、顯示清單、擴充功能和字型點陣圖。 WGL 函式類似于將 OpenGL 連接至 X 視窗系統的 GLX 擴充功能。 這些函數的名稱具有 "wgl" 前置詞。

-   適用于像素格式和雙重緩衝的新 Windows 函數

    這些函式支援每個視窗的像素格式和雙重緩衝 (，以) windows 的平滑影像變更。 這些新功能只適用于 OpenGL 圖形視窗。

 

 




