---
title: defaultvalue 屬性
description: '\ Defaultvalue \ 屬性可讓您指定具類型選擇性參數的預設值。'
ms.assetid: a974a0f7-7b08-4f17-bb28-0e23e6aa97db
keywords:
- defaultvalue 屬性 MIDL
topic_type:
- apiref
api_name:
- defaultvalue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f38fe7dfc99c5c9c1c6a7cae1a5fdd5750c5f3e9af37e56706b27300876da1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067348"
---
# <a name="defaultvalue-attribute"></a>defaultvalue 屬性

**\[ Defaultvalue \]** 屬性可讓您指定具類型選擇性參數的預設值。

``` syntax
interface interface-name
{
  return-type function-name(
        mandatory-param-list, 
        [[attribute-list,] defaultvalue(value)] param-type param-name
        [ , optional-param-list]);
}
```

## <a name="parameters"></a>參數

<dl> <dt>

*介面-名稱* 
</dt> <dd>

指定介面的名稱。

</dd> <dt>

*傳回類型* 
</dt> <dd>

指定函式的傳回型別。

</dd> <dt>

*函數名稱* 
</dt> <dd>

指定將套用 **\[ defaultvalue \]** 屬性的函數名稱。

</dd> <dt>

*強制-param 清單* 
</dt> <dd>

指定一或多個必要參數。

</dd> <dt>

*屬性清單* 
</dt> <dd>

指定適用于參數的一或多個屬性清單（以逗號分隔）。

</dd> <dt>

*param 類型* 
</dt> <dd>

指出選用參數的類型。

</dd> <dt>

*參數名稱* 
</dt> <dd>

指定選擇性參數的名稱。

</dd> <dt>

*選用-param 清單* 
</dt> <dd>

指定零個或多個額外的參數，每個參數都必須有預設值。

</dd> </dl>

## <a name="remarks"></a>備註

您為參數指定的預設值可以是任何常數，也可以是解析成常數的運算式（可由 **VARIANT** 表示）。 具體而言，您無法將 **\[ defaultvalue \]** 屬性套用至屬於結構、陣列或 **SAFEARRAY** 類型的參數。

MIDL 編譯器接受下列參數排序 (從左至右) ：

1.  必要參數 (沒有 **\[ \] defaultvalue** 或 **\[** [**選擇性**](optional.md) **\]** 屬性的參數) ，
2.  具有或不具有 **\[ defaultvalue \]** 屬性的選擇性參數，
3.  具有 **\[ 選擇性 \]** 屬性且不含 **\[ defaultvalue \]** 屬性的參數。
4.  **\[**[**lcid**](lcid.md) **\]** 參數（如果有的話）
5.  **\[**[**retval**](retval.md) **\]** 參數

## <a name="examples"></a>範例

``` syntax
interface IFace : IUnknown
{
    HRESULT Ex1([defaultvalue(44)] LONG i);
    HRESULT Ex2([defaultvalue(44)] SHORT i);
...
};

interface QueryDef : IUnknown
{
    HRESULT OpenRecordset( [in, defaultvalue(DBOPENTABLE)]
    LONG Type,
    [out,retval] Recordset **pprst);
}
//  Type is now known to be a LONG type (good for browser in VBA and
//  good for a C/C++ programmer) and has a default value of
//  DBOPENTABLE
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**介面**](interface.md)
</dt> <dt>

[**Lcid**](lcid.md)
</dt> <dt>

[**選**](optional.md)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**retval**](retval.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 