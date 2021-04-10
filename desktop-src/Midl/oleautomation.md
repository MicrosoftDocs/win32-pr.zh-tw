---
title: oleautomation 屬性
description: MIDL oleautomation 屬性和自動化的相容性。
ms.assetid: 4a1c9a02-d637-4595-87b3-5fe903149357
keywords:
- oleautomation 屬性 MIDL
topic_type:
- apiref
api_name:
- oleautomation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b827aba4cb0871f7130e658299c6d8836557a156
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023457"
---
# <a name="oleautomation-attribute"></a>oleautomation 屬性

**Oleautomation** 屬性指出介面與 Automation 相容。

``` syntax
[ 
    oleautomation, 
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

指定 Uuidgen.exe 公用程式所產生的 UUID 字串。

</dd> <dt>

*介面屬性清單* 
</dt> <dd>

指定適用于整個介面的其他屬性。

</dd> <dt>

*介面-名稱* 
</dt> <dd>

指定介面的名稱。

</dd> <dt>

*基底介面* 
</dt> <dd>

指定此衍生介面繼承成員函式、狀態碼和介面屬性之自動化介面的名稱。 所有自動化介面都是衍生自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 或 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)。

</dd> </dl>

## <a name="remarks"></a>備註

針對 **\[ oleautomation \]** 介面的成員指定的參數和傳回型別必須是自動化相容的，如下表所示。



| 類型                                            | Description                                                                                                                                                                                                   |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **boolean**                                     | 可以具有值 VARIANT \_ TRUE 或 VARIANT FALSE 的資料項目 \_ 。 大小對應于 VARIANT \_ BOOL。                                                                                                     |
| **unsigned char**                               | 8位不帶正負號的資料項目。                                                                                                                                                                                     |
| **double**                                      | 64位 IEEE 浮點數。                                                                                                                                                                            |
| **float**                                       | 32位 IEEE 浮點數。                                                                                                                                                                            |
| **int**                                         | 帶正負號的整數，其大小與系統相依。 在32位平臺上，MIDL 會將 [**int**](int.md) 視為32位帶正負號的整數。                                                                               |
| **long**                                        | 32 位元帶正負號的整數。                                                                                                                                                                                        |
| **short**                                       | 16位帶正負號的整數。                                                                                                                                                                                        |
| **BSTR**                                        | 長度前置字串，如 Automation 主題 [BSTR](/previous-versions/windows/desktop/automat/bstr)中所述。                                                                                                    |
| **CURRENCY**                                    | 8個位元組的固定浮點數。                                                                                                                                                                          |
| **DATE**                                        | 64位、浮點數自1899年12月30日起算的小數。                                                                                                                                     |
| **SCODE**                                       | 適用于16位系統–對應至 VT 錯誤的內建錯誤類型 \_ 。                                                                                                                                         |
| **Typedef 列舉** *Myenum*                      | 帶正負號的整數，其大小與系統相依。                                                                                                                                                               |
| **介面 IDispatch \***                      | [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 (VT \_ 分派) 的指標。                                                                                                                |
| **介面 IUnknown \***                       | 不是衍生自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (VT 未知) 的介面指標 \_ 。  (任何 OLE 介面都可由其 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面表示。 )  |
| 分配 **介面** *Typename \** （& a）                | 衍生自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (VT 分派) 的介面指標 \_ 。                                                                                                    |
| **Coclass** *Typename \** （& a）                      | Coclass 名稱 (VT \_ 未知) 的指標。                                                                                                                                                                      |
| **\[ oleautomation \] 介面**-  *Typename \** | 衍生自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)之介面的指標。                                                                                                                                      |
| **SAFEARRAY** (*TypeName*)                        | *TypeName* 是上述任何一種類型。 這些類型的陣列。                                                                                                                                                   |
| **TypeName \***                                 | *TypeName* 是上述任何一種類型。 型別的指標。                                                                                                                                                      |
| **十進位**                                     | 96位不帶正負號的二進位整數，以10的可變乘冪來調整。 十進位資料類型，可提供數位大小和小數位數 (的座標) 。                                                       |



 

如果參數的類型是與 automation 相容的型別、與 Automation 相容的型別指標，或 Automation 相容型別的 SAFEARRAY，則參數與 Automation 相容。

如果類型為 HRESULT、SCODE 或 [**void**](void.md)，則傳回類型與 Automation 相容。 不過，MIDL 要求介面方法會傳回 HRESULT 或 SCODE。 傳回 **void** 會產生編譯器錯誤。

如果成員的傳回型別及其所有參數都是自動化相容的，則成員與 Automation 相容。

如果介面衍生自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)或 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)，介面就會與自動化相容; 它具有 **\[ OLEAUTOMATION \]** 屬性，而且所有的 VTBL 專案都是自動化相容的。 若為32位平臺，介面中所有方法的呼叫慣例都必須是 STDCALL。 若是16位系統，所有方法都必須有 CDECL 呼叫慣例。

每個 [**介面介面**](dispinterface.md) 都有隱含的自動化相容性。 因此，您不應該在 **介面介面** 上使用 **\[ oleautomation \]** 屬性。

當您使用 MIDL 編譯器 [**/osf**](-osf.md)參數進行編譯時，無法使用 **\[ oleautomation \]** 屬性。

### <a name="flags"></a>Flags

TYPEFLAG \_ FOLEAUTOMATION

## <a name="examples"></a>範例

``` syntax
library Hello
{
    importlib("stdole32.tlb");
    [
        uuid(12345678-1234-1234-1234-123456789ABC),
        helpstring("Application object for the Hello application."),
        oleautomation,
        dual
    ]
    interface IHello : IDispatch
    {
        // Interface definition statements.
    }

    // Other library definition statements.
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**uuid**](uuid.md)
</dt> </dl>

 

 