---
title: dp3-ps
description: 計算來源註冊的三個元件點乘積。 |dp3-ps
ms.assetid: a365acd1-89c0-4340-8f51-8e478f84ddc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49e957078832f11885ea82baf8438d712394133eb77ad8eeaba705ff0d32a9d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024628"
---
# <a name="dp3---ps"></a>dp3-ps

計算來源註冊的三個元件點乘積。

## <a name="syntax"></a>Syntax



| dp3 dst、src0、src1 |
|---------------------|



 

其中

-   dst 是目的地註冊。
-   src0 是來源註冊。
-   src1 是來源註冊。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dp3                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

下列程式碼片段會顯示執行的作業：


```
dest.x = dest.y = dest.z = dest.w = 
  (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
```



此指令會在向量管線中執行，並一律寫出至色彩通道。 在第1版 \_ 中，此指令仍會使用向量管線，但可能會寫入至任何通道。

具有目的地 register 的指令 ( xyz) 寫入遮罩可與 dp3 共同發行，如下所示。


```
dp3 r0.rgb, t0, v0            // Copy scalar result to color components
+mov r2.a, t0                 // Copy alpha component from t0 in parallel 
```



您可以使用「 [來源登錄」已簽署的調整](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) 輸入引數修飾詞 (\_ bx2) 套用至其輸入引數的 dp3 指令，如果它們尚未擴充至已簽署的動態範圍。 針對光源著色器， (sat) 的飽和指令修飾詞 \_ 通常會用來將負數值夾具至黑色，如下列範例所示。


```
dp3_sat r0, t0_bx2, v0_bx2    // t0 is a bump map, v0 contains the light direction
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




