---
description: 圖形狀態 &\# 8212; 裁剪區域、轉換和品質設定 &\# 8212; 儲存在繪圖物件中。
ms.assetid: 98b9fa12-02e7-42bf-9cbd-03ee696188f6
title: 圖形容器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26af00a17f793a1f3ce587963343556b8c4ad685f930b707bd81de1008d610ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118248667"
---
# <a name="graphics-containers"></a>圖形容器

圖形狀態（剪下區域、轉換和品質設定）會儲存在 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件中。 Windows GDI+ 可讓您使用容器，在 **圖形** 物件中暫時取代或增強部分狀態。 您可以藉由呼叫 **graphics 物件的** [**Graphics：： BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit))方法來啟動容器，然後藉由呼叫 [**graphics：： EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)方法來結束容器。 在 **graphics：： BeginContainer** 與 **Graphics：： EndContainer** 之間，您對 **圖形** 物件所做的任何狀態變更都屬於容器，而不會覆寫 **圖形** 物件的現有狀態。

下列範例會在 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件中建立容器。 **圖形** 物件的世界轉換是將200單位轉譯為右邊的轉換，而容器的世界轉換則是轉譯100單位。


```
myGraphics.TranslateTransform(200.0f, 0.0f);

myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.TranslateTransform(0.0f, 100.0f);
   myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
myGraphics.EndContainer(myGraphicsContainer);

myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
```



請注意，在上述範例中， `myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50)` 在對 [**graphics：： BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) 和 [**graphics：： EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) 的呼叫之間進行的語句，會產生不同的矩形，而不是呼叫 **圖形：： EndContainer** 之後所做的相同語句。 只有水準轉譯會套用至在容器外部進行的 **graphicswindow.drawrectangle** 呼叫。 這兩種轉換（200單位的水準轉譯和100單位的垂直轉譯）適用于 [**圖形：:D**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) 在容器內進行的 rawrectangle 呼叫。 下圖顯示兩個矩形。

![視窗的螢幕擷取畫面，其中有兩個以藍色畫筆繪製的矩形，一個位於另一個上方](images/aboutgdip05-art17.png)

容器可以嵌套在容器內。 下列範例會在 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件內建立容器，並在第一個容器內建立另一個容器。 **圖形** 物件的世界轉換是 x 方向的平移100單位和 y 方向的80單位。 第一個容器的世界轉換是30度的旋轉。 第二個容器的世界轉換是以 x 方向的2因數來進行調整。 對圖形進行的呼叫 [**：:D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) 方法是在第二個容器內進行。


```
myGraphics.TranslateTransform(100.0f, 80.0f, MatrixOrderAppend);

container1 = myGraphics.BeginContainer();
   myGraphics.RotateTransform(30.0f, MatrixOrderAppend);

   container2 = myGraphics.BeginContainer();
      myGraphics.ScaleTransform(2.0f, 1.0f);
      myGraphics.DrawEllipse(&myPen, -30, -20, 60, 40);
   myGraphics.EndContainer(container2);

myGraphics.EndContainer(container1);
```



下圖顯示橢圓形。

![視窗的螢幕擷取畫面，其中包含旋轉的藍色橢圓形，其中心標示為 (100，80) ](images/aboutgdip05-art18.png)

請注意，這三個轉換都適用于 [**圖形：:D**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) 在第二個 (最內層) 容器中進行的 rawellipse 呼叫。 另外也請注意轉換的順序：第一次調整，然後旋轉，然後轉譯。 最內層的轉換會先套用，而最外層的轉換最後會套用。

[**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件的任何屬性都可以設定在容器中， (在圖形的呼叫之間 [**：： BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit))和 [**graphics：： EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)) 。 例如，您可以在容器內設定裁剪區域。 任何在容器內完成的繪圖都會限制為該容器的裁剪區域，而且也會限制為任何外部容器的裁剪區域和 **圖形** 物件本身的裁剪區域。

到目前為止所討論的屬性（世界轉換和裁剪區域）都會由嵌套容器合併。 其他屬性會暫時由嵌套容器取代。 例如，如果您將平滑模式設定為在容器內 SmoothingModeAntiAlias，則在該容器內呼叫的任何繪圖方法都會使用消除鋸齒平滑模式，但是在 [**圖形：： EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) 之後呼叫的繪圖方法會使用在 [**圖形：： BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit))呼叫之前所處的平滑模式。

如需合併 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件和容器之世界轉換的另一個範例，假設您想要繪製眼睛，並將它放在一系列臉部的不同位置。 下列範例會在座標系統的原點繪製中央的眼睛。


```
void DrawEye(Graphics* pGraphics)
{
   GraphicsContainer eyeContainer;
   
   eyeContainer = pGraphics->BeginContainer();

      Pen myBlackPen(Color(255, 0, 0, 0));
      SolidBrush myGreenBrush(Color(255, 0, 128, 0));
      SolidBrush myBlackBrush(Color(255, 0, 0, 0));

      GraphicsPath myTopPath;
      myTopPath.AddEllipse(-30, -50, 60, 60);

      GraphicsPath myBottomPath;
      myBottomPath.AddEllipse(-30, -10, 60, 60);

      Region myTopRegion(&myTopPath);
      Region myBottomRegion(&myBottomPath);

      // Draw the outline of the eye.
      // The outline of the eye consists of two ellipses.
      // The top ellipse is clipped by the bottom ellipse, and
      // the bottom ellipse is clipped by the top ellipse.
      pGraphics->SetClip(&myTopRegion);
      pGraphics->DrawPath(&myBlackPen, &myBottomPath);
      pGraphics->SetClip(&myBottomRegion);
      pGraphics->DrawPath(&myBlackPen, &myTopPath);

      // Fill the iris.
      // The iris is clipped by the bottom ellipse.
      pGraphics->FillEllipse(&myGreenBrush, -10, -15, 20, 22);

      // Fill the pupil.
      pGraphics->FillEllipse(&myBlackBrush, -3, -7, 6, 9);

   pGraphics->EndContainer(eyeContainer);
}
```



下圖顯示眼睛和座標軸。

![圖例顯示由三個省略號組成的眼睛：大綱、鳶尾花和小學生各有一個橢圓形](images/aboutgdip05-art19.png)

上述範例中定義的 DrawEye 函式會接收 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件的位址，並立即在該 **圖形** 物件中建立容器。 此容器會將呼叫 DrawEye 函式的任何程式碼，從 DrawEye 函數執行期間所做的屬性設定中隔離。 例如，DrawEye 函式中的程式碼會設定 **Graphics** 物件的裁剪區域，但是當 DrawEye 將控制權傳回給呼叫常式時，裁剪區域就會與呼叫 DrawEye 之前的相同。

下列範例會繪製三個橢圓形 (臉部) ，每一個都有眼睛。


```
// Draw an ellipse with center at (100, 100).
myGraphics.TranslateTransform(100.0f, 100.0f);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Draw the eye at the center of the ellipse.
DrawEye(&myGraphics);

// Draw an ellipse with center at 200, 100.
myGraphics.TranslateTransform(100.0f, 0.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Rotate the eye 40 degrees, and draw it 30 units above
// the center of the ellipse.
myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.RotateTransform(-40.0f);
   myGraphics.TranslateTransform(0.0f, -30.0f, MatrixOrderAppend);
   DrawEye(&myGraphics);
myGraphics.EndContainer(myGraphicsContainer);

// Draw a ellipse with center at (300.0f, 100.0f).
myGraphics.TranslateTransform(100.0f, 0.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Stretch and rotate the eye, and draw it at the 
// center of the ellipse.
myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.ScaleTransform(2.0f, 1.5f);
   myGraphics.RotateTransform(45.0f, MatrixOrderAppend);
   DrawEye(&myGraphics);
myGraphics.EndContainer(myGraphicsContainer);
```



下圖顯示三個省略號。

![視窗的螢幕擷取畫面，其中包含三個省略號，每個都包含不同大小和旋轉的眼睛](images/aboutgdip05-art20.png)

在先前的範例中，所有的省略號都是使用呼叫來繪製 `DrawEllipse(&myBlackPen, -40, -60, 80, 120)` ，這會繪製以座標系統原點為中心的橢圓形。 您可以藉由設定 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件的世界轉換，將橢圓形移離工作區的左上角。 此語句會導致第一個橢圓形的中心為 (100，100) 。 此語句會導致第二個橢圓形的中心成為第一個橢圓形中間的100個單位。 同樣地，第三個橢圓形的中心是第二個橢圓形中央的100單位。

上一個範例中的容器用來轉換相對於指定橢圓形中心的眼睛。 第一眼是在沒有轉換的橢圓中央繪製，因此 DrawEye 呼叫不在容器內。 第二眼是旋轉40度，並繪製在橢圓形中央上方的30個單位，因此 DrawEye 函式和設定轉換的方法會在容器內呼叫。 第三個眼睛會在橢圓形的中央伸展和旋轉並繪製。 就像第二眼一樣，DrawEye 函式和設定轉換的方法會在容器內呼叫。

 

 
