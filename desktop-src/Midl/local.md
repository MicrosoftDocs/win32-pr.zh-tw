---
title: local 屬性
description: '\ Local \ 屬性指定對 MIDL 編譯器而言，介面或函式不是遠端的。'
ms.assetid: 17ad3d87-4ca4-4e9b-91bc-280c03830f54
keywords:
- local 屬性 MIDL
topic_type:
- apiref
api_name:
- local
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a40b1842bf637d3b7fcaab7a0c13319def1d1663
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106966424"
---
# <a name="local-attribute"></a>local 屬性

**\[ Local \]** 屬性指定對 MIDL 編譯器而言，介面或函式不是遠端的。

``` syntax
[ 
    local 
    [, interface-attribute-list] 
] 
interface interface-name
{
}

[ 
    object, 
    uuid(string-uuid), 
    local [, interface-attribute-list] 
]
interface interface-name
{
}

[ local [, function-attribute-list] ] function-declarator ;
```

## <a name="parameters"></a>參數

<dl> <dt>

*介面屬性清單* 
</dt> <dd>

指定適用于整個介面的其他屬性。 屬性 **\[** [**端點**](endpoint.md) **\]** 、 **\[** [**版本**](version.md) **\]** 和 **\[** [**指標 \_ 預設值**](pointer-default.md) **\]** 都是選擇性的。 當您使用 [**/app \_ config**](-app-config.md)參數進行編譯時， **\[** [**隱含 \_ 控制碼**](implicit-handle.md) **\]** 或 **\[** [**自動 \_ 控制碼**](auto-handle.md) **\]** 也可以存在。 以逗號分隔多個屬性。

</dd> <dt>

*介面-名稱* 
</dt> <dd>

指定軟體元件可以用來描繪介面的名稱。

</dd> <dt>

*字串-uuid* 
</dt> <dd>

指定 Uuidgen.exe 公用程式所產生的 UUID 字串。 如果您不是使用 MIDL 編譯器參數 [**/osf**](-osf.md)，可以用引號括住 UUID 字串。

</dd> <dt>

*函數-屬性清單* 
</dt> <dd>

指定套用至函數的零或多個屬性。 有效的函式屬性為 **\[** [**回呼**](callback.md) **\]** 、指標屬性 **\[** [**ref**](ref.md) **\]** 、 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md) **\]** ; 以及使用方式屬性 **\[** [**字串**](string.md) **\]** 、 **\[** [**忽略**](ignore.md)和 **\]** **\[** [**內容 \_ 控制碼**](context-handle.md) **\]** 。 以逗號分隔多個屬性。

</dd> <dt>

*函式宣告子* 
</dt> <dd>

指定函數的型別規範、函式名稱和參數清單。

</dd> </dl>

## <a name="remarks"></a>備註

**\[ 本機 \]** 屬性可以套用至個別的函式或整個介面。

在介面標頭中使用時， **\[ 本機 \]** 屬性可讓您使用 MIDL 編譯器作為標頭產生器。 編譯器不會為任何函式產生存根，也不會確定可以傳送標頭。

若為 RPC 介面， **\[ 本機 \]** 屬性不能與 **\[** [**uuid**](uuid.md) **\]** 屬性同時使用。 **\[ Uuid \]** 或 **\[ local \]** 都必須存在於介面標頭中，而您所選擇的必須只出現一次。

針對 (物件介面屬性識別的 COM 介面 **\[** [](object.md) **\]**) ，介面屬性清單可以包含 **\[ 本機 \]** 屬性，即使 **\[** [**uuid**](uuid.md) **\]** 屬性存在也一樣。

在個別函式中使用時， **\[ 區域 \]** 屬性會指定不會產生任何存根的本機程式。 使用 **\[ local \]** 作為函式屬性是 DCE IDL 的 Microsoft 擴充功能。 因此，當您使用 MIDL [**/osf**](-osf.md) 參數進行編譯時，就無法使用這個屬性。

請注意，沒有屬性的介面可以匯入基底 IDL 檔案中。 不過，介面必須只包含沒有任何程式的資料類型。 如果介面中包含一個程式，則必須指定 local 或 UUID 屬性。

## <a name="examples"></a>範例

``` syntax
/* IDL file #1 */ 
[
    local
] 
interface local_procs 
{ 
    void MyLocalProc(void);
} 
 
/* IDL file #2 */ 
[
    object, 
    uuid(12345678-1234-1234-123456789ABC), 
    local
] 
interface local_object_procs : IUnknown
{ 
    void MyLocalObjectProc(void);
} 
 
/* IDL file #3 */ 
[
    uuid(87654321-1234-1234-123456789ABC)
] 
interface mixed_procs 
{ 
    [local] void MyLocalProc(void); 
    HRESULT MyRemoteProc([in] short sParam); 
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**/app \_ 設定**](-app-config.md)
</dt> <dt>

[**自動 \_ 處理**](auto-handle.md)
</dt> <dt>

[**回撥**](callback.md)
</dt> <dt>

[**內容 \_ 控制碼**](context-handle.md)
</dt> <dt>

[**端點**](endpoint.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**忽略**](ignore.md)
</dt> <dt>

[**隱含 \_ 控制碼**](implicit-handle.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**物件**](object.md)
</dt> <dt>

[**指標 \_ 預設值**](pointer-default.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**字串**](string.md)
</dt> <dt>

[**獨特**](unique.md)
</dt> <dt>

[**uuid**](uuid.md)
</dt> <dt>

[**版本**](version.md)
</dt> </dl>

 

 




