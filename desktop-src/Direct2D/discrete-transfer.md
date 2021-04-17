---
title: 離散傳送效果
description: 使用離散傳輸效果，利用從您提供的值清單建立的步驟轉移函式，來對應影像的色彩濃度。
ms.assetid: 5A612002-2B1D-4FC3-B364-AACD9FD44BEC
keywords:
- 離散傳送效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c05ef08f9ddf053eaa686cb0f88d4183194d9e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104559176"
---
# <a name="discrete-transfer-effect"></a>離散傳送效果

使用離散傳輸效果，利用從您提供的值清單建立的步驟轉移函式，來對應影像的色彩濃度。

這項效果的 CLSID 是 CLSID \_ D2D1DiscreteTransfer。

-   [範例影像](#example-image)
-   [效果屬性](#effect-properties)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="example-image"></a>範例影像

此處的影像顯示離散傳送效果的輸入和輸出。



| 之前                                                            |
|-------------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg)        |
| After                                                             |
| ![轉換後的影像。](images/12-discretetransfer.png) |



 


```C++
ComPtr<ID2D1Effect> discreteTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DiscreteTransfer, &discreteTransferEffect);

discreteTransferEffect->SetInput(0, bitmap);

float table[3] = {0.0f, 0.5f, 1.0f};
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_RED_TABLE, table);
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_GREEN_TABLE, table);
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_BLUE_TABLE, table);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(discreteTransferEffect.Get());
m_d2dContext->EndDraw();
```



傳送函式是以輸入清單為基礎： V = (V0、V1、V2、V3、V？ ，V<sub>n</sub>) 其中 N 是元素數目-1。

輸入圖元濃度以 C 表示。輸出圖元強度（C）會以方程式計算：

若為值 C，請挑選值 k，如下所示：

![處理常式的公式。](images/discrete-transfer1.png)

輸出 C 可以使用方程式： C ' = V 來計算：

此效果適用于直接和預乘的 Alpha 影像。 效果會輸出預乘的 Alpha 點陣圖。

以下是當輸入為時，離散傳送函式的圖表看起來的樣子 `[0.25, 0.5, 0.75, 1.0]` 。

![離散傳送函數的圖元濃度圖形。](images/discrete-transfer-graph.png)

## <a name="effect-properties"></a>效果屬性

> [!Note]  
> 離散傳輸屬性的所有通道值都不會用到，而且最小值為0.0 和1.0。

 



| 顯示名稱和索引列舉                                              | 類型和預設值                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedTable<br/> D2D1 \_ DISCRETETRANSFER \_ 的 \_ 成分紅色 \_ 資料表<br/>         | 浮動\[\]<br/> {0.0 f、1.0 f}<br/> | 值的清單，用來定義 Red 通道的傳送函式。                                                                                                                                                                                                                                                                                                                                                                                 |
| RedDisable<br/> D2D1 \_ DISCRETETRANSFER \_ 的 \_ RED \_ DISABLE<br/>     | BOOL<br/> FALSE<br/>             | 如果您將此設定為 TRUE，則效果不會將傳送函式套用至紅色通道。 如果您將此設定為 FALSE，效果會將 RedDiscreteTransfer 函式套用至紅色通道。                                                                                                                                                                                                                                                                 |
| GreenTable<br/> D2D1 \_ DISCRETETRANSFER \_ 的 \_ \_ 表表表<br/>     | 浮動\[\]<br/> {0.0 f、1.0 f}<br/> | 值的清單，這些值會定義綠色通道的傳送函數。                                                                                                                                                                                                                                                                                                                                                                                  |
| GreenDisable<br/> D2D1 \_ DISCRETETRANSFER，a \_ \_ 綠 \_ DISABLE<br/> | BOOL<br/> FALSE<br/>             | 如果您將此設定為 TRUE，則效果不會將傳送函式套用至綠色通道。 如果您將此設定為 FALSE，效果會將 GreenDiscreteTransfer 函式套用至綠色通道。                                                                                                                                                                                                                                                           |
| BlueTable<br/> D2D1 \_ DISCRETETRANSFER \_ 的 \_ BLUE \_ 資料表<br/>       | 浮動\[\]<br/> {0.0 f、1.0 f}<br/> | 值的清單，這些值會定義藍色通道的傳送函數。                                                                                                                                                                                                                                                                                                                                                                                   |
| BlueDisable<br/> D2D1 \_ DISCRETETRANSFER \_ 的 \_ BLUE \_ DISABLE<br/>   | BOOL<br/> FALSE<br/>             | 如果您將此設定為 TRUE，則效果不會將傳送函式套用至藍色通道。 如果您將此設定為 FALSE，效果會將 BlueDiscreteTransfer 函式套用至藍色通道。                                                                                                                                                                                                                                                              |
| AlphaTable<br/> D2D1 \_ DISCRETETRANSFER \_ 的 \_ ALPHA \_ 表<br/>     | 浮動\[\]<br/> {0.0 f、1.0 f}<br/> | 值的清單，這些值會定義 Alpha 通道的傳送函式。                                                                                                                                                                                                                                                                                                                                                                                  |
| AlphaDisable<br/> D2D1 \_ DISCRETETRANSFER \_ 的 \_ ALPHA \_ 停用<br/> | BOOL<br/> FALSE<br/>             | 如果您將此設定為 TRUE，則效果不會將傳送函式套用至 Alpha 通道。 如果您將此設定為 FALSE，效果會將 AlphaDiscreteTransfer 函式套用至 Alpha 色板。                                                                                                                                                                                                                                                           |
| ClampOutput<br/> D2D1 DISCRETETRANSFER 的一種 \_ \_ \_ 夾具 \_ 輸出<br/>   | BOOL<br/> FALSE<br/>             | 效果在效果之前個色彩值是否會將值傳遞給圖形中的下一個效果。 效果會在 premultiplies Alpha 之前個值。<br/> 如果您將此設定為 TRUE，效果會將值設為夾具。 如果您將此值設定為 FALSE，效果將不會顯示色彩值，但其他效果和輸出介面可能會在這些值的精確度不夠高時，將這些值設定為夾具。<br/> |



 

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

 

