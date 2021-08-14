---
title: byte 屬性
description: Byte 關鍵字會指定8位的資料項目。
ms.assetid: d6401e05-5498-4d66-8f70-2c794ed26527
keywords:
- byte 屬性 MIDL
topic_type:
- apiref
api_name:
- byte
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a271cc81fe97fb25850bfe4dcb7d2edb55ba3c69805dab17d013bc646768e87f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384720"
---
# <a name="byte-attribute"></a>byte 屬性

**Byte** 關鍵字會指定8位的資料項目。

``` syntax
byte identifier-name;
```

## <a name="parameters"></a>參數

<dl> <dt>

*識別碼-名稱* 
</dt> <dd>

指定有效的 MIDL 識別碼。 有效的 MIDL 識別碼最多包含31個英數位元和/或底線字元，而且開頭必須是字母或底線字元。

</dd> </dl>

## <a name="remarks"></a>備註

**位元組** 資料項目不會在網路上進行傳輸，因為可能會有 [**char**](char-idl.md)類型的轉換。

**位元組** 類型是介面定義語言 (IDL) 的其中一種基底類型。 **Byte** 類型可以做為 [**常數**](const.md)宣告、 [**typedef**](typedef.md)宣告、一般宣告和函式宣告子中的類型指定名稱， (為函式傳回型別規範，以及) 的參數類型規範。 如需類型規範出現的內容，請參閱 [ (IDL) 檔案的介面定義](interface-definition-idl-file.md)。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[MIDL 基底類型](midl-base-types.md)
</dt> <dt>

[**char**](char-idl.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**著**](typedef.md)
</dt> </dl>

 

 




