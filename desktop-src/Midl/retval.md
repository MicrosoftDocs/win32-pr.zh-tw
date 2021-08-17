---
title: retval 屬性
description: '\ Retval \ 屬性會指定接收成員傳回值的參數。'
ms.assetid: 3a5f1469-7828-4c38-b58f-195a47b2a66f
keywords:
- retval 屬性 MIDL
topic_type:
- apiref
api_name:
- retval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72655883b24c83890cf2f5604cb8f7335c6943b32e5e69611dba415689b03e22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146301"
---
# <a name="retval-attribute"></a>retval 屬性

**\[ Retval \]** 屬性指定接收成員傳回值的參數。

``` syntax
return-type function-name(
    [out, retval [, optional-attributes]] data-type * param-name,
    ...);
```

## <a name="parameters"></a>參數

<dl> <dt>

*傳回類型* 
</dt> <dd>

遠端程式之傳回值的資料類型。

</dd> <dt>

*函數名稱* 
</dt> <dd>

用來叫用遠端程式的名稱。

</dd> <dt>

*選用-屬性* 
</dt> <dd>

零或多個 MIDL 屬性。

</dd> <dt>

*資料類型* 
</dt> <dd>

透過參數傳遞的資料型別。

</dd> <dt>

*參數名稱* 
</dt> <dd>

參數的識別碼名稱。

</dd> </dl>

## <a name="remarks"></a>備註

您可以在描述方法或取得屬性之介面成員的參數上使用 **\[ retval \]** 屬性。  (在具有 propget 屬性之方法的最後一個參數上需要屬性 **\[** [](propget.md) **\]** 。 ) 參數必須有 **\[** [**out**](out-idl.md) **\]** 屬性，而且必須是指標類型。

您無法將 **\[** [**選擇性**](optional.md) **\]** 屬性套用至 **\[ \] retval** 參數。

MIDL 編譯器接受下列參數排序 (從左至右) ：

1.  未 **\[**) [**defaultvalue**](defaultvalue.md) **\]** 或 **\[** [**選擇性**](optional.md) **\]** 屬性 (參數所需的參數。
2.  具有或不具有 **\[** [**defaultvalue**](defaultvalue.md)屬性的選擇性參數 **\]** 。
3.  具有 **\[** [**選擇性**](optional.md) **\]** 屬性且不含 **\[** [**defaultvalue**](defaultvalue.md) **\]** 屬性的參數。
4.  **\[**[**lcid**](lcid.md) **\]** 參數（如果有的話）。
5.  **\[ retval \]** 參數。

具有 **\[ retval \]** 屬性的參數不會顯示在使用者導向的瀏覽器中。

### <a name="flags"></a>Flags

IDLFLAG \_ FRETVAL

## <a name="examples"></a>範例

``` syntax
HRESULT MyMethod([out, retval] InMyFace** ReturnVal);
HRESULT MyOtherMethod([out, retval] VARIANT_BOOL* ReturnVal);
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

[**選**](optional.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 