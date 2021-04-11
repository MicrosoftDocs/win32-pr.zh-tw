---
title: wchar_t 屬性
description: Wchar \_ t 關鍵字會指定寬字元類型。
ms.assetid: e21b2587-909a-4e2b-8c6d-6cc570bf509f
keywords:
- wchar_t 屬性 MIDL
topic_type:
- apiref
api_name:
- wchar_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0be9af276a8f87fe5ee7a4dfeb499b864de92f4
ms.sourcegitcommit: 686cb805bed0e89573fc68d145809f50c6b0e6d5
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2020
ms.locfileid: "104023134"
---
# <a name="wchar_t-attribute"></a>wchar \_ t 屬性

**Wchar \_ t** 關鍵字會指定寬字元類型。

``` syntax
wchar_t identifier-name;
```

## <a name="parameters"></a>參數

<dl> <dt>

*識別碼-名稱* 
</dt> <dd>

指定有效的 MIDL 識別碼。 有效的 MIDL 識別碼最多包含31個英數位元和/或底線字元，而且開頭必須是字母或底線字元。

</dd> </dl>

## <a name="remarks"></a>備註

**Wchar \_ t 型別** 是由 MIDL 定義為不 [**帶正負**](unsigned.md)號的 [**短**](short.md) (16 位) 資料物件。

MIDL 編譯器允許重新定義 **wchar \_ t**，但只有在它與先前的定義一致時才允許。

寬字元類型是其中一種預先定義的 MIDL 類型。 寬字元類型可顯示為 [**const**](const.md) 宣告、 [**typedef**](typedef.md) 宣告、一般宣告和函式宣告子中的類型指定名稱， (為函式傳回型別規範，以及) 的參數類型規範。 如需類型規範出現的內容，請參閱 [ (IDL) 檔案的介面定義](interface-definition-idl-file.md)。

**\[ 字串 \]** 屬性可以套用至 **wchar \_ t** 類型的指標或陣列。

在字元或字串常數之前使用 **L** 字元，以指定寬字元類型常數。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[MIDL 基底類型](midl-base-types.md)
</dt> <dt>

[**字元**](char-idl.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**著**](typedef.md)
</dt> <dt>

[**符號**](unsigned.md)
</dt> </dl>

 

 




