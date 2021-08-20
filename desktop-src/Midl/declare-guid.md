---
title: declare_guid 關鍵字
description: Declare \_ guid 關鍵字會指示 MIDL 將 guid 變數發出至產生的標頭檔。
keywords:
- declare_guid 關鍵字 MIDL
topic_type:
- apiref
api_name:
- declare_guid
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: a6854836ef0c45d1892bda9edb250a8c8cfa7d69862ac3424e2a2e96a43991d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117991505"
---
# <a name="declare_guid-keyword"></a>declare \_ guid 關鍵字

**Declare \_ guid** 關鍵字會指示 MIDL 將 guid 變數發出至產生的標頭檔。

``` syntax
declare_guid(variable-name, guid)
```

## <a name="parameters"></a>參數

<dl> <dt>

*變數名稱* 
</dt> <dd>

在產生的標頭檔中指定識別碼的變數名稱。

</dd> <dt>

*guid*
</dt> <dd>

指定將套用至所產生標頭檔中變數名稱的 [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) 。

</dd> </dl>

## <a name="examples"></a>範例

``` syntax
declare_guid(SID_Widget, 5144C348-169E-4359-A79D-5482461D9929)  
```

## <a name="remarks"></a>備註

使用 `declare_guid` 相當於使用 `cpp_quote` 來產生宏的調用 `EXTERN_GUID` 。

上述範例會產生下列輸出：

```C
cpp_quote("EXTERN_GUID(SID_Widget, 0x5144c348, 0x169e, 0x4359, 0xa7, 0x9d, 0x54, 0x82, 0x46, 0x1d, 0x99, 0x29);")
```

`declare_guid`提供語句是為了方便起見。 它的優點是使用與[ `uuid` 屬性](uuid.md)相同的 GUID 語法。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**cpp_quote**](cpp-quote.md)
</dt> <dt>

[**uuid 屬性**](uuid.md)
</dt> <dt>

[**GUID 結構**](/windows/win32/api/guiddef/ns-guiddef-guid)
</dt> </dl>
