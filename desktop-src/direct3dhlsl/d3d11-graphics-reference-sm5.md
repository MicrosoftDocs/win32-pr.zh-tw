---
title: 著色器模型5
description: 本章節包含 HLSL 著色器模型5的參考頁面。
ms.assetid: ec646940-8901-45c5-a44c-434c8acae2aa
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a252c8ad3cc12c443506fbcc3802d9f1f7c15cfbe8cc62d937fcb9ca8723a8da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119371458"
---
# <a name="shader-model-5"></a>著色器模型5

本章節包含 HLSL 著色器模型5的參考頁面。

著色器模型5是 [著色器模型 4](dx-graphics-hlsl-sm4.md)中功能的超集合。 它是使用通用著色器核心設計的，可為所有可程式化的著色器提供一組通用的功能，這些著色器只能使用 HLSL 進行程式設計。



| 功能                   | 功能                                                                                                                                             |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| 指令集           | [**HLSL 內建函式**](dx-graphics-hlsl-intrinsic-functions.md)                                                                               |
| 頂點著色器最大值         | 沒有限制                                                                                                                                         |
| 圖元著色器最大值          | 沒有限制                                                                                                                                         |
| 新增著色器設定檔 | cs \_ 4 \_ 0、gs \_ 4 \_ 0 \* 、ps \_ 4 \_ 0 \* 、vs \_ 4 \_ 0 \* 、cs \_ 4 \_ 1、gs \_ 4 \_ 1 \* 、ps \_ 4 \_ 1 \* 、vs \_ 4 \_ 1 \* 、cs \_ 5 \_ 0、ds \_ 5 \_ 0、gs \_ 5 \_ 0、hs \_ 5 \_ 0、ps \_ 5 \_ 0、vs \_ 5 \_ 0 |



 

\* -gs \_ 4 \_ 0、gs \_ 4 \_ 1、ps \_ 4 \_ 0、ps \_ 4 \_ 1、vs \_ 4 \_ 0 和 vs \_ 4 \_ 1 是在著色器模型4.0 中引進，但 directx 11 會將 [結構化緩衝區](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) 和位元組位址緩衝區的支援新增至在 DirectX 10 硬體上執行的著色器模型4。

著色器模型5引進了 [計算著色器](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader) ，可提供高速的一般用途計算。

最完整的著色器模型5功能清單包含在 [Direct3D 11 功能](/windows/desktop/direct3d11/direct3d-11-features)清單中。

[著色器模型5元件](shader-model-5-assembly--directx-hlsl-.md)一節描述著色器模型5所支援的元件指示。

## <a name="in-this-section"></a>本節內容



| Item                                                                                                                                                                                                                                                        | 描述                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="Shader_Model_5_Attributes"></span><span id="shader_model_5_attributes"></span><span id="SHADER_MODEL_5_ATTRIBUTES"></span>[著色器模型5屬性](d3d11-graphics-reference-sm5-attributes.md)<br/>                                     | 著色器模型5屬性的參考頁面。<br/>          |
| <span id="Shader_Model_5_Intrinsic_Functions"></span><span id="shader_model_5_intrinsic_functions"></span><span id="SHADER_MODEL_5_INTRINSIC_FUNCTIONS"></span>[著色器模型5內建函式](d3d11-graphics-reference-sm5-intrinsics.md)<br/> | 著色器模型5內建函式的參考頁面。<br/> |
| <span id="Shader_Model_5_Objects"></span><span id="shader_model_5_objects"></span><span id="SHADER_MODEL_5_OBJECTS"></span>[著色器模型5物件](d3d11-graphics-reference-sm5-objects.md)<br/>                                                    | 著色器模型5物件和方法的參考頁面。<br/> |
| <span id="Shader_Model_5_System_Values"></span><span id="shader_model_5_system_values"></span><span id="SHADER_MODEL_5_SYSTEM_VALUES"></span>[著色器模型5系統值](d3d11-graphics-reference-sm5-system-values.md)<br/>                      | 著色器模型5系統值的參考頁面。<br/>       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型與著色器設定檔](dx-graphics-hlsl-models.md)
</dt> </dl>

 

