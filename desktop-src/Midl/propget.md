---
title: propget 屬性
description: '\ Propget \ 屬性會指定屬性存取子函數。 屬性的名稱必須與函數相同。'
ms.assetid: 0b76ece3-e19b-4c80-883c-ff414bc2e435
keywords:
- propget 屬性 MIDL
topic_type:
- apiref
api_name:
- propget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aaa55521042adc07f4242a44060e2442f087e609d0e3995d8c77457c8653c66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383333"
---
# <a name="propget-attribute"></a>propget 屬性

**\[ Propget \]** 屬性會指定屬性存取子函數。 屬性的名稱必須與函數相同。

``` syntax
[propget [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a>參數

<dl> <dt>

*選用屬性-屬性* 
</dt> <dd>

零或多個屬性屬性。

</dd> <dt>

*傳回類型* 
</dt> <dd>

遠端程式所傳回的資料類型。

</dd> <dt>

*函數名稱* 
</dt> <dd>

遠端程式的名稱。

</dd> <dt>

*parameters* 
</dt> <dd>

遠端程式的零或多個參數。

</dd> </dl>

## <a name="remarks"></a>備註

具有 propget 屬性（attribute）的函式也應該具有 **\[** [**out**](out-idl.md) **\]** 和 **\[** [**retval**](retval.md)屬性（property）做為指標類型的最後一個參數 **\]** 。 如果最後一個參數沒有 \[ out、retval \] 屬性，則會將函式的傳回值視為 \[ out、retval \] 參數。 例如，具有原型的函式

``` syntax
[propget] short MyFunction([in] long aLongValue);
```

被視為

``` syntax
[propget] HRESULT MyFunction([in] long aLongValue, [out,retval] short *outValue);
```

最多可以為函式指定 **\[ \] propget**、 **\[** [**propput**](propput.md) **\]** 和 **\[** [**propputref**](propputref.md)其中一個 **\]** 。

如果 lcid 屬性用於函式的參數清單中，而該函式 **\[** [](lcid.md) **\]** 包含具有 **\[** [**propput**](propput.md) **\]** 屬性的參數，則 **\[ lcid \]** 參數必須是最後一個的第二個。

### <a name="flags"></a>Flags

叫用 \_ PROPERTYGET

## <a name="examples"></a>範例

``` syntax
interface MyInterface : IDispatch                         
{                
    [propget, 
     helpstring("A meaningful comment.")] HRESULT Method1(
         [out, retval] int* ReturnVal); 

    [propput, 
     helpstring("Another meaningful comment.")] HRESULT Method1(
         [in] int Value);
        
    [propget, 
     helpstring("A meaningful comment."), id(1)] HRESULT Method2(
         [out, retval] YourInterface** ReturnVal); 

    [propputref, 
     helpstring("Another meaningful comment."), 
     id(1)] HRESULT Method2([in] YourPoint* Point);
}                 
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**retval**](retval.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 