---
title: 程式庫屬性
description: Library 語句包含 MIDL 編譯器用來產生類型程式庫的所有資訊。
ms.assetid: d73acb17-abe4-4c31-a264-a131d1f9fa51
keywords:
- 程式庫屬性 MIDL
topic_type:
- apiref
api_name:
- library
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fc1f836174a57f6edfddd0575a10d40367c061c034369a1582cc8bf8ce17a53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086368"
---
# <a name="library-attribute"></a>程式庫屬性

**Library** 語句包含 MIDL 編譯器用來產生類型程式庫的所有資訊。

``` syntax
[
    uuid(uuid-number), 
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
}
```

## <a name="parameters"></a>參數

<dl> <dt>

*uuid-數位* 
</dt> <dd>

指定媒體櫃的通用唯一識別碼。

</dd> <dt>

*選用-屬性-清單* 
</dt> <dd>

指定適用于整個連結 **庫** 語句的其他屬性。 允許的屬性包括 **\[** [**control**](control.md) **\]** 、 **\[** [**helpcoNtext**](helpcontext.md) **\]** 、 **\[** [**説明**](helpfile.md) **\]** 、 **\[** [**helpstring**](helpstring.md) **\]** 、 **\[** [**hidden**](hidden.md) **\]** 、 **\[** [**lcid**](lcid.md) **\]** 、 **\[** [**受限**](restricted.md) **\]** 及 **\[** [**版本**](version.md) **\]** 。

</dd> <dt>

*程式庫名稱* 
</dt> <dd>

軟體元件參考連結 **庫** 的名稱。

</dd> <dt>

*程式庫定義語句* 
</dt> <dd>

定義連結 **庫** 內容的一或多個 MIDL 語句。

</dd> </dl>

## <a name="remarks"></a>備註

程式庫區塊內的語句可以使用在程式庫區塊內部或外部宣告的元素。 程式庫語句可以使用這些專案做為基底類型、繼承自這些元素，或直接在行上參考它們，如下所示：

``` syntax
interface MyFace 
{
    // Interface definition statements
};

[
    // library attributes
] 
library
{
    interface MyFace;

    // Other library definition statements.
};
```

MIDL 編譯器會建立類型程式庫，其中包含程式庫區塊內每個元素的定義，以及程式庫區塊內所定義和參考之任何專案的定義。

如需從單一 IDL 檔案產生類型程式庫和 proxy 存根和標頭的詳細資訊，請參閱 [從單一 idl 檔案產生 PROXY DLL 和型別程式庫](generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file-2.md)。

## <a name="examples"></a>範例

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("Hello 2.0 Type Library"), 
    lcid(0x0409), 
    version(2.0)
] 
library Hello 
{
    /* Library definition statements */
};
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[型別程式庫的內容](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[**控制**](control.md)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**helpfile**](helpfile.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**隱藏**](hidden.md)
</dt> <dt>

[**Lcid**](lcid.md)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**限制**](restricted.md)
</dt> <dt>

[**版本**](version.md)
</dt> </dl>

 

 