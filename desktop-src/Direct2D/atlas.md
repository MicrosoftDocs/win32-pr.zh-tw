---
title: 塔效果
description: 您可以使用此效果來輸出影像的一部分，但是將區域保留在部分外部，以用於後續作業。
ms.assetid: D35E32CB-4DF7-408F-A717-1E421DDC8763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f9e1d4c6df0698d47a35eb2cbdaf670b98ed125
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466320"
---
# <a name="atlas-effect"></a>塔效果

您可以使用此效果來輸出影像的一部分，但是將區域保留在部分外部，以用於後續作業。

這項效果的 CLSID 是 CLSID \_ D2D1Atlas。

如果您想要載入由許多較小的影像組成的大型影像，例如 sprite 的各種框架，則塔效果相當有用。

若要建立輸出效果：

1.  將輸入裁剪至指定的 *InputRect* 屬性。
2.  將結果的原點轉譯為 (0，0) 。

> [!Note]  
> 只有當兩個矩形之間的圖元在輸入上為透明黑色時， *InputPaddingRect* 屬性才應該較大。 這可能會導致 Direct2D 更能以最佳方式執行圖形。

 

以下是效果的範例。 此映射很小，而且很簡單，可供說明之用。

![輸入影像。](images/atlas.png)

上述影像是效果的輸入。 此處的程式碼會建立一個塔效果、設定輸入、設定輸入矩形，然後繪製輸出。


```C++
ComPtr<ID2D1Effect> atlasEffect;

// Create the Atlas Effect.
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Atlas, &atlasEffect));

// Set the input.
atlasEffect->SetInputEffect(0, inputImage.Get());

// The images here are 150 x 150 pixels.
float size = 150.0f;

// Compensate for the padding between images.
float padding = 10.0f;

// The input rectangle.  150 x 150 pixels with 10 pixel padding
D2D1_Vector_4F inputRect = D2D1::Vector4F(size + (padding * 2), padding, size, size);

DX::ThrowIfFailed(atlasEffect->SetValue(D2D1_ATLAS_PROP_INPUT_RECT, inputRect));

// Draw the image
m_d2dContext->DrawImage(atlasEffect.Get());
```



上述程式碼會選取位於第二個三角形周圍的矩形。 它周圍的填補會被忽略。 以下是產生的影像。

![輸出影像。](images/atlas2.png)

> [!Note]  
> 這種情況下，您可以選擇指定 *InputPaddingRect* ，因為填補是透明的黑色。 矩形會是 `D2D1::Vector4F(size + (padding * 2), 0, size + padding, size + padding);` 。

 

## <a name="effect-properties"></a>效果屬性



| 顯示名稱和索引列舉                                             | Description                                                                                                                                                                  |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InputRect<br/> D2D1 \_ 塔 \_ 的 \_ 輸入 \_ 矩形<br/>                 | 傳遞給下一個效果的影像部分。<br/> 類型為 D2D1 \_ VECTOR \_ 4F。<br/> 預設值為 (-FLT \_ max、-FLT \_ MAX、FLT \_ max、FLT \_ max) 。 <br/> |
| InputPaddingRect<br/> D2D1 \_ 塔 \_ 的 \_ 輸入 \_ 填補 \_ 矩形<br/> | 針對輸出矩形取樣的大小上限。<br/> 類型為 D2D1 \_ VECTOR \_ 4F。<br/> 預設值為 (-FLT \_ max、-FLT \_ MAX、FLT \_ max、FLT \_ max) 。<br/>   |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端 | 適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\] |
| 最低支援的伺服器 | 適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\] |
| 標頭                   | d2d1effects。h                                                                      |
| 程式庫                  | d2d1 .lib，dxguid .lib                                                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

