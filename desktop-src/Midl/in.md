---
title: in 屬性
description: '\ In \ 屬性工作表示參數要從呼叫程式傳遞至呼叫的程式。'
ms.assetid: 85d5617e-8b73-449a-9627-2c8d5ab2b629
keywords:
- 在屬性 MIDL 中
topic_type:
- apiref
api_name:
- in
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb78ad08dd5ba5494181d3fb2adecb7a8441e4716c42ba6cd4f1c119b3ccb046
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067228"
---
# <a name="in-attribute"></a>in 屬性

**\[ In \]** 屬性工作表示要將參數從呼叫程式傳遞至被呼叫的進程。

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ in [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...);
```

## <a name="parameters"></a>參數

<dl> <dt>

*函數-屬性清單* 
</dt> <dd>

指定套用至函數的零或多個屬性。 有效的函式屬性為 **\[ 回呼 \]**、 **\[ local \]**、指標屬性 **\[ ref \]**、 **\[ unique \]** 或 **\[ ptr \]**，以及使用方式屬性 **\[ 字串 \]**、 **\[ 忽略 \]** 和 **\[ 內容 \_ 控制碼 \]**。

</dd> <dt>

*類型規範* 
</dt> <dd>

指定 **基底 \_ 類型**、 [**結構**](struct.md)、 [**等**](union.md)位或 [**列舉**](enum.md) 類型或類型識別碼。 選擇性的儲存規格可以在 *類型* 規範之前。

</dd> <dt>

*指標宣告子* 
</dt> <dd>

指定零個或多個指標宣告子。 指標宣告子與 C 中使用的指標宣告子相同：它是由指示項 \* 、最 **遠** 的修飾詞和限定詞 [**const**](const.md)所構成。

</dd> <dt>

*函數名稱* 
</dt> <dd>

指定遠端程式的名稱。

</dd> <dt>

*參數屬性清單* 
</dt> <dd>

指定適用于指定之參數類型的零或多個屬性。 具有 **\[ \] in** 屬性的參數屬性也可以取得 **\[ \] 方向屬性，** **\[ 第一個 \_ \]** **\[ \]** **\[ \]** **\[ \_ \]** 欄位屬性 **\[ \_ \]****是、 \[ \]** last、length、 **\[ max \_ 、size 是和 switch type、指標屬性 ref、unique 或 ptr，以及 usage 屬性內容控制碼和字串。 \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ \]** **\[ \]** Usage 屬性 **\[ ignore \]** 不能用來做為參數屬性。 以逗號分隔多個屬性。

</dd> <dt>

*符中* 
</dt> <dd>

指定標準的 C 宣告子，例如識別碼、指標宣告子，以及陣列宣告子。 如需詳細資訊，請參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md) [**、陣列、陣列和**](arrays-1.md)[指標](/windows/desktop/Rpc/arrays-and-pointers)。 函式宣告子中的參數宣告子（例如參數名稱）是選擇性的。

</dd> </dl>

## <a name="remarks"></a>備註

**\[ In \]** 屬性（attribute）具有反向屬性（attribute），表示要從呼叫的程式將 **\[** [](out-idl.md) **\]** 參數傳回給呼叫的進程。 **\[ In \]** 和 **\[ out \]** 屬性稱為方向性參數屬性，因為它們會指定傳遞參數的方向。 參數可以定義為 **\[ in \]**、 **\[ out \]** 或 **\[ in**、 **out \]**。

**\[ In \]** 屬性會識別由用戶端存根封送處理至伺服器的參數。

當未指定方向參數屬性時，預設會將 **\[ in \]** 屬性套用至參數。

## <a name="examples"></a>範例

``` syntax
HRESULT MyFunction([in] short count);
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**midl \_ 使用者 \_ 配置**](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[**out**](out-idl.md)
</dt> </dl>

 

 