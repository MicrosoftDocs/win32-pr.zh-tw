---
title: optional 屬性
description: '\ Optional \ 屬性指定成員函式的選擇性參數。'
ms.assetid: 683e5c9e-5b25-4beb-99ce-cfae4fee4ea6
keywords:
- 選擇性屬性 MIDL
topic_type:
- apiref
api_name:
- optional
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b446cf2a7a14e5909d2c99d41fd918147d23c6f1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842263"
---
# <a name="optional-attribute"></a>optional 屬性

**\[ 選擇性 \]** 屬性會指定成員函式的選擇性參數。

``` syntax
return-type function-name([optional [, other-attributes]] parameter-type parameter-name)
```

## <a name="parameters"></a>參數

<dl> <dt>

*傳回類型* 
</dt> <dd>

指定函式的傳回型別。

</dd> <dt>

*函數名稱* 
</dt> <dd>

指定 IDL 檔案中所定義的函式名稱。

</dd> <dt>

*其他屬性* 
</dt> <dd>

零或多個選擇性 MIDL 屬性。

</dd> <dt>

*參數類型* 
</dt> <dd>

選用參數的資料類型。

</dd> <dt>

*參數-名稱* 
</dt> <dd>

指定選擇性參數的名稱。

</dd> </dl>

## <a name="remarks"></a>備註

只有當參數的類型為 **variant** 或 **variant** 時， **\[ \] 選擇性** 的屬性才有效 \* 。

MIDL 編譯器接受下列參數排序 (從左至右) ：

1.  必要參數 (沒有 **\[** [**defaultvalue**](defaultvalue.md) **\]** 或 **\[ 選擇性 \]** 屬性的參數) ，
2.  具有或不具有 **\[** [**defaultvalue**](defaultvalue.md)屬性的選擇性參數 **\]** ，
3.  具有 **\[ 選擇性 \]** 屬性且不含 **\[** [**defaultvalue**](defaultvalue.md) **\]** 屬性的參數。
4.  **\[**[**lcid**](lcid.md) **\]** 參數（如果有的話）
5.  **\[**[**retval**](retval.md) **\]** 參數

您無法將 **\[ 選擇性 \]** 屬性套用至也有 **\[** [**lcid**](lcid.md) **\]** 或 **\[** [**retval**](retval.md) **\]** 屬性的參數。

## <a name="examples"></a>範例

``` syntax
HRESULT MyFunc([in, optional] VARIANT Param1, 
               [out, optional] VARIANT Param2)
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**值**](defaultvalue.md)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Lcid**](lcid.md)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**retval**](retval.md)
</dt> </dl>

 

 