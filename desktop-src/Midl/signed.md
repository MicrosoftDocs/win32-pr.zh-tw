---
title: 已簽署屬性
description: 帶正負號的關鍵字表示整數變數中最重要的位代表正負號位，而不是資料位。
ms.assetid: 6116089a-647e-485b-8f79-9c9267aa4810
keywords:
- 簽署的屬性 MIDL
topic_type:
- apiref
api_name:
- signed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 500b87c849f31082a036d605db0947650e914bed
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103840968"
---
# <a name="signed-attribute"></a>已簽署屬性

**帶正負** 號的關鍵字表示整數變數中最重要的位代表正負號位，而不是資料位。

``` syntax
[[ signed ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a>參數

<dl> <dt>

*type-qualifier* 
</dt> <dd>

可以是 [**char**](char-idl.md)、 [**wchar \_ t**](wchar-t.md)、 [**long**](long.md)、 [**short**](short.md)和 [**small**](small.md)的任何一個。

</dd> <dt>

*識別碼-名稱* 
</dt> <dd>

指定有效的 MIDL 識別碼。 有效的 MIDL 識別碼最多包含31個英數位元和/或底線字元，而且開頭必須是字母或底線字元。

</dd> </dl>

## <a name="remarks"></a>備註

這個關鍵字是選擇性的，可以搭配任何字元和整數類型 [**char**](char-idl.md)、 [**wchar \_ t**](wchar-t.md)、 [**long**](long.md)、 [**short**](short.md)和 [**small**](small.md)使用。 您可以選擇性地在類型限定詞之後包含關鍵字 [**int**](int.md) ， **long**、 **short** 和 **small**。

當您使用 MIDL 編譯器參數 [**char**](char-idl.md)時，在產生的標頭檔中，會以 **帶正負**[**號或不帶正負號**](unsigned.md)的關鍵字來顯示出現在 IDL 檔案中的字元和整數類型（不含明確的正負號關鍵字）。 為了避免混淆，請指定整數和字元類型的正負號。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[MIDL 基底類型](midl-base-types.md)
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

[**小**](small.md)
</dt> <dt>

[**符號**](unsigned.md)
</dt> <dt>

[**wchar \_ t**](wchar-t.md)
</dt> </dl>

 

 




