---
title: 著色器模型4
description: 著色器模型4是著色器模型3中功能的超集合，不同之處在于著色器模型4不支援著色器模型1中的功能。
ms.assetid: 76155749-11e9-41ff-881d-8f77f2729364
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c863d952990cd05394244fe662650df59568eeaf
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466965"
---
# <a name="shader-model-4"></a>著色器模型4

著色器模型4是 [著色器模型 3](dx-graphics-hlsl-sm3.md)中功能的超集合，不同之處在于著色器模型4不支援著色器模型1中的功能。 它是使用通用著色器核心所設計，可提供一組通用的功能給所有可程式化的著色器，這些著色器只能使用 HLSL 進行程式設計。




| 功能 | 功能 | 
|---------|------------|
| 指令集 | <a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL 函式</strong></a> | 
| 註冊集 | 您可以使用 HLSL 語義（例如元件封裝），透過常數和材質緩衝區中的成員來存取暫存器集。<ul><li>圖元著色器暫存器 (請參閱暫存器 <a href="dx-graphics-hlsl-sm4-registers-ps-4-0.md">-ps_4_0</a> 和暫存器 <a href="dx-graphics-hlsl-sm4-registers-ps-4-1.md">-ps_4_1</a>) </li><li>頂點著色器暫存器 (請參閱暫存器 <a href="dx-graphics-hlsl-sm4-registers-vs-4-0.md">-vs_4_0</a> 和暫存器 <a href="dx-graphics-hlsl-sm4-registers-vs-4-1.md">-vs_4_1</a>) </li><li>幾何著色器暫存器 (查看暫存器 <a href="dx-graphics-hlsl-sm4-registers-gs-4-0.md">-gs_4_0</a> 和暫存器 <a href="dx-graphics-hlsl-sm4-registers-gs-4-1.md">-gs_4_1</a>) </li></ul> | 
| 頂點著色器最大值 | 沒有限制 | 
| 圖元著色器最大值 | 沒有限制 | 
| 新增著色器設定檔 | gs_4_0、ps_4_0、vs_4_0、gs_4_1 *、ps_4_1*、gs_4_1 * | 
| 已新增新的 Effect-Framework 設定檔 | fx_4_0，fx_4_1 * | 




 

\*\_ \_ \_ \_ \_ \_ \_ \_ 在 Direct3D 10.1 或更高版本上，支援 gs 4 1、ps 4 1、vs 4 1 和 fx 4 1。

著色器模型4支援新的管線階段（幾何著色器階段），可用來建立或修改現有的幾何。 它也包含兩個新的物件類型：資料流程輸出物件的設計目的是要從幾何階段串流資料，以及實作為紋理取樣函數的樣板化紋理物件。

-   [一般著色器核心](dx-graphics-hlsl-common-core.md)
-   [常數](dx-graphics-hlsl-constants.md)
-   [Geometry-著色器物件](dx-graphics-hlsl-geometry-shader.md)
-   [資料流程輸出物件](dx-graphics-hlsl-so-type.md)
-   [材質物件](dx-graphics-hlsl-to-type.md)

著色器模型4支援封裝規則，這些規則會規定資料儲存時如何排列緊密的資料。 [常數變數的封裝規則](dx-graphics-hlsl-packing-rules.md)中描述這些規則

[著色器模型4元件](dx-graphics-hlsl-sm4-asm.md)一節描述著色器模型4和著色器模型4.1 支援的元件指示。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型與著色器設定檔](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




