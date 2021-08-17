---
title: RWTexture2DArray
description: 讀取/寫入資源。 |RWTexture2DArray
ms.assetid: 6a6f3655-f1c0-4d5b-91a2-d79da65858b8
keywords:
- RWTexture2DArray HLSL
topic_type:
- apiref
api_name:
- RWTexture2DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e9ae4d4c7c47012b71a70916f5861975176b86e6612cb2a4fec3ea6c9c6e17cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095128"
---
# <a name="rwtexture2darray"></a>RWTexture2DArray

讀取/寫入資源。



| 方法                                                             | 描述                   |
|--------------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture2darray-getdimensions.md) | 取得資源維度。 |
| [**載入**](rwtexture2darray-load.md)                              | 讀取紋理資料。           |
| [**運算子\[\]**](sm5-object-rwtexture2darray-operatorindex.md)  | 取得資源變數。     |



 

您可以在 **RWTexture2DArray** 物件前面加上儲存類別 **globallycoherent**。 此儲存類別會造成記憶體阻礙和同步處理，以排清整個 GPU 上的資料，讓其他群組可以看到寫入。 如果沒有這個規範，記憶體屏障或同步將只會在目前群組內排清 UAV。

**RWTexture2DArray** 物件需要物件的宣告語句中的元素類型。 例如，下列宣告是正確的：


```
RWTexture2DArray<float> tex;
```



由於 **RWTexture2DArray** 物件是 UAV 類型的物件，因此它的屬性與著色器資源檢視不同 (SRV) 型別物件，例如 [**Texture2DArray**](sm5-object-texture2darray.md) 物件。 例如，您可以讀取和寫入 **RWTexture2DArray** 物件，但只能從 **Texture2DArray** 物件讀取。

**RWTexture2DArray** 物件無法使用來自 [**Texture2DArray**](sm5-object-texture2darray.md)物件的方法，例如 [範例](dx-graphics-hlsl-to-sample.md)。 不過，因為您可以為相同的資源建立多個檢視類型，所以您可以將多個紋理類型宣告為多個著色器中的單一材質。 例如，您可以在計算著色器中宣告並使用 **RWTexture2DArray** 物件做為 *tex* ，然後在圖元著色器中宣告並使用 **Texture2DArray** 物件做為 *tex* 。

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

 

 




