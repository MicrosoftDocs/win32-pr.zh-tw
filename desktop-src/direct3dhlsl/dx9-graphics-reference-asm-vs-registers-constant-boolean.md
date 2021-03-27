---
title: '常數布林值暫存器 (HLSL 與參考) '
description: 此暫存器是靜態流程式控制制指示中所使用的位集合 (例如，如果 bool 與 else-vs-endif-vs) 。
ms.assetid: bd02d03b-c228-481a-9c98-7442be4cdd07
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9b32841f060a29fce2918daca8f8fd008529bef1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971748"
---
# <a name="constant-boolean-register-hlsl-vs-reference"></a>常數布林值暫存器 (HLSL 與參考) 

此暫存器是靜態流程式控制制指示中所使用的位集合 (例如，[如果 bool-vs](if-bool---vs.md)  -  [else-vs](else---vs.md)  -  [endif-vs](endif---vs.md)) 。 其中有16個，因此著色器可以有16個獨立的分支條件。 您可以使用 [defb-vs](defb---vs.md) 或 [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb)來設定它們。

在 Direct3D 8 和 Direct3D 9 之間變更著色器常數的行為。

-   針對 Direct3D 9，使用 defx 設定的常數會將值指派給著色器常數空間。 使用 defx 宣告之常數的存留期只限于該著色器的執行。 相反地，使用 Api 設定的常數 SetXXXShaderConstantX 會初始化全域空間中的常數。 在呼叫 SetxxxShaderConstants 之前，不會將全域空間中的常數複製到 (著色器) 可見的本機空間。
-   針對 Direct3D 8，使用 defx 或 Api 設定的常數都會將值指派給著色器常數空間。 每次執行著色器時，目前的著色器都會使用常數，而不考慮用來設定它們的技巧。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器暫存器](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 