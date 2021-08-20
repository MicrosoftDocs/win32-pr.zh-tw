---
title: '高階著色器語言 (HLSL) '
description: HLSL 是一種類似 C 的高階著色器語言，您可以搭配 DirectX 中的可程式化著色器來使用。
ms.assetid: 09cdd8d6-0cf5-4f7e-b480-f748d2fa9ca9
ms.topic: article
ms.date: 01/11/2021
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.custom: contperf-fy21q3
ms.openlocfilehash: 9f518102b7b3305103ed85231a791c542418a04c
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812894"
---
# <a name="high-level-shader-language-hlsl"></a>高階著色器語言 (HLSL) 

HLSL 是一種類似 C 的高階著色器語言，您可以搭配 DirectX 中的可程式化著色器來使用。

例如，您可以使用 HLSL 來撰寫 [頂點著色器](../direct3d11/vertex-shader-stage.md)或 [圖元著色器](../direct3d11/pixel-shader-stage.md)，並在您的 [Direct3D](../direct3d12/directx-12-programming-guide.md) 應用程式中，于轉譯器的執行中使用這些著色器。

或者，您也可以使用 HLSL 來撰寫計算著色器，以執行物理模擬。 不過，比方說，如果您想要撰寫自己的卷積運算子來 (影像處理) 作為計算著色器中的 HLSL，則在該案例中，如果您改用[直接機器學習 (DirectML) ](/windows/ai/directml/dml) ，就會獲得更好的效能。

HLSL 的建立 (從 DirectX 9 開始) 設定可程式化 3D [管線](../direct3d11/overviews-direct3d-11-graphics-pipeline.md)。 您可以使用 HLSL 指示來編寫整個管線的程式。

## <a name="where-to-go-next"></a>接下來要前往哪裡

* [HLSL 程式設計指南](./dx-graphics-hlsl-pguide.md)
* [HLSL 的參考](./dx-graphics-hlsl-reference.md)

### <a name="programming-guide-for-hlsl"></a>HLSL 程式設計指南

如需 HLSL 的概念簡介，請參閱 [HLSL 的程式設計指南](./dx-graphics-hlsl-pguide.md)。

程式設計指南會討論不同種類的著色器階段，以及如何建立、編譯、優化、系結和連結著色器。

您也可以在這裡找到有關連續產生的著色器模型版本（已發行）的總覽，以及 HLSL 著色器模型5的最新版說明。

### <a name="reference-for-hlsl"></a>HLSL 的參考

如需 HLSL 參考檔，請參閱 [HLSL 的參考](./dx-graphics-hlsl-reference.md)。

參考章節包含 HLSL 內建的語言語法和內建函式的完整清單，以簡化您的程式碼需求。

此外，您還可以找到著色器模型與設定檔的討論，以及 HLSL 著色器模型1最多的著色器模型參考內容。 此外也有內容涵蓋元件指示、D3DCompiler 工具，以及著色器可以傳回之錯誤和警告的相關資訊。