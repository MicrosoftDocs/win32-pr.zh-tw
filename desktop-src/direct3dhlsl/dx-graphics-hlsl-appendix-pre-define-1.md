---
title: '\#定義指示詞 (常數) '
description: 預處理器指示詞，可將有意義的名稱指派給您應用程式中的常數。
ms.assetid: cc9b34a3-4c83-4999-99ec-e6261ecb2785
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: deae1ca92c2280cd31cbec2bf3482c61fcf2b88a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "104022866"
---
# <a name="define-directive-constant"></a>\#定義指示詞 (常數) 

預處理器指示詞，可將有意義的名稱指派給您應用程式中的常數。



| \#定義 *identifiertoken-字串* |
|-----------------------------------|



 

## <a name="parameters"></a>參數



| 項目                                                                                                                       | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*識別碼*<br/>                                          | 常數的識別碼。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="token-string__optional_"></span><span id="TOKEN-STRING__OPTIONAL_"></span>*token-字串* \[選\]<br/> | 常數的值。 這個參數是由一系列的 token 所組成，例如關鍵字、常數或完整語句。 一或多個空白字元必須將此參數與 *識別碼* 參數分開;這個空白字元不會被視為替代文字的一部分，也不會在文字的最後一個標記之後的任何空白字元。 <br/> 如果您排除此參數，則會從原始程式檔中移除 *識別碼* 參數的所有實例。 識別碼仍會保持定義，並且可使用[ \# if 已定義](dx-graphics-hlsl-appendix-pre-ifdef.md)、 \# ifdef 和 ifndef 指示詞進行測試 \# 。 <br/> |



 

## <a name="remarks"></a>備註

在來源檔案中的 [ \# 定義](dx-graphics-hlsl-appendix-pre-define.md)指示詞之後發生之 *識別碼* 參數的所有實例，都會以 *token 字串* 參數的值取代。 只有在形成權杖時，才會取代識別碼;例如，如果識別碼出現在批註、字串內或較長識別碼的一部分，則不會取代該識別碼。

[ \# Undef](dx-graphics-hlsl-appendix-pre-undef.md)指示詞會指示預處理器忘記定義識別碼; 如需詳細資訊，請參閱 \# (DirectX HLSL) 的 undef 指示詞。

使用/D 編譯器選項定義常數的效果，與在檔案開頭使用[ \# define](dx-graphics-hlsl-appendix-pre-define.md)指示詞的效果相同。 最多可以使用/D 選項來定義30個常數。 如需如何使用此方法的範例，請參閱[ \# ifdef 和 ) ](dx-graphics-hlsl-appendix-pre-ifdef.md)的範例一節。

## <a name="examples"></a>範例

下列範例會將識別碼寬度定義為整數常數80，然後根據寬度和整數常數10定義長度。


```
#define WIDTH       80
#define LENGTH      ( WIDTH + 10 )
```



每個後續的長度實例都會取代為 (寬度 + 10) ，而寬度 + 10 的每個後續實例則會由運算式 (80 + 10) 取代。 寬度 + 10 左右的括弧很重要，因為它們控制語句中的解讀，如下所示。


```
var = LENGTH * 20;
```



在前置處理階段之後，語句會變成下列結果，其評估結果為1800。


```
var = ( 80 + 10 ) * 20;
```



如果沒有括弧，結果會是下列結果，其會評估為280。


```
var = 80 + 10 * 20;
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (DirectX HLSL) 的預處理器指示詞 ](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#定義多載](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[\# (DirectX HLSL) 的 undef 指示詞 ](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 





