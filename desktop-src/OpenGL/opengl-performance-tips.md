---
title: OpenGL 效能秘訣
description: OpenGL 效能秘訣
ms.assetid: f85bf725-1361-49b9-894c-c803b2dead60
keywords:
- OpenGL，效能秘訣
- OpenGL、最佳作法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7e5b6fa33f8d6841d0fd47d1a655ef99facc84e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673263"
---
# <a name="opengl-performance-tips"></a>OpenGL 效能秘訣

這些程式設計實務會優化應用程式的效能：

-   當只有單一材質屬性在每個頂點上 (快速地變動時，請使用 [**glColorMaterial**](glcolormaterial.md) ，例如) 。 使用 [**glMaterial**](glmaterial-functions.md) 進行不頻繁的變更，或當超過單一材質屬性時，快速地變動。
-   使用 [**glLoadIdentity**](glloadidentity.md) 初始化矩陣，而不是載入您自己的身分識別矩陣複本。
-   使用特定的矩陣呼叫（例如 [**glRotate**](glrotate.md)、 [**glTranslate**](gltranslate.md)和 [**glScale**](glscale.md)），而不是撰寫您自己的旋轉、轉譯和調整矩陣，以及呼叫 [**glMultMatrix**](glmultmatrix.md)。
-   使用 [**glPushAttrib**](glpushattrib.md) 和 [**glPopAttrib**](glpopattrib.md) 來儲存和還原狀態值。 只有當您的應用程式需要其本身計算的狀態值時，才使用查詢函數。
-   使用顯示清單來封裝可能需要大量記憶體的狀態變更。 例如，請將完全指定紋理所需的所有 [**glTexImage**](glteximage1d.md) 呼叫放 (，可能) 也會將相關聯的 [**glTexParameter**](gltexparameter-functions.md)、 [**glPixelStore**](glpixelstore-functions.md)和 [**glPixelTransfer**](glpixeltransfer.md) 呼叫放入單一顯示清單中。 呼叫此顯示清單來選取材質。
-   使用顯示清單來封裝將會重複繪製之固定物件的轉譯呼叫。
-   若要將用戶端/伺服器環境中的網路頻寬降到最低，請使用評估工具甚至是簡單的介面鑲嵌。
-   可能的話，為了避免產生 GL 正規化的額外負荷 \_ ，請提供單位長度的法線。 因為 [**glScale**](glscale.md) 幾乎一律需要啟用 GL 正規化 \_ ，所以請避免在執行光源時使用 **glScale** 。
-   如果不需要平滑陰影，請將 [**glShadeModel**](glshademodel.md) 設定為 [一般] \_ 。
-   如果可能的話，請針對每個框架使用單一 [**glClear**](glclear.md) 呼叫。 請勿使用 **glClear** 來清除緩衝區的小型子領域加寬;您只能使用它來完全或幾乎完全清除緩衝區。
-   若要繪製多個獨立三角形，請使用單一呼叫，而不是多個呼叫來 [**glBegin**](glbegin.md) ( GL \_ 三角形 ) 或 **glBegin** ( GL \_ 多邊形 ) 的呼叫。 同樣：

    若要繪製單一三角形，請使用 GL \_ 三角形，而非 gl \_ 多邊形。

    使用單一呼叫來 [**glBegin**](glbegin.md) ( GL \_ 四邊形 ) ，而不是重複呼叫 **glBegin** ( gl \_ 多邊形 ) 。

    使用單一呼叫 [**glBegin**](glbegin.md) ( GL \_ 線 ) 來繪製多個獨立的線段，而不是多次呼叫 **glBegin** ( \_ GL 行 ) 。

-   一般情況下，請使用向量形式的命令來傳遞預先計算資料，並使用純量形式的命令來傳遞計算接近呼叫時間的值。
-   避免進行多餘的模式變更，例如將色彩設定為平面陰影多邊形的每個頂點之間的相同值。
-   繪製或複製影像時，請停用柵格化和個別片段作業，以將資源優化。 OpenGL 可以將材質套用至圖元影像。

 

 




