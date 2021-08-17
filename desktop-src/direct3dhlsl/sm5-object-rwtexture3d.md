---
title: RWTexture3D
description: 讀取/寫入資源。 |RWTexture3D
ms.assetid: 4d02810e-4f3c-4b20-b057-0ff27d6732b5
keywords:
- RWTexture3D HLSL
topic_type:
- apiref
api_name:
- RWTexture3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5bc2630d339bfb465b570ba62b346cd931301425f4feeb4367407ffd52336e7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789861"
---
# <a name="rwtexture3d"></a>RWTexture3D

讀取/寫入資源。



| 方法                                                        | 描述                   |
|---------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture3d-getdimensions.md) | 取得資源維度。 |
| [**載入**](rwtexture3d-load.md)                              | 讀取紋理資料。           |
| [**運算子\[\]**](sm5-object-rwtexture3d-operatorindex.md)  | 取得資源變數。     |



 

您可以在 **RWTexture3D** 物件前面加上儲存類別 **globallycoherent**。 此儲存類別會造成記憶體阻礙和同步處理，以排清整個 GPU 上的資料，讓其他群組可以看到寫入。 如果沒有這個規範，記憶體屏障或同步將只會在目前群組內排清 UAV。

**RWTexture3D** 物件需要物件的宣告語句中的元素類型。 例如，下列宣告是正確的：


```
RWTexture3D<float> tex;
```



由於 **RWTexture3D** 物件是 UAV 類型的物件，因此它的屬性與著色器資源檢視不同 (SRV) 型別物件，例如 [**Texture3D**](sm5-object-texture3d.md) 物件。 例如，您可以讀取和寫入 **RWTexture3D** 物件，但只能從 **Texture3D** 物件讀取。

**RWTexture3D** 物件無法使用來自 [**Texture3D**](sm5-object-texture3d.md)物件的方法，例如 [範例](dx-graphics-hlsl-to-sample.md)。 不過，因為您可以為相同的資源建立多個檢視類型，所以您可以將多個紋理類型宣告為多個著色器中的單一材質。 例如，您可以在計算著色器中宣告並使用 **RWTexture3D** 物件做為 *tex* ，然後在圖元著色器中宣告並使用 **Texture3D** 物件做為 *tex* 。

> [!Note]  
> 當您在相同的資源中建立多個檢視類型時，執行時間會強制執行特定的使用模式。 例如，執行時間不允許您同時讓相同資源的資源和 SRV 對應的 UAV 對應同時啟用。

 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此物件。



| 著色器模型                                                                | 支援 |
|-----------------------------------------------------------------------------|-----------|
| [著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型 | 是       |



 

下列著色器類型支援此物件：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型5物件](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




