---
title: object 屬性
description: '\ Object \ 介面屬性會識別 COM 介面。'
ms.assetid: 51e34ef3-eea7-45f4-b961-a9f742700fe5
keywords:
- 物件屬性 MIDL
topic_type:
- apiref
api_name:
- object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ddf51e020cdcd5d13dde6938a58ea5e51f22d9dd03f8632312b3d6b8453a9ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383506"
---
# <a name="object-attribute"></a>object 屬性

**\[ 物件 \]** 介面屬性會識別 COM 介面。  (不包含 **\[ 物件 \]** 屬性的介面屬性清單，表示 DCE RPC 介面。 ) 

``` syntax
[ 
    object, 
    uuid(string-uuid)
    [ , interface-attribute-list] 
] 
interface interface-name : base-interface
{
...    
}
```

## <a name="parameters"></a>參數

<dl> <dt>

*字串-uuid* 
</dt> <dd>

Uuidgen.exe 公用程式所產生的 UUID 字串。 您可以用引號括住 UUID 字串。

</dd> <dt>

*介面屬性清單* 
</dt> <dd>

適用于整個介面的其他屬性。

</dd> <dt>

*介面-名稱* 
</dt> <dd>

介面的名稱。

</dd> <dt>

*基底介面* 
</dt> <dd>

從其中衍生這個介面的 COM 介面。 基底介面必須是 [**iunknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)、 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)或另一個直接或間接衍生自 **iunknown** 或 **idispatch** 的 COM 介面。

</dd> </dl>

## <a name="remarks"></a>備註

COM 介面的介面屬性清單必須包含 **\[** [**uuid**](uuid.md) **\]** 屬性，但它不能包含 **\[** [**version**](version.md) **\]** 屬性。

根據預設，使用 MIDL 編譯器編譯 COM 介面會產生建立 proxy DLL 所需的檔案。 此 DLL 包含的程式碼可支援用戶端應用程式和物件服務器使用自訂 COM 介面。 但是，如果 COM 介面的介面屬性清單指定 **\[** [**區域**](local.md) **\]** 屬性，MIDL 編譯器只會產生介面標頭檔。

MIDL 編譯器會自動產生 COM 介面的介面資料型別。 或者，您可以使用 [**typedef**](typedef.md) 搭配 [**interface**](interface.md) 關鍵字來明確定義介面資料類型。 然後，介面規格可以在函數參數和傳回值、 [**結構**](struct.md) 和等 [**位成員，**](union.md) 以及其他類型宣告中使用介面資料類型。 下列範例說明如何使用自動產生的 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) 資料類型：

``` syntax
[
    object, 
    uuid (ABCDEFOO-1234-1234-5678-ABCDEF123456)
] 
interface IStream : IUnknown
{ 
    typedef IStream * LPSTREAM; 
    // Other interface definition statements.
}
```

在 COM 介面中，會假設所有介面成員函式都是虛擬函式。 虛擬函式將 **this** 指標隱含為第一個參數。 虛擬函式資料表包含每個介面成員函式的專案。

非 **\[** [**區域**](local.md) **\]** 物件介面成員函式必須有 HRESULT 或 SCODE 的傳回值。  (請注意，舊版 MIDL 允許的成員函數傳回 [**void**](void.md)。 不過，從 MIDL 3.0 版開始，傳回 **void** 會產生編譯器錯誤。 ) 具有 HRESULT 或 SCODE 的傳回值表示如果在遠端呼叫期間產生例外狀況，則產生的 proxy 會攔截例外狀況，並傳回傳回值中的例外狀況代碼。 如果您的應用程式可以承受忽略遠端程序呼叫期間發生的錯誤，您可以指定 HRESULT 做為傳回型別，而不會在呼叫後檢查傳回值。

如果您要重新編譯舊的應用程式，當伺服器將新引進的結果傳送至用戶端時，變更傳回型別可能會引發回溯相容性問題。 除了變更傳回型別之外，您還可以使用 [](void.md)呼叫 as 屬性來標記傳回 void 的函式 **\[** [**\_**](call-as.md) **\]** ，使其成為區域函數。 然後使用相同的參數，但以 HRESULT 的傳回型別來定義相關的遠端函式。 視需要，區域函式會根據該 HRESULT 值引發例外狀況。

當您使用 MIDL 編譯器 [**/osf**](-osf.md)參數進行編譯時，無法使用 **\[ 物件 \]** 屬性。

## <a name="examples"></a>範例

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    object
] 
interface IMyInterface : IUnknown
{
    // Interface definition statements.
}

[
    uuid(87654321-1234-1234-1234-123456789ABC), 
    object, 
    local
] 
interface ILocalInterface : ISomeOldCOMInterface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**呼叫 \_ as**](call-as.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**iid \_ 為**](iid-is.md)
</dt> <dt>

[**介面**](interface.md)
</dt> <dt>

[**當地**](local.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**著**](typedef.md)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> <dt>

[**版本**](version.md)
</dt> </dl>

 

 