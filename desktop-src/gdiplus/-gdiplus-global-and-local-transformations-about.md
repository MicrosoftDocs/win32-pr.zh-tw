---
description: 全域轉換是一種轉換，適用于給定繪圖物件所繪製的每個專案。
ms.assetid: 9f744c2a-f1f3-4a7e-ab0c-37aa1df01623
title: 全域和區域轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2682fef6a6236b9da7ec0ec1e5ab5484ad9f90d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564200"
---
# <a name="global-and-local-transformations"></a>全域和區域轉換

全域轉換是一種轉換，適用于給定 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件所繪製的每個專案。 若要建立全域轉換，請建立 **圖形** 物件，然後呼叫其 [**Graphics：： SetTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settransform) 方法。 **Graphics：： SetTransform** 方法會操作與 **圖形** 物件相關聯的 [**矩陣**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix)物件。 儲存在該 **矩陣** 物件中的轉換稱為「 *世界」轉換*。 全球轉換可以是簡單仿射轉換或複雜的仿射轉換序列，但不論其複雜度為何，全球轉換都會儲存在單一 **矩陣** 物件中。

[**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別提供數種方法來建立複合世界轉換： [**Graphics：： MultiplyTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-multiplytransform)、 [**graphics：： RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform)、 [**graphics：： ScaleTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-scaletransform)和 [**Graphics：： TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform)。 下列範例會繪製一個橢圓形兩次：一次在建立世界轉換之前和之後。 轉換會先在 y 方向以0.5 因數進行調整，然後轉譯 x 方向的50單位，然後旋轉30度。


```
myGraphics.DrawEllipse(&myPen, 0, 0, 100, 50);
myGraphics.ScaleTransform(1.0f, 0.5f);
myGraphics.TranslateTransform(50.0f, 0.0f, MatrixOrderAppend);
myGraphics.RotateTransform(30.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myPen, 0, 0, 100, 50);
```



下圖顯示原始的橢圓形和轉換的橢圓形。

![視窗的螢幕擷取畫面，其中包含兩個重迭的省略號;其中一個是較窄和旋轉的](images/aboutgdip05-art14.png)

> [!Note]  
> 在上述範例中，橢圓形會旋轉大約座標系統的原點，位於工作區的左上角。 這會產生不同的結果，而不是對它自己的中心旋轉省略號。

 

本機轉換是套用至要繪製之特定專案的轉換。 例如， [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) 物件具有 [**GraphicsPath：： transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) 方法，可讓您轉換該路徑的資料點。 下列範例會繪製沒有轉換的矩形，以及具有旋轉轉換的路徑。  (假設沒有任何世界轉換。 ) 


```
 
Matrix myMatrix;
myMatrix.Rotate(45.0f);
myGraphicsPath.Transform(&myMatrix);
myGraphics.DrawRectangle(&myPen, 10, 10, 100, 50);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



您可以結合世界轉換與本機轉換，以達成各種不同的結果。 例如，您可以使用「世界」轉換來修訂座標系統，並使用「本機」轉換來旋轉和縮放在新座標系統上繪製的物件。

假設您希望座標系統的原點為200圖元，從工作區的左邊緣到工作區的最上層150圖元。 此外，假設您希望量值的單位是圖元，而 X 軸指向右邊，y 軸則指向右邊。 預設座標系統的 y 軸是向下指向，因此您需要在水準軸上執行反映。 下圖顯示這類反映的矩陣。

![顯示三個矩陣的圖解](images/aboutgdip05-art15.png)

接下來，假設您需要對右邊和150單位執行平移200單位。

下列範例會藉由設定 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件的世界轉換來建立剛剛描述的座標系統。


```
Matrix myMatrix(1.0f, 0.0f, 0.0f, -1.0f, 0.0f, 0.0f);
myGraphics.SetTransform(&myMatrix);
myGraphics.TranslateTransform(200.0f, 150.0f, MatrixOrderAppend);
```



下列程式碼 (放在上述範例中的程式碼之後) 會建立一個路徑，其中包含在新座標系統原點的左上角單一矩形。 矩形會填滿一次，而不會有本機轉換，一次是使用本機轉換。 「本機」轉換包含水準縮放比例，後面接著一個30度的旋轉。


```
// Create the path.
GraphicsPath myGraphicsPath;
Rect myRect(0, 0, 60, 60);
myGraphicsPath.AddRectangle(myRect);

// Fill the path on the new coordinate system.
// No local transformation
myGraphics.FillPath(&mySolidBrush1, &myGraphicsPath);

// Transform the path.
Matrix myPathMatrix;
myPathMatrix.Scale(2, 1);
myPathMatrix.Rotate(30, MatrixOrderAppend);
myGraphicsPath.Transform(&myPathMatrix);

// Fill the transformed path on the new coordinate system.
myGraphics.FillPath(&mySolidBrush2, &myGraphicsPath);
```



下圖顯示新的座標系統和兩個矩形。

![x 和 y 軸的螢幕擷取畫面，以及以半透明 rectagle 重迭的藍色正方形（圍繞其左下角旋轉）](images/aboutgdip05-art16.png)

 

 



