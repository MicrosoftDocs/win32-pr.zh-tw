---
title: 'RestartStrip (DirectX HLSL Stream-Output 物件) '
description: 結束目前的基本區域並啟動新的帶。 如果目前的帶狀沒有發出足夠的頂點來填滿基本拓撲，則會捨棄結尾不完整的基本。
ms.assetid: ca8eb7cf-1b4a-4082-b768-01390c5f8b47
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aafd6407d556a6d0b4269c38192107edbc7cb1fa
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120193"
---
# <a name="restartstrip-directx-hlsl-stream-output-object"></a>RestartStrip (DirectX HLSL Stream-Output 物件) 

結束目前的基本區域並啟動新的帶。 如果目前的帶狀沒有發出足夠的頂點來填滿基本拓撲，則會捨棄結尾不完整的基本。

RestartStrip () ;



 

## <a name="parameters"></a>參數



| 項目                                                                                     | 描述 |
|------------------------------------------------------------------------------------------|-------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span>**沒有**<br/> |             |



 

## <a name="return-value"></a>傳回值

無

## <a name="remarks"></a>備註

區域剪下會導致目前的帶狀結束，並啟動新的帶。 您可以藉由明確地呼叫這個方法，或藉由轉譯最大的索引值 ( 1 來完成帶剪，也就是在) 的16位索引中，以0xffffffff 表示32位的索引或0xffff。 索引實例繪製的每個實例都會自動剪下剪下。 即使拓撲不是三角形帶，也是如此。

> [!Note]  
> 只有在 [功能等級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10.0 或更高的裝置上，才可支援重新開機和1個「魔術值」。

 

輸出一律會假設為三角形帶。 若要讓輸出成為三角形清單，您必須在每個三角形之間呼叫 RestartStrip。 不支援三角形風扇。

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                              | 支援 |
|-----------------------------------------------------------|-----------|
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 是       |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 否        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 否        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 否        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[資料流程輸出物件](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

