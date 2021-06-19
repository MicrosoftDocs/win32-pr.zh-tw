---
title: Direct3D 12 Raytracing HLSL 著色器
description: 查看描述高階著色器語言 (HLSL) 著色器（支援 Direct3D 12 raytracing 管線）之文章的連結。
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca19081b1ea963851e82d18912153434c3e38d1
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394833"
---
# <a name="direct3d-12-raytracing-hlsl-shaders"></a>Direct3D 12 Raytracing HLSL 著色器

下列 HLSL 著色器支援 Direct3D 12 raytracing 管線。 這些著色器是編譯成程式庫的函式，其中包含目標模型 lib_6_3，並由著色器函式上的屬性 *[著色器 ( "shadertype" ) ]* 識別。 請參閱 **內建函式** 和 **系統值** ，以查看每個著色器類型所允許的內容。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                       | 描述                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**任何命中著色器**](any-hit-shader.md)<br/>                              | 當光線交集不透明時，所叫用的著色器。<br/>                                                                                                                                                                                                                                              |
| [**可呼叫著色器**](callable-shader.md)<br/>                              | 從具有 **CallShader** 內建的另一個著色器叫用的著色器。<br/>                                                                                                                                                                                                                                              |
| [**最接近的點擊著色器**](closest-hit-shader.md)<br/>                              | 當它已啟用，且已判定最接近的點擊，或光線交集搜尋結束時，即會叫用著色器。<br/>                                                                                                                                                                                                                                              |
| [**交集著色器**](intersection-shader.md)<br/>                              | 著色器，用來針對與關聯的周框方塊 (周框方塊) 相交的光線，執行自訂交集基本專案。<br/>                                                                                                                                                                                                                                              |
| [**遺漏著色器**](miss-shader.md)<br/>                              | 找不到或不接受光線交集時，所叫用的著色器。<br/>                                                                                                                                                                                                                                              |
| [**光線產生著色器**](ray-generation-shader.md)<br/>                              | 呼叫 [**TraceRay**](traceray-function.md) 以產生光線的著色器。<br/>                                                                                                                                                                                                                                              |

## <a name="related-topics"></a>相關主題

<dl> <dt>

[核心參考](direct3d-12-core-reference.md)
</dt> <dt>

[Direct3D 12 參考](direct3d-12-reference.md)
</dt> </dl>

 

 





