---
title: propput 屬性
description: '\ Propput \ 屬性指定屬性設定函數。 屬性的名稱必須與函數相同。'
ms.assetid: ffd8af15-42a4-4852-a29b-1fc66f673978
keywords:
- propput 屬性 MIDL
topic_type:
- apiref
api_name:
- propput
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79bf5520a3f4f4872801145064f49a8108cf602a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092662"
---
# <a name="propput-attribute"></a>propput 屬性

**\[ Propput \]** 屬性會指定屬性設定函數。 屬性的名稱必須與函數相同 *。*

``` syntax
[propput [,optional-property-attributes]] return-type function-name( parameters);
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

具有 **\[ propput \]** 屬性的函式也必須具有（其最後一個參數）具有 **\[** [**in**](in.md) **\]** 屬性的參數。

最多可以為函式 **\[** 指定 [**propget**](propget.md) **\]** 、 **\[ \] propput** 和 **\[** [**propputref**](propputref.md) **\]** 其中一個。

如果 lcid 屬性用於函式的參數清單中，而該函式 **\[** [](lcid.md) **\]** 包含具有 **\[ propput \]** 屬性的參數，則 **\[ lcid \]** 參數必須是最後一個的第二個。

### <a name="flags"></a>Flags

叫用 \_ PROPERTYPUT

## <a name="examples"></a>範例

``` syntax
interface InMyFace : IDispatch                         
{
    [propget, 
     helpstring("A meaningful comment.")] HRESULT Method1(
         [out, retval] int* ReturnVal); 

    [propput, 
     helpstring("Another meaningful comment.")] HRESULT Method1(
         [in] int Value);
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[MIDL 與 MKTYPLIB.EXE 之間的差異](differences-between-midl-and-mktyplib.md)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 