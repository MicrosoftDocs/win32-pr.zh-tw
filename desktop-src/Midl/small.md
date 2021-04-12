---
title: small 屬性
description: Small 關鍵字會指定8位的整數。
ms.assetid: 368e8836-1baa-4547-a62b-f34ac38bbdb2
keywords:
- small 屬性 MIDL
topic_type:
- apiref
api_name:
- small
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a0f106f1be1ba6d0acabf877b5dbefab3eaff6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104372883"
---
# <a name="small-attribute"></a>small 屬性

**Small** 關鍵字會指定8位的整數。

``` syntax
small identifier-name;
```

## <a name="parameters"></a>參數

<dl> <dt>

*識別碼-名稱* 
</dt> <dd>

指定有效的 MIDL 識別碼。 有效的 MIDL 識別碼最多包含31個英數位元和/或底線字元，而且開頭必須是字母或底線字元。

</dd> </dl>

## <a name="remarks"></a>備註

**Small** 關鍵字的前面可以是關鍵字 [**帶正負**](signed.md)號或不 [**帶正負**](unsigned.md)號的關鍵字。 [**Int**](int.md)關鍵字是選擇性的，可以省略。 對 MIDL 編譯器而言，預設會 **簽署** 一個小整數，而且與 **帶正負** 號的小整數同義。

**小** 整數類型是 IDL 語言的其中一種基底類型。 **小** 整數類型可顯示為 [**const**](const.md)宣告、 [**typedef**](typedef.md)宣告、一般宣告和函式宣告子中的類型指定名稱， (為函式傳回型別規範和) 的參數類型規範。 如需類型規範出現的內容，請參閱 [ (IDL) 檔案的介面定義](interface-definition-idl-file.md)。

您可以使用 MIDL 編譯器參數 [**/char**](-char.md)來修改 **small** 型別的正負號。 若要避免混淆，請使用 [**已簽署**](signed.md) 和 [**未簽署**](unsigned.md)的關鍵字來指定整數類型的正負號。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**/char**](-char.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**int**](int.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**signed**](signed.md)
</dt> <dt>

[**符號**](unsigned.md)
</dt> <dt>

[**著**](typedef.md)
</dt> </dl>

 

 




