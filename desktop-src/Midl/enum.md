---
title: enum 屬性
description: 關鍵字列舉可識別列舉型別。
ms.assetid: 1aaa3c36-17f7-42ff-8f4c-66133fcf4a1a
keywords:
- enum 屬性 MIDL
topic_type:
- apiref
api_name:
- enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681244c9d852c25d8e63ad389b03f16e6db8148c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312219"
---
# <a name="enum-attribute"></a>enum 屬性

關鍵字 **列舉** 可識別列舉型別。

``` syntax
enum [tag ] 
{ 
    identifier [=integer-value ] 
    [ , ... ] 
}
```

## <a name="parameters"></a>參數

<dl> <dt>

*標籤* 
</dt> <dd>

指定列舉類型的選擇性標記。

</dd> <dt>

*identifier* 
</dt> <dd>

指定特定列舉。

</dd> <dt>

*整數值* 
</dt> <dd>

指定常數整數值。

</dd> </dl>

## <a name="remarks"></a>備註

**列舉** 型別可以在 [**typedef**](typedef.md) 宣告、一般宣告和函式宣告子中顯示為類型指定名稱， (為函式傳回型別或) 的參數類型指定名稱。 如需類型規範出現的內容，請參閱 [ (IDL) 檔案的介面定義](interface-definition-idl-file.md)。

在 MIDL 編譯器的預設模式中，您可以將整數值指派給枚舉器。  (當您使用 [**/osf**](-osf.md) 參數進行編譯時，無法使用此功能。 ) 與 C 語言列舉值相同，列舉值名稱必須是唯一的，但是列舉值不需要。

未提供指派運算子時，識別碼會從左至右對應至連續的整數，從零開始。 當提供指派運算子時，指派的值會從最近指派的值開始。

識別碼的最大數目是65535。

**列舉** 類型的物件是 [**int**](int.md)類型，而其大小與系統相依。 根據預設，在透過網路 [**傳輸時，**](short.md) **列舉** 類型的物件會被視為不 [**帶正負**](unsigned.md)號的16位物件。 範圍 0-32767 以外的值會導致執行時間例外狀況 RPC \_ X \_ 列舉 \_ 值 \_ 超出 \_ \_ 範圍。 若要將物件傳輸為32位實體，請將 **\[** [**v1 \_ 列舉**](v1-enum.md) **\]** 屬性套用至 **列舉** typedef。

## <a name="examples"></a>範例

``` syntax
typedef enum {Monday=2, Tuesday, Wednesday, Thursday, Friday} workdays; 
 
typedef enum {Clemens=21, Palmer=22, Ryan=34} pitchers;
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**int**](int.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**著**](typedef.md)
</dt> <dt>

[**符號**](unsigned.md)
</dt> <dt>

[**v1 \_ 列舉**](v1-enum.md)
</dt> </dl>

 

 




