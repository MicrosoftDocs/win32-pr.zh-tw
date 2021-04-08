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
# <a name="urlprefix-strings"></a>UrlPrefix 字串

在 HTTP 伺服器 API 中， *UrlPrefix* 是寬字元 (Utf-16) Unicode 字串，其標準格式會指定 URL 命名空間的區段。 它是用來保留使用者帳戶的 URL 命名空間區段，或是為進程註冊 URL 命名空間的區段。

## <a name="urlprefix-format"></a>UrlPrefix 格式

UrlPrefix 具有下列語法：

"配置：//host： port/relativeURI"

UrlPrefix 的配置、主機和埠元素必須存在且非空白，且必須遵守下列規則：

<dl> <dt>

<span id="scheme"></span><span id="SCHEME"></span>方案
</dt> <dd>

必須是 HTTP 或 HTTPs，但全部都是小寫。

</dd> <dt>

<span id="host"></span><span id="HOST"></span>主機
</dt> <dd>

必須是完整功能變數名稱、IPv4 或 IPv6 常值字串，或萬用字元。 與配置（必須是小寫）不同的是，主機部分不區分大小寫。 根據指定其主機部分的方式，UrlPrefix 會分成下列四個路由類別的其中一種，如下所述：

<dl> <dd>強式萬用字元</dd> <dd>明確</dd> <dd>IP 系結弱式萬用字元</dd> <dd>弱式萬用字元</dd> </dl> </dd> <dt>

<span id="port"></span><span id="PORT"></span>港口
</dt> <dd>

十進位數值字串，不是以零開頭，且代表有效的 TCP 通訊埠編號 (1 到 65535) 。 此值不能是萬用字元。

</dd> <dt>

<span id="relativeURI"></span><span id="relativeuri"></span><span id="RELATIVEURI"></span>relativeURI
</dt> <dd>

RelativeURI 元素是選擇性的，但如果存在，則必須一律在後面加上斜線字元 ( "/" ) 。 這是一個前置字串，表示相對於配置、主機和埠值所指定之電腦命名空間中的子樹。 不同于配置（必須是小寫），relativeURI 部分不區分大小寫。

</dd> </dl>

正確格式的 >urlprefixes 範例如下：

-   `https://www.adatum.com:80/vroot/`
-   `https://adatum.com:443/secure/database/`
-   `https://+:80/vroot/`

## <a name="host-specifier-categories"></a>Host-Specifier 分類

為了彈性且容易使用，HTTP 伺服器 API 支援四種不同的方式來指定主機。 以下是四個主機規範分類，依優先順序排列：

<dl> <dt>

<span id="Strong_wildcard__Plus_Sign_"></span><span id="strong_wildcard__plus_sign_"></span><span id="STRONG_WILDCARD__PLUS_SIGN_"></span>強式萬用字元 (加正負號) 
</dt> <dd>

當 UrlPrefix 的主項目目是由單一加號 (+) 所組成時，UrlPrefix 會比對其配置、埠和 relativeURI 專案內容中所有可能的主機名稱，並落在強式萬用字元類別中。

當應用程式需要處理定址至一或多個 relativeURIs 的要求時，無論這些要求如何抵達電腦或其主機標頭中指定的網站為何，強式萬用字元都很有用。 在此情況下使用強式萬用字元，就不需要指定完整的主機和/或 IP 位址清單。

</dd> <dt>

<span id="Explicit"></span><span id="explicit"></span><span id="EXPLICIT"></span>明確
</dt> <dd>

明確的主機名稱（例如主機元素中的完整功能變數名稱）會將 UrlPrefix 放在明確分類中。 這種類型的 host 元素會直接與連入要求的主機標頭相符。

明確主機規格適用于多網站應用程式，例如根據要求導向的網站提供不同內容的 Web 服務器。

</dd> <dt>

<span id="IP-bound_weak_wildcard"></span><span id="ip-bound_weak_wildcard"></span><span id="IP-BOUND_WEAK_WILDCARD"></span>IP 系結弱式萬用字元
</dt> <dd>

當 IP 位址顯示為主項目目時，UrlPrefix 會落在 IP 系結的弱式萬用字元類別中。 這種 UrlPrefix 會比對指定的 IP 介面（具有指定的配置、埠和 relativeURI）的任何主機名稱，以及未經過強式萬用字元或明確 UrlPrefix 比對的主機名稱。 IP 位址會採用主機元素中兩種形式的其中一種：

<dl> <dt>

<span id="IPv4_Literal_String"></span><span id="ipv4_literal_string"></span><span id="IPV4_LITERAL_STRING"></span>IPv4 常值字串
</dt> <dd>

IPv4 常值是由四個小數點的十進位數所組成，每個都在0-255 範圍內，例如192.168.0.0。

</dd> <dt>

<span id="IPv6_Literal_String"></span><span id="ipv6_literal_string"></span><span id="IPV6_LITERAL_STRING"></span>IPv6 常值字串
</dt> <dd>

IPv6 常值字串會以方括弧括住，且包含以冒號分隔的十六進位數位;例如： \[ ：： 1 \] 或 \[ 3ffe： FFFF：：6ECB： 0101 \] 。

</dd> </dl>

IP 系結弱式-萬用字元主機規範適用于根據傳入要求所採用的路由而改變所提供內容的應用程式。 請勿依賴以 IP 系結的弱式萬用字元主機規範來強制執行安全性。

</dd> <dt>

<span id="Weak_wildcard__asterisk_"></span><span id="weak_wildcard__asterisk_"></span><span id="WEAK_WILDCARD__ASTERISK_"></span>弱式萬用字元 (星號) 
</dt> <dd>

當星號 (\*) 顯示為主項目目時，UrlPrefix 會落在弱式萬用字元分類中。 這種 UrlPrefix 會比對任何與指定之配置、埠和 relativeURI 相關聯的主機名稱，而這些名稱尚未由強式萬用字元、明確或 IP 系結的弱式萬用字元 UrlPrefix 進行比對。

在某些情況下，此主機規格可以用來做為預設的 catch，也可以用來指定大型的 URL 命名空間區段，而不需要使用許多 >urlprefixes。

</dd> </dl>

## <a name="urlprefix-conflict-detection-during-reservation-and-registration"></a>在保留和註冊期間 UrlPrefix 衝突偵測

基於保留和註冊的目的，UrlPrefix 的四個不同類別會分開處理，而不會彼此參考。 只要它們是在不同的類別中，就可以註冊衝突的 >urlprefixes。 只有在相同的類別中，衝突會導致保留嘗試失敗。

例如，可能會同時保留明確的 UrlPrefix `https://www.adatum.com:80/vroot/` 和衝突的強式萬用字元 UrlPrefix `https://+:80/vroot/` ，因為它們屬於不同的類別。 不過，後續嘗試保留 https://+:80/vroot/ 給不同使用者的嘗試將會失敗，因為它會與自己類別中的現有保留發生衝突。

## <a name="routing-behavior"></a>路由行為

路由傳送傳入的 HTTP 要求時，HTTP 伺服器 API 會以強式萬用字元類別開頭，並比較該類別中已註冊和保留 >urlprefixes 的傳入 URL。

如果傳入的 URL 符合保留但不符合註冊，HTTP 伺服器 API 就會失敗要求。 這可防止較低優先順序的註冊無法挑選非預期的要求。 失敗的狀態為 400 ( 「不正確的要求」 ) 而不是 503 ( 「服務無法使用」 ) ，因為503傳回有時會由負載平衡閘道錯誤地解讀，以指出伺服器已超載。

如果在類別中找到相符的註冊，則會將要求路由傳送至與該註冊相關聯的要求佇列。 要求一律會路由傳送至與分類中最長相符 UrlPrefix 相關聯的佇列。

如果在類別目錄中找不到相符項，則 HTTP 伺服器 API 會繼續進行明確的分類，並重複相同的程式。 總而言之，檢查分類的順序如下：

1.  強式萬用字元
2.  明確
3.  IP-Bound 弱式萬用字元
4.  弱式萬用字元

如果在任何類別中都找不到相符項，HTTP 伺服器 API 就會傳送狀態碼為400的回應，表示無法路由傳送要求。

## <a name="longest-match-rule"></a>最長相符規則

在每個 UrlPrefix 類別內，HTTP 伺服器 API 會將要求路由傳送至與最長相符 UrlPrefix 相關聯的佇列。 例如，假設下列兩個 >urlprefixes 註冊到不同的佇列：

- `Queue1 https://www.adatum.com:80/`
- `Queue2 https://www.adatum.com:80/dir/sna/`

HTTP 伺服器 API 會將的要求路由傳送 `https://www.adatum.com:80/default.htm` 至 Queue1，並將要求傳送 `https://www.adatum.com:80/dir/sna/snadefault.htm` 至 Queue2。 它會將要求路由傳送 `https://www.adatum.com:80/dir/app.htm` 至 Queue1，因為最長的完整相符項是使用 `https://www.adatum.com:80/` UrlPrefix，而不是 `https://www.adatum.com:80/dir/sna` UrlPrefix。

 

 




