---
title: 'dcl_usage output (sm1、sm2、sm3 與 asm) '
description: 各種類型的輸出暫存器已折迭為十二個輸出暫存器 (兩個用於色彩、八個用於材質、一個用於位置，另一個用於霧和點大小) 。
ms.assetid: 500ca6b3-0f8a-446e-b1b9-edc51f006ad4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c653c5af43bd3392f97e30571ac56ded66cbfc04
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990986"
---
# <a name="dcl_usage-output-sm1-sm2-sm3---vs-asm"></a>dcl \_ 使用方式輸出 (sm1、sm2、sm3-vs asm) 

各種類型的輸出暫存器已折迭為十二個輸出暫存器 (兩個用於色彩、八個用於材質、一個用於位置，另一個用於霧和點大小) 。 這些可用於使用者想要插入圖元著色器的任何內容：材質座標、色彩、霧化等等。

輸出暫存器需要包含語義的宣告。 例如，藉由宣告具有位置或點大小語義的輸出暫存器，就會取代舊的位置和點大小暫存器。

在十二個輸出暫存器中，任何十個 (不一定 o0 至 o9) 有四個元件 (xyzw) ，另一個則必須宣告為 position (，而且也必須同時包含四個元件) ，也可以選擇性地將這四個元件全部包含在純量點大小。

## <a name="syntax"></a>Syntax

宣告輸出暫存器的語法類似于輸入暫存器的宣告：



|                                  |
|----------------------------------|
| dcl \_ 語義 o \[ . 寫入 \_ 遮罩\] |



 

其中：

-   dcl \_ 語義可以使用與輸入宣告相同的一組語義。 語義名稱來自 [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (，而且會與索引配對，例如 position3) 。 不使用 positiont0 語義時，一律必須有一個輸出暫存器，才能處理頂點。 Positiont0 語義和 pointsize0 語義是唯一的意義，只是允許從頂點到圖元著色器的連結。 若為具有流量控制的著色器，則會假設已宣告最糟的案例輸出。 如果著色器實際上未輸出它所宣告的內容，則不會 (預設值，因為流量控制) 。
-   o 是輸出暫存器。 請 [參閱 \_ 輸出](dx9-graphics-reference-asm-vs-registers-vs-3-0.md)暫存器。
-   寫入 \_ 遮罩表示可以多次宣告的相同輸出暫存器 (因此，每次都有唯一的寫入遮罩可將不同的語義套用至個別的元件) 。 不過，在宣告中不能多次使用相同的語義。 這表示向量必須是四個或更少的元件，且不能跨四個元件的暫存器界限 (個別的暫存器) 。 使用點大小語義時，它應該有完整的寫入遮罩，因為它會被視為純量。 使用位置語義時，它應該要有完整的寫入遮罩，因為必須寫入全部四個元件。

## <a name="remarks"></a>備註



| 頂點著色器版本 | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|-------|
| dcl \_ 使用方式             | x    | x     |



 

所有的 [dcl \_ 使用](dcl-usage-input-register---vs.md) 方式指令都必須出現在第一個可執行指令之前。

## <a name="declaration-examples"></a>宣告範例


```
vs_3_0
dcl_color4     o3.x    // color4 is a semantic name.
dcl_texcoord3  o3.yz   // Different semantics can be packed into one register.
dcl_fog        o3.w 
dcl_tangent    o4.xyz
dcl_position   o7.xyzw // position must be declared to some unique register 
                       //   in a vertex shader, with all 4 components.

dcl_psize      o6      // Pointsize cannot have a mask 
                       //   (that is, mask is full .xyzw)
                       // This is an implied scalar register. 
                       // No other semantics can be assigned to any components
                       //   of this register.
                       // If pointsize declaration is not used (typical),
                       //   only 11 "out" registers are available, not 12.
                       // Pixel shaders cannot see this value.

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 