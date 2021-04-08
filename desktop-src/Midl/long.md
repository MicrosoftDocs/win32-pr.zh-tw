---
title: long 屬性
description: Long 關鍵字會指定32位的整數。
ms.assetid: 5619e482-e3c3-4898-a70b-afd337d2749a
keywords:
- long 屬性 MIDL
topic_type:
- apiref
api_name:
- long
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ea9af3bfac85ff375f6d5433b4e9f3ed37d8f7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103932663"
---
# <a name="long-attribute"></a>long 屬性

**Long** 關鍵字會指定32位的整數。

``` syntax
[ signed | unsigned ] long [ int ] declarator-list;
```

## <a name="parameters"></a>參數

<dl> <dt>

*宣告子清單* 
</dt> <dd>

指定一或多個標準 C 宣告子，例如識別碼、指標宣告子和陣列宣告子。 在遠端程序呼叫中傳輸的結構中，不允許 (函式宣告子和位欄位宣告。 未傳輸的結構中允許這些宣告子。 ) 以逗號分隔多個宣告子。

</dd> </dl>

## <a name="remarks"></a>備註

**Long** 關鍵字的前面可以是關鍵字 [**帶正負**](signed.md)號或不 [**帶正負**](unsigned.md)號的關鍵字。 [**Int**](int.md)關鍵字是選擇性的，可以省略。 若為 MIDL 編譯器，則預設會簽署長整數，而且與帶正負號的 **long int** 同義。在32位平臺上， **long** 與 **int** 同義。

**長** 整數類型是 IDL 語言的其中一種基底類型。 **長** 整數類型可顯示為 [**const**](const.md)宣告、 [**typedef**](typedef.md)宣告、一般宣告和函式宣告子中的類型指定名稱， (為函式傳回型別規範，以及) 的參數類型規範。 如需類型規範出現的內容，請參閱 [ (IDL) 檔案的介面定義](interface-definition-idl-file.md)。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**const**](const.md)
</dt> <dt>

[MIDL 基底類型](midl-base-types.md)
</dt> <dt>

[**超**](hyper.md)
</dt> <dt>

[**int**](int.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**signed**](signed.md)
</dt> <dt>

[**小**](small.md)
</dt> <dt>

[**著**](typedef.md)
</dt> <dt>

[**符號**](unsigned.md)
</dt> </dl>

 

 




