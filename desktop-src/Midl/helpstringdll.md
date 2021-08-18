---
title: helpstringdll 屬性
description: '\ Helpstringdll \ 屬性會設定用來執行檔字串查閱之 DLL 的名稱。'
ms.assetid: 1b9b962c-c355-4428-b5ea-dc7fd48b50a9
keywords:
- helpstringdll 屬性 MIDL
topic_type:
- apiref
api_name:
- helpstringdll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f773ed18e72f184305275ce238ddf0576c81447181a0b7fb420c30341935f5e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067248"
---
# <a name="helpstringdll-attribute"></a>helpstringdll 屬性

**\[ Helpstringdll \]** 屬性會設定用來執行檔字串查閱之 DLL 的名稱。

``` syntax
[
    helpstringdll(help-text-string)
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
};
```

## <a name="parameters"></a>參數

<dl> <dt>

*說明-文字字串* 
</dt> <dd>

以零結束的字元字串，指定 DLL 的完整檔案名。

</dd> <dt>

*選用-屬性-清單* 
</dt> <dd>

適用于整個程式庫語句的其他屬性。

</dd> <dt>

*程式庫名稱* 
</dt> <dd>

軟體元件將用來表示此連結 [**庫**](library.md)的識別碼。

</dd> <dt>

*程式庫定義語句* 
</dt> <dd>

定義連結 [**庫**](library.md)介面的一個或多個 MIDL 語句。

</dd> </dl>

## <a name="remarks"></a>備註

使用程式庫語句上的 **\[ helpstringdll \]** 屬性，將動態連結程式庫的完整檔案名指定為字元字串。 這可讓使用者使用物件檢視器來查看 DLL 的描述。

使用 **ITypeLib2** 和 **ITypeInfo2** 介面中的 **GetDocumentation2** 函式來取出說明字串。

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

 

 