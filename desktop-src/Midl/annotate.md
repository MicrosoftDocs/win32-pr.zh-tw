---
title: 標注屬性
description: '\ 批註 \ 屬性可讓您為指定的方法、參數或結構欄位指定 SAL 批註字串。'
ms.assetid: D0A35DCD-BD2F-455B-A040-5D63E4572D83
keywords:
- 標注屬性 MIDL
topic_type:
- apiref
api_name:
- annotate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 820310c6aca0e5269d6febff5dc7d3208413110c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "103683554"
---
# <a name="annotate-attribute"></a>標注屬性

**\[ 批註 \]** 屬性可讓您為指定的方法、參數或結構欄位指定 SAL 批註字串。

``` syntax
[ annotation(â€œstringâ€0,  [, function-attribute-list] ] function-declarator ;
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ annotation(â€œstringâ€) [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...);
```

## <a name="parameters"></a>參數

<dl> <dt>

*string* 
</dt> <dd>

指定的 SAL 批註字串。

</dd> <dt>

*函數-屬性清單* 
</dt> <dd>

指定套用至函數的零或多個屬性。 有效的函式屬性包括 [**\[ \] 回呼**](callback.md)、指標屬性 [**\[ \] ref**](ref.md)、 [**\[ unique \]**](unique.md)或 [**\[ ptr \]**](ptr.md)，以及使用方式屬性 [**\[ 字串 \]**](string.md)、 [**\[ 忽略 \]**](ignore.md)和 [**\[ 內容 \_ 控制碼 \]**](context-handle.md)。 多個屬性必須以逗號分隔。

</dd> <dt>

*函式宣告子* 
</dt> <dd>

指定函數的型別規範、函式名稱和參數清單。

</dd> <dt>

*類型規範* 
</dt> <dd>

指定 **基底 \_ 類型**、 [**\[ 結構 \]**](struct.md)、[**等**](union.md)位或 [**\[ 列舉 \]**](enum.md)類型或類型識別碼。 選擇性的儲存規格可以在 *類型* 規範之前。

</dd> <dt>

*指標宣告子* 
</dt> <dd>

指定零個或多個指標宣告子。 指標宣告子與 C 中使用的指標宣告子相同：它是由指示項 \* 、最 **遠** 的修飾詞和限定詞 [**\[ const \]**](const.md)所構成。

</dd> <dt>

*函數名稱* 
</dt> <dd>

指定遠端程式的名稱。

</dd> <dt>

*參數屬性清單* 
</dt> <dd>

指定適用于參數類型的零或多個屬性。 具有 [**\[ \] in**](in.md)屬性的參數屬性也可以取得 [**\[ \] 方向屬性**](out-idl.md) [**\[ \]**](string.md) [**\[ \_ \]**](length-is.md) [**\[ \]**](unique.md) [**\[ \]**](ptr.md) [**\[ \_ \]**](last-is.md) [**\[ \]**](ref.md) [**\[ \_ ，第 \] 一個**](first-is.md)欄位屬性 [**\[ \_ 是、last、length、max、size、size、以及 switch type、指標屬性 ref、unique 或 ptr; 以及 usage 屬性內容控制碼和字串。 \]**](max-is.md) [**\[ \_ \]**](switch-type.md) [**\[ \_ \]**](context-handle.md) [**\[ \_ \]**](size-is.md) Usage 屬性 [**\[ ignore \]**](ignore.md)不能用來做為參數屬性。 多個屬性必須以逗號分隔。

</dd> <dt>

*符中* 
</dt> <dd>

指定標準的 C 宣告子，例如識別碼、指標宣告子，以及陣列宣告子。 如需詳細資訊，請參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md) [**\[ \] 、陣列、陣列和**](../rpc/arrays.md)[指標](/windows/desktop/Rpc/arrays-and-pointers)。 函式宣告子中的參數宣告子（例如參數名稱）是選擇性的。

</dd> </dl>

## <a name="remarks"></a>備註

**\[ 批註 \]** 屬性允許覆寫 midl 產生的 SAL 注釋，或將它們加入至 midl 未明確產生注釋的位置。 如果未在命令列上指定 [**/sal**](-sal.md) ，則會忽略這個屬性。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/sal**](-sal.md)
</dt> <dt>

[**/sal \_ 本機**](-sal-local.md)
</dt> </dl>

 

 