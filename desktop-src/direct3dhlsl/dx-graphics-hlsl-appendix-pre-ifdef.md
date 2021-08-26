---
title: " ifdef 和 ifndef 指示詞"
description: 判斷是否已定義特定預處理器常數或宏的預處理器指示詞。
ms.assetid: c1cc2e1d-2599-45ec-9629-56c4b42e0d0e
keywords:
- ifdef 和 ifndef 指示詞 HLSL
topic_type:
- apiref
api_name:
- ifdef and ifndef Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 584cde8856c48aeafed5665016a71146f8c2ffb341b837faa6bf35d627152c39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068318"
---
# <a name="ifdef-and-ifndef-directives"></a>\#ifdef 和 \# ifndef 指示詞

判斷是否已定義特定預處理器常數或宏的預處理器指示詞。



| \#ifdef *識別碼* .。。  |
|---------------------------|
| \#endif                   |
| \#ifndef *識別碼* .。。 |
| \#endif                   |



 

## <a name="parameters"></a>參數



| 項目                                                                              | 描述                                               |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*識別碼*<br/> | 要檢查之常數或宏的識別碼。 <br/> |



 

## <a name="remarks"></a>備註

您可以在 \# \# 可使用[ \# if](dx-graphics-hlsl-appendix-pre-if.md)的任何地方使用 ifdef 和 ifndef 指示詞。 \#Ifdef 語句相當於 ) 指示詞。 這些指示詞只會檢查使用[ \# define](dx-graphics-hlsl-appendix-pre-define.md)指示詞所定義的識別碼是否存在，而不會檢查 c 或 c + + 原始程式碼中宣告的識別碼。

提供這些指示詞的目的只是為了保留與舊版語言的相容性。 偏好使用 [已定義](dx-graphics-hlsl-appendix-pre-if.md) 的運算子搭配 if 指示詞 \# 。

Ifndef 指示詞會 \# 檢查由 ifdef 檢查的條件是否相反 \# 。 如果未定義識別碼，則條件為 true (非零) ;否則，條件為 false (零) 。

## <a name="examples"></a>範例

identifier 可以從命令列使用 /D 選項傳遞。 使用 /D 最多可以指定 30 個巨集。 這個選項在檢查定義是否存在時很實用，因為可以從命令列傳遞定義。 下列範例會使用此行為來判斷是否要在測試模式中執行應用程式。


```
// PROG.CPP
#ifndef test
  #define final
#endif
int main()
{
}
```



使用下列命令進行編譯時，會在測試模式中編譯進程 .cpp;否則，它會在最終模式中進行編譯。


```
CL.EXE /Dtest prog.cpp
```



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ (DirectX HLSL) 的預處理器指示詞 ](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#如果為，) ](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





