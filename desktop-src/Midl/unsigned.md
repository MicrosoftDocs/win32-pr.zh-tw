---
title: 未簽署的屬性
description: 不帶正負號的關鍵字表示整數變數中最重要的位代表資料位，而不是帶正負號的位。
ms.assetid: bfcc6bec-895e-45e1-b162-b79651662aa6
keywords:
- 不帶正負號的屬性 MIDL
topic_type:
- apiref
api_name:
- unsigned
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 383a8fc0379ca81abb9ad0a88edab8750661bdfa429e32e7e91d193aa0fd2938
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146171"
---
# <a name="unsigned-attribute"></a>未簽署的屬性

不 **帶正負** 號的關鍵字表示整數變數中最重要的位代表資料位，而不是帶正負號的位。

``` syntax
[[ unsigned ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a>參數

<dl> <dt>

*type-qualifier* 
</dt> <dd>

可以是 [**char**](char-idl.md)、 [**wchar \_ t**](wchar-t.md)、 [**long**](long.md)、 [**int**](int.md)、 [**short**](short.md)和 [**small**](small.md)的任何一個。

</dd> <dt>

*識別碼-名稱* 
</dt> <dd>

指定有效的 MIDL 識別碼。 有效的 MIDL 識別碼最多包含31個英數位元和/或底線字元，而且開頭必須是字母或底線字元。

</dd> </dl>

## <a name="remarks"></a>備註

這個關鍵字是選擇性的，可以搭配任何字元和整數類型 [**char**](char-idl.md)、 [**wchar \_ t**](wchar-t.md)、 [**long**](long.md)、 [**short**](short.md)和 [**small**](small.md)使用。 您可以選擇性地在類型限定詞之後包含關鍵字 [**int**](int.md) ， **long**、 **short** 和 **small**。

當您使用 MIDL 編譯器參數 [**/char**](-char.md)時，會在產生的標頭檔中，以 [**帶正負**](signed.md)**號或不帶正負號** 的關鍵字來顯示出現在 IDL 檔案中的字元和整數類型。 為了避免混淆，請指定整數和字元類型的正負號。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[MIDL 基底類型](midl-base-types.md)
</dt> <dt>

[**char**](char-idl.md)
</dt> <dt>

[**/char**](-char.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**int**](int.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**簽署**](signed.md)
</dt> <dt>

[**小**](small.md)
</dt> <dt>

[**wchar \_ t**](wchar-t.md)
</dt> </dl>

 

 




