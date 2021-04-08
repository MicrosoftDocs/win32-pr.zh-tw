---
title: lcid 屬性
description: '\ Lcid \ 屬性指定地區設定識別碼，並啟用地區設定特定的 MIDL 編譯器支援。'
ms.assetid: 40457a1a-251c-41cd-bfa6-9d506601ff5e
keywords:
- lcid 屬性 MIDL
topic_type:
- apiref
api_name:
- lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa22b231c63583c6d16e6a50f3e9987c5b61128
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681806"
---
# <a name="lcid-attribute"></a>lcid 屬性

**\[ Lcid \]** 屬性指定地區設定識別碼，並啟用地區設定特定的 MIDL 編譯器支援。

``` syntax
[
    uuid(uuid-number), 
    lcid(localeID)
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
}

function-name([parameter-attribute-list, lcid] long  parameter-name,. . .);
```

## <a name="parameters"></a>參數

<dl> <dt>

*uuid-數位* 
</dt> <dd>

指定 [**媒體**](library.md)櫃的通用唯一識別碼。

</dd> <dt>

*localeID* 
</dt> <dd>

指定 Windows 國家語言支援中使用的32位地區設定識別碼。 一般而言，地區設定識別碼會以十六進位提供。

</dd> <dt>

*選用-屬性-清單* 
</dt> <dd>

要套用至連結 [**庫**](library.md)的零或多個屬性。

</dd> <dt>

*程式庫名稱* 
</dt> <dd>

軟體元件參考連結 [**庫**](library.md)的名稱。

</dd> <dt>

*程式庫定義語句* 
</dt> <dd>

定義連結 [**庫**](library.md)內容的一或多個 MIDL 語句。

</dd> <dt>

*函數名稱* 
</dt> <dd>

在 IDL 檔案中指定函數的名稱。

</dd> <dt>

*參數屬性清單* 
</dt> <dd>

將套用至函數參數的零或多個 MIDL 屬性。

</dd> <dt>

*參數-名稱* 
</dt> <dd>

指定 IDL 檔案中的參數名稱。

</dd> </dl>

## <a name="remarks"></a>備註

**\[ Lcid \]** 語法有兩種不同的形式; 屬性的影響取決於您所使用的語法，例如連結 [**庫**](library.md)語句語法或參數語法。

當套用至連結 [**庫**](library.md)語句，以及 localeID 引數（如第一個範例所示）時， **\[ lcid \]** 屬性會識別類型程式庫或函式引數的地區設定，並可讓您在程式庫區塊內使用國際字元。

自 MIDL 編譯器的版本3.01.75 起，此屬性所提供的地區設定識別碼不只會裝飾產生的類型程式庫，而是實際變更編譯器的行為。 在連結 [**庫**](library.md)語句中， **\[ \]** MIDL 會根據所指定的地區設定，接受當地語系化的輸入。 特別是，日文、中文和韓文等亞洲語言的完整支援 (提供完整的 DBCS 支援) 。 當地語系化所支援的功能包括：批註、字串、helpstrings 和識別碼。

使用 [**/lcid**](-lcid.md) 編譯器參數，讓整個輸入檔案都能使用此當地語系化支援，包括檔案名和目錄路徑，而不是只在程式庫區塊內。

當套用至參數時， **\[ lcid \]** 屬性可讓您將地區設定識別碼傳遞至函式，如第二個範例所示。 下列限制適用于 **\[ lcid \]** 參數：

-   函數最多可以有一個 **\[ lcid \]** 參數。
-   參數的資料類型必須為 [**long**](long.md)。
-   參數的方向必須是 **\[** [](in.md) **\]** 。
-   **\[ Lcid \]** 參數必須遵照任何其他參數，但 **\[** [**retval**](retval.md) **\]** 參數除外。
-   您無法將 **\[ lcid \]** 屬性套用至 [**介面介面**](dispinterface.md)或 [**coclass**](coclass.md)參數。

## <a name="examples"></a>範例

``` syntax
[  
    uuid(12345678-1234-1234-1234-123456789ABC),
    lcid(0x09),
    version(1.0)
] 
library MyLibrary
{
    /* Library definition statements */
};

interface IMyFace : IDispatch
{
    [propget] HRESULT MyFunc([in, lcid] long LocaleID,
                          [out, retval] BSTR * ReturnVal);
    // Other interface definition statements
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**/lcid**](-lcid.md)
</dt> <dt>

[**圖書館**](library.md)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**retval**](retval.md)
</dt> </dl>

 

 