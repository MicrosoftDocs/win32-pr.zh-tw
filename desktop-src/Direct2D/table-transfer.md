---
title: 資料表傳送效果
description: 使用表格傳輸效果，以使用從插即您提供的值清單來建立的傳送函式，來對應影像的色彩濃度。
ms.assetid: FB426909-3C91-4709-9E3A-E45C7AE345A3
keywords:
- 資料表傳送效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8c533b55fd55c983b976633b766a6d8d273631d6111de9e2e36387f711f5f14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118665001"
---
# <a name="table-transfer-effect"></a>資料表傳送效果

使用表格傳輸效果，以使用從插即您提供的值清單來建立的傳送函式，來對應影像的色彩濃度。

這項效果的 CLSID 是 CLSID \_ D2D1TableTransfer。

-   [範例影像](#example-image)
-   [效果屬性](#effect-properties)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="example-image"></a>範例影像

此處的影像顯示資料表傳送效果的輸入和輸出。



| 之前                                                         |
|----------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg)     |
| After                                                          |
| ![轉換後的影像。](images/11-tabletransfer.png) |



 


```C++
ComPtr<ID2D1Effect> tableTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1TableTransfer, &tableTransferEffect);

tableTransferEffect->SetInput(0, bitmap);

float table[2] = {0.75f, 1.0f};
tableTransferEffect->SetValue(D2D1_TABLETRANSFER_PROP_BLUE_TABLE, table);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(tableTransferEffect.Get());
m_d2dContext->EndDraw();
```



傳送函式是根據輸入的清單 V = (V0、V1、V2、V3、V？ ，V<sub>n</sub>) 其中 N 是元素數目-1。

輸入圖元濃度以 C 表示。輸出圖元濃度，C 可以使用方程式來計算。

若為值 C，請挑選值 k，例如： k/N = C < (k + 1) /N

輸出 C 使用下列方程式計算： C ' = V？ + (C-k/N) \* n \* (V???單? -V？ ) 

此效果適用于直接和預乘的 Alpha 影像。 效果會輸出預乘的 Alpha 點陣圖。

以下是當 table 屬性設定為時，資料表傳送函式的圖表看起來的樣子 `[0.0, 0.25, 1.0]` 。

![表格傳送函數的圖元濃度圖形。](images/table-transfer-graph.png)

## <a name="effect-properties"></a>效果屬性

> [!Note]  
> 資料表傳輸屬性的所有通道值都不會有任何限制，而且最小值為0.0 和1.0。

 



| 顯示名稱和索引列舉                                           | 類型和預設值                       | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedTable<br/> D2D1 \_ TABLETRANSFER \_ 的 \_ 成分紅色 \_ 資料表<br/>         | 浮動\[\]<br/> {0.0 f、1.0 f}<br/> | 值的清單，用來定義 Red 通道的傳送函式。                                                                                                                                                                                                                                                                                                                                                                                  |
| RedDisable<br/> D2D1 \_ TABLETRANSFER \_ 的 \_ RED \_ DISABLE<br/>     | BOOL<br/> FALSE<br/>             | 如果您將此設定為 TRUE，則效果不會將傳送函式套用至紅色通道。 如果您將此設定為 FALSE，則會將 RedTableTransfer 函式套用至紅色通道。                                                                                                                                                                                                                                                                             |
| GreenTable<br/> D2D1 \_ TABLETRANSFER \_ 的 \_ \_ 表表表<br/>     | 浮動\[\]<br/> {0.0 f、1.0 f}<br/> | 值的清單，用來定義綠色通道的傳送函數。                                                                                                                                                                                                                                                                                                                                                                                |
| GreenDisable<br/> D2D1 \_ TABLETRANSFER，a \_ \_ 綠 \_ DISABLE<br/> | BOOL<br/> FALSE<br/>             | 如果您將此設定為 TRUE，則效果不會將傳送函式套用至綠色通道。 如果您將此設定為 FALSE，則會將 GreenTableTransfer 函式套用至綠色通道。                                                                                                                                                                                                                                                                       |
| BlueTable<br/> D2D1 \_ TABLETRANSFER \_ 的 \_ BLUE \_ 資料表<br/>       | 浮動\[\]<br/> {0.0 f、1.0 f}<br/> | 值的清單，用來定義藍色通道的傳送函數。                                                                                                                                                                                                                                                                                                                                                                                 |
| BlueDisable<br/> D2D1 \_ TABLETRANSFER \_ 的 \_ BLUE \_ DISABLE<br/>   | BOOL<br/> FALSE<br/>             | 如果您將此設定為 TRUE，則效果不會將傳送函式套用至藍色通道。 如果您將此設定為 FALSE，則會將 BlueTableTransfer 函式套用至藍色通道。                                                                                                                                                                                                                                                                          |
| AlphaTable<br/> D2D1 \_ 資料表 \_ 傳送 \_ 的 \_ ALPHA \_ 表<br/>   | 浮動\[\]<br/> {0.0 f、1.0 f}<br/> | 值的清單，用來定義 Alpha 色板的傳送函數。                                                                                                                                                                                                                                                                                                                                                                                |
| AlphaDisable<br/> D2D1 \_ TABLETRANSFER \_ 的 \_ ALPHA \_ 停用<br/> | BOOL<br/> FALSE<br/>             | 如果您將此設定為 TRUE，則效果不會將傳送函式套用至 Alpha 通道。 如果您將此設定為 FALSE，則會將 AlphaTableTransfer 函式套用至 Alpha 色板。                                                                                                                                                                                                                                                                       |
| ClampOutput<br/> D2D1 TABLETRANSFER 的一種 \_ \_ \_ 夾具 \_ 輸出<br/>   | BOOL<br/> FALSE<br/>             | 效果在效果之前個色彩值是否會將值傳遞給圖形中的下一個效果。 效果會在 premultiplies Alpha 之前個值。<br/> 如果您將此設定為 TRUE，效果會將值設為夾具。 如果您將此值設定為 FALSE，效果將不會顯示色彩值，但其他效果和輸出介面可能會在這些值的精確度不夠高時，將這些值設定為夾具。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端 | Windows 7 傳統型應用程式的 Windows 8 和平臺更新 \[ \| Windows 儲存應用程式\] |
| 最低支援的伺服器 | Windows 7 傳統型應用程式的 Windows 8 和平臺更新 \[ \| Windows 儲存應用程式\] |
| 標頭                   | d2d1effects。h                                                                      |
| 程式庫                  | d2d1 .lib，dxguid .lib                                                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

