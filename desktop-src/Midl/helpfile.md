---
title: helpfile 屬性
description: '\ 保護 \ 屬性會設定類型程式庫的說明檔名稱。 程式庫中的所有類型都會共用相同的說明檔。'
ms.assetid: caa248b1-a1a7-4c36-886a-079a66a01907
keywords:
- 説明的屬性 MIDL
topic_type:
- apiref
api_name:
- helpfile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1557d96f35913e5e1ed9b784bedfc430e6c4d77b65954583ca6923e4728af9a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384018"
---
# <a name="helpfile-attribute"></a>helpfile 屬性

[輔助檔] 屬性會設定類型程式庫的說明檔名稱。 **\[ \]** 程式庫中的所有類型都會共用相同的說明檔。

``` syntax
[
    uuid(uuid-number), 
    helpfile("filename") 
    [, optional-attribute-list]
] 
library 
{
    library statements
};
```

## <a name="parameters"></a>參數

<dl> <dt>

*uuid-數位* 
</dt> <dd>

指定 [**媒體**](library.md)櫃的通用唯一識別碼。

</dd> <dt>

*filename* 
</dt> <dd>

指定包含解說文字的檔案名。

</dd> <dt>

*選用-屬性-清單* 
</dt> <dd>

指定 MIDL 編譯器將套用至連結 [**庫**](library.md)的零或多個屬性。

</dd> <dt>

*程式庫語句* 
</dt> <dd>

指定定義程式庫介面的一或多個 MIDL 語句。

</dd> </dl>

## <a name="remarks"></a>備註

使用 **ITypeLib** 和 **ITypeInfo** 介面中的 **GetDocumentation** 函式來取出檔案名。

## <a name="examples"></a>範例

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpfile("filename.hlp"),
    lcid(0x0409), 
    version(2.0)
]
library Hello
{
    /* Library definition statements here. */
};
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**圖書館**](library.md)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 