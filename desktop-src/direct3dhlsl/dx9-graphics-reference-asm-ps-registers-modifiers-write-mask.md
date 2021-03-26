---
title: 目的地註冊寫入遮罩
description: 寫入遮罩可控制在完成指令之後，要寫入目的地暫存器的哪些元件。
ms.assetid: 376a28c8-8a88-4807-a8ab-f59448d965e8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 80f649770b84174dbb716967e9d941034c3966f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932583"
---
# <a name="destination-register-write-mask"></a>目的地註冊寫入遮罩

寫入遮罩可控制在完成指令之後，要寫入目的地暫存器的哪些元件。 只要元件的順序為 rgba 或 xyzw，就可以使用輸出寫入遮罩。 也就是說，rba 和. xw 是有效的遮罩。 材質暫存器有一組規則，而非材質暫存器有另一組規則。

## <a name="syntax"></a>Syntax



| writemask |
|---------------|



 

其中

-   dst 是目的地註冊。
-   writemask 是任一組的遮罩序列： (x、y、z、w) 或 (紅色、綠色、藍色、Alpha) 。

## <a name="remarks"></a>備註

以下是可用的目的地寫入遮罩。



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| xyzw (預設)        | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| .xyz                  | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| w                    | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| 任意遮罩        |      |      |      | x    | x    | x    | x     | x    | x     |



 

任意的遮罩可讓任何一組通道合併以產生遮罩。 通道必須列在 order r、g、b 和 a-例如 rba，這會更新目的地的紅色、藍色和 Alpha 通道。 您可以在第1版或更高版本中取得任意的遮罩 \_ 。

如果未指定目的地寫入遮罩，目的地寫入遮罩會預設為 rgba 案例。 換句話說，會更新目的地暫存器中的所有通道。

針對 1 \_ 0 到 1 3 的版本 \_ ， [dp3-ps](dp3---ps.md) dp3 算術指令只能使用 rgb 或 rgba 輸出寫入遮罩。

目的地暫存器寫入遮罩僅支援算數運算。 它們不能用於紋理定址指示，除了第1版的 \_ 指令、 [texcrd-ps](texcrd---ps.md) 和 [texld-ps \_ 2 \_ 0 和更新](texld---ps-2-0.md)版本之外。

預設值是寫入全部四個色彩通道。


```
// All four color channels can be written by explicitly listing them.
mul r0.rgba, t0, v0

// Or, the default mask can be used to write all four channels.
mul r0, t0, v0
```



Alpha 寫入遮罩也稱為純量寫入遮罩，因為它使用純量管線。


```
add r0.a, t1, v1
```



因此，此指示會將 t1 的 Alpha 元件總和和 v1 的 Alpha 元件，有效地放入 r0 中。

色彩寫入遮罩是用來控制對色彩通道的寫入。


```
// The color write mask is also referred to as the vector write mask, 
//   because it uses the vector pipeline.
mul r0.rgb, t0, v0
```



在第1版中 \_ ，只要遮罩的順序為 r、g、b、a，就可以將目的地寫入遮罩用於任何組合中。


```
// This example updates the red, blue, and alpha channels.
mov r0.rba, r1
```



共同發行的指令允許同時發出兩個可能不同的指令。 這可透過執行 Alpha 管線和 RGB 管線中的指示來完成。


```
  mul r0.rgb, t0, v0
+ add r1.a,   t1, c1
```



以這種方式配對指示的優點是，它可讓您以平行方式在向量和純量管線中執行不同的作業。

這些頂點著色器輸出暫存器會限制為下列寫入遮罩：



| 註冊類型 | 必要的寫入遮罩                                              |
|---------------|------------------------------------------------------------------|
| oFog          | 此純量暫存器不允許明確的寫入遮罩        |
| 選擇          | 此純量暫存器不允許明確的寫入遮罩        |
| oPos          | xyzw (預設值)                                       |
| oT\#          | 合併遮罩：. x. \| \| \| xyzw (是預設)  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器暫存器修飾詞](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




