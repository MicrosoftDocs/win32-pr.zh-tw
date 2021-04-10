---
title: char 屬性
description: Char 關鍵字會指定8位的資料項目。
ms.assetid: 3c9ba8bb-5aea-4166-acf6-b251377e5384
keywords:
- char 屬性 MIDL
topic_type:
- apiref
api_name:
- char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eab719f6f8ea6e21ccc5b389b12a66b617d5773
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841476"
---
# <a name="char-attribute"></a>char 屬性

**Char** 關鍵字會指定8位的資料項目。

``` syntax
char identifier-name;
```

## <a name="parameters"></a>參數

<dl> <dt>

*識別碼-名稱* 
</dt> <dd>

指定有效的 MIDL 識別碼。 有效的 MIDL 識別碼最多包含31個英數位元和/或底線字元，而且開頭必須是字母或底線字元。

</dd> </dl>

## <a name="remarks"></a>備註

關鍵字 **char** 可識別具有8個位的資料項目。 對 MIDL 編譯器而言， **char** 預設為不帶正負號，並與不帶 [**正負**](unsigned.md)號的 **char** 同義。

在這個版本的 Microsoft RPC 中，ASCII 和 EBCDIC 之間的轉換字元轉譯表內建于執行時間程式庫中，使用者無法變更。

**Char** 類型是介面定義語言 (IDL) 的其中一種基底類型。 **Char** 類型可以做為 [**常數**](const.md)宣告、 [**typedef**](typedef.md)宣告、一般宣告和函式宣告子中的類型指定名稱， (為函式傳回型別規範和) 的參數類型規範。 如需類型規範出現的內容，請參閱 [ (IDL) 檔案的介面定義](interface-definition-idl-file.md)。

DCE IDL 編譯器不接受套用至 **char** 類型的關鍵字 [**簽署**](signed.md)。 因此，當您使用 MIDL 編譯器 [**/osf**](-osf.md) 參數時，就無法使用這項功能。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[MIDL 基底類型](midl-base-types.md)
</dt> <dt>

[**位元組**](byte.md)
</dt> <dt>

[**/char**](-char.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**signed**](signed.md)
</dt> <dt>

[**字串**](string.md)
</dt> <dt>

[**著**](typedef.md)
</dt> <dt>

[**符號**](unsigned.md)
</dt> <dt>

[**wchar \_ t**](wchar-t.md)
</dt> </dl>

 

 




