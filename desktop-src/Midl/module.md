---
title: module 屬性
description: Module 語句會定義一組函數，通常是一組 DLL 進入點。
ms.assetid: 4dec207f-98bc-4784-a3c9-506ffe7523fe
keywords:
- module 屬性 MIDL
topic_type:
- apiref
api_name:
- module
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a83528a1ec632fcf2309438e6228220544a32408b310ea90260b8bcfda3cb6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642806"
---
# <a name="module-attribute"></a>module 屬性

**Module** 語句會定義一組函數，通常是一組 DLL 進入點。

``` syntax
[
    attributes
]
module modulename 
{
    elementlist
};
```

## <a name="parameters"></a>參數

<dl> <dt>

*attributes* 
</dt> <dd>

在 \[ [](uuid.md) \] \[ [](version.md) \] module 語句之前，會接受 uuid、version、 \[ [**helpstring**](helpstring.md) \] 、 \[ [**helpcoNtext**](helpcontext.md) \] 、 \[ [**hidden**](hidden.md) \] 和 \[ [**dllname**](dllname-str-.md) \] 屬性。  如需模組定義之前所接受屬性的詳細資訊，請參閱 OLE Automation 書籍中的 [屬性描述](/previous-versions/windows/desktop/automat/attribute-descriptions)。 需要 \[ **dllname** \] 屬性。 如果省略 \[ **uuid** \] 屬性，系統就不會在系統中唯一指定該模組。

</dd> <dt>

*modulename* 
</dt> <dd>

模組的名稱。

</dd> <dt>

*elementlist* 
</dt> <dd>

DLL 中每個函式的常數定義清單和函式原型。 函式定義中可以出現任何數目的函式定義。 函數清單中的函式具有下列形式：

\[*屬性* \]*returntype* \[*呼叫慣例 funcname* \] (*參數*) ;

\[*屬性* \][**const**](const.md) constanttype *constname*  =  *constval*;

Const 只 \[ 接受 [**helpstring**](helpstring.md) \] 和 \[ [**helpcoNtext**](helpcontext.md) \] 屬性。 [](const.md)

模組中的函式接受下列屬性： \[ [**helpstring**](helpstring.md) \] 、 \[ [**helpcoNtext**](helpcontext.md) \] 、 \[ [**string**](string.md) \] 、 \[ [**entry**](entry.md) \] 、 \[ [**propget**](propget.md) \] 、 \[ [**propput**](propput.md) \] 、 \[ [**propputref**](propputref.md) \] 和 \[ [**vararg**](vararg.md) \] 。 如果 \[ 指定了 **vararg** \] ，則最後一個參數必須是 **VARIANT** 類型的安全陣列。

選擇性的呼叫慣例可以是 \_ \_ pascal/ \_ pascal/pascal、 \_ \_ cdecl/ \_ cdecl/cdecl 或 \_ \_ stdcall/ \_ stdcall/stdcall 中的一個。 *呼叫慣例型別 paramname* 最多可以包含兩個前置底線。

參數清單是以逗號分隔的清單：

\[*屬性*\]

此類型可以是任何先前宣告的類型或內建類型、任何類型的指標，或內建類型的指標。 參數上的屬性為：

\[[**in**](in.md) \] 、 \[ [**out**](out-idl.md) \] 、 \[ [**optional**](optional.md) \] 。

如果 \[ 使用 [**選擇性**](optional.md) \] ，則這些參數的類型必須是 **variant** 或 **variant** \* 。

</dd> </dl>

## <a name="remarks"></a>備註

模組的標頭檔 ( .h) 輸出是一系列的函式原型。 **模組** 關鍵字和周圍括弧會從標頭中移除 ( .h) 檔案輸出，但是會在原型之前插入批註 (//**模組** *modulename*) 。 關鍵字 **extern** 會在宣告之前插入。

## <a name="examples"></a>範例

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("This is not GDI.EXE"), 
    helpcontext(190), 
    dllname("MATH.DLL")
] 
module somemodule
{ 
    [helpstring("Color for the frame")] 
            unsigned long const COLOR_FRAME = 0xH80000006; 
    [helpstring("Not a rectangle but a square"), 
     entry(1)] 
            pascal double square([in] double x); 
};
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**const**](const.md)
</dt> <dt>

[型別程式庫的內容](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[**dllname**](dllname-str-.md)
</dt> <dt>

[**進入**](entry.md)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**隱藏**](hidden.md)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> <dt>

[**vararg**](vararg.md)
</dt> <dt>

[**版本**](version.md)
</dt> </dl>

 

 