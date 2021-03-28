---
title: 來源註冊已簽署的調整
description: 從每個通道減去0.5，並依2.0 調整結果。 名稱 bx2 來自偏差和相應減少-二，也就是它所執行的作業。
ms.assetid: ad94145a-2687-4c20-b3ed-70270a0c53bf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 214f4fcb6ad4f382a97b8c8d75a733124c31d68a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104184194"
---
# <a name="source-register-signed-scaling"></a>來源註冊已簽署的調整

從每個通道減去0.5，並依2.0 調整結果。 名稱 bx2 來自偏差和相應減少-二，也就是它所執行的作業。

## <a name="syntax"></a>Syntax


```
source register_bx2
```



## <a name="register"></a>註冊

來源註冊。 如需註冊類型的詳細資訊，請參閱[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 \_ \_ ps \_ 1 \_ 3 \_ \_ ps \_ 1 \_ 4 註冊](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)。

## <a name="remarks"></a>備註

這項作業通常用來將資料從 \[ 0.0 擴充至 \] 1.0 1.0 至 \[ 1.0 \] 。 這個修飾詞是設計來搭配算術指令使用。 此修飾詞通常用於輸入點乘積指令 ([dp3-ps](dp3---ps.md)) 。 對 \_ 範圍0到1以外的資料使用 bx2 可能會產生未定義的結果。

已簽署的調整作業會套用至下一個指令執行之前從註冊讀取的資料。 此作業會套用至所有四色通道 (RGBA) ，如下所示：


```
y = 2(x - 0.5)
```



註冊的內容不會變更。 修飾詞只會套用至從註冊讀取的資料。

此修飾詞與 [來源](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) 暫存器有互斥，因此無法套用至相同的暫存器。

版本資訊：

-   針對 ps \_ 1 \_ 0 和 ps \_ 1 \_ 1，您可以 \_ 在任何來源登錄上使用 bx2，以取得表單 texm3x2 \* 和 texm3x3 的材質指示 \* 。 \_bx2 不能用於任何其他的材質指示，例如 [texreg2ar-ps](texreg2ar---ps.md) 或 [texreg2gb](texreg2gb---ps.md)。
-   針對 ps \_ 1 \_ 2 和 ps \_ 1 \_ 3，您可以 \_ 在任何來源登錄上使用 bx2，以取得任何 tex \* 指令，但不包括： [texreg2ar-ps](texreg2ar---ps.md)、 [texreg2gb-ps](texreg2gb---ps.md)、 [texbem-ps](texbem---ps.md) 或 [texbeml-ps](texbeml---ps.md)。

## <a name="example"></a>範例

此範例會取樣材質、將資料轉換為-1 到 + 1 的範圍，並計算點乘積。


```
tex t0                        ; Read a texture color.
dp3_sat r0, t0_bx2, v0_bx2    ; Calculate a dot product.
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器來源登錄修飾詞](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




