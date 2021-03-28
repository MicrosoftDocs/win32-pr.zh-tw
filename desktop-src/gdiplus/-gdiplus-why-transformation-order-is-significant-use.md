---
description: 單一矩陣物件可以儲存單一轉換或一連串的轉換。
ms.assetid: 1dc68ff8-6b17-4934-82da-ab2fc612aafa
title: 為何轉換順序很重要
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7350d63456902ff47183faa08170b3b2fef481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972136"
---
# <a name="why-transformation-order-is-significant"></a>為何轉換順序很重要

單一 [**矩陣**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) 物件可以儲存單一轉換或一連串的轉換。 後者稱為「 *複合*  *轉換*」。 複合轉換的矩陣是藉由將個別轉換的矩陣相乘來取得的。

在複合轉換中，個別轉換的順序很重要。 例如，如果您第一次旋轉，然後進行調整，然後轉譯，則會得到不同的結果，而不是您第一次轉譯、接著旋轉然後調整規模。 在 Windows GDI + 中，複合轉換是由左至右建立。 如果 S、R 和 T 分別是縮放、旋轉和轉譯矩陣，則產品 SRT 會以該順序 () 是第一次調整的複合轉換矩陣，然後旋轉然後轉譯。 產品 SRT 所產生的矩陣與產品 TRS 所產生的矩陣不同。

其中一個原因是很重要的是，旋轉和縮放等轉換是針對座標系統的原點進行的。 調整位於原點中央的物件會產生不同的結果，而不是縮放已從原點移出的物件。 同樣地，旋轉位於原點中央的物件會產生不同的結果，而不是旋轉離開來源的物件。

下列範例結合了調整、旋轉和轉譯 (順序) 形成複合轉換。 傳遞至 [**Graphics：： RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform)方法的引數 [* * * * MatrixOrderAppend *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) * 會指定旋轉將遵循調整。 同樣地，傳遞給 [**Graphics：： TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform)方法的引數 [* * * * MatrixOrderAppend *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) * * 會指定轉譯會在旋轉之後。


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.TranslateTransform(150.0f, 150.0f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



下列範例會執行與上述範例相同的方法呼叫，但是呼叫的順序會反轉。 產生的作業順序會先轉譯，然後再旋轉，然後調整，以產生與第一個尺規不同的結果，然後再旋轉，然後轉譯：


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



在複合轉換中反轉個別轉換順序的其中一種方式，是反轉方法呼叫序列的順序。 控制作業順序的第二種方式是變更矩陣順序引數。 下列範例與上一個範例相同，不同之處在于 [* * * * MatrixOrderAppend * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) * * 已變更為 [* * * * MatrixOrderPrepend * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder)* *。 矩陣乘法是在 order SRT 中完成，其中 S、R 和 T 分別是調整、旋轉和轉譯的矩陣。 複合轉換的順序是先進行調整，然後再旋轉，然後轉譯。


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f,MatrixOrderPrepend);
graphics.RotateTransform(28.0f, MatrixOrderPrepend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderPrepend);
graphics.DrawRectangle(&pen, rect);
```



上述範例的結果與我們在本節的第一個範例中達成的結果相同。 這是因為我們反轉方法呼叫的順序和矩陣相乘的順序。

 

 



