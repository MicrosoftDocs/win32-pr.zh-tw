---
description: 每個地區設定都有一個唯一識別碼，這是由語言識別項和排序次序識別碼組成的32位值。
ms.assetid: ea45b0e5-7df7-47fb-8dad-fccfbe53fec0
title: 地區設定識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7b2f11189f44b8555081d589f3e9ba2ed131cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970946"
---
# <a name="locale-identifiers"></a>地區設定識別碼

每個 [地區](locales-and-languages.md) 設定都有一個唯一識別碼，這是由 [語言識別項](language-identifiers.md) 和 [排序次序識別碼](sort-order-identifiers.md)組成的32位值。 地區設定識別碼是標準的國際數值縮寫，而且具有唯一識別其中一個已安裝作業系統定義之地區設定所需的元件。 NLS 支援預先定義的地區設定識別碼和自訂識別碼。

> [!Note]  
> 地區設定名稱可與 Windows Vista 中引進的函式搭配使用，該函式會採用 [地區設定名稱](locale-names.md) 做為參數，而不是地區設定識別碼。 如需詳細資訊，請參閱 [呼叫「地區設定名稱」函數](calling-the--locale-name--functions.md)。 最好是使用地區設定名稱，而非地區設定識別碼。

 

下圖顯示地區設定識別碼中的位格式。

``` syntax
+-------------+---------+-------------------------+
|   Reserved  | Sort ID |      Language ID        |
+-------------+---------+-------------------------+
31         20 19     16 15                      0   bit
```

## <a name="predefined-locale-identifiers"></a>預先定義的地區設定識別碼

NLS 所支援的預先定義地區設定識別碼，會定義在 [ (NLS) API 參考的國家語言支援](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c)中。

NLS 使用下列地區設定資訊常數來表示地區設定識別碼。

-   [地區 \_ 設定SLANGUAGE](locale-slanguage.md) 或 [地區設定 \_ SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md)
-   [地區設定 \_ SNAME](locale-sname.md)
-   [地區設定 \_ SSCRIPTS](locale-sscripts.md)
-   [地區設定 \_ IDEFAULTANSICODEPAGE](locale-idefault-constants.md)

## <a name="custom-locale-identifiers"></a>自訂地區設定識別碼

**Windows Vista：** NLS 支援下列地區設定資訊常數所代表的自訂地區設定識別碼。

-   [地區設定 \_ 自訂 \_ 預設值](locale-custom-constants.md)
-   [地區設定 \_ 自訂 \_ UI \_ 預設值](locale-custom-constants.md)
-   [未指定地區設定的 \_ 自訂 \_](locale-custom-constants.md)

## <a name="building-a-locale"></a>建立地區設定

您可以使用 NLS 提供的 Locale Builder 公用程式來建立地區設定。 如需詳細資訊，請參閱 [Microsoft Locale Builder](https://www.microsoft.com/download/details.aspx?id=41158)。

您的應用程式可以使用 [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) 宏來建立地區設定識別碼。 或者，也可以使用其中一個對應至下列常數的預設識別碼。

-   [地區設定不 \_ 變](locale-invariant.md)
-   [地區設定 \_ 系統 \_ 預設值](locale-system-default.md)
-   [地區設定 \_ 使用者 \_ 預設值](locale-user-default.md)

## <a name="retrieval-of-locale-identifiers"></a>地區設定識別碼的抓取

應用程式可以使用 [**GetSystemDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlcid) 和 [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid) 函數來取得目前的地區設定識別碼。 每個執行緒都可以使用 [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) 和 [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale)來設定和取出其本身的地區設定。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[地區設定和語言](locales-and-languages.md)
</dt> <dt>

[語言識別碼](language-identifiers.md)
</dt> <dt>

[地區設定名稱](locale-names.md)
</dt> <dt>

[排序次序識別碼](sort-order-identifiers.md)
</dt> <dt>

[**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid)
</dt> </dl>

 

 
