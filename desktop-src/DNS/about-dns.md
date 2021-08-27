---
title: 關於 DNS
description: 網域名稱系統 (DNS) 是一種業界標準通訊協定，用來在以 IP 為基礎的網路上尋找電腦。 使用者可以記住顯示名稱，例如 www.microsoft.com 比以數位為基礎的位址更簡單，例如 207.46.131.137) 簡單。
ms.assetid: 3a899ba4-4338-4119-aa68-a969d196c4f5
keywords:
- 關於網域名稱系統 DNS
- 網域名稱系統 DNS，關於
- 網域名稱系統 DNS，說明
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cc286c18aa60a930a243c1500cf4707d0d42874fc9556fcb090df582334f077
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084788"
---
# <a name="about-dns"></a>關於 DNS

網域名稱系統 (DNS) 是一種業界標準通訊協定，用來在以 IP 為基礎的網路上尋找電腦。 使用者可以記住顯示名稱，例如， `www.microsoft.com` 比以數位為基礎的位址（例如 207.46.131.137) 簡單）更容易。

IP 網路（例如網際網路和 Windows 網路）依賴以數位為基礎的位址來傳輸整個網路中的資料;因此，必須將顯示名稱 (（例如) ）轉譯 `www.microsoft.com` 為網路可 (辨識的數位位址，例如 207.46.131.137) 簡單) 。 DNS 是 Windows 中所選擇的服務，以找出這類資源並將其轉譯為 IP 位址。

dns 是 Active Directory 的主要定位器服務，因此可將 dns 視為 Windows 和 Active Directory 的基礎服務。 Windows 提供的函式可讓應用程式設計人員使用 dns 函式，例如以程式設計方式進行 dns 查詢、比較記錄和查詢名稱。

許多 DNS 函式實際上都是函式類型，在此函式中有函式的基底名稱，但其用途取決於字元編碼。 例如， [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) 函式會列在 DNS 應用程式設計介面的函式參考中， (API) 為 **DnsQuery**，但是在應用程式中使用時，會依據字元編碼是否為 ANSI (指定，方法是附加至函式類型名稱) 、將 W 附加至函式類型名稱 (，或透過將 utf-16 附加至函式類型名稱) 指定的 \_ \_ utf-8 (\_ 。 因此， **DnsQuery** 函式的函式呼叫實際上會是下列其中一項：

\_ \_ 針對 ANSI 編碼 DnsQuery (a) 

\_ \_ Unicode 編碼的 DnsQuery w (w) 

DnsQuery \_ utf8 (\_ UTF8 for utf-8 編碼) 

所有需要此慣例的函式在其函式定義的前幾個句子中明確陳述這項需求。 使用適當的函式名稱;例如，您不能直接呼叫 [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) ，而不是 DnsQuery \_ 。

 

 




