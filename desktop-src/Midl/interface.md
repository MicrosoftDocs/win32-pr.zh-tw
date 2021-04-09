---
title: interface 屬性
description: Interface 關鍵字會指定介面的名稱。 IDL 檔案和 ACF 中都必須提供介面名稱。
ms.assetid: 239b782e-57de-493c-b2f4-310d1859a9ae
keywords:
- 介面屬性 MIDL
topic_type:
- apiref
api_name:
- interface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852c29b2ba7b43e9d8b15863e60db8ad2fbde33f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842156"
---
# <a name="interface-attribute"></a>interface 屬性

**Interface** 關鍵字會指定介面的名稱。 IDL 檔案和 ACF 中都必須提供介面名稱。

``` syntax
[ 
    interface-attribute-list 
] 
interface interface-name [ : base-interface ]
{
}

typedef interface interface-name declarator-list
```

## <a name="parameters"></a>參數

<dl> <dt>

*介面屬性清單* 
</dt> <dd>

指定套用至整個介面的屬性。 IDL 檔案的有效介面屬性包括 **\[** [**endpoint**](endpoint.md) **\]** 、 **\[** [**local**](local.md) **\]** 、 **\[** [**object**](object.md) **\]** 、 **\[** [**指標 \_ default**](pointer-default.md) **\]** 、 **\[** [**uuid**](uuid.md) **\]** 和 **\[** [**version**](version.md) **\]** 。 ACF 的有效介面屬性包括 **\[** [**編碼**](encode.md) **\]** 、解碼 **\[** [](decode.md) **\]** 、 **\[** [**自動 \_ 處理**](auto-handle.md) **\]** 或 **\[** [**隱含 \_ 控制碼**](implicit-handle.md) **\]** ，以及程式 **\[** [**代碼**](code.md) **\]** 或 **\[** [**了 nocode**](nocode.md) **\]** 。

</dd> <dt>

*介面-名稱* 
</dt> <dd>

指定介面的名稱。 介面名稱必須是唯一的名稱，且開頭必須是字母或底線字元。

</dd> <dt>

*基底介面* 
</dt> <dd>

指定此衍生介面繼承成員函式、狀態碼和介面屬性之介面的名稱。 衍生介面不會繼承型別定義。 若要這樣做，請使用 [**import**](import.md) 關鍵字匯入基底介面的 IDL 檔案。

</dd> <dt>

*宣告子清單* 
</dt> <dd>

指定標準的 C 宣告子，例如識別碼、指標宣告子，以及陣列宣告子。 如需詳細 [**資訊，請**](arrays-1.md)參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md)、陣列和 [陣列和指標](/windows/desktop/Rpc/arrays-and-pointers)。 宣告子清單包含一或多個宣告子， *並* 以逗號分隔。

</dd> </dl>

## <a name="remarks"></a>備註

IDL 檔案和 ACF 中的介面名稱必須相同，除非您使用 MIDL 編譯器參數 [**/acf**](-acf.md)。

介面名稱會形成介面控制碼資料結構名稱的第一個部分，這是 RPC 執行時間函數的參數。 如需詳細資訊，請參閱 [**RPC \_ IF \_ 控制碼**](/windows/desktop/Rpc/rpc-if-handle)。

如果介面標頭包含 **\[** [](object.md) **\]** 用來指出 COM 介面的物件屬性，它也必須包含 **\[** [**uuid**](uuid.md) **\]** 屬性，而且必須指定從中衍生的基底 COM 介面。 如需 COM 介面的詳細資訊，請參閱 **\[** [**物件**](object.md) **\]** 。

您也可以使用 **interface** 關鍵字搭配 [**typedef**](typedef.md) 關鍵字來定義介面資料類型。

## <a name="examples"></a>範例

``` syntax
/* use of interface keyword in IDL file for an RPC interface */ 
[ 
    uuid (00000000-0000-0000-0000-000000000000), 
    version (1.0) 
] 
interface remote_if_2 
{  
    // Interface definition statements.
} 
 
/* use of interface keyword in ACF for an RPC interface */ 
[
    implicit_handle( handle_t xa_bhandle ) 
] 
interface remote_if_2 
{ 
    // Attribute configuration statements.
} 
 
/* use of interface keyword in IDL file for a COM interface */ 
[ 
    object, uuid (00000000-0000-0000-0000-000000000000) 
] 
interface IDerivedInterface : IBaseInterface 
{  
    import "base.idl" 
    Save(); 
} 
 
/* use of interface keyword to define an interface pointer type */ 
typedef interface IStorage *LPSTORAGE;
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[應用程式佈建檔 (ACF) ](application-configuration-file-acf-.md)
</dt> <dt>

[**端點**](endpoint.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**當地**](local.md)
</dt> <dt>

[**物件**](object.md)
</dt> <dt>

[**指標 \_ 預設值**](pointer-default.md)
</dt> <dt>

[**RPC \_ IF \_ 控制碼**](/windows/desktop/Rpc/rpc-if-handle)
</dt> <dt>

[**著**](typedef.md)
</dt> <dt>

[**uuid**](uuid.md)
</dt> <dt>

[**版本**](version.md)
</dt> </dl>

 

 