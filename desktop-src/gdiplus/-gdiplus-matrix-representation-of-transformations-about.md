---
description: M&\# 215; n 矩陣是以 m 資料列和 n 資料行排列的一組數位。 下圖顯示數個矩陣。
ms.assetid: 62215ae0-b095-42b2-911c-aa7607a8b61a
title: 以矩陣來表示轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0577cae38c401e842cff2ff14179594f9118dfd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690344"
---
# <a name="matrix-representation-of-transformations"></a>以矩陣來表示轉換

*M × n* 矩陣是以 *m* 列和 *n* 資料行排列的一組數位。 下圖顯示數個矩陣。

![顯示不同維度的六個矩陣的圖例](images/aboutgdip05-art04.png)

您可以藉由新增個別元素，加入兩個相同大小的矩陣。 下圖顯示兩個矩陣加法範例。

![說明如何執行矩陣加法的圖例](images/aboutgdip05-art05.png)

*M × n* 矩陣可乘以 *n × p* 矩陣，而結果為 *m × p* 矩陣。 第一個矩陣中的資料行數目必須與第二個矩陣中的資料列數目相同。 例如，4×2矩陣可乘以2×3矩陣，以產生4×3矩陣。

您可以將矩陣的平面和資料列和資料行中的點視為向量。 例如， (2，5) 是具有兩個元件的向量，而 (3，7，1) 是具有三個元件的向量。 兩個向量的點乘積定義如下：

 (a，b) • (c，d) = ac + bd

 (a，b，c) • (d，e，f) = ad + 為 + cf

例如， (2，3) 和 (5 的點乘積，4) 是 (2)  (5) + (3)  (4) = 22。  (2，5，1) 和 (4，3，1) 的點乘積為 (2)  (4) + (5)  (3) + (1)  (1) = 24。 請注意，兩個向量的點乘積是數位，而不是另一個向量。 另請注意，只有在兩個向量具有相同數目的元件時，您才可以計算點乘積。

讓 (i，j) 成為 **第** i 個數據列和 j #**第** 一個資料行中的矩陣 A 專案。 例如， (3，2) 是 3 **rd** 資料列和 2 **nd** 資料行中矩陣 A 的專案。 假設 A、B 和 C 是矩陣，而 AB = C。C 的專案計算方式如下：

C (i，j) = (的資料列 i) • (a B B 的資料行 j) 

下圖顯示數個矩陣乘法範例。

![顯示如何執行矩陣乘法的圖例](images/aboutgdip05-art06.png)

如果您將平面中的某個點視為1×2矩陣，您可以藉由將該點乘以2×2矩陣來進行轉換。 下圖顯示套用到點 (2，1) 的數個轉換。

![顯示如何使用矩陣乘法來調整、旋轉或反映平面中某個點的圖例](images/aboutgdip05-art07.png)

上圖中顯示的所有轉換都是線性轉換。 某些其他轉換（例如平移）並不是線性的，且無法表示為與2×2矩陣相乘。 假設您想要開始使用 (2，1) 的點，請將它旋轉90度，將其轉譯為 x 方向的3個單位，並以 y 方向轉譯為4個單位。 您可以執行矩陣乘法，然後再加上矩陣加法來完成這項操作。

![顯示矩陣乘法和加法如何旋轉點並將其轉譯兩次的圖例](images/aboutgdip05-art08.png)

線性轉換 (乘以2×2矩陣) 接著平移 (加上1×2矩陣) 稱為「仿射」轉換。 另一種方式是將仿射轉換儲存在一組矩陣中 (一個用於線性部分，而另一個用於轉譯) 是在3×3矩陣中儲存整個轉換。 若要進行這項工作，平面中的點必須以虛擬的第三座標儲存在1×3矩陣中。 一般的技巧是讓所有的第三個座標等於1。 例如，點 (2，1) 是以矩陣 \[ 2 1 1 表示 \] 。 下圖顯示仿射轉換 (旋轉90度;以 x 方向轉譯3個單位，y 方向的4個單位) 以單一3×3矩陣的乘法表示。

![顯示矩陣乘法如何執行仿射轉換的圖例](images/aboutgdip05-art09.png)

在上述範例中， (2，1) 的點對應到 (2，6) 的點。 請注意，3×3矩陣的第三個數據行包含數位0、0、1。 這一律會是仿射轉換的3×3矩陣的情況。 重要的數位是資料行1和2中的六個數字。 矩陣左上2×2部分代表轉換的線性部分，而第三列中的前兩個專案表示轉譯。

![圖例顯示對仿射轉換的3x3 矩陣而言，前兩個數據行是最重要的](images/aboutgdip05-art10.png)

在 Windows GDI + 中，您可以在 [**矩陣**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) 物件中儲存仿射轉換。 由於矩陣的第三個數據行（代表仿射轉換）一律 (0、0、1) ，因此當您建立 **矩陣** 物件時，您只需要在前兩個數據行中指定六個數字。 語句會建立 `Matrix myMatrix(0.0f, 1.0f, -1.0f, 0.0f, 3.0f, 4.0f);` 上圖所示的矩陣。

## <a name="composite-transformations"></a>複合轉換

複合轉換是一種轉換序列，後面接著另一個。 請考慮下列清單中的矩陣和轉換：

-   矩陣 A 旋轉90度度
-   矩陣 B 以 x 方向的2因數來調整
-   矩陣 C 以 y 方向轉譯3個單位

如果您是以矩陣 2 1 1 表示的點 (2，1) （由矩陣表示），然後 \[ \] 再乘 A、B、C，則點 (2，1) 將會依照列出的順序來進行三個轉換。

\[2 1 1 \] ABC = \[ – 2 5 1\]

與其將複合轉換的三個部分儲存在三個不同的矩陣中，您可以將 A、B 和 C 兩者相乘，以取得儲存整個複合轉換的單一3×3矩陣。 假設 ABC = D。然後，點乘以 D 會將相同的結果與點乘 A，然後 B，再加上 C。

\[2 1 1 \] D = \[ – 2 5 1\]

下圖顯示矩陣 A、B、C 和 D。

![圖例顯示如何藉由將組成矩陣相乘來執行多個轉換](images/aboutgdip05-art12.png)

您可以藉由將個別的轉換矩陣相乘來形成複合轉換的矩陣，表示任何一系列的仿射轉換都可以儲存在單一 [**矩陣**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) 物件中。

> [!Note]  
> 複合轉換的順序很重要。 一般而言，旋轉、接著調整規模，然後轉譯與縮放比例不同，然後旋轉然後轉譯。 同樣地，矩陣乘法的順序也很重要。 一般來說，ABC 與 k 不同。

 

[**矩陣**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix)類別提供數種方法來建立複合轉換：[**矩陣：：乘法**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-multiply)、 [**matrix：：旋轉**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotate)、 [**Matrix：： RotateAt**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotateat)、 [**matrix：： Scale**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-scale)、 [**matrix：：切變**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear)和 [**matrix：：轉譯**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-translate)。 下列範例會建立複合轉換的矩陣，其會先旋轉30度，然後在 y 方向以2的因數進行縮放，然後以 x 方向轉譯5個單位。


```
Matrix myMatrix;
myMatrix.Rotate(30.0f);
myMatrix.Scale(1.0f, 2.0f, MatrixOrderAppend);
myMatrix.Translate(5.0f, 0.0f, MatrixOrderAppend);
```



下圖顯示矩陣。

![顯示矩陣，其中包含以三角函數表示的值，以及包含這些函式之近似值的矩陣](images/aboutgdip05-art13.png)

 

 



