---
title: dual 屬性
description: 雙重屬性（attribute）會識別透過 IDispatch 公開屬性和方法的介面，以及直接透過 VTBL 來公開屬性和方法。
ms.assetid: 1c214f10-57eb-4a05-99a8-a09770666a74
keywords:
- 雙重屬性 MIDL
topic_type:
- apiref
api_name:
- dual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39a9e44de464f58fd1ffc0606551b9a0203ae9e9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933220"
---
# <a name="dual-attribute"></a>dual 屬性

**雙重** 屬性（attribute）會識別透過 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)公開屬性和方法的介面，以及直接透過 VTBL 來公開屬性和方法。

``` syntax
[
    uuid(uuid-number), 
    oleautomation,
    dual 
  [ , optional-attribute-list]
]
interface interface-name
{
    . . .
};
```

## <a name="parameters"></a>參數

<dl> <dt>

*uuid-數位* 
</dt> <dd>

指定介面的通用唯一識別碼

</dd> <dt>

*選用-屬性-清單* 
</dt> <dd>

指定零個或多個其他 MIDL 屬性的清單。

</dd> <dt>

*介面-名稱* 
</dt> <dd>

將套用 **雙重** 屬性之介面的名稱。

</dd> </dl>

## <a name="remarks"></a>備註

**雙重** 屬性所識別的介面必須與 Automation 相容，並且衍生自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)。 在分配介面上不允許此屬性。

**雙重** 屬性會建立同時為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面和元件物件模型 (COM) 介面的介面。 雙介面之 VTBL 的前七個專案是 **IDispatch** 的七個成員，而其餘專案則用於直接存取雙重介面的成員。 針對雙重介面成員指定的所有參數和傳回型別都必須是自動化相容的類型。

雙重介面的所有成員都必須傳遞 HRESULT 作為函數傳回值。 需要傳回其他值的成員（例如屬性存取子函數）應該將最後一個參數指定為 [**out**](out-idl.md)， [**retval**](retval.md)，表示傳回函數值的 output 參數。 此外，需要支援多個地區設定的成員應傳遞 [**lcid**](lcid.md) 參數。

雙重介面可提供直接的 VTBL 系結速度和 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 系結的彈性。 基於這個理由，建議您盡可能使用雙重介面。

> [!Note]  
> 如果您的應用程式藉由在介面呼叫內轉換 *this* 指標來存取物件資料，您應該針對自己的 vtbl 指標檢查物件中的 vtbl 指標，以確定您已連接到適當的 proxy。

 

在介面上指定 **雙重** 表示介面與 Automation 相容，因此會同時 \_ 設定 TYPEFLAG FDUAL 和 TYPEFLAG \_ FOLEAUTOMATION 旗標。

### <a name="flags"></a>Flags

TYPEFLAG \_ FDUAL、TYPEFLAG \_ FOLEAUTOMATION

## <a name="examples"></a>範例

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    oleautomation, dual
]
interface IHello : IDispatch
{
    //Diverse properties and methods defined here.
};
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**介面**](interface.md)
</dt> <dt>

[**Lcid**](lcid.md)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**擴展**](out-idl.md)
</dt> <dt>

[**retval**](retval.md)
</dt> </dl>

 

 