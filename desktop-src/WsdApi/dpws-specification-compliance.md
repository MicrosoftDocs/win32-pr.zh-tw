---
description: 本主題說明 WSDAPI 如何在 Web 服務 (DPWS) 規格的裝置設定檔中，執行選用功能。 它也會說明在 WSDAPI 的執行中省略了哪些 DPWS 功能。
ms.assetid: 54d51e56-8022-4696-b488-4b3a226224d8
title: DPWS 規格合規性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce59ba29e8e36fd5030732c0b61a2dfd164d9c887bdd9881a775c8b1ce6ec353
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130822"
---
# <a name="dpws-specification-compliance"></a>DPWS 規格合規性

本主題說明 WSDAPI 如何在 Web 服務 (DPWS) 規格的 [裝置設定檔](https://specs.xmlsoap.org/ws/2006/02/devprof/) 中，執行選用功能。 它也會說明在 WSDAPI 的執行中省略了哪些 DPWS 功能。

DPWS 規格可提供一致的方式來處理裝置的訊息。 它也會新增特定的限制和建議，以簡化在 embedded 硬體上支援 web 服務的程式。

DPWS 規格會使用指定的實作為建議或限制的條款，來描述選用功能。 省略的功能可能是 DPWS 規格中所述的功能，不是由 WSDAPI 所執行，也可能是 WSDAPI 在 DPWS 規格中指定之方法中所執行的功能。

本主題將遵循 DPWS 區段的版面配置。 每一節會說明 WSDAPI 執行如何處理特定的限制、需求和選用功能。 本主題最適合與 DPWS 規格一起閱讀。

## <a name="dpws-30-messaging"></a>DPWS 3.0 訊息

### <a name="dpws-31-uri-formats"></a>DPWS 3.1 URI 格式

限制 R0025 和 R0027 會將 uri 限制為最大 \_ URI \_ 大小八位。 WSDAPI 會依照指定強制執行這兩項限制。

### <a name="dpws-32-udp-messaging"></a>DPWS 3.2 UDP 訊息

建議 R0029 建議您不要傳送 udp 封包大於傳輸單位 (MTU) 的 udp 封包。 WSDAPI 不會執行這種建議，並且可讓執行程式傳送和接收大於 MTU 的探索訊息。

### <a name="dpws-33-http-messaging"></a>DPWS 3.3 HTTP 通訊

R0001 需要服務支援區區塊轉送。 WSDAPI 接受要求訊息中的區塊資料，並且會在要求訊息中傳送區塊資料。

R0012 和 R0013 描述 SOAP HTTP 系結的必要部分。 針對 R0012，WSDAPI 會實作為 SOAP HTTP 系結，但在 WSDAPI 完成傳送 HTTP 要求之前，不會開始讀取 HTTP 回應。 WSDAPI 會在 R0013 中執行所需的訊息交換模式，並在 R0014 中執行選擇性回應的 SOAP 節點，而不會在 R0015 中執行選擇性的 web 方法功能。 WSDAPI 也支援 R0030 和 R0017 中的需求。

### <a name="dpws-34-soap-envelope"></a>DPWS 3.4 SOAP 封套

WSDAPI 支援 R0034，並預設會強制執行 R0003 和 R0026。 更明確地說，根據 R0003 和 R0026，如果 WSDAPI 收到的 SOAP 信封大於透過 HTTP 的最大 \_ 信封大小，就 \_ 會遭到拒絕，且連接會關閉。

### <a name="dpws-35-ws-addressing"></a>DPWS 3.5 WS-Addressing

R0004 會在 WSDAPI 中反映裝置 API 的建議使用方式，並在 WSDAPI 中由用戶端 API 支援。 由於這是建議，因此，WSDAPI 可讓用戶端和裝置使用 uri 以外 `urn:uuid` 的 uri 作為其裝置端點，以確保最高的相容性。 由於 WSDAPI 中的裝置 API 不會在初始化之間保存狀態，因此應用程式開發人員會在 WSDAPI 中使用裝置 API 來確保正確支援 R0005 和 R0006。 WSDAPI 中的用戶端 API 會假設裝置身分識別是唯一的且保存的，而在 WSDAPI (（例如 PnP X) ）中建立用戶端 API 的功能將需要此資訊，才能在裝置重新開機時適當地辨識裝置。

R0007 建議使用端點參考中的參考屬性。 WSDAPI 仍會辨識並接受具有參考屬性的端點，而開發人員可以選擇使用它們，但根據預設，WSDAPI 不會在其所建立的端點中填入它們。 同樣地，使用 R0042 時，當 WSDAPI 建立服務端點時，會使用 HTTP 或 HTTPS 傳輸位址，但不會要求裝置在其服務端點中使用 HTTP 或 HTTPS 傳輸位址。 當嘗試與未使用 HTTP 或 HTTPS 的服務通訊時，用戶端的行為未定義。

發生錯誤時，R0031 會限制回復端點，並說明錯誤不是匿名時要傳送的錯誤。 WSDAPI 會在傳送訊息時強制回復端點使用正確的值，而且如果 WSDAPI 收到具有不正確回復端點的要求訊息，將會正確地錯誤。 如果回復端點無效，R0041 會提供可卸載錯誤的選項。 WSDAPI 不會卸載錯誤，而是會將要求通道上的容錯回復（定址為匿名端點），以便與用戶端進行通訊。

最後，SOAP 標頭（R0019 和 R0040）有兩個限制，這兩個 WSDAPI 都符合並強制執行接收的訊息。

### <a name="dpws-36-attachments"></a>DPWS 3.6 附件

WSDAPI 支援附件並符合 R0022。 WSDAPI 也會符合 R0037。 傳送附件時，WSDAPI 一律會將所有 MIME 部分的內容傳輸編碼設定為「二進位」。 不過，WSDAPI 不會強制執行 R0036。 當接收 MIME 部分的內容傳輸編碼未設定為 "binary" 時，會發生 WSDAPI 的行為未定義。

DPWS 也會定義 MIME 部分排序子句。 若為 R0038，WSDAPI 將強制執行部分排序，如果 SOAP 封套不是第一個 MIME 部分，則會拒絕 MIME 訊息。 若為 R0039，WSDAPI 一律會傳送 SOAP 封套作為第一個 MIME 部分。

## <a name="dpws-40-discovery"></a>DPWS 4.0 探索

R1013 和 R1001 會區分裝置探索和服務探索。 WSDAPI 符合 R1013。 裝載的執行符合 R1001，但 WSDAPI 不會在用戶端上強制執行這種建議。

DPWS 也提供類型和範圍比對規則的指引。 WSDAPI 支援所有在 [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) 中定義的範圍比對規則（LDAP 除外）。 WSDAPI 也提供可延伸的模型來定義自訂範圍比對規則，藉此符合 R1019。 裝載 API 也一律會 `wsdp:Device` 在每個 R1020 的探索中提供該類型，但用戶端 api 不需要它存在。 在 WSDAPI 上建立的其他應用程式（例如 PnP X）確實需要在 `wsdp:Device` 探索中有該類型。

為了方便探索和系結，WSDAPI 支援 R1009 和 R1016。 根據 R1018，WSDAPI 會忽略未傳送至匿名位址的多播 UDP。 R1015、R1021 和 R1022 會定義探查訊息的 HTTP 系結，而此訊息是由 WSDAPI 支援（如所述）。

## <a name="dpws-50-description"></a>DPWS 5.0 描述

WSDAPI 會在用戶端上強制執行 R2044。 在裝載端，WSDAPI 只會在 `wsx:Metadata` SOAP 封套主體中提供元素。 R2045 可讓裝置支援 [WS-傳輸](https://specs.xmlsoap.org/ws/2004/09/transfer/WS-Transfer.pdf) 功能的子集。 裝載 API 一律會產生 `wsa:ActionNotSupported` 錯誤。

### <a name="dpws-51-characteristics"></a>DPWS 5.1 特性

DPWS 描述裝置的基本特性。 除了本主題所述的限制之外，還會針對特定字串和 Uri 定義長度限制。 WSDAPI 會在傳送訊息之前或剖析其內容之後，強制執行此 DPWS 區段5.1 中的長度限制。

DPWS 也會描述中繼資料版本的必要中繼資料區段和迴圈。 用戶端實行會強制存在 ThisModel 和 ThisDevice 中繼資料。 裝載的執行也會適當地管理中繼資料版本，並且一律提供這些區段，並遵守 R2038、R2012、R2001、R2039、R2014 和 R2002。

### <a name="dpws-52-hosting"></a>DPWS 5.2 裝載

本節說明服務和關聯中繼資料的階層。 WSDAPI 不會強制執行 ServiceId 的唯一性，如本節中的用戶端或裝置端所述。

WSDAPI 確實符合 R2040，如果沒有裝載的服務，則裝載的執行可能會傳送沒有關聯性區段的中繼資料回應。 用戶端執行正確接受中繼資料回應。

R2029 可讓中繼資料回應中有多個關聯性區段，而這會讓 WSDAPI 正確接受。 R2030 和 R2042 描述了在裝載 API 中正確執行的中繼資料版本管理。

### <a name="dpws-53-wsdl"></a>DPWS 5.3 WSDL

如果服務提供 Web 服務描述語言 (WSDL) 資料，用戶端執行就可以取得服務定義和即時操作服務。 這會由晚期繫結用戶端使用。 WSDAPI 用戶端實行會接受從服務提供的 WSDL，但用戶端不會驗證它，用戶端也不會提供晚期繫結程式設計模型。 裝載執行可以用來提供 WSDL，但不需要主機，因為服務層級中繼資料不是由主機本身管理。

### <a name="dpws-54-ws-policy"></a>DPWS 5.4 WS-Policy

DPWS 描述要用於裝置的原則判斷提示。 由於 WSDAPI 未提供，且不會解讀 WSDL，因此無法辨識和強制執行內嵌于 WSDL 資料中的原則。

## <a name="dpws-60-eventing"></a>DPWS 6.0 事件

### <a name="dpws-61-subscription"></a>DPWS 6.1 訂用帳戶

DPWS 需要推送傳遞的支援。 WSDAPI 會在服務端上執行推播傳遞，藉此遵循 R3009 和 R3010，而且只會在用戶端接受推播傳遞模式。 R3017 和 R3018 如果無法辨識或位址，就需要服務的特定錯誤 `NotifyTo` `EndTo` 。 WSDAPI 不會提前驗證這些位址，也不會產生這些錯誤。 不過，用戶端執行將會正確地辨識這些錯誤。 同樣地，R3019 是選擇性的，而 WSDAPI 不會執行這項建議，但用戶端執行會正確地辨識 `SubscriptionEnd` 訊息，並會通知應用程式發生傳遞失敗。

### <a name="dpws-611-filtering"></a>DPWS 6.1.1 篩選

WSDAPI 符合 R3008 並會執行 `Action` 篩選。 在遵循 R3011 和 R3012 時，WSDAPI 不會在所述的狀況下產生錯誤。 如果它無法辨識要求進行篩選的動作，則 WSDAPI 也會執行 R3020 所述的錯誤。

### <a name="dpws-62-subscription-duration-and-renewal"></a>DPWS 6.2 訂用帳戶持續時間和續約

WSDAPI 符合 R3005、R3006 和 R3016。 WSDAPI 一律會使用 `xs:duration` `xs:dateTime` ，但如果有提供，就會接受，因此不會在 R3013 中發出選擇性錯誤。 WSDAPI 支援 `GetStatus` 且不會 `wsa:ActionNotSupported` 針對每個 R3015 發出錯誤。 `wsa:ActionNotSupported`如果服務以它回應要求，則會接受錯誤 `GetStatus` 。

## <a name="dpws-70-security"></a>DPWS 7.0 安全性

DPWS 描述適用于裝置的建議安全性模型。 WSDAPI 不會依照說明來執行這些建議，且不會依照所述強制執行本節中的限制。

## <a name="dpws-appendix-i"></a>DPWS 附錄 I

DPWS 從其他規格 amends 全域常數以符合裝置。 WSDAPI 會使用此區段中的常數，並使用這些常數覆寫 [WS 探索](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) 執行中的預設常數。 使用 WSDAPI 進行 WS-Discovery 的應用程式將會系結至在 DPWS 中定義的常數，而不會系結至在 [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)中定義的常數。

 

 



