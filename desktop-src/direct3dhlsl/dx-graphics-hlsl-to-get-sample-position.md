---
title: 'GetSamplePosition (DirectX HLSL 材質物件) '
description: 取得指定之範例的位置。
ms.assetid: 4e622b85-82d6-4339-b03a-becbe5f9aa57
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 95be6d9b6c4cbf70aed059399af0892a3c75f0a3462b6ef2b0732e8180f4e123
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068108"
---
# <a name="getsampleposition-directx-hlsl-texture-object"></a>GetSamplePosition (DirectX HLSL 材質物件) 

取得指定之範例的位置。

ret 物件. GetSamplePosition ( int s ) ;



 

## <a name="parameters"></a>參數



| 項目                                                                                           | 描述                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*物件*<br/> | Texture2DMS 或 Texture2DMSArray [材質物件](dx-graphics-hlsl-to-type.md) 類型。<br/> |
| <span id="s"></span><span id="S"></span>*！*<br/>                                         | \[以 \] 零為基底的範例索引。<br/>                                                      |



 

## <a name="return-value"></a>傳回值

傳回 (x，y) 樣本位置，這是兩個元件的浮點數向量。

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          | x         |          | x         |          | x         |



 

-   在 Direct3D 10.1 或更高版本中可以使用著色器模型4.1。

## <a name="remarks"></a>備註

圖元著色器可依取樣頻率進行評估 (針對每個樣本) 或圖元頻率執行圖元著色器， (每圖元) 執行一次圖元著色器。 將 SV \_ SampleIndex 語義附加至圖元著色器輸入，以取樣頻率叫用圖元著色器，然後輸入值會在取樣轉譯目標時當做樣本索引。

您可以透過數種方式來插入圖元著色器輸入。 若要插入：

-   圖元中心，請勿使用任何語義。
-   範例，請使用 SV \_ SampleIndex 語義。
-   距心位置，請使用[ \_ 距心](dx-graphics-hlsl-struct.md)修飾詞。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[材質物件](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





