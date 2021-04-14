---
title: def pragma 指示詞
description: 手動設定浮點著色器暫存器的 Pragma 指示詞。
ms.assetid: 45db94c4-f6f6-4c88-9bf2-4eaa9abf7844
keywords:
- def pragma 指示詞 HLSL
topic_type:
- apiref
api_name:
- def pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a921e17f8ddee4aaabfe50e75f42ce44812863d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104990679"
---
# <a name="def-pragma-directive"></a>def pragma 指示詞

手動設定浮點著色器暫存器的 Pragma 指示詞。



| \#pragma def ( *target*、 *register*、 *val1*、 *val2*、*val3*、 *val4* )  |
|---------------------------------------------------------------------|



 

## <a name="parameters"></a>參數



| 項目                                                                        | 描述                                                                 |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="target"></span><span id="TARGET"></span>*目標*<br/>       | 包含要配置之註冊的目標。 <br/>                  |
| <span id="register"></span><span id="REGISTER"></span>*註冊*<br/> | 要配置的浮點著色器暫存器。 <br/>                     |
| <span id="val0"></span><span id="VAL0"></span>*val0*<br/>             | 要配置給指定之暫存器的值的第一個位元組。 <br/>  |
| <span id="val1"></span><span id="VAL1"></span>*val1*<br/>             | 要配置給指定之暫存器的值的第二個位元組。 <br/> |
| <span id="val2"></span><span id="VAL2"></span>*val2*<br/>             | 要配置給指定之註冊的值的第三個位元組。 <br/>  |
| <span id="val3"></span><span id="VAL3"></span>*val3*<br/>             | 要配置給指定之註冊的值的第四個位元組。 <br/> |



 

## <a name="remarks"></a>備註

Def pragma 可讓開發人員 prefill 具有指定值的浮點著色器暫存器。 不常使用這個 pragma。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[ (DirectX HLSL) 的預處理器指示詞 ](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\# (DirectX HLSL) 的 pragma 指示詞 ](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





