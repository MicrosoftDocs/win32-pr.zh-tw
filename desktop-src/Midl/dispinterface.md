---
title: dispinterface 屬性
description: 介面介面語句會定義一組屬性和方法，您可以在其上呼叫 IDispatch 調用。
ms.assetid: d85a8e2b-0155-4d68-bb38-e86f4807e7de
keywords:
- 分派介面屬性 MIDL
topic_type:
- apiref
api_name:
- dispinterface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7cc2b6087b53ff81aa7270a209266dd8248884
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842267"
---
# <a name="dispinterface-attribute"></a>dispinterface 屬性

**介面介面** 語句會定義一組屬性和方法，您可以在其上呼叫 **IDispatch：： Invoke**。 您可以藉由明確地列出一組支援的方法和屬性 (語法 1) ，或 (語法 2) 列出單一介面，來定義一個介面。

``` syntax
[
    [attributes]
]
dispinterface dispinterface-name
{
    properties:
        property-list
    methods:
        method-list
};

[
  [attributes]
]
dispinterface dispinterface-name
{
    interface interface-name
};
```

## <a name="parameters"></a>參數

<dl> <dt>

*attributes* 
</dt> <dd>

指定適用于整個 **介面介面** 的屬性。 接受下列屬性： **\[** [**helpstring**](helpstring.md) **\]** 、 **\[** [**helpcoNtext**](helpcontext.md) **\]** 、的內容： **\[** [](helpfile.md) **\]** 、 **\[** [**hidden**](hidden.md) **\]** 、 **\[** [**nonextensible**](nonextensible.md) **\]** 、 **\[** [**oleautomation**](oleautomation.md) **\]** 、 **\[** [**受限**](restricted.md) **\]** 、 **\[** [**uuid**](uuid.md) **\]** 和 **\[** [**version**](version.md) **\]** 。

</dd> <dt>

*介面介面名稱* 
</dt> <dd>

類型程式庫中已知的分配 **介面** 名稱。 這個名稱在類型程式庫中必須是唯一的。

</dd> <dt>

*屬性清單* 
</dt> <dd>

 (語法 1) 物件所支援的選擇性屬性清單，以變數的形式宣告。 這是在方法清單中宣告屬性函式的簡短形式。 如需詳細資訊，請參閱「批註」一節。

</dd> <dt>

*方法-清單* 
</dt> <dd>

 (語法 1) 清單，其中包含在 **介面介面** 中每個方法和屬性的函式原型。 任何數目的函式定義都可以出現在 *methlist* 中。 *Methlist* 中的函式具有下列形式：

**\[ 屬性 \]** *returntype methname 類型 paramname ***(*** 參數 * * * ) ;**

在 **介面介面** 中的方法上接受下列屬性： **\[ helpstring \]**、 **\[ helpcoNtext \]**、 **\[** [**propget**](propget.md) **\]** 、 **\[** [**propput**](propput.md) **\]** 、 **\[** [**propputref**](propputref.md) **\]** 、 **\[** [**string**](string.md) **\]** 和 **\[** [**vararg**](vararg.md) **\]** 。 如果指定了 **\[ \] vararg** ，則最後一個參數必須是 **VARIANT** 類型的安全陣列。

參數清單是以逗號分隔的清單，其中的每個元素都具有下列格式：

**\[***屬性***\]**

*類型* 可以是任何宣告的或內建類型，或任何類型的指標。 參數上的屬性為：

**\[**[**in**](in.md) **\]** 、 **\[** [**out**](out-idl.md) **\]** 、 **\[** [**optional**](optional.md) **\]** 、 **\[ string \]**

</dd> <dt>

*介面-名稱* 
</dt> <dd>

 (語法 2) 要宣告為 IDispatch 介面的介面名稱。

</dd> </dl>

## <a name="remarks"></a>備註

MIDL 編譯器接受下列參數排序 (從左至右) ：

1.  必要參數 (沒有 \[ defaultvalue \] 或 \[ 選擇性屬性的參數 \]) ，
2.  具有或不具有 defaultvalue 屬性的選擇性參數 \[ \] ，
3.  具有 \[ 選擇性 \] 屬性且不含 \[ defaultvalue \] 屬性的參數。
4.  \[[**lcid**](lcid.md) \] 參數（如果有的話）
5.  \[[**retval**](retval.md) \]參數

方法函數的指定方式與 [**模組**](module.md)的參考頁面中所述完全相同，但 \[ [](entry.md) \] 不允許專案屬性。 請注意，STDOLE32。TLB (STDOLE。您必須匯入16位系統上的 TLB) ，因為分配 **介面** 繼承自 IDispatch。

您可以在屬性或方法清單中宣告屬性。 宣告屬性清單中的屬性並不表示屬性支援的存取類型 (也就是 get、put 或 putref) 。 \[ [](readonly.md) \] 針對不支援 put 或 putref 的屬性指定 readonly 屬性。 如果您在方法清單中宣告屬性函式，則一個屬性的函式都有相同的識別碼。

使用第一個語法時，需要屬性：和方法：標記是必要的。 \[ [](id.md) \] 每個成員也都需要 id 屬性。 例如：

``` syntax
properties: 
    [id(0)] int Value;    // Default property. 
methods: 
    [id(1)] HRESULT Show();
```

與介面成員不同的是，因為在 HRESULT 錯誤碼之外，無法使用 [**retval**](retval.md) 屬性來傳回值。 \[ [](lcid.md) \] 因為 IDispatch：： Invoke 傳遞 lcid，所以 lcid 屬性同樣對分配介面無效。 不過，您可以重新宣告使用這些屬性的介面。

使用第二個語法，可將支援 IDispatch 的介面和先前在 ODL 腳本中宣告的介面重新宣告為 IDispatch 介面，如下所示：

``` syntax
dispinterface helloPro 
{ 
    interface hello; 
};
```

上述範例會宣告 hello 的所有成員，以及 hello 繼承為支援 IDispatch 的所有成員。 在此情況下，如果 hello 先前是使用 \[ \] 傳回 hresult 的 lcid 和 \[ retval 成員宣告，則 \] mktyplib.exe 會移除每個 \[ lcid \] 參數和 HRESULT 傳回型別，而會將傳回型別標記為 \[ retval \] 參數的傳回型別。

> [!Note]  
> Mktyplib.exe 工具已淘汰。 請改用 MIDL 編譯器。

 

分派介面的屬性和方法不是介面介面之 VTBL 的一部分。 因此， [CreateStdDispatch](/windows/win32/api/oleauto/nf-oleauto-createstddispatch) 和 [DispInvoke](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) 不能用來執行 IDispatch：： Invoke。 當應用程式需要透過 Automation 公開現有的非 VTBL 函式時，就會使用此介面。 這些應用程式可以藉由檢查 dispidMember 參數並直接呼叫對應的函式，來執行 IDispatch：： Invoke。

## <a name="examples"></a>範例

``` syntax
[ 
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    version(1.0), 
    helpstring("Useful help string."), 
    helpcontext(2480)
] 
dispinterface MyDispatchObject 
{ 
    properties: 
        [id(1)] int x;    //An integer property named x 
        [id(2)] BSTR y;   //A string property named y 
    methods: 
        [id(3)] HRESULT show();    //No arguments, no result 
        [id(11)] int computeit(int inarg, double *outarg); 
}; 
 
[
    uuid(1e123456-1f3c-1069-996b-00dd010fe676)
] 
dispinterface MyObject 
{ 
    properties: 
    methods: 
        [id(1), propget, bindable, defaultbind, displaybind] long x(); 
 
        [id(1), propput, bindable, defaultbind, 
         displaybind] HRESULT x(long rhs); 
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[**defaultbind**](defaultbind.md)
</dt> <dt>

[**displaybind**](displaybind.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**helpfile**](helpfile.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**隱藏**](hidden.md)
</dt> <dt>

[**在**](in.md)
</dt> <dt>

[**介面**](interface.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**選**](optional.md)
</dt> <dt>

[**擴展**](out-idl.md)
</dt> <dt>

[**nonextensible**](nonextensible.md)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[**限制**](restricted.md)
</dt> <dt>

[**字串**](string.md)
</dt> <dt>

[**uuid**](uuid.md)
</dt> <dt>

[**vararg**](vararg.md)
</dt> <dt>

[**版本**](version.md)
</dt> </dl>

 

 