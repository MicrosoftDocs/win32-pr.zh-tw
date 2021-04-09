---
title: UrlPrefix 字串
description: 在 HTTP 伺服器 API 中，UrlPrefix 是寬字元 (UTF-16) Unicode 字串，其標準格式會指定 URL 命名空間的區段。
ms.assetid: 4f317bf6-ee6a-47a8-a531-78534217109d
keywords:
- UrlPrefix 字串 HTTP 伺服器 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bddc484f26bc1b3de5d20196dadec9201d3ea272
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "103684217"
---
# <a name="urlprefix-strings"></a><span data-ttu-id="4ead5-104">UrlPrefix 字串</span><span class="sxs-lookup"><span data-stu-id="4ead5-104">UrlPrefix Strings</span></span>

<span data-ttu-id="4ead5-105">在 HTTP 伺服器 API 中， *UrlPrefix* 是寬字元 (Utf-16) Unicode 字串，其標準格式會指定 URL 命名空間的區段。</span><span class="sxs-lookup"><span data-stu-id="4ead5-105">In the HTTP Server API, a *UrlPrefix* is a wide-character (UTF-16) Unicode string with a canonical form that specifies a section of URL namespace.</span></span> <span data-ttu-id="4ead5-106">它是用來保留使用者帳戶的 URL 命名空間區段，或是為進程註冊 URL 命名空間的區段。</span><span class="sxs-lookup"><span data-stu-id="4ead5-106">It is used to reserve a section of URL namespace for a user account or register a section of URL namespace for a process.</span></span>

## <a name="urlprefix-format"></a><span data-ttu-id="4ead5-107">UrlPrefix 格式</span><span class="sxs-lookup"><span data-stu-id="4ead5-107">UrlPrefix Format</span></span>

<span data-ttu-id="4ead5-108">UrlPrefix 具有下列語法：</span><span class="sxs-lookup"><span data-stu-id="4ead5-108">A UrlPrefix has the following syntax:</span></span>

<span data-ttu-id="4ead5-109">"配置：//host： port/relativeURI"</span><span class="sxs-lookup"><span data-stu-id="4ead5-109">"scheme://host:port/relativeURI"</span></span>

<span data-ttu-id="4ead5-110">UrlPrefix 的配置、主機和埠元素必須存在且非空白，且必須遵守下列規則：</span><span class="sxs-lookup"><span data-stu-id="4ead5-110">The scheme, host and port elements of a UrlPrefix must be present and non-empty, and must obey the following rules:</span></span>

<dl> <dt>

<span data-ttu-id="4ead5-111"><span id="scheme"></span><span id="SCHEME"></span>方案</span><span class="sxs-lookup"><span data-stu-id="4ead5-111"><span id="scheme"></span><span id="SCHEME"></span>scheme</span></span>
</dt> <dd>

<span data-ttu-id="4ead5-112">必須是 HTTP 或 HTTPs，但全部都是小寫。</span><span class="sxs-lookup"><span data-stu-id="4ead5-112">Must be either http or https, all in lowercase.</span></span>

</dd> <dt>

<span data-ttu-id="4ead5-113"><span id="host"></span><span id="HOST"></span>主機</span><span class="sxs-lookup"><span data-stu-id="4ead5-113"><span id="host"></span><span id="HOST"></span>host</span></span>
</dt> <dd>

<span data-ttu-id="4ead5-114">必須是完整功能變數名稱、IPv4 或 IPv6 常值字串，或萬用字元。</span><span class="sxs-lookup"><span data-stu-id="4ead5-114">Must be a fully qualified domain name, an IPv4 or IPv6 literal string, or a wildcard.</span></span> <span data-ttu-id="4ead5-115">與配置（必須是小寫）不同的是，主機部分不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="4ead5-115">Unlike the scheme, which must be lowercase, the host portion is case-insensitive.</span></span> <span data-ttu-id="4ead5-116">根據指定其主機部分的方式，UrlPrefix 會分成下列四個路由類別的其中一種，如下所述：</span><span class="sxs-lookup"><span data-stu-id="4ead5-116">Depending on how its host portion is specified, a UrlPrefix falls into one of the following four routing categories, which are described in more detail below:</span></span>

<dl> <dd><span data-ttu-id="4ead5-117">強式萬用字元</span><span class="sxs-lookup"><span data-stu-id="4ead5-117">Strong wildcard</span></span></dd> <dd><span data-ttu-id="4ead5-118">明確</span><span class="sxs-lookup"><span data-stu-id="4ead5-118">Explicit</span></span></dd> <dd><span data-ttu-id="4ead5-119">IP 系結弱式萬用字元</span><span class="sxs-lookup"><span data-stu-id="4ead5-119">IP-bound weak wildcard</span></span></dd> <dd><span data-ttu-id="4ead5-120">弱式萬用字元</span><span class="sxs-lookup"><span data-stu-id="4ead5-120">Weak wildcard</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="4ead5-121"><span id="port"></span><span id="PORT"></span>港口</span><span class="sxs-lookup"><span data-stu-id="4ead5-121"><span id="port"></span><span id="PORT"></span>port</span></span>
</dt> <dd>

<span data-ttu-id="4ead5-122">十進位數值字串，不是以零開頭，且代表有效的 TCP 通訊埠編號 (1 到 65535) 。</span><span class="sxs-lookup"><span data-stu-id="4ead5-122">A decimal numeric string that does not start with zero and that represents a valid TCP port number (1 to 65,535).</span></span> <span data-ttu-id="4ead5-123">此值不能是萬用字元。</span><span class="sxs-lookup"><span data-stu-id="4ead5-123">This value cannot be a wildcard.</span></span>

</dd> <dt>

<span data-ttu-id="4ead5-124"><span id="relativeURI"></span><span id="relativeuri"></span><span id="RELATIVEURI"></span>relativeURI</span><span class="sxs-lookup"><span data-stu-id="4ead5-124"><span id="relativeURI"></span><span id="relativeuri"></span><span id="RELATIVEURI"></span>relativeURI</span></span>
</dt> <dd>

<span data-ttu-id="4ead5-125">RelativeURI 元素是選擇性的，但如果存在，則必須一律在後面加上斜線字元 ( "/" ) 。</span><span class="sxs-lookup"><span data-stu-id="4ead5-125">The relativeURI element is optional, but if present must always be followed by a slash character ("/").</span></span> <span data-ttu-id="4ead5-126">這是一個前置字串，表示相對於配置、主機和埠值所指定之電腦命名空間中的子樹。</span><span class="sxs-lookup"><span data-stu-id="4ead5-126">This is a prefix string that indicates a subtree within the machine's namespace specified relative to the scheme, host and port values.</span></span> <span data-ttu-id="4ead5-127">不同于配置（必須是小寫），relativeURI 部分不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="4ead5-127">Unlike the scheme, which must be lowercase, the relativeURI portion is case-insensitive.</span></span>

</dd> </dl>

<span data-ttu-id="4ead5-128">正確格式的 >urlprefixes 範例如下：</span><span class="sxs-lookup"><span data-stu-id="4ead5-128">Examples of properly formed UrlPrefixes are:</span></span>

-   `https://www.adatum.com:80/vroot/`
-   `https://adatum.com:443/secure/database/`
-   `https://+:80/vroot/`

## <a name="host-specifier-categories"></a><span data-ttu-id="4ead5-129">Host-Specifier 分類</span><span class="sxs-lookup"><span data-stu-id="4ead5-129">Host-Specifier Categories</span></span>

<span data-ttu-id="4ead5-130">為了彈性且容易使用，HTTP 伺服器 API 支援四種不同的方式來指定主機。</span><span class="sxs-lookup"><span data-stu-id="4ead5-130">For flexibility and ease of use, the HTTP Server API supports four different ways to specify hosts.</span></span> <span data-ttu-id="4ead5-131">以下是四個主機規範分類，依優先順序排列：</span><span class="sxs-lookup"><span data-stu-id="4ead5-131">The four host-specifier categories are listed below in order of precedence:</span></span>

<dl> <dt>

<span data-ttu-id="4ead5-132"><span id="Strong_wildcard__Plus_Sign_"></span><span id="strong_wildcard__plus_sign_"></span><span id="STRONG_WILDCARD__PLUS_SIGN_"></span>強式萬用字元 (加正負號) </span><span class="sxs-lookup"><span data-stu-id="4ead5-132"><span id="Strong_wildcard__Plus_Sign_"></span><span id="strong_wildcard__plus_sign_"></span><span id="STRONG_WILDCARD__PLUS_SIGN_"></span>Strong wildcard (Plus Sign)</span></span>
</dt> <dd>

<span data-ttu-id="4ead5-133">當 UrlPrefix 的主項目目是由單一加號 (+) 所組成時，UrlPrefix 會比對其配置、埠和 relativeURI 專案內容中所有可能的主機名稱，並落在強式萬用字元類別中。</span><span class="sxs-lookup"><span data-stu-id="4ead5-133">When the host element of a UrlPrefix consists of a single plus sign (+), the UrlPrefix matches all possible host names in the context of its scheme, port and relativeURI elements, and falls into the strong wildcard category.</span></span>

<span data-ttu-id="4ead5-134">當應用程式需要處理定址至一或多個 relativeURIs 的要求時，無論這些要求如何抵達電腦或其主機標頭中指定的網站為何，強式萬用字元都很有用。</span><span class="sxs-lookup"><span data-stu-id="4ead5-134">A strong wildcard is useful when an application needs to serve requests addressed to one or more relativeURIs, regardless of how those requests arrive on the machine or what site they specify in their Host headers.</span></span> <span data-ttu-id="4ead5-135">在此情況下使用強式萬用字元，就不需要指定完整的主機和/或 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="4ead5-135">Use of a strong wildcard in this situation avoids the need to specify an exhaustive list of host and/or IP-addresses.</span></span>

</dd> <dt>

<span data-ttu-id="4ead5-136"><span id="Explicit"></span><span id="explicit"></span><span id="EXPLICIT"></span>明確</span><span class="sxs-lookup"><span data-stu-id="4ead5-136"><span id="Explicit"></span><span id="explicit"></span><span id="EXPLICIT"></span>Explicit</span></span>
</dt> <dd>

<span data-ttu-id="4ead5-137">明確的主機名稱（例如主機元素中的完整功能變數名稱）會將 UrlPrefix 放在明確分類中。</span><span class="sxs-lookup"><span data-stu-id="4ead5-137">An explicit host name such as a fully qualified domain name in the host element places a UrlPrefix in the explicit category.</span></span> <span data-ttu-id="4ead5-138">這種類型的 host 元素會直接與連入要求的主機標頭相符。</span><span class="sxs-lookup"><span data-stu-id="4ead5-138">This kind of host element is matched directly against the Host headers of incoming requests.</span></span>

<span data-ttu-id="4ead5-139">明確主機規格適用于多網站應用程式，例如根據要求導向的網站提供不同內容的 Web 服務器。</span><span class="sxs-lookup"><span data-stu-id="4ead5-139">Explicit host specifications are useful for multi-site applications such as Web servers that deliver different content depending on the site to which the request was directed.</span></span>

</dd> <dt>

<span data-ttu-id="4ead5-140"><span id="IP-bound_weak_wildcard"></span><span id="ip-bound_weak_wildcard"></span><span id="IP-BOUND_WEAK_WILDCARD"></span>IP 系結弱式萬用字元</span><span class="sxs-lookup"><span data-stu-id="4ead5-140"><span id="IP-bound_weak_wildcard"></span><span id="ip-bound_weak_wildcard"></span><span id="IP-BOUND_WEAK_WILDCARD"></span>IP-bound weak wildcard</span></span>
</dt> <dd>

<span data-ttu-id="4ead5-141">當 IP 位址顯示為主項目目時，UrlPrefix 會落在 IP 系結的弱式萬用字元類別中。</span><span class="sxs-lookup"><span data-stu-id="4ead5-141">When an IP address appears as the host element, then the UrlPrefix falls into the IP-bound Weak Wildcard category.</span></span> <span data-ttu-id="4ead5-142">這種 UrlPrefix 會比對指定的 IP 介面（具有指定的配置、埠和 relativeURI）的任何主機名稱，以及未經過強式萬用字元或明確 UrlPrefix 比對的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="4ead5-142">This kind of UrlPrefix matches any host name for the specified IP interface with the specified scheme, port and relativeURI, and that has not already been matched by a strong-wildcard or explicit UrlPrefix.</span></span> <span data-ttu-id="4ead5-143">IP 位址會採用主機元素中兩種形式的其中一種：</span><span class="sxs-lookup"><span data-stu-id="4ead5-143">The IP address takes one of two forms in the host element:</span></span>

<dl> <dt>

<span data-ttu-id="4ead5-144"><span id="IPv4_Literal_String"></span><span id="ipv4_literal_string"></span><span id="IPV4_LITERAL_STRING"></span>IPv4 常值字串</span><span class="sxs-lookup"><span data-stu-id="4ead5-144"><span id="IPv4_Literal_String"></span><span id="ipv4_literal_string"></span><span id="IPV4_LITERAL_STRING"></span>IPv4 Literal String</span></span>
</dt> <dd>

<span data-ttu-id="4ead5-145">IPv4 常值是由四個小數點的十進位數所組成，每個都在0-255 範圍內，例如192.168.0.0。</span><span class="sxs-lookup"><span data-stu-id="4ead5-145">An IPv4 literal consists of four dotted decimal numbers, each in the range 0-255, such as 192.168.0.0.</span></span>

</dd> <dt>

<span data-ttu-id="4ead5-146"><span id="IPv6_Literal_String"></span><span id="ipv6_literal_string"></span><span id="IPV6_LITERAL_STRING"></span>IPv6 常值字串</span><span class="sxs-lookup"><span data-stu-id="4ead5-146"><span id="IPv6_Literal_String"></span><span id="ipv6_literal_string"></span><span id="IPV6_LITERAL_STRING"></span>IPv6 Literal String</span></span>
</dt> <dd>

<span data-ttu-id="4ead5-147">IPv6 常值字串會以方括弧括住，且包含以冒號分隔的十六進位數位;例如： \[ ：： 1 \] 或 \[ 3ffe： FFFF：：6ECB： 0101 \] 。</span><span class="sxs-lookup"><span data-stu-id="4ead5-147">An IPv6 literal string is enclosed in square brackets and contains hex numbers separated by colons; for example: \[::1\] or \[3ffe:ffff::6ECB:0101\].</span></span>

</dd> </dl>

<span data-ttu-id="4ead5-148">IP 系結弱式-萬用字元主機規範適用于根據傳入要求所採用的路由而改變所提供內容的應用程式。</span><span class="sxs-lookup"><span data-stu-id="4ead5-148">IP-bound weak-wildcard host specifiers are intended for applications that vary the content they serve based on the route taken by incoming requests.</span></span> <span data-ttu-id="4ead5-149">請勿依賴以 IP 系結的弱式萬用字元主機規範來強制執行安全性。</span><span class="sxs-lookup"><span data-stu-id="4ead5-149">Do not rely on IP-bound weak-wildcard host specifiers to enforce security.</span></span>

</dd> <dt>

<span data-ttu-id="4ead5-150"><span id="Weak_wildcard__asterisk_"></span><span id="weak_wildcard__asterisk_"></span><span id="WEAK_WILDCARD__ASTERISK_"></span>弱式萬用字元 (星號) </span><span class="sxs-lookup"><span data-stu-id="4ead5-150"><span id="Weak_wildcard__asterisk_"></span><span id="weak_wildcard__asterisk_"></span><span id="WEAK_WILDCARD__ASTERISK_"></span>Weak wildcard (asterisk)</span></span>
</dt> <dd>

<span data-ttu-id="4ead5-151">當星號 (\*) 顯示為主項目目時，UrlPrefix 會落在弱式萬用字元分類中。</span><span class="sxs-lookup"><span data-stu-id="4ead5-151">When an asterisk (\*) appears as the host element, then the UrlPrefix falls into the weak wildcard category.</span></span> <span data-ttu-id="4ead5-152">這種 UrlPrefix 會比對任何與指定之配置、埠和 relativeURI 相關聯的主機名稱，而這些名稱尚未由強式萬用字元、明確或 IP 系結的弱式萬用字元 UrlPrefix 進行比對。</span><span class="sxs-lookup"><span data-stu-id="4ead5-152">This kind of UrlPrefix matches any host name associated with the specified scheme, port and relativeURI that has not already been matched by a strong-wildcard, explicit, or IP-bound weak-wildcard UrlPrefix.</span></span>

<span data-ttu-id="4ead5-153">在某些情況下，此主機規格可以用來做為預設的 catch，也可以用來指定大型的 URL 命名空間區段，而不需要使用許多 >urlprefixes。</span><span class="sxs-lookup"><span data-stu-id="4ead5-153">This host specification can be used as a default catch-all in some circumstances, or can be used to specify a large section of URL namespace without having to use many UrlPrefixes.</span></span>

</dd> </dl>

## <a name="urlprefix-conflict-detection-during-reservation-and-registration"></a><span data-ttu-id="4ead5-154">在保留和註冊期間 UrlPrefix 衝突偵測</span><span class="sxs-lookup"><span data-stu-id="4ead5-154">UrlPrefix Conflict Detection During Reservation and Registration</span></span>

<span data-ttu-id="4ead5-155">基於保留和註冊的目的，UrlPrefix 的四個不同類別會分開處理，而不會彼此參考。</span><span class="sxs-lookup"><span data-stu-id="4ead5-155">For reservation and registration purposes, the four different categories of UrlPrefix are treated separately, without reference to one another.</span></span> <span data-ttu-id="4ead5-156">只要它們是在不同的類別中，就可以註冊衝突的 >urlprefixes。</span><span class="sxs-lookup"><span data-stu-id="4ead5-156">It is possible to register conflicting UrlPrefixes as long as they are in different categories.</span></span> <span data-ttu-id="4ead5-157">只有在相同的類別中，衝突會導致保留嘗試失敗。</span><span class="sxs-lookup"><span data-stu-id="4ead5-157">Only within the same category does a conflict cause a reservation attempt to fail.</span></span>

<span data-ttu-id="4ead5-158">例如，可能會同時保留明確的 UrlPrefix `https://www.adatum.com:80/vroot/` 和衝突的強式萬用字元 UrlPrefix `https://+:80/vroot/` ，因為它們屬於不同的類別。</span><span class="sxs-lookup"><span data-stu-id="4ead5-158">For example, it would be possible to reserve both the explicit UrlPrefix `https://www.adatum.com:80/vroot/` and the conflicting strong wildcard UrlPrefix `https://+:80/vroot/`, since they belong to different categories.</span></span> <span data-ttu-id="4ead5-159">不過，後續嘗試保留 https://+:80/vroot/ 給不同使用者的嘗試將會失敗，因為它會與自己類別中的現有保留發生衝突。</span><span class="sxs-lookup"><span data-stu-id="4ead5-159">However, a subsequent attempt to reserve https://+:80/vroot/ to a different user would fail because it would conflict with an existing reservation in its own category.</span></span>

## <a name="routing-behavior"></a><span data-ttu-id="4ead5-160">路由行為</span><span class="sxs-lookup"><span data-stu-id="4ead5-160">Routing Behavior</span></span>

<span data-ttu-id="4ead5-161">路由傳送傳入的 HTTP 要求時，HTTP 伺服器 API 會以強式萬用字元類別開頭，並比較該類別中已註冊和保留 >urlprefixes 的傳入 URL。</span><span class="sxs-lookup"><span data-stu-id="4ead5-161">When routing an incoming HTTP request, the HTTP Server API starts with the strong wildcard category and compares the incoming URL with both registered and reserved UrlPrefixes in that category.</span></span>

<span data-ttu-id="4ead5-162">如果傳入的 URL 符合保留但不符合註冊，HTTP 伺服器 API 就會失敗要求。</span><span class="sxs-lookup"><span data-stu-id="4ead5-162">If the incoming URL matches a reservation but not a registration, the HTTP Server API fails the request.</span></span> <span data-ttu-id="4ead5-163">這可防止較低優先順序的註冊無法挑選非預期的要求。</span><span class="sxs-lookup"><span data-stu-id="4ead5-163">This prevents a lower-priority registrations from being able to pick up requests not intended for it.</span></span> <span data-ttu-id="4ead5-164">失敗的狀態為 400 ( 「不正確的要求」 ) 而不是 503 ( 「服務無法使用」 ) ，因為503傳回有時會由負載平衡閘道錯誤地解讀，以指出伺服器已超載。</span><span class="sxs-lookup"><span data-stu-id="4ead5-164">The status on failure is 400 ("Bad Request") rather than 503 ("Service not available"), because a 503 return is sometimes mistakenly interpreted by load-balancing gateways as indicating that the server was overloaded.</span></span>

<span data-ttu-id="4ead5-165">如果在類別中找到相符的註冊，則會將要求路由傳送至與該註冊相關聯的要求佇列。</span><span class="sxs-lookup"><span data-stu-id="4ead5-165">If a matching registration is found within the category, the request is routed to the request queue associated with that registration.</span></span> <span data-ttu-id="4ead5-166">要求一律會路由傳送至與分類中最長相符 UrlPrefix 相關聯的佇列。</span><span class="sxs-lookup"><span data-stu-id="4ead5-166">The request is always routed to the queue associated with the longest matching UrlPrefix within a category.</span></span>

<span data-ttu-id="4ead5-167">如果在類別目錄中找不到相符項，則 HTTP 伺服器 API 會繼續進行明確的分類，並重複相同的程式。</span><span class="sxs-lookup"><span data-stu-id="4ead5-167">If no match is found in the category, then the HTTP Server API proceeds to the explicit category and repeats the same procedure.</span></span> <span data-ttu-id="4ead5-168">總而言之，檢查分類的順序如下：</span><span class="sxs-lookup"><span data-stu-id="4ead5-168">To summarize, the order in which the categories are examined is as follows:</span></span>

1.  <span data-ttu-id="4ead5-169">強式萬用字元</span><span class="sxs-lookup"><span data-stu-id="4ead5-169">Strong wildcard</span></span>
2.  <span data-ttu-id="4ead5-170">明確</span><span class="sxs-lookup"><span data-stu-id="4ead5-170">Explicit</span></span>
3.  <span data-ttu-id="4ead5-171">IP-Bound 弱式萬用字元</span><span class="sxs-lookup"><span data-stu-id="4ead5-171">IP-Bound weak wildcard</span></span>
4.  <span data-ttu-id="4ead5-172">弱式萬用字元</span><span class="sxs-lookup"><span data-stu-id="4ead5-172">Weak wildcard</span></span>

<span data-ttu-id="4ead5-173">如果在任何類別中都找不到相符項，HTTP 伺服器 API 就會傳送狀態碼為400的回應，表示無法路由傳送要求。</span><span class="sxs-lookup"><span data-stu-id="4ead5-173">If no match is found in any of the categories, the HTTP Server API sends a response with a status code of 400 to indicate that the request cannot be routed.</span></span>

## <a name="longest-match-rule"></a><span data-ttu-id="4ead5-174">最長相符規則</span><span class="sxs-lookup"><span data-stu-id="4ead5-174">Longest Match Rule</span></span>

<span data-ttu-id="4ead5-175">在每個 UrlPrefix 類別內，HTTP 伺服器 API 會將要求路由傳送至與最長相符 UrlPrefix 相關聯的佇列。</span><span class="sxs-lookup"><span data-stu-id="4ead5-175">Within each UrlPrefix category, HTTP Server API routes a request to the queue associated with the longest matching UrlPrefix.</span></span> <span data-ttu-id="4ead5-176">例如，假設下列兩個 >urlprefixes 註冊到不同的佇列：</span><span class="sxs-lookup"><span data-stu-id="4ead5-176">For example, suppose the following two UrlPrefixes are registered to different queues:</span></span>

- `Queue1 https://www.adatum.com:80/`
- `Queue2 https://www.adatum.com:80/dir/sna/`

<span data-ttu-id="4ead5-177">HTTP 伺服器 API 會將的要求路由傳送 `https://www.adatum.com:80/default.htm` 至 Queue1，並將要求傳送 `https://www.adatum.com:80/dir/sna/snadefault.htm` 至 Queue2。</span><span class="sxs-lookup"><span data-stu-id="4ead5-177">The HTTP Server API routes a request for `https://www.adatum.com:80/default.htm` to Queue1, and a request for `https://www.adatum.com:80/dir/sna/snadefault.htm` to Queue2.</span></span> <span data-ttu-id="4ead5-178">它會將要求路由傳送 `https://www.adatum.com:80/dir/app.htm` 至 Queue1，因為最長的完整相符項是使用 `https://www.adatum.com:80/` UrlPrefix，而不是 `https://www.adatum.com:80/dir/sna` UrlPrefix。</span><span class="sxs-lookup"><span data-stu-id="4ead5-178">It routes a request for `https://www.adatum.com:80/dir/app.htm` to Queue1 because the longest complete match is with the `https://www.adatum.com:80/` UrlPrefix, not with the `https://www.adatum.com:80/dir/sna` UrlPrefix.</span></span>

 

 




