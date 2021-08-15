---
title: Direct3D 轉換管線
description: 本文提供 Direct3D 應用程式開發人員如何藉由直接操作 Direct3D 矩陣來設定 Direct3D 轉換管線參數的技術說明。
ms.assetid: 48ae49f0-1162-c292-4bd4-34da5aadd2df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6377e3b17cfb4ceb6eda1f4cf59a93c12fd3e6b2f7e43f29f622ed6ee12c271
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118152332"
---
# <a name="the-direct3d-transformation-pipeline"></a>Direct3D 轉換管線

本文提供 Direct3D 應用程式開發人員如何藉由直接操作 Direct3D 矩陣來設定 Direct3D 轉換管線參數的技術說明。

-   [概觀](#overview)
-   [轉換管線](#the-transformation-pipeline)
-   [使用量提示](#usage-tips)

## <a name="overview"></a>概觀

Direct3D 使用三個轉換在像素座標（螢幕空間）中變更您的 3D 模型座標。 這些轉換為世界轉換、檢視轉換和投影轉換。

「世界轉換」可控制如何將模型座標轉換成全局座標。 全球轉換可以包含翻譯、旋轉和 scalings，但不適用於燈光。 如需有關使用世界轉換的詳細資訊，請參閱「 [世界轉換](/windows/desktop/direct3d9/world-transform)」。

View 轉換控制從全局座標轉換成「相機空間」，以決定世界中的相機位置。 如需使用 view 轉換的範例，請參閱 [視圖轉換](/windows/desktop/direct3d9/view-transform)。

投影轉換會將幾何從相機空間變更為「剪輯空間」，並套用透視扭曲。 「剪輯空間」一詞是指在此轉換期間將幾何裁剪到視圖磁片區的方式。 如需使用投影轉換的範例，請參閱 [投射轉換](/windows/desktop/direct3d9/projection-transform)。

最後，裁剪空間中的幾何會轉換成圖元座標， (螢幕空間) 。 這項轉換是由 [視口] 設定所控制。

剪切和轉換頂點必須在同質空間中進行 (單純放置的空間、座標系統) 包含第四個元素的空間，但大部分應用程式的最終結果都必須是「螢幕空間」中所定義的非同質三維 (3D) 座標。 這表示輸入頂點和裁剪磁片區必須轉譯成同質空間，才能執行裁剪，然後轉譯回非同質空間來顯示。

這三個 Direct3D 轉換（世界、觀點和投射轉換）都是由 Direct3D 矩陣所定義。 Direct3D 矩陣是 [**D3DMATRIX**](/windows/desktop/direct3d9/d3dmatrix) 結構所定義的4x4 同質矩陣。 雖然 Direct3D 矩陣不是標準物件，但它們並不是由 COM 介面表示，您可以建立和設定它們，就像是任何其他 Direct3D 物件一樣。 如需 Direct3D 矩陣的詳細資訊，請參閱 [轉換](/windows/desktop/direct3d9/transforms)。

## <a name="the-transformation-pipeline"></a>轉換管線

如果模型座標中的頂點是由 Pm = (Xm、Ym、Zm、1) ，則下圖中顯示的轉換會套用到計算畫面座標 Ps = (Xs、Y) 、Zs、Ws) 。

![螢幕空間轉換的模型空間](images/d3dxfrm61.gif)

以下是上圖所示的階段說明：

1.  世界矩陣 Mworld 會將頂點從模型空間轉換成世界空間。 此矩陣的設定方式如下：

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_WORLD, matrix address) 
    ```

    Direct3D 的執行假設這個矩陣的最後一個資料行是 (0、0、0、1) 。 如果使用者指定的矩陣具有不同的最後一個資料行，但光源和模糊不正確，則不會傳回任何錯誤。

2.  視圖矩陣 Mview 會將頂點從世界空間轉換成相機空間。 此矩陣的設定方式如下：

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_VIEW, matrix address) 
    ```

    Direct3D 的執行假設這個矩陣的最後一個資料行是 (0、0、0、1) 。 如果使用者指定的矩陣具有不同的最後一個資料行，但光源和模糊不正確，則不會傳回任何錯誤。

3.  投射矩陣 Mproj 會將頂點從相機空間轉換成投射空間。 此矩陣的設定方式如下：

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_PROJECTION, matrix address) 
    ```

    投射矩陣的最後一個資料行應該是 (0、0、1、0) 或 (0、0、a、0) ，以取得正確的霧化和光源效果;建議 (0、0、1、0) 表單。

    在投影空間中，所有點的剪輯磁片區都是 Xp = (Xp、Yp、Zp、Wp) 定義為：

    ``` syntax
        -Wp < Xp <= Wp 
        -Wp < Yp <= Wp 
        0 < Zp <= Wp 
    ```

    不滿足這些方程式的所有點都將會被裁剪。

    如果視圖磁片區定義為：

    -   在接近裁剪平面之相機空間中的 Sw 螢幕視窗寬度
    -   Sh-接近裁剪平面之相機空間中的螢幕視窗高度
    -   Zn-沿著相機空間中的 Z 軸距離接近裁剪平面的距離
    -   Zf-沿著相機空間中的 Z 軸距離到最遠的裁剪平面

    然後可以撰寫透視圖投影矩陣，如下所示：

    ![顯示透視圖投影矩陣。](images/d3dxfrm62.gif)

    其中 Mij 是 Mproj 的成員。

    針對正向投射，我們有：

    ![正向投射](images/d3dxfrm63.gif)

    Direct3D 假設透視圖投影矩陣的形式如下：

    ![透視圖投影矩陣](images/d3dxfrm64.gif)

    如果透視圖投影矩陣沒有此表單，則會有一些成品。 例如，資料表霧化將無法運作。

4.  Direct3D 可讓使用者變更剪輯磁片區，如下所示：

    ![變更剪輯音量](images/d3dxfrm65.gif)

    這可以重寫為：

    ![變更剪輯磁片區重寫](images/d3dxfrm66.gif)

    其中：

    ``` syntax
        Cx, Cy - dvClipX, dvClipY from D3DVIEWPORT9  
        Cw, Ch - dvClipWidth, dvClipHeight from D3DVIEWPORT9  
        Zmin, Zmax - dvMinZ, dvMaxZ from D3DVIEWPORT9  
    ```

    這項轉換可以提供更高的精確度，而且相當於調整和移動剪切的磁片區。

    對應的 Mclip 矩陣為：

    ![mclip 矩陣](images/d3dxfrm67.gif)

    頂點的轉換方式如下：

    ``` syntax
        dvClipWidth = 2   
        dvClipHeight = 2   
        dvClipX = -1   
        dvClipY = 1   
        dvMinZ = 0   
        dvMaxZ = 1   
    ```

    如果您不想要調整剪輯磁片區，您可以將資料區參數設定為預設值：

    ``` syntax
        (Xc, Yc, Zc, Wc) = (Xp, Yp, Zp, Wp) * Mclip   
    ```

5.  如果使用者 \_ 在 DrawPrimitive 呼叫中指定 D3DDP DONOTCLIP 旗標，則裁剪階段是選擇性的。 在此情況下，可以結合所有矩陣 (包括 Mvs) 。
6.  區形調整矩陣 Mvs 會將座標調整為位於 [視口] 視窗內，並將 Y 軸從最多向下翻轉：

    ![視口調整矩陣 mvs](images/d3dxfrm68.gif)

    其中：

    ``` syntax
        dwX, dwY - viewport offsets in pixels from D3DVIEWPORT9 
        dwWidth, dwHeight - viewport width and height in pixels from D3DVIEWPORT9    
    ```

7.  最後，會計算螢幕座標，並將其傳遞至轉譯器：

    ![計算並傳遞至轉譯器的螢幕座標](images/d3dxfrm69.gif)

## <a name="usage-tips"></a>使用量提示

以下是如何使用 Direct3D 轉換管線的一些秘訣：

-   世界上的最後一個資料行和視圖矩陣應該是 (0、0、0、1) ，否則光源將會不正確。
-   除非您完全瞭解所需的內容，否則請將 [視口] 參數設定為 [建立身分識別 Mclip 矩陣]。

    ``` syntax
        dvClipWidth = 2 
        dvClipHeight = 2
        dvClipX = -1
        dvClipY = 1
        dvMinZ = 0 
        dvMaxZ = 1
    ```

 

 