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
# <a name="locale-identifiers"></a><span data-ttu-id="60163-103">地區設定識別碼</span><span class="sxs-lookup"><span data-stu-id="60163-103">Locale Identifiers</span></span>

<span data-ttu-id="60163-104">每個 [地區](locales-and-languages.md) 設定都有一個唯一識別碼，這是由 [語言識別項](language-identifiers.md) 和 [排序次序識別碼](sort-order-identifiers.md)組成的32位值。</span><span class="sxs-lookup"><span data-stu-id="60163-104">Each [locale](locales-and-languages.md) has a unique identifier, a 32-bit value that consists of a [language identifier](language-identifiers.md) and a [sort order identifier](sort-order-identifiers.md).</span></span> <span data-ttu-id="60163-105">地區設定識別碼是標準的國際數值縮寫，而且具有唯一識別其中一個已安裝作業系統定義之地區設定所需的元件。</span><span class="sxs-lookup"><span data-stu-id="60163-105">The locale identifier is a standard international numeric abbreviation and has the components necessary to uniquely identify one of the installed operating system-defined locales.</span></span> <span data-ttu-id="60163-106">NLS 支援預先定義的地區設定識別碼和自訂識別碼。</span><span class="sxs-lookup"><span data-stu-id="60163-106">NLS supports both predefined locale identifiers and custom identifiers.</span></span>

> [!Note]  
> <span data-ttu-id="60163-107">地區設定名稱可與 Windows Vista 中引進的函式搭配使用，該函式會採用 [地區設定名稱](locale-names.md) 做為參數，而不是地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="60163-107">Locale names can be used with functions introduced in Windows Vista that take a [locale name](locale-names.md) as a parameter, instead of a locale identifier.</span></span> <span data-ttu-id="60163-108">如需詳細資訊，請參閱 [呼叫「地區設定名稱」函數](calling-the--locale-name--functions.md)。</span><span class="sxs-lookup"><span data-stu-id="60163-108">For more information, see [Calling the "Locale Name" Functions](calling-the--locale-name--functions.md).</span></span> <span data-ttu-id="60163-109">最好是使用地區設定名稱，而非地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="60163-109">Use of locale names instead of locale identifiers is always preferable.</span></span>

 

<span data-ttu-id="60163-110">下圖顯示地區設定識別碼中的位格式。</span><span class="sxs-lookup"><span data-stu-id="60163-110">The following illustration shows the format of the bits in a locale identifier.</span></span>

``` syntax
+-------------+---------+-------------------------+
|   Reserved  | Sort ID |      Language ID        |
+-------------+---------+-------------------------+
31         20 19     16 15                      0   bit
```

## <a name="predefined-locale-identifiers"></a><span data-ttu-id="60163-111">預先定義的地區設定識別碼</span><span class="sxs-lookup"><span data-stu-id="60163-111">Predefined Locale Identifiers</span></span>

<span data-ttu-id="60163-112">NLS 所支援的預先定義地區設定識別碼，會定義在 [ (NLS) API 參考的國家語言支援](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c)中。</span><span class="sxs-lookup"><span data-stu-id="60163-112">The predefined locale identifiers supported by NLS are defined in the [National Language Support (NLS) API Reference](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).</span></span>

<span data-ttu-id="60163-113">NLS 使用下列地區設定資訊常數來表示地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="60163-113">NLS uses the following locale information constants to represent locale identifiers.</span></span>

-   <span data-ttu-id="60163-114">[地區 \_ 設定SLANGUAGE](locale-slanguage.md) 或 [地區設定 \_ SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md)</span><span class="sxs-lookup"><span data-stu-id="60163-114">[LOCALE\_SLANGUAGE](locale-slanguage.md) or [LOCALE\_SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md)</span></span>
-   [<span data-ttu-id="60163-115">地區設定 \_ SNAME</span><span class="sxs-lookup"><span data-stu-id="60163-115">LOCALE\_SNAME</span></span>](locale-sname.md)
-   [<span data-ttu-id="60163-116">地區設定 \_ SSCRIPTS</span><span class="sxs-lookup"><span data-stu-id="60163-116">LOCALE\_SSCRIPTS</span></span>](locale-sscripts.md)
-   [<span data-ttu-id="60163-117">地區設定 \_ IDEFAULTANSICODEPAGE</span><span class="sxs-lookup"><span data-stu-id="60163-117">LOCALE\_IDEFAULTANSICODEPAGE</span></span>](locale-idefault-constants.md)

## <a name="custom-locale-identifiers"></a><span data-ttu-id="60163-118">自訂地區設定識別碼</span><span class="sxs-lookup"><span data-stu-id="60163-118">Custom Locale Identifiers</span></span>

<span data-ttu-id="60163-119">**Windows Vista：** NLS 支援下列地區設定資訊常數所代表的自訂地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="60163-119">**Windows Vista:** NLS supports the custom locale identifiers represented by the following locale information constants.</span></span>

-   [<span data-ttu-id="60163-120">地區設定 \_ 自訂 \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="60163-120">LOCALE\_CUSTOM\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="60163-121">地區設定 \_ 自訂 \_ UI \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="60163-121">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="60163-122">未指定地區設定的 \_ 自訂 \_</span><span class="sxs-lookup"><span data-stu-id="60163-122">LOCALE\_CUSTOM\_UNSPECIFIED</span></span>](locale-custom-constants.md)

## <a name="building-a-locale"></a><span data-ttu-id="60163-123">建立地區設定</span><span class="sxs-lookup"><span data-stu-id="60163-123">Building a Locale</span></span>

<span data-ttu-id="60163-124">您可以使用 NLS 提供的 Locale Builder 公用程式來建立地區設定。</span><span class="sxs-lookup"><span data-stu-id="60163-124">You can use the Locale Builder utility provided by NLS to build locales.</span></span> <span data-ttu-id="60163-125">如需詳細資訊，請參閱 [Microsoft Locale Builder](https://www.microsoft.com/download/details.aspx?id=41158)。</span><span class="sxs-lookup"><span data-stu-id="60163-125">For more information, see [Microsoft Locale Builder](https://www.microsoft.com/download/details.aspx?id=41158).</span></span>

<span data-ttu-id="60163-126">您的應用程式可以使用 [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) 宏來建立地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="60163-126">Your application can construct a locale identifier using the [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) macro.</span></span> <span data-ttu-id="60163-127">或者，也可以使用其中一個對應至下列常數的預設識別碼。</span><span class="sxs-lookup"><span data-stu-id="60163-127">Alternatively it can use one of the default identifiers corresponding to the constants listed below.</span></span>

-   [<span data-ttu-id="60163-128">地區設定不 \_ 變</span><span class="sxs-lookup"><span data-stu-id="60163-128">LOCALE\_INVARIANT</span></span>](locale-invariant.md)
-   [<span data-ttu-id="60163-129">地區設定 \_ 系統 \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="60163-129">LOCALE\_SYSTEM\_DEFAULT</span></span>](locale-system-default.md)
-   [<span data-ttu-id="60163-130">地區設定 \_ 使用者 \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="60163-130">LOCALE\_USER\_DEFAULT</span></span>](locale-user-default.md)

## <a name="retrieval-of-locale-identifiers"></a><span data-ttu-id="60163-131">地區設定識別碼的抓取</span><span class="sxs-lookup"><span data-stu-id="60163-131">Retrieval of Locale Identifiers</span></span>

<span data-ttu-id="60163-132">應用程式可以使用 [**GetSystemDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlcid) 和 [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid) 函數來取得目前的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="60163-132">An application can retrieve the current locale identifiers by using the [**GetSystemDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlcid) and [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid) functions.</span></span> <span data-ttu-id="60163-133">每個執行緒都可以使用 [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) 和 [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale)來設定和取出其本身的地區設定。</span><span class="sxs-lookup"><span data-stu-id="60163-133">Each thread can set and retrieve its own locale with [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) and [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale).</span></span>

## <a name="related-topics"></a><span data-ttu-id="60163-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="60163-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60163-135">地區設定和語言</span><span class="sxs-lookup"><span data-stu-id="60163-135">Locales and Languages</span></span>](locales-and-languages.md)
</dt> <dt>

[<span data-ttu-id="60163-136">語言識別碼</span><span class="sxs-lookup"><span data-stu-id="60163-136">Language Identifiers</span></span>](language-identifiers.md)
</dt> <dt>

[<span data-ttu-id="60163-137">地區設定名稱</span><span class="sxs-lookup"><span data-stu-id="60163-137">Locale Names</span></span>](locale-names.md)
</dt> <dt>

[<span data-ttu-id="60163-138">排序次序識別碼</span><span class="sxs-lookup"><span data-stu-id="60163-138">Sort Order Identifiers</span></span>](sort-order-identifiers.md)
</dt> <dt>

[<span data-ttu-id="60163-139">**MAKELCID**</span><span class="sxs-lookup"><span data-stu-id="60163-139">**MAKELCID**</span></span>](/windows/desktop/api/Winnt/nf-winnt-makelcid)
</dt> </dl>

 

 
