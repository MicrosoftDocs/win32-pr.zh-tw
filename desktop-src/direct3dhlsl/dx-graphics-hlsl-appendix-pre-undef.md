---
title: " undef 指示詞"
description: 預處理器指示詞，移除先前使用 \ 定義指示詞定義之常數或宏的目前定義。
ms.assetid: ba6bbe6b-ecfa-40cb-887f-e42b6e22c7bd
keywords:
- undef 指示詞 HLSL
topic_type:
- apiref
api_name:
- undef Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7358dc60d002e784394f64773934a18f7413e493
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312554"
---
# <a name="undef-directive"></a>\#undef 指示詞

預處理器指示詞，移除先前使用[ \# define](dx-graphics-hlsl-appendix-pre-define.md)指示詞定義之常數或宏的目前定義。



| \#undef *識別碼* |
|----------------------|



 

## <a name="parameters"></a>參數



| 項目                                                                              | 描述                                                                                                                                                      |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*識別碼*<br/> | 要移除其定義之常數或宏的識別碼。 如果您要 undefining 宏，請只提供識別碼，而不是參數清單。 <br/> |



 

## <a name="remarks"></a>備註

您可以將 \# undef 指示詞套用至沒有先前定義的識別碼; 如此可確保未定義識別碼。 不會在 undef 語句內執行宏取代 \# 。

Undef 指示詞 \# 通常會與[ \# 定義](dx-graphics-hlsl-appendix-pre-define.md)指示詞配對，以在原始程式中建立一個區域，其中識別碼具有特殊意義。 例如，原始程式的特定函式可以使用資訊清單常數，以定義不會影響程式其他部分的環境特定值。 Undef 指示詞 \# 也適用于 [) 指示詞，以控制來來源程式的條件式編譯。

您可以使用/U 選項從命令列未定義常數和宏，後面接著要定義的識別碼。 這相當於在原始程式檔的開頭加入一連串的 undef 指示詞 \# 。

## <a name="examples"></a>範例

下列範例示範如何使用 undef 指示詞 \# 來移除符號常數和宏的定義。


```
#define WIDTH           80
#define ADD( X, Y )     (X) + (Y)

#undef WIDTH
#undef ADD
```



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ (DirectX HLSL) 的預處理器指示詞 ](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\# (DirectX HLSL 定義指示詞) ](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[\#如果為，) ](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





