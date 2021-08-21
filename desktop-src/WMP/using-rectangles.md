---
title: '使用矩形 (Windows Media Player SDK) '
description: 使用矩形
ms.assetid: b3fc16b4-dc93-43c0-a97d-5234e36437c8
keywords:
- 視覺效果、矩形
- 自訂視覺效果，矩形
- 視覺效果，轉譯函數
- 自訂視覺效果，轉譯函數
- 轉譯函數、矩形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79dd46928ccf8f8a0a465fa71fbb6b1bc1b4f48cbdb5c37b4b93ffd21c78c6b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117293"
---
# <a name="using-rectangles-windows-media-player-sdk"></a>使用矩形 (Windows Media Player SDK) 

矩形可用來指定 Microsoft Windows 中的矩形區域。 您可以在視窗中建立許多矩形，但 Windows Media Player 透過[IWMPEffects：： Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render)函數提供一個矩形的值。 如果您的外掛程式使用視窗轉譯，矩形就是視窗的工作區。 這稱為中國矩形，它會定義 Windows Media Player 將顯示視覺效果的矩形。 請經常使用此方法，以確保您不會在 Windows Media Player 所提供的矩形範圍之外進行繪製。

矩形有四個定義它的值。 它們是 left、top、right 和底端。 矩形的左上角是由左和上定義，而矩形的右下角則由右下角定義。

使用下列程式碼來取得繪圖矩形的範圍。 您需要這麼做，是因為使用者可能會調整視窗的大小，而您想要確定一律是在使用者可以看到的區域中繪製。


```C++
int leftside = prc->left;
int rightside = prc->right;
int topside = prc->top;
int bottomside = prc->bottom;

```



例如，若要從左至右繪製，請在視窗的頂端，使用如下的程式碼：


```C++
::MoveToEx( hdc, prc->left, prc->top, NULL );  
::LineTo(hdc, prc->right, prc->top);

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**執行轉譯**](implementing-render.md)
</dt> </dl>

 

 




