---
title: 處理統一資源定位器
description: 統一資源定位器 (URL) 是網際網路上資源的位置和存取方法的 compact 表示。
ms.assetid: bb59ada6-f49f-412c-a32c-4fb9495b1222
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08157738d99e78ff4d458a3bdd1b1e2e661ce538
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "104560312"
---
# <a name="handling-uniform-resource-locators"></a><span data-ttu-id="82ee6-103">處理統一資源定位器</span><span class="sxs-lookup"><span data-stu-id="82ee6-103">Handling Uniform Resource Locators</span></span>

<span data-ttu-id="82ee6-104">統一資源定位器 (URL) 是網際網路上資源的位置和存取方法的 compact 表示。</span><span class="sxs-lookup"><span data-stu-id="82ee6-104">A Uniform Resource Locator (URL) is a compact representation of the location and access method for a resource located on the Internet.</span></span> <span data-ttu-id="82ee6-105">每個 URL 都是由 (HTTP、HTTPS 或 FTP) 的配置以及配置特定的字串所組成。</span><span class="sxs-lookup"><span data-stu-id="82ee6-105">Each URL consists of a scheme (HTTP, HTTPS, or FTP) and a scheme-specific string.</span></span> <span data-ttu-id="82ee6-106">這個字串也可以包含目錄路徑、搜尋字串或資源名稱的組合。</span><span class="sxs-lookup"><span data-stu-id="82ee6-106">This string can also include a combination of a directory path, search string, or name of the resource.</span></span> <span data-ttu-id="82ee6-107">WinINet 函數可讓您建立、合併、細分和正常化 Url。</span><span class="sxs-lookup"><span data-stu-id="82ee6-107">The WinINet functions provide the ability to create, combine, break down, and canonicalize URLs.</span></span> <span data-ttu-id="82ee6-108">如需 Url 的詳細資訊，請參閱統一資源定位器上的 [RFC-1738](https://www.ietf.org/rfc/rfc1738.txt) (URL) 。</span><span class="sxs-lookup"><span data-stu-id="82ee6-108">For more information on URLs, see [RFC-1738](https://www.ietf.org/rfc/rfc1738.txt) on Uniform Resource Locators (URL).</span></span>

<span data-ttu-id="82ee6-109">URL 函數會以工作導向的方式運作。</span><span class="sxs-lookup"><span data-stu-id="82ee6-109">The URL functions operate in a task-oriented manner.</span></span> <span data-ttu-id="82ee6-110">未驗證為函式提供的 URL 內容和格式。</span><span class="sxs-lookup"><span data-stu-id="82ee6-110">The content and format of the URL that is given to the function is not verified.</span></span> <span data-ttu-id="82ee6-111">呼叫應用程式應該追蹤這些函式的使用方式，以確保資料採用預期的格式。</span><span class="sxs-lookup"><span data-stu-id="82ee6-111">The calling application should track the use of these functions to ensure that the data is in the intended format.</span></span> <span data-ttu-id="82ee6-112">例如，使用沒有旗標時， [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) 函數會將字元 "%" 轉換成 escape 序列 "%25"。</span><span class="sxs-lookup"><span data-stu-id="82ee6-112">For example, the [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) function would convert the character "%" into the escape sequence "%25" when using no flags.</span></span> <span data-ttu-id="82ee6-113">如果在正式 URL 上使用 [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) ，則會將 escape 序列 "%25" 轉換成 escape 序列 "%2525"，這將無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="82ee6-113">If [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) is used on the canonicalized URL, the escape sequence "%25" would be converted into the escape sequence "%2525", which would not work properly.</span></span>

-   [<span data-ttu-id="82ee6-114">什麼是正式的 URL？</span><span class="sxs-lookup"><span data-stu-id="82ee6-114">What Is a Canonicalized URL?</span></span>](#what-is-a-canonicalized-url)
-   [<span data-ttu-id="82ee6-115">使用 WinINet 函數來處理 Url</span><span class="sxs-lookup"><span data-stu-id="82ee6-115">Using the WinINet Functions to Handle URLs</span></span>](#using-the-wininet-functions-to-handle-urls)
-   [<span data-ttu-id="82ee6-116">正常化 Url</span><span class="sxs-lookup"><span data-stu-id="82ee6-116">Canonicalizing URLs</span></span>](#what-is-a-canonicalized-url)
-   [<span data-ttu-id="82ee6-117">結合基底和相對 Url</span><span class="sxs-lookup"><span data-stu-id="82ee6-117">Combining Base and Relative URLs</span></span>](#combining-base-and-relative-urls)
-   [<span data-ttu-id="82ee6-118">破解 Url</span><span class="sxs-lookup"><span data-stu-id="82ee6-118">Cracking URLs</span></span>](#cracking-urls)
-   [<span data-ttu-id="82ee6-119">建立 Url</span><span class="sxs-lookup"><span data-stu-id="82ee6-119">Creating URLs</span></span>](#creating-urls)
-   [<span data-ttu-id="82ee6-120">直接存取 Url</span><span class="sxs-lookup"><span data-stu-id="82ee6-120">Accessing URLs Directly</span></span>](#accessing-urls-directly)

## <a name="what-is-a-canonicalized-url"></a><span data-ttu-id="82ee6-121">什麼是正式的 URL？</span><span class="sxs-lookup"><span data-stu-id="82ee6-121">What Is a Canonicalized URL?</span></span>

<span data-ttu-id="82ee6-122">所有 Url 的格式都必須遵循接受的語法和語義，才能透過網際網路存取資源。</span><span class="sxs-lookup"><span data-stu-id="82ee6-122">The format of all URLs must follow the accepted syntax and semantics in order to access resources through the Internet.</span></span> <span data-ttu-id="82ee6-123">標準化是將 URL 格式化以遵循此接受語法和語義的程式。</span><span class="sxs-lookup"><span data-stu-id="82ee6-123">Canonicalization is the process of formatting a URL to follow this accepted syntax and semantics.</span></span>

<span data-ttu-id="82ee6-124">必須編碼的字元包括在美國-ASCII 編碼字元集中沒有對應圖形字元的任何字元 (十六進位 80-FF、在美國-ASCII 編碼字元集中未使用，以及十六進位的 00-1f 和7F，也就是控制字元) 、空格、"%" (用來編碼其他字元) ，以及不安全的字元 (<、>、 \# \| \\ ^、~、 \[ 、 \] 和 ' ) 。</span><span class="sxs-lookup"><span data-stu-id="82ee6-124">Characters that must be encoded include any characters that have no corresponding graphic character in the US-ASCII coded character set (hexadecimal 80-FF, which are not used in the US-ASCII coded character set, and hexadecimal 00-1F and 7F, which are control characters), blank spaces, "%" (which is used to encode other characters), and unsafe characters (<, >, ", \#, {, }, \|, \\, ^, ~, \[, \], and ').</span></span>

## <a name="using-the-wininet-functions-to-handle-urls"></a><span data-ttu-id="82ee6-125">使用 WinINet 函數來處理 Url</span><span class="sxs-lookup"><span data-stu-id="82ee6-125">Using the WinINet Functions to Handle URLs</span></span>

<span data-ttu-id="82ee6-126">下表摘要說明 URL 函數。</span><span class="sxs-lookup"><span data-stu-id="82ee6-126">The following table summarizes the URL functions.</span></span>



| <span data-ttu-id="82ee6-127">函式</span><span class="sxs-lookup"><span data-stu-id="82ee6-127">Function</span></span>                                                   | <span data-ttu-id="82ee6-128">描述</span><span class="sxs-lookup"><span data-stu-id="82ee6-128">Description</span></span>                                        |
|------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="82ee6-129">**InternetCanonicalizeUrl**</span><span class="sxs-lookup"><span data-stu-id="82ee6-129">**InternetCanonicalizeUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) | <span data-ttu-id="82ee6-130">正常化 URL。</span><span class="sxs-lookup"><span data-stu-id="82ee6-130">Canonicalizes the URL.</span></span>                             |
| [<span data-ttu-id="82ee6-131">**InternetCombineUrl**</span><span class="sxs-lookup"><span data-stu-id="82ee6-131">**InternetCombineUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla)           | <span data-ttu-id="82ee6-132">結合基底和相對 Url。</span><span class="sxs-lookup"><span data-stu-id="82ee6-132">Combines base and relative URLs.</span></span>                   |
| [<span data-ttu-id="82ee6-133">**InternetCrackUrl**</span><span class="sxs-lookup"><span data-stu-id="82ee6-133">**InternetCrackUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla)               | <span data-ttu-id="82ee6-134">將 URL 字串剖析為元件。</span><span class="sxs-lookup"><span data-stu-id="82ee6-134">Parses a URL string into components.</span></span>               |
| [<span data-ttu-id="82ee6-135">**InternetCreateUrl**</span><span class="sxs-lookup"><span data-stu-id="82ee6-135">**InternetCreateUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla)             | <span data-ttu-id="82ee6-136">從元件建立 URL 字串。</span><span class="sxs-lookup"><span data-stu-id="82ee6-136">Creates a URL string from components.</span></span>              |
| [<span data-ttu-id="82ee6-137">**InternetOpenUrl**</span><span class="sxs-lookup"><span data-stu-id="82ee6-137">**InternetOpenUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)                 | <span data-ttu-id="82ee6-138">開始取出 FTP、HTTP 或 HTTPS 資源。</span><span class="sxs-lookup"><span data-stu-id="82ee6-138">Begins retrieving an FTP, HTTP, or HTTPS resource.</span></span> |



 

## <a name="canonicalizing-urls"></a><span data-ttu-id="82ee6-139">正常化 Url</span><span class="sxs-lookup"><span data-stu-id="82ee6-139">Canonicalizing URLs</span></span>

<span data-ttu-id="82ee6-140">正常化 URL 是將 URL 轉換成可接受格式的程式，其中可能會包含不安全的字元，例如空格、保留的字元等等。</span><span class="sxs-lookup"><span data-stu-id="82ee6-140">Canonicalizing a URL is the process that converts a URL, which might contain unsafe characters such as blank spaces, reserved characters, and so on, into an accepted format.</span></span>

<span data-ttu-id="82ee6-141">[**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla)函式可以用來將 url 正常化。</span><span class="sxs-lookup"><span data-stu-id="82ee6-141">The [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) function can be used to canonicalize URLs.</span></span> <span data-ttu-id="82ee6-142">這個函式是以工作為導向，因此應用程式應謹慎追蹤其使用方式。</span><span class="sxs-lookup"><span data-stu-id="82ee6-142">This function is very task-oriented, so the application should track its use carefully.</span></span> <span data-ttu-id="82ee6-143">[**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) 不會驗證傳遞給它的 url 是否已正式運作，而且它所傳回的 url 是否有效。</span><span class="sxs-lookup"><span data-stu-id="82ee6-143">[**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) does not verify that the URL passed to it is already canonicalized and that the URL that it returns is valid.</span></span>

<span data-ttu-id="82ee6-144">下列五個旗標控制 [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) 處理特定 URL 的方式。</span><span class="sxs-lookup"><span data-stu-id="82ee6-144">The following five flags control how [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) handles a particular URL.</span></span> <span data-ttu-id="82ee6-145">旗標可以搭配使用。</span><span class="sxs-lookup"><span data-stu-id="82ee6-145">The flags can be used in combination.</span></span> <span data-ttu-id="82ee6-146">如果未使用任何旗標，則函式預設會編碼 URL。</span><span class="sxs-lookup"><span data-stu-id="82ee6-146">If no flags are used, the function encodes the URL by default.</span></span>



| <span data-ttu-id="82ee6-147">值</span><span class="sxs-lookup"><span data-stu-id="82ee6-147">Value</span></span>                     | <span data-ttu-id="82ee6-148">意義</span><span class="sxs-lookup"><span data-stu-id="82ee6-148">Meaning</span></span>                                                                                                                                                                                                 |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82ee6-149">ICU \_ 瀏覽器 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="82ee6-149">ICU\_BROWSER\_MODE</span></span>        | <span data-ttu-id="82ee6-150">請勿在 "" 或 "？" 之後編碼或解碼字元 \# ，而且不要在 "？" 之後移除尾端空白字元。</span><span class="sxs-lookup"><span data-stu-id="82ee6-150">Do not encode or decode characters after "\#" or "?", and do not remove trailing white space after "?".</span></span> <span data-ttu-id="82ee6-151">如果未指定此值，則會編碼整個 URL，並移除尾端空白字元。</span><span class="sxs-lookup"><span data-stu-id="82ee6-151">If this value is not specified, the entire URL is encoded, and trailing white space is removed.</span></span> |
| <span data-ttu-id="82ee6-152">ICU \_ 解碼</span><span class="sxs-lookup"><span data-stu-id="82ee6-152">ICU\_DECODE</span></span>               | <span data-ttu-id="82ee6-153">在剖析 URL 之前，將所有的% XX 序列轉換成字元，包括 escape 序列。</span><span class="sxs-lookup"><span data-stu-id="82ee6-153">Convert all %XX sequences to characters, including escape sequences, before the URL is parsed.</span></span>                                                                                                          |
| <span data-ttu-id="82ee6-154">ICU \_ \_ 只編碼空格 \_</span><span class="sxs-lookup"><span data-stu-id="82ee6-154">ICU\_ENCODE\_SPACES\_ONLY</span></span> | <span data-ttu-id="82ee6-155">僅編碼空格。</span><span class="sxs-lookup"><span data-stu-id="82ee6-155">Encode spaces only.</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="82ee6-156">ICU \_ 無 \_ 編碼</span><span class="sxs-lookup"><span data-stu-id="82ee6-156">ICU\_NO\_ENCODE</span></span>           | <span data-ttu-id="82ee6-157">請勿將 unsafe 字元轉換成 escape 序列。</span><span class="sxs-lookup"><span data-stu-id="82ee6-157">Do not convert unsafe characters to escape sequences.</span></span>                                                                                                                                                   |
| <span data-ttu-id="82ee6-158">ICU \_ 無 \_ 中繼</span><span class="sxs-lookup"><span data-stu-id="82ee6-158">ICU\_NO\_META</span></span>             | <span data-ttu-id="82ee6-159">請勿移除中繼序列 (例如 "." 和 "..."從 URL ) 。</span><span class="sxs-lookup"><span data-stu-id="82ee6-159">Do not remove meta sequences (such as "." and "..") from the URL.</span></span>                                                                                                                                       |



 

<span data-ttu-id="82ee6-160">ICU 解碼 \_ 旗標只能用於正式的 url，因為它會假設所有的% XX 序列都是 escape 程式碼，並將它們轉換成程式碼所表示的字元。</span><span class="sxs-lookup"><span data-stu-id="82ee6-160">The ICU\_DECODE flag should be used only on canonicalized URLs, because it assumes that all %XX sequences are escape codes and converts them into the characters indicated by the code.</span></span> <span data-ttu-id="82ee6-161">如果 URL 中的 "%" 符號不是 escape 程式碼的一部分，則 ICU 解碼仍會 \_ 將它視為一個。</span><span class="sxs-lookup"><span data-stu-id="82ee6-161">If the URL has a "%" symbol in it that is not part of an escape code, ICU\_DECODE still treats it as one.</span></span> <span data-ttu-id="82ee6-162">此特性可能會導致 [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) 建立不正確 URL。</span><span class="sxs-lookup"><span data-stu-id="82ee6-162">This characteristic might cause [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) to create an invalid URL.</span></span>

<span data-ttu-id="82ee6-163">若要使用 [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) 傳回完全解碼的 URL，您 \_ \_ 必須指定 icu 解碼和 icu \_ 。</span><span class="sxs-lookup"><span data-stu-id="82ee6-163">To use [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) to return a completely decoded URL, the ICU\_DECODE and ICU\_NO\_ENCODE flags must be specified.</span></span> <span data-ttu-id="82ee6-164">此設定會假設傳遞給 [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) 的 URL 先前已正式正式。</span><span class="sxs-lookup"><span data-stu-id="82ee6-164">This setup assumes that the URL being passed to [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) has been previously canonicalized.</span></span>

## <a name="combining-base-and-relative-urls"></a><span data-ttu-id="82ee6-165">結合基底和相對 Url</span><span class="sxs-lookup"><span data-stu-id="82ee6-165">Combining Base and Relative URLs</span></span>

<span data-ttu-id="82ee6-166">相對 URL 是相對於絕對基底 URL 之資源位置的精簡標記法。</span><span class="sxs-lookup"><span data-stu-id="82ee6-166">A relative URL is a compact representation of the location of a resource relative to an absolute base URL.</span></span> <span data-ttu-id="82ee6-167">剖析器必須知道基底 URL，而且通常會包含配置、網路位置和 URL 路徑的部分。</span><span class="sxs-lookup"><span data-stu-id="82ee6-167">The base URL must be known to the parser and usually includes the scheme, network location, and parts of the URL path.</span></span> <span data-ttu-id="82ee6-168">應用程式可以呼叫 [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) 來合併相對 url 與其基底 url。</span><span class="sxs-lookup"><span data-stu-id="82ee6-168">An application can call [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) to combine the relative URL with its base URL.</span></span> <span data-ttu-id="82ee6-169">[**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) 也會正常化結果 URL。</span><span class="sxs-lookup"><span data-stu-id="82ee6-169">[**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) also canonicalizes the resultant URL.</span></span>

## <a name="cracking-urls"></a><span data-ttu-id="82ee6-170">破解 Url</span><span class="sxs-lookup"><span data-stu-id="82ee6-170">Cracking URLs</span></span>

<span data-ttu-id="82ee6-171">[**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla)函式會將 url 分隔成其元件元件，並傳回傳遞給函式的 [**url \_ 元件**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa)結構所表示的元件。</span><span class="sxs-lookup"><span data-stu-id="82ee6-171">The [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) function separates a URL into its component parts and returns the components indicated by the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure that is passed to the function.</span></span>

<span data-ttu-id="82ee6-172">組成 [**URL \_ 元件**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) 結構的元件包括配置編號、主機名稱、埠號碼、使用者名稱、密碼、URL 路徑和其他資訊 (例如) 的搜尋參數。</span><span class="sxs-lookup"><span data-stu-id="82ee6-172">The components that make up the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure are the scheme number, host name, port number, user name, password, URL path, and additional information (such as search parameters).</span></span> <span data-ttu-id="82ee6-173">除了配置和埠號碼以外，每個元件都具有保存資訊的字串成員，以及保存字串成員長度的成員。</span><span class="sxs-lookup"><span data-stu-id="82ee6-173">Each component, except the scheme and port numbers, has a string member that holds the information, and a member that holds the length of the string member.</span></span> <span data-ttu-id="82ee6-174">配置和埠號碼只有儲存對應值的成員;所有成功呼叫 [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla)都會傳回它們。</span><span class="sxs-lookup"><span data-stu-id="82ee6-174">The scheme and port numbers have only a member that stores the corresponding value; they are both returned on all successful calls to [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla).</span></span>

<span data-ttu-id="82ee6-175">若要取得 [**URL \_ 元件**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) 結構中特定元件的值，儲存該元件之字串長度的成員必須設定為非零值。</span><span class="sxs-lookup"><span data-stu-id="82ee6-175">To get the value of a particular component in the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure, the member that stores the string length of that component must be set to a nonzero value.</span></span> <span data-ttu-id="82ee6-176">字串成員可以是緩衝區的位址或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="82ee6-176">The string member can be either the address of a buffer or **NULL**.</span></span>

<span data-ttu-id="82ee6-177">如果指標成員包含緩衝區的位址，字串長度成員必須包含該緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="82ee6-177">If the pointer member contains the address of a buffer, the string length member must contain the size of that buffer.</span></span> <span data-ttu-id="82ee6-178">[**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) 會以字串形式傳回緩衝區中的元件資訊，並將字串長度儲存在字串長度成員中。</span><span class="sxs-lookup"><span data-stu-id="82ee6-178">[**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) returns the component information as a string in the buffer and stores the string length in the string length member.</span></span>

<span data-ttu-id="82ee6-179">如果指標成員為 **Null**，則字串長度成員可以設定為任何非零值。</span><span class="sxs-lookup"><span data-stu-id="82ee6-179">If the pointer member is **NULL**, the string length member can be set to any nonzero value.</span></span> <span data-ttu-id="82ee6-180">[**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) 會儲存 url 字串中包含元件資訊之第一個字元的位址，並將字串長度設定為與元件相關之 url 字串其餘部分中的字元數。</span><span class="sxs-lookup"><span data-stu-id="82ee6-180">[**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) stores the address of the first character of the URL string that contains the component information and sets the string length to the number of characters in the remaining part of the URL string that pertains to the component.</span></span>

<span data-ttu-id="82ee6-181">所有的指標成員都會設定為 **Null** ，並將非零長度的成員指向 URL 字串中的適當起點。</span><span class="sxs-lookup"><span data-stu-id="82ee6-181">All pointer members set to **NULL** with a nonzero length member point to the appropriate starting point in the URL string.</span></span> <span data-ttu-id="82ee6-182">長度成員中儲存的長度必須用來判斷個別元件資訊的結尾。</span><span class="sxs-lookup"><span data-stu-id="82ee6-182">The length stored in the length member must be used to determine the end of the individual component's information.</span></span>

<span data-ttu-id="82ee6-183">若要正確地完成初始化 [**url \_ 元件**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) 結構， **wstructsize** 成員必須設定為 [**url \_ 元件**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) 結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="82ee6-183">To finish initializing the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure properly, the **dwStructSize** member must be set to the size of the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure, in bytes.</span></span>

<span data-ttu-id="82ee6-184">下列範例會在 PreOpen1 的編輯方塊中傳回 URL 的元件， \_ 並將元件傳回至 idc PreOpenList 的清單方塊 \_ 。</span><span class="sxs-lookup"><span data-stu-id="82ee6-184">The following example returns the components of the URL in the edit box, IDC\_PreOpen1, and returns the components to the list box, IDC\_PreOpenList.</span></span> <span data-ttu-id="82ee6-185">若只要顯示個別元件的資訊，此函式會在字串中的元件資訊之後立即複製字元，並暫時將它取代為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="82ee6-185">To display only the information for an individual component, this function copies the character immediately after the component's information in the string and temporarily replaces it with a **NULL**.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <strsafe.h>
#include <wininet.h>
#include <stdlib.h>

#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  CRACKER_BUFFER_SIZE           MAX_PATH

// For sample source code implementing the InternetErrorOut( ) 
// function referenced below, see the "Handling Errors" topic  
// under "Using WinInet"
extern BOOL WINAPI InternetErrorOut( HWND hWnd, DWORD dwError,
                                     LPCTSTR szFailingFunctionName );

// Forward declaration of listUrlPart helper functions:
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength );
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, int partValue );

// Static list describing the URL Scheme types 
// enumerated in INTERNET_SCHEME:
TCHAR* schemeType[] =
{
  TEXT( "[Partial URL]" ),                //  0
  TEXT( "[Unknown scheme]" ),             //  1
  TEXT( "[Default scheme]" ),             //  2
  TEXT( "FTP" ),                          //  3
  TEXT( "Gopher" ),                       //  4
  TEXT( "HTTP" ),                         //  5
  TEXT( "HTTPS" ),                        //  6
  TEXT( "File" ),                         //  7
  TEXT( "News" ),                         //  8
  TEXT( "MailTo" ),                       //  9
  TEXT( "Socks" ),                        // 10
  TEXT( "JavaScript" ),                   // 11
  TEXT( "VBScript" )                      // 12
};
#define  CRACKER_SCHEME_TYPE_ARRAY_SIZE      13

BOOL WINAPI Cracker( HWND hDlg, int nURLtextBoxId, int nListBoxId )
{
   int i, j;
   TCHAR* failedFunctionName;
   TCHAR URL_buffer[CRACKER_BUFFER_SIZE];

   URL_COMPONENTS URLparts;

   URLparts.dwStructSize = sizeof( URLparts );

   // The following elements determine which components are displayed
   URLparts.dwSchemeLength    = 1;
   URLparts.dwHostNameLength  = 1;
   URLparts.dwUserNameLength  = 1;
   URLparts.dwPasswordLength  = 1;
   URLparts.dwUrlPathLength   = 1;
   URLparts.dwExtraInfoLength = 1;

   URLparts.lpszScheme     = NULL;
   URLparts.lpszHostName   = NULL;
   URLparts.lpszUserName   = NULL;
   URLparts.lpszPassword   = NULL;
   URLparts.lpszUrlPath    = NULL;
   URLparts.lpszExtraInfo  = NULL;

   SendDlgItemMessage( hDlg, nListBoxId, LB_RESETCONTENT, 0, 0 );
   if( !GetDlgItemText( hDlg, nURLtextBoxId, 
                        URL_buffer, CRACKER_BUFFER_SIZE ) )
   {
       failedFunctionName = TEXT( "GetDlgItemText" );
       goto CrackerError_01;
   }

   if( FAILED( StringCchLength( URL_buffer, CRACKER_BUFFER_SIZE, 
                                (size_t*) &i ) ) )
   {
       failedFunctionName = TEXT( "StringCchLength" );
       goto CrackerError_01;
   }

   if( !InternetCrackUrl( URL_buffer, (DWORD)_tcslen( URL_buffer ), 0, 
                          &URLparts ) )
   {
       failedFunctionName = TEXT( "InternetCrackUrl" );
       goto CrackerError_01;
   }

   failedFunctionName = TEXT( "listURLpart" );

   i = URLparts.nScheme + 2;
   if( ( i >= 0 ) && ( i < CRACKER_SCHEME_TYPE_ARRAY_SIZE ) )
   {
       StringCchLength( schemeType[i], 
                        CRACKER_BUFFER_SIZE, 
                        (size_t*) &j );
       if( !listURLpart( hDlg, nListBoxId, 
                         TEXT("Scheme type"), 
                         schemeType[i], j ))
           goto CrackerError_01;
   }

   if( !listURLpart( hDlg, nListBoxId, TEXT( "Scheme text" ), 
                     URLparts.lpszScheme, 
                     URLparts.dwSchemeLength ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Host name" ), 
                     URLparts.lpszHostName, 
                     URLparts.dwHostNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Port number" ), 
                     (int) URLparts.nPort ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "User name" ), 
                     URLparts.lpszUserName, 
                     URLparts.dwUserNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Password" ), 
                     URLparts.lpszPassword, 
                     URLparts.dwPasswordLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Path" ), 
                     URLparts.lpszUrlPath, 
                     URLparts.dwUrlPathLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Extra information"), 
                     URLparts.lpszExtraInfo, 
                     URLparts.dwExtraInfoLength))
           goto CrackerError_01;

   return( TRUE );

CrackerError_01:
// For sample source code of the InternetErrorOut( ) function 
// referenced below, see the "Handling Errors" 
// topic under "Using WinInet"
   InternetErrorOut( hDlg, GetLastError( ), failedFunctionName );
   return FALSE;
}

// listURLpart( ) helper function for string parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];
  LPTSTR nextStart;
  size_t nextSize;

  if( partLength == 0 )  // Just skip empty ones
    return( TRUE );

  if( FAILED( StringCchCopyEx( outputBuffer, 
                              (size_t) CRACKER_BUFFER_SIZE,
                               szPartName, &nextStart, 
                               &nextSize, 0 ) ) ||
      FAILED( StringCchCopyEx( nextStart, nextSize, TEXT( ": " ), 
                               &nextStart, &nextSize, 0 ) ) ||
      FAILED( StringCchCopyNEx( nextStart, nextSize, part, 
                                (size_t) partLength,
                                &nextStart, &nextSize, 0 ) ) )
    return( FALSE );

  *nextStart = 0;
  if( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                          (LPARAM)outputBuffer ) < 0 )
    return( FALSE );
  return( TRUE );
}

// listURLpart( ) helper function for numeric parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, int partValue )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];

  if( FAILED( StringCchPrintf( outputBuffer, 
                               (size_t) CRACKER_BUFFER_SIZE,
                               TEXT( "%s: %d" ), szPartName, 
                               partValue ) ) ||
      ( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                            (LPARAM)outputBuffer ) < 0 ) )
    return( FALSE );
  return( TRUE );
}
```



## <a name="creating-urls"></a><span data-ttu-id="82ee6-186">建立 Url</span><span class="sxs-lookup"><span data-stu-id="82ee6-186">Creating URLs</span></span>

<span data-ttu-id="82ee6-187">[**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla)函式會使用 [**URL \_ 元件**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa)結構中的資訊來建立統一資源定位器。</span><span class="sxs-lookup"><span data-stu-id="82ee6-187">The [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) function uses the information in the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure to create a Uniform Resource Locator.</span></span>

<span data-ttu-id="82ee6-188">組成 [**URL \_ 元件**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) 結構的元件包括配置、主機名稱、埠號碼、使用者名稱、密碼、URL 路徑和其他資訊 (例如) 的搜尋參數。</span><span class="sxs-lookup"><span data-stu-id="82ee6-188">The components that make up the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure are the scheme, host name, port number, user name, password, URL path, and additional information (such as search parameters).</span></span> <span data-ttu-id="82ee6-189">除了埠號碼以外，每個元件都具有保存資訊的字串成員，以及保存字串成員長度的成員。</span><span class="sxs-lookup"><span data-stu-id="82ee6-189">Each component, except the port number, has a string member that holds the information, and a member that holds the length of the string member.</span></span>

<span data-ttu-id="82ee6-190">針對每個必要元件，指標成員應該包含保存資訊的緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="82ee6-190">For each required component, the pointer member should contain the address of the buffer holding the information.</span></span> <span data-ttu-id="82ee6-191">如果指標成員包含以零結尾的字串位址，則長度成員應設定為零。如果指標成員包含非以零終止的字串位址，則長度成員應設定為字串長度。</span><span class="sxs-lookup"><span data-stu-id="82ee6-191">The length member should be set to zero if the pointer member contains the address of a zero-terminated string; the length member should be set to the string length if the pointer member contains the address of a string that is not zero-terminated.</span></span> <span data-ttu-id="82ee6-192">任何不需要的元件之指標成員都必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="82ee6-192">The pointer member of any components that are not required must be **NULL**.</span></span>

## <a name="accessing-urls-directly"></a><span data-ttu-id="82ee6-193">直接存取 Url</span><span class="sxs-lookup"><span data-stu-id="82ee6-193">Accessing URLs Directly</span></span>

<span data-ttu-id="82ee6-194">您可以使用 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)、 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)和 [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) 功能，直接存取網際網路上的 FTP 和 HTTP 資源。</span><span class="sxs-lookup"><span data-stu-id="82ee6-194">FTP, and HTTP resources on the Internet can be accessed directly by using the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), and [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) functions.</span></span> <span data-ttu-id="82ee6-195">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 會在傳遞至函式的 URL 上開啟與資源的連接。</span><span class="sxs-lookup"><span data-stu-id="82ee6-195">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) opens a connection to the resource at the URL passed to the function.</span></span> <span data-ttu-id="82ee6-196">建立此連接時，有兩個可能的步驟。</span><span class="sxs-lookup"><span data-stu-id="82ee6-196">When this connection is made, there are two possible steps.</span></span> <span data-ttu-id="82ee6-197">首先，如果資源是檔案， [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) 可以進行下載;其次，如果資源是目錄， [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) 可以列舉目錄中的檔案 (除非使用 CERN proxy) 。</span><span class="sxs-lookup"><span data-stu-id="82ee6-197">First, if the resource is a file, [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) can download it; second, if the resource is a directory, [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) can enumerate the files within the directory (except when using CERN proxies).</span></span> <span data-ttu-id="82ee6-198">如需 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)的詳細資訊，請參閱 [讀取](common-functions.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="82ee6-198">For more information on [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), see [Reading Files](common-functions.md).</span></span> <span data-ttu-id="82ee6-199">如需 [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)的詳細資訊，請參閱 [尋找下一個](common-functions.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="82ee6-199">For more information on [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), see [Finding the Next File](common-functions.md).</span></span>

<span data-ttu-id="82ee6-200">對於需要透過 CERN proxy 運作的應用程式， [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 可以用來存取 FTP 目錄和檔案。</span><span class="sxs-lookup"><span data-stu-id="82ee6-200">For applications that need to operate through a CERN proxy, [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) can be used to access FTP directories and files.</span></span> <span data-ttu-id="82ee6-201">FTP 要求會進行封裝，以像是 CERN proxy 會接受的 HTTP 要求。</span><span class="sxs-lookup"><span data-stu-id="82ee6-201">The FTP requests are packaged to appear like an HTTP request, which the CERN proxy would accept.</span></span>

<span data-ttu-id="82ee6-202">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)會使用 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)函數所建立的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼和資源的 URL。</span><span class="sxs-lookup"><span data-stu-id="82ee6-202">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) uses the [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function and the URL of the resource.</span></span> <span data-ttu-id="82ee6-203">URL 必須包含配置 (HTTP：、ftp：、file：適用于 \[ 本機檔案 \] 或 HTTPs： \[ 適用于超文字通訊協定安全 \]) 和網路位置 (例如 `www.microsoft.com`) 。</span><span class="sxs-lookup"><span data-stu-id="82ee6-203">The URL must include the scheme (http:, ftp:, file: \[for a local file\], or https: \[for hypertext protocol secure\]) and network location (such as `www.microsoft.com`).</span></span> <span data-ttu-id="82ee6-204">URL 也可以包含路徑 (例如/isapi/gomscom.asp？TARGET =/windows/feature/) 和資源名稱 (例如 default.htm) 。</span><span class="sxs-lookup"><span data-stu-id="82ee6-204">The URL can also include a path (for example, /isapi/gomscom.asp?TARGET=/windows/feature/) and resource name (for example, default.htm).</span></span> <span data-ttu-id="82ee6-205">針對 HTTP 或 HTTPS 要求，可以包含其他標頭。</span><span class="sxs-lookup"><span data-stu-id="82ee6-205">For HTTP or HTTPS requests, additional headers can be included.</span></span>

<span data-ttu-id="82ee6-206">[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)、 [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)、 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)和 [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (HTTP 或 HTTPS url，只) 可以使用 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 所建立的控制碼來下載資源。</span><span class="sxs-lookup"><span data-stu-id="82ee6-206">[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), and [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (HTTP or HTTPS URLs only) can use the handle that is created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) to download the resource.</span></span>

<span data-ttu-id="82ee6-207">下圖說明每個函式所要使用的控制碼。</span><span class="sxs-lookup"><span data-stu-id="82ee6-207">The following diagram illustrates which handles to use with each function.</span></span>

![搭配函式使用的控制碼](images/ax-wnt02.png)

<span data-ttu-id="82ee6-209">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)會使用 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)所建立的根 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼。</span><span class="sxs-lookup"><span data-stu-id="82ee6-209">The root [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) is used by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span> <span data-ttu-id="82ee6-210">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)所建立的 **HINTERNET** 控制碼可用於 [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)、 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)、 [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) (不會在這裡顯示) 和 [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (HTTP 或 HTTPS url) 。</span><span class="sxs-lookup"><span data-stu-id="82ee6-210">The **HINTERNET** handle created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) can be used by [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) (not shown here), and [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (HTTP or HTTPS URLs only).</span></span>

<span data-ttu-id="82ee6-211">如需詳細資訊，請參閱 [**HINTERNET 控制碼**](appendix-a-hinternet-handles.md)。</span><span class="sxs-lookup"><span data-stu-id="82ee6-211">For more information, see [**HINTERNET Handles**](appendix-a-hinternet-handles.md).</span></span>

> [!Note]  
> <span data-ttu-id="82ee6-212">WinINet 不支援伺服器實施。</span><span class="sxs-lookup"><span data-stu-id="82ee6-212">WinINet does not support server implementations.</span></span> <span data-ttu-id="82ee6-213">此外，它不應該從服務使用。</span><span class="sxs-lookup"><span data-stu-id="82ee6-213">In addition, it should not be used from a service.</span></span> <span data-ttu-id="82ee6-214">針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。</span><span class="sxs-lookup"><span data-stu-id="82ee6-214">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 