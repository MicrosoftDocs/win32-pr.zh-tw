---
title: STRINGTABLE 資源
description: 定義應用程式的一或多個字串資源。 字串資源就是以 null 結束的 Unicode 或 ASCII 字串，可在需要時從可執行檔載入，使用 Loadstring 時函數。
ms.assetid: 5868245d-3445-4792-86f5-253945310d36
keywords:
- STRINGTABLE 資源功能表與其他資源
topic_type:
- apiref
api_name:
- STRINGTABLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7994b6853195ba164c766ca6ee275e4535ab1249c0c78907ab996b9dc644013a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720648"
---
# <a name="stringtable-resource"></a>STRINGTABLE 資源

定義應用程式的一或多個字串資源。 字串資源就是以 null 結束的 Unicode 或 ASCII 字串，可在需要時從可執行檔載入，使用 [**loadstring 時**](/windows/win32/api/winuser/nf-winuser-loadstringa) 函數。

有兩種方式可將 **STRINGTABLE** 語句格式化：

``` syntax
STRINGTABLE  [optional-statements] {stringID string  ...}
```

\- 或 -

``` syntax
STRINGTABLE
  [optional-statements]
BEGIN
stringID string
. . .
END
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*選用語句*
</dt> <dd>

這個參數可以是零或多個下列語句。



| 陳述式                                                        | 描述                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**特性**](characteristics-statement.md) *dword*     | 有關可供讀取和寫入資源檔的工具使用之資源的使用者定義資訊。 如需詳細資訊，請參閱 [**特性**](characteristics-statement.md)。 |
| [**語言**](language-statement.md)*語言*、*語言* | 指定資源的語言。 如需詳細資訊，請參閱 [**語言**](language-statement.md)。                                                                              |
| [**版本**](version-statement.md) *dword*                     | 資源的使用者定義版本號碼，可供讀取和寫入資源檔的工具使用。 如需詳細資訊，請參閱 [**版本**](version-statement.md)。              |



 

</dd> <dt>

<span id="stringID"></span><span id="stringid"></span><span id="STRINGID"></span>*Stringid 指定*
</dt> <dd>

識別資源的不帶正負號16位整數。

</dd> <dt>

<span id="string"></span><span id="STRING"></span>*字串*
</dt> <dd>

以引號括住的一或多個字串。 字串不能超過4097個字元，而且必須在原始程式檔中佔用一行。 若要將換行字元加入字串，請使用此字元序列： \\ 012。 例如，"Line one \\ 012Line 二" 會定義如下所示的字串：

``` syntax
Line one
Line two
```

若要在字串中內嵌引號，請使用下列順序： ""。 例如，"" "第三行" "" 會定義如下所示的字串：

``` syntax
"Line three"
```

若要將 Unicode 字元編碼，請使用 "L"，後面接著以引號括住的 Unicode 字元。 如需範例，請參閱範例一節。

資源編譯器也支援 *字串* 中的行接續。 如需範例，請參閱範例一節。

</dd> </dl>

此外，也支援某些屬性以提供回溯相容性。 如需詳細資訊，請參閱 [一般資源屬性](common-resource-attributes.md)。

## <a name="remarks"></a>備註

RC 會為每個區段配置16個字串，並使用識別碼值來判斷要包含字串的區段。 識別碼不同于底部4位的字串會放置在相同的區段中。 如需詳細資訊，請參閱 [Q196774](https://support.microsoft.com/kb/196774)。

## <a name="examples"></a>範例

下列範例示範如何使用 **STRINGTABLE** 語句來顯示 ASCII 字串：

``` syntax
#define IDS_HELLO    1
#define IDS_GOODBYE  2

STRINGTABLE
{
    IDS_HELLO,   "Hello"
    IDS_GOODBYE, "Goodbye"
} 
```

下列範例顯示如何編碼 Unicode 字元：

``` syntax
STRINGTABLE
BEGINIDS_CHINESESTRING L"\x5e2e\x52a9"
IDS_RUSSIANSTRING L"\x0421\x043f\x0440\x0430\x0432\x043a\x0430"
IDS_ARABICSTRING L"\x062a\x0639\x0644\x064a\x0645\x0627\x062a"
END
```

下列範例會顯示具有 ASCII 和 Unicode 的字串。 請注意，沒有初始 "L" 的字串會使用2位數的 escape 格式：

``` syntax
STRINGTABLE
BEGIN
IDS_1 L"5\x00BC-Inch Floppy Disk"
IDS_1a "5\xBC-Inch Floppy Disk"
IDS_2 L"Don't confuse \x2229 (intersection) with \x222A (union)"
IDS_3 "Copyright \xA92001"
IDS_3a L"Copyright \x00a92001"
END
```

下列範例會顯示如何使用行接續：

``` syntax
STRINGTABLE
BEGIN
IDS_VERYLONGSTRING "blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah"
END
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Loadstring 時**](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> <dt>

[**加速器**](accelerators-resource.md)
</dt> <dt>

[**特徵**](characteristics-statement.md)
</dt> <dt>

[**語言**](language-statement.md)
</dt> <dt>

[**功能表**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**版本**](version-statement.md)
</dt> </dl>

 

 