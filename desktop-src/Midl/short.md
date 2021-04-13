---
title: short 屬性
description: Short 關鍵字會指定16位整數。
ms.assetid: 622464a3-0d79-421a-8742-8a3746fe1533
keywords:
- short 屬性 MIDL
topic_type:
- apiref
api_name:
- short
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b993c830c631b5b95246a7a191388ce897dbaafb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312741"
---
# <a name="short-attribute"></a>short 屬性

**Short** 關鍵字會指定16位整數。

``` syntax
[[ signed | unsigned ]] short [[ int ]] declarator-list;
```

## <a name="parameters"></a>參數

<dl> <dt>

*宣告子清單* 
</dt> <dd>

指定一或多個標準 C 宣告子，例如識別碼、指標宣告子和陣列宣告子。 在遠端程序呼叫中傳輸的結構中，不允許 (函式宣告子和位欄位宣告。 未傳輸的結構中允許這些宣告子。 ) 以逗號分隔多個宣告子。

</dd> </dl>

## <a name="remarks"></a>備註

**Short** 關鍵字的前面可以是關鍵字 [**帶正負**](signed.md)號或不 [**帶正負**](unsigned.md)號的關鍵字。 [**Int**](int.md)關鍵字是選擇性的，可以省略。 對 MIDL 編譯器而言，預設會簽署簡短的整數，並以帶正負號的 **short** 整數為同義。

**Short** 整數類型是 IDL 語言的其中一種基底類型。 **Short** 整數型別可以在 [**const**](const.md)宣告、 [**typedef**](typedef.md)宣告、一般宣告和函式宣告子中顯示為類型指定名稱， (為函式傳回型別規範，以及) 的參數類型規範。 如需類型規範出現的內容，請參閱 [ (IDL) 檔案的介面定義](interface-definition-idl-file.md)。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[MIDL 基底類型](midl-base-types.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**int**](int.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**signed**](signed.md)
</dt> <dt>

[**小**](small.md)
</dt> <dt>

[**符號**](unsigned.md)
</dt> </dl>

 

 




