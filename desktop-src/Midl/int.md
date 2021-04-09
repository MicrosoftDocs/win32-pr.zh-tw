---
title: int 屬性
description: 關鍵字 int 指定32位平臺上的32位帶正負號的整數。 在16位平臺上，關鍵字 int 是選擇性的關鍵字，可伴隨關鍵字 small、short 和 long。
ms.assetid: ad6ce0ff-e87b-4701-b9d2-a69c34e0339b
keywords:
- int 屬性 MIDL
topic_type:
- apiref
api_name:
- int
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f916c4f03023c756b71a2e3cbb38acd9f41f1e8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678243"
---
# <a name="int-attribute"></a>int 屬性

關鍵字 **int** 指定32位平臺上的32位帶正負號的整數。 在16位平臺上，關鍵字 **int** 是選擇性的關鍵字，可伴隨關鍵字 [**small**](small.md)、 [**short**](short.md)和 [**long**](long.md)。

``` syntax
[ signed | unsigned ] integer-modifier [ int ] declarator-list;
```

## <a name="parameters"></a>參數

<dl> <dt>

*整數修飾詞* 
</dt> <dd>

指定關鍵字 [**small**](small.md)、 [**short**](short.md)、 [**long**](long.md)、[**超**](hyper.md)、 [**\_ \_ int3264**](--int3264.md)或 [**\_ \_ int64**](--int64.md)，以選取整數資料的大小。 在16位平臺上，大小限定詞必須存在。

</dd> <dt>

*宣告子清單* 
</dt> <dd>

指定一或多個標準 C 宣告子，例如識別碼、指標宣告子和陣列宣告子。 在遠端程序呼叫中傳輸的結構中，不允許 (函式宣告子和位欄位宣告。 未傳輸的結構中允許這些宣告子。 ) 以逗號分隔多個宣告子。

</dd> </dl>

## <a name="remarks"></a>備註

整數類型是介面定義語言 (IDL) 的基底類型。 它們可以在 [**typedef**](typedef.md) 宣告、一般宣告和函式宣告子中顯示為類型指定名稱， (為函式傳回型別規範，以及) 的參數類型規範。 如需類型規範出現的內容，請參閱 [ (IDL) 檔案的介面定義](interface-definition-idl-file.md)。

如果未提供整數符號規格，則整數類型會預設為 [**已簽署**](signed.md)。

DCE IDL 編譯器不允許關鍵字 [**簽署**](signed.md) 來指定整數類型的正負號。 因此，當您使用 MIDL 編譯器 [**/osf**](-osf.md) 參數時，就無法使用這項功能。

如果可以避免，Microsoft 不建議使用 \_ \_ int3264 進行遠端處理。 如需有關其使用方式和限制的詳細資訊，請參閱 [**\_ \_ int3264**](--int3264.md)的主題。

## <a name="examples"></a>範例

``` syntax
signed short int i = 0; 
int j = i; 
typedef struct 
{ 
    small int         i1; 
    short             i2; 
    unsigned long int i3; 
} INTSIZETYPE; 
 
HRESULT MyFunc([in] long int lCount);
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[MIDL 基底類型](midl-base-types.md)
</dt> <dt>

[**枚舉**](enum.md)
</dt> <dt>

[**超**](hyper.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**signed**](signed.md)
</dt> <dt>

[**小**](small.md)
</dt> <dt>

[**結構**](struct.md)
</dt> <dt>

[**著**](typedef.md)
</dt> <dt>

[**聯盟**](union.md)
</dt> </dl>

 

 




