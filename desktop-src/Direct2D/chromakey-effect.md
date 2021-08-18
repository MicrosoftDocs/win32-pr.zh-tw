---
title: 色度鍵效果
description: 將指定的色彩加或減到 Alpha 的誤差。 例如，色度按鍵可以移除影像的背景，以進行綠色螢幕重迭效果。
ms.assetid: f7bb5c65-f406-f947-c05d-2756cff99d21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 485cec7842c8460169b9c335eb74e9cc6d5a13e0541a49fc99835dfaa591efc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075584"
---
# <a name="chroma-key-effect"></a>色度鍵效果

將指定的色彩加或減到 Alpha 的誤差。 例如，色度按鍵可以移除影像的背景，以進行綠色螢幕重迭效果。

這項效果的 CLSID 是 CLSID \_ D2D1ChromaKey。

-   [範例影像](#example-image)
-   [範例程式碼](#sample-code)
-   [效果屬性](#effect-properties)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="example-image"></a>範例影像

![效果輸出的範例](images/chromakey-effect.png)

> [!Note]  
> 在此範例中，色度按鍵效果的輸出是具有棋盤透明背景的第二個影像。 第三個影像會將它與背景影像合併，以進行最後的綠色螢幕重迭。

## <a name="sample-code"></a>範例程式碼

```cppcx
ComPtr<ID2D1Effect> chromakeyEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ChromaKey, &chromakeyEffect);
 
chromakeyEffect->SetInput(0, bitmap);
chromaKeyEffect->SetValue(D2D1_CHROMAKEY_PROP_COLOR, {0.0f, 1.0f, 0.0f, 0.0f});
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_TOLERANCE, 0.2f);
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_INVERT_ALPHA, false);
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_FEATHER, false);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(chromakeyEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>效果屬性

色度按鍵效果的屬性是由 [**D2D1 \_ CHROMAKEY \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_chromakey_prop) 屬性列舉所定義。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|--------------------------|---------------------------------------------------|
| 最低支援的用戶端 | Windows 10 \[桌面應用程式 \| Windows 儲存應用程式\] |
| 最低支援的伺服器 | Windows 10 \[桌面應用程式 \| Windows 儲存應用程式\] |
| 標頭                   | d2d1effects \_ 2。h                                  |
| 程式庫                  | d2d1 .lib，dxguid .lib                              |

## <a name="related-topics"></a>相關主題

* [ID2D1Effect 介面](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
