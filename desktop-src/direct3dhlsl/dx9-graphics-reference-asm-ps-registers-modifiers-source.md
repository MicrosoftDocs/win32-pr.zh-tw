---
title: 圖元著色器來源登錄修飾詞
description: 在指令執行之前，請使用來源登錄修飾詞來變更從註冊程式讀取的值。
ms.assetid: b45d0919-7878-4184-ad4a-5623aae9d1f1
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a9dd4476dd7a1a885edb2e62a29b5127f5ff0a14
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129675"
---
# <a name="pixel-shader-source-register-modifiers"></a>圖元著色器來源登錄修飾詞

在指令執行之前，請使用來源登錄修飾詞來變更從註冊程式讀取的值。 來源暫存器的內容會保持不變。 修飾詞可用來調整註冊資料的範圍，以準備進行指令。 一組稱為選取器的修飾詞會從單一通道複製或複寫資料 (r、g、b、) 到其他通道。

## <a name="ps_1_1---ps_1_4"></a>ps \_ 1 \_ 1-ps \_ 1 \_ 4

下表列出支援每個修飾詞的版本：



| 來源暫存器修飾符                                                                                    | Syntax         | \_第1版 | \_第1版     | 第1版 \_     | \_第1版     |
|--------------------------------------------------------------------------------------------------------------|----------------|---------|------|------|------|
| [偏見](dx9-graphics-reference-asm-ps-registers-modifiers-bias.md)                                           | 註冊 \_ 偏差 | X       | X    | X    | X    |
| [轉化](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)                                       | 1-報名   | X       | X    | X    | X    |
| [negate](dx9-graphics-reference-asm-ps-registers-modifiers-negate.md)                                       | \- 註冊    | X       | X    | X    | X    |
| [依2調整](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md)                                 | 註冊 \_ x2   |         |      |      | X    |
| [經過簽署的調整](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md)                         | 註冊 \_ bx2  | X       | X    | X    | X    |
| [texld 和 texcrd 修飾詞](dx9-graphics-reference-asm-ps-registers-modifiers-ps-1-4.md)                   | 註冊 \_ d\*  | X       | X    | X    | X    |
| [來源註冊 swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) | register. xyzw  | X       | X    | X    | X    |



 

來源暫存器修飾詞只能用於算術指令。 它們不能用於紋理位址指令。 例外狀況是 [由 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) 個修飾詞所調整。 針對第1版 \_ ，已簽署的小數位數可用於任何 texm 指令的來源引數 \* 。 在第1版 \_ 或第1版 \_ 中，已簽署的小數位數可用於任何材質位址指令的來源引數。

部分修飾詞的特定限制：

-   您可以利用偏差、帶正負號的調整或 scalex2 修飾詞，將否定的符號結合在一起。 如果結合，則會最後執行否定。
-   反轉無法與任何其他修飾詞結合。
-   反轉、否定、偏差、帶正負號的調整和 scalex2 可以與任何選取器結合。
-   來源登錄修飾詞不應該用於常數暫存器，因為它們會導致未定義的結果。 在第1版 \_ 中，不允許常數的修飾詞，而且驗證將會失敗。

## <a name="ps_2_0-and-above"></a>ps \_ 2 \_ 0 和更新版本

針對 ps \_ 2 \_ 0 和更新版本，修飾詞的數目已經過簡化。

### <a name="negate"></a>Negate

否定來源暫存器的內容。



| 元件修飾詞 | 描述     |
|--------------------|-----------------|
| \- R               | 來源否定 |



 

否定修飾詞不能用在這些指示的第二個來源登錄上： [m3x2-ps](m3x2---ps.md)、 [m3x3-ps](m3x3---ps.md)、 [m3x4-ps](m3x4---ps.md)、 [m4x3-ps](m4x3---ps.md)和 [m4x4-ps](m4x4---ps.md)。



| 圖元著色器版本 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|-------|------|-------|
| \-                    | x    | x    | x     | x    | x     |



 

### <a name="absolute-value"></a>絕對值

取得註冊的絕對值。



| 圖元著色器版本 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|-------|------|-------|
| abs                   |      |      |       | x    | x     |



 

如果任何第3版著色器從一或多個常數浮點數暫存器 (c \#) 讀取，下列其中一個條件必須為 true。

-   所有常數浮點數暫存器都必須使用 abs 修飾詞。
-   沒有常數浮點數暫存器可以使用 abs 修飾詞。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器暫存器修飾詞](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




