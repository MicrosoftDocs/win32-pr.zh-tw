---
title: " line 指示詞"
description: 預處理器指示詞，可將編譯器內部儲存的行號和檔案名設定為指定的值。
ms.assetid: 307410af-bd78-4b3d-b515-adf58298f35f
keywords:
- line 指示詞 HLSL
topic_type:
- apiref
api_name:
- line Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0932138ce5aec85ad3d3e7058db0c2a93e131181
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373032"
---
# <a name="line-directive"></a>\#line 指示詞

預處理器指示詞，可將編譯器內部儲存的行號和檔案名設定為指定的值。



| \#line *lineNumber* "*filename*" |
|----------------------------------|



 

## <a name="parameters"></a>參數



| 項目                                                                                                                              | 描述                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="lineNumber"></span><span id="linenumber"></span><span id="LINENUMBER"></span>*lineNumber*<br/>                    | 要設定的行號。 這可以是任何整數常數。 只要結果評估為正確的語法，就可以在前置處理標記上執行宏取代。 <br/>                     |
| <span id="filename__optional__________"></span><span id="FILENAME__OPTIONAL__________"></span>*檔案名* \[選\] <br/> | 要設定的檔案名。 檔案名可以是任意的字元組合，且必須用雙引號括住 ( "" ) 。 如果省略此參數，則先前的檔案名會維持不變。 <br/> |



 

## <a name="remarks"></a>備註

編譯器會使用行號和檔案名來參考它在編譯期間找到的錯誤。 行號通常參考目前的輸入行，檔名則參考目前的輸入檔。 每次一行程式碼處理後，行號會遞增。 如果您變更行號和檔名，編譯器會忽略先前的值並以新的值繼續處理。 \#程式產生器通常會使用 line 指示詞，使錯誤訊息參考原始來源檔案，而非產生的程式。

翻譯工具會使用行號和檔案名來決定預先定義之宏檔案 \_ \_ \_ \_ 和 \_ \_ 行 \_ \_ 的值。 您可以使用這些巨集，將自述性的錯誤訊息插入程式文字中。 檔案 \_ \_ \_ \_ 宏會展開為字串，其內容是檔案名，以雙引號括住 ( "" ) 。

## <a name="examples"></a>範例

下列範例會將行號設定為151，並將檔案名設定為 "copy. c"。


```
#line 151 "copy.c"
```



在下列範例中， \_ \_ \_ \_ \_ \_ \_ \_ 如果指定的判斷提示不是 true，則宏判斷提示會使用預先定義的宏行和檔案來列印來源檔案的相關錯誤訊息。


```
#define ASSERT(cond)

if( !(cond) )\
{printf( "assertion error line %d, file(%s)\n", \
__LINE__, __FILE__ );}
```



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ (DirectX HLSL) 的預處理器指示詞 ](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





