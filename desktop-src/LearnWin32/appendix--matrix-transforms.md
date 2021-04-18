---
title: 附錄矩陣轉換
description: 本主題提供2D 圖形的矩陣轉換數學總覽。
ms.assetid: 8cc01f45-dd84-4f3e-a5f2-26edc5cbdfa1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5a9b09f75b17e4baf8afe5e7fde8643c06982f
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/28/2021
ms.locfileid: "104561986"
---
# <a name="appendix-matrix-transforms"></a>附錄：矩陣轉換

本主題提供2D 圖形的矩陣轉換數學總覽。 不過，您不需要知道矩陣數學，也可以在 Direct2D 中使用轉換。 如果您對數學有興趣，請閱讀本主題。否則，請隨意略過本主題。

-   [矩陣簡介](#introduction-to-matrices)
    -   [矩陣作業](#matrix-operations)
-   [仿射轉換](#affine-transforms)
    -   [轉譯轉換](#translation-transform)
    -   [調整轉換](#scaling-transform)
    -   [繞著原點旋轉](#rotation-around-the-origin)
    -   [圍繞任意點旋轉](#rotation-around-an-arbitrary-point)
    -   [扭曲轉換](#skew-transform)
-   [代表 Direct2D 中的轉換](#representing-transforms-in-direct2d)
-   [下一步](#next)

## <a name="introduction-to-matrices"></a>矩陣簡介

矩陣是實數的矩形陣列。 矩陣的 *順序* 是資料列和資料行的數目。 例如，如果矩陣有3個數據列和2個數據行，則順序為3×2。 矩陣通常會顯示以方括弧括住的矩陣元素：

![3 x 2 矩陣。](images/matrix01.png)

標記法：矩陣是以大寫字母來指定。 元素是由小寫字母所指定。 注標表示元素的資料列和資料行編號。 例如，第一個 *ij* 是矩陣 a 之 i'th 資料列和 j'th 資料行的元素。

下圖顯示的是 i × j 矩陣，並在矩陣的每個資料格中有個別元素。

![具有 i 個數據列和 j 資料行的矩陣。](images/matrix15.png)

### <a name="matrix-operations"></a>矩陣作業

本節說明在矩陣上定義的基本作業。

*加法*。 藉由加入 A 和 B 的對應元素，即可取得兩個矩陣的加總 + B：

<dl> A + b = \[ a *ij* \]  +  \[ b *ij* \]  =  \[ a *ij* + B *ij*\]
</dl>

純量 *乘法*。 這項作業會將矩陣乘以實數。 假設有一個實數 *，則* 會將 a 的每個元素乘以 *k* 來取得純量產品 kA。

<dl> kA = k \[ a *ij* \]  =  \[ k × a *ij*\]
</dl>

*矩陣乘法*。 假設有兩個矩陣 A 和 B 的 order (m x n) 和 (n × p) ，則產品 C = A × B 是訂單 (m × p) 的矩陣，定義如下：

![顯示矩陣乘法的公式。](images/matrix02.png)

或者，等同：

<dl> c *ij* = a *i* 1 x b1 *j* + a *i* 2 x b2 *j* + ... + a *in* + b *nj*  
</dl>

也就是說，若要計算每個專案 c *ij*，請執行下列動作：

1.  取得 A 的 i'th 資料列和 B 的 j'th 資料行。
2.  將資料列和資料行中的每個元素配對：第一個資料行專案的第一個資料列專案、第二個數據行專案的第二個數據列專案，依此類推。
3.  加總結果。

以下範例會將 (2 × 2) 矩陣乘以 (2 × 3) 矩陣。

![矩陣乘法。](images/matrix03.png)

矩陣乘法不是可交換的。 也就是說，A × B ≠ B × A。此外，從定義中，它會遵循並非每個矩陣配對都可以相乘。 左側矩陣中的資料行數目必須等於右邊矩陣中的資料列數目。 否則，×運算子未定義。

*識別矩陣*。 識別矩陣（指定 I）是定義如下的正方形矩陣：

<dl> 如果 *i* j，我的 *ij* = 1  =  **，否則為0。  
</dl>

換句話說，識別矩陣包含每個元素1，其中的資料列編號等於資料行編號，而所有其他元素則為零。 例如，以下是3×3身分識別矩陣。

![識別矩陣。](images/matrix04.png)

下列 equalities 會保留任何矩陣 M。

<dl> M x I = M  
I x M = M  
</dl>

## <a name="affine-transforms"></a>仿射轉換

*仿射轉換* 是將一個座標空間對應到另一個座標空間的數學運算。 換句話說，它會將一組點對應到另一組點。 仿射轉換有一些功能可讓它們在電腦圖形中很實用。

-   仿射轉換會保留 *共* 的。 如果有三個以上的點落在一行，它們仍會形成轉換之後的一行。 直條保持直接。
-   兩個仿射轉換的組合是仿射轉換。

2D 空間的仿射轉換具有下列格式。

![顯示2D 空間的仿射轉換。](images/matrix05.png)

如果您套用先前指定的矩陣乘法定義，您可以顯示兩個仿射轉換的乘積為另一個仿射轉換。 若要使用仿射轉換來轉換2D 點，點會以1×3矩陣表示。

<dl> P = \| x y 1 \|  
</dl>

前兩個元素包含點的 x 和 y 座標。 第三個元素會放置1，讓數學運算正常運作。 若要套用轉換，請將這兩個矩陣相乘，如下所示。

<dl> P ' = P × M  
</dl>

這會擴充至下列各項。

![仿射轉換。](images/matrix06.png)

其中

<dl> x ' = ax + cy + e  
y ' = bx + dy + f  
</dl>

若要取得已轉換的點，請採用矩陣 P 的前兩個元素。

<dl> p = (x '，y ' ) = (ax + cy + e，bx + dy + f)   
</dl>

> [!Note]  
> 1× *n* 矩陣稱為「資料 *列向量*」。 Direct2D 和 Direct3D 都使用資料列向量來代表2D 或3D 空間中的點。 您可以使用資料行向量 (*n* × 1) 和轉換轉換矩陣來取得相等的結果。 大部分的圖形文字都會使用直條圖向量形式。 本主題提供與 Direct2D 和 Direct3D 一致的資料列向量形式。

 

接下來的幾個部分會衍生基本轉換。

### <a name="translation-transform"></a>轉譯轉換

轉譯轉換矩陣的格式如下。

![轉譯轉換。](images/matrix07.png)

在此方程式中插入點 *P* 會產生：

<dl> P ' = (*x*  +  *dx*， *y*  +  *dy*) 
</dl>

這會對應至 X 軸 (x，y) 在 Y 軸的 X 軸和 *dy* 中由 *dx* 轉譯。

![顯示兩個點轉譯的圖表。](images/graphics22.png)

### <a name="scaling-transform"></a>調整轉換

縮放變換矩陣的格式如下。

![調整轉換。](images/matrix09.png)

在此方程式中插入點 *P* 會產生：

<dl> P ' = (*x* ∙ *dx*， *y* ∙ *dy*) 
</dl>

這會對應到點 (x，y) 以 *dx* 和 *dy* 來調整。

![顯示雙點比例的圖表。](images/graphics23.png)

### <a name="rotation-around-the-origin"></a>繞著原點旋轉

沿著原點旋轉點的矩陣具有下列格式。

![顯示旋轉轉換的公式。](images/matrix11.png)

轉換的點為：

<dl> P ' = (*x* CosΘ– ysinΘ， *x* sinΘ + *y* cosΘ) 
</dl>

證明。 若要顯示 P ' 代表旋轉，請考慮下圖。

![顯示原點周圍旋轉的圖表。](images/graphics24.png)

假設︰

<dl> <dt>

<span id="P____x_y_"></span><span id="p____x_y_"></span><span id="P____X_Y_"></span>P = (x，y) 
</dt> <dd>

要轉換的原始點。

</dd> <dt>

Φ
</dt> <dd>

由線條 (0，0) 到 P 所形成的角度。

</dd> <dt>

Θ
</dt> <dd>

用來旋轉與原點 (x，y) 的角度。

</dd> <dt>

<span id="P_____x__y__"></span><span id="p_____x__y__"></span><span id="P_____X__Y__"></span>P ' = (x '，y ' ) 
</dt> <dd>

已轉換的點。

</dd> <dt>

<span id="R"></span><span id="r"></span>R
</dt> <dd>

行的長度 (0、0) 至 P。也是旋轉圓形的半徑。

</dd> </dl>

> [!Note]  
> 此圖表會使用幾何中使用的標準座標系統，其中正面 y 軸會指向。 Direct2D 會使用 Windows 座標系統，其中正 y 軸會向下點。

 

X 軸和線條 (0，0) 至 P ' 之間的角度為Φ + Θ。 下列身分識別會保存：

<dl> x = R cosΦ  
y = R sinΦ  
x ' = R cos (Φ + Θ)   
y ' = R sin (Φ + Θ)   
</dl>

現在以Θ的角度來解決 x ' 和 y '。 依三角加法公式：

<dl> x ' = R (cosΦcosΘ– sinΦsinΘ) = RcosΦcosΘ– RsinΦsinΘ  
y ' = R (sinΦcosΘ + cosΦsinΘ) = RsinΦcosΘ + RcosΦsinΘ  
</dl>

取代，我們取得：

<dl> x ' = xcosΘ– ysinΘ  
y ' = xsinΘ + ycosΘ  
</dl>

對應至稍早所示的已轉換點 P '。

### <a name="rotation-around-an-arbitrary-point"></a>圍繞任意點旋轉

若要旋轉 (x，y) 以外的某個點，則會使用下列矩陣。

![旋轉轉換。](images/matrix13.png)

您可以使用 (x，y) 的點作為來源，來衍生此矩陣。

![顯示圍繞點旋轉的圖表。](images/graphics25.png)

讓 (x1，y1) 是旋轉點 (x0 的結果點，y0) 圍繞 (x，y) 的位置。 我們可以依照下列方式衍生 x1。

<dl> x1 = (x0 – x) cosΘ– (y0 – y) sinΘ + x  
x1 = x0cosΘ– y0sinΘ + \[ (1 – cosΘ) + ysinΘ \]  
</dl>

現在使用先前的公式 x1 = ax0 + cy0 + e，將此方程式插回到轉換矩陣。 使用相同的程式來衍生 y1。

### <a name="skew-transform"></a>扭曲轉換

扭曲轉換是由四個參數所定義：

-   Θ：沿著 X 軸扭曲的數量，以 y 軸的角度來測量。
-   Φ：沿著 y 軸扭曲的數量，以 X 軸的角度來測量。
-    (*px*、 *.py*) ：執行扭曲的點的 x 和 y 座標。

扭曲轉換會使用下列矩陣。

![扭曲轉換。](images/matrix14.png)

轉換的點為：

<dl> P ' = (*x*  +  *y* tanΘ– *.py* tanΘ、 *y*  +  *x* tanΦ) – *.py* tanΦ
</dl>

或等同：

<dl> P ' = (*x* + (*y* – *.py*) tanΘ、 *y* + (*x* – *px*) tanΦ) 
</dl>

若要查看這項轉換的運作方式，請個別考慮每個元件。 Θ參數會將 x 方向的每個點依等於 tanΘ的數量移動。 下圖顯示Θ和 X 軸扭曲之間的關聯性。

![顯示沿著 X 軸扭曲的圖表。](images/graphics26.png)

以下是套用至矩形的相同扭曲：

![套用至矩形時，沿著 X 軸顯示扭曲的圖表。](images/graphics27.png)

Φ參數的效果相同，但沿著 y 軸：

![顯示沿著 y 軸扭曲的圖表。](images/graphics28.png)

下圖顯示套用至矩形的 y 軸扭曲。

![圖表會顯示套用至矩形時沿著 y 軸的扭曲。](images/graphics29.png)

最後，參數 *px* 和 *.py* 會將沿著 X 軸和 y 軸扭曲的中心點移位。

## <a name="representing-transforms-in-direct2d"></a>代表 Direct2D 中的轉換

所有 Direct2D 轉換都是仿射轉換。 Direct2D 不支援非仿射轉換。 轉換會以 [**D2D1 \_ 矩陣 \_ 3X2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) 結構表示。 此結構定義了3×2矩陣。 因為仿射轉換的第三個數據行一律是相同的 (\[ 0、0、1 \]) ，而且因為 Direct2D 不支援非仿射轉換，所以不需要指定整個3×3矩陣。 就內部而言，Direct2D 會使用3×3矩陣來計算轉換。

[**D2D1 \_ 矩陣 \_ 3X2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f)的成員是根據其索引位置進行命名： **\_ 11** 成員是元素 (1、1) 、 **\_ 12** 個成員是元素 (1、2) 等等。 雖然您可以直接將結構成員初始化，但建議您使用 [**D2D1：： Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) 類別。 這個類別會繼承 **D2D1 \_ 矩陣 \_ 3X2 \_ F** ，並提供 helper 方法來建立任何基本的仿射轉換。 此類別也會定義用來撰寫兩個或多個轉換的 [**運算子 \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) ，如在 Direct2D 中套用 [轉換](applying-transforms-in-direct2d.md)所述。

## <a name="next"></a>下一個

[模組4：使用者輸入](module-4--user-input.md)

 

 