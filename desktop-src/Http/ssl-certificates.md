---
title: SSL 憑證
description: 安全通訊端層 (SSL) 已成為保護網際網路連線的標準，可用來防止網路遭到竊聽。 SSL 通訊協定可讓用戶端和伺服器彼此驗證並協商加密演算法。
ms.assetid: 2b78f609-473f-467b-8bf4-709b790bca53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e15e4e6f2b0fe9e3bb058ba506f8a36728540443
ms.sourcegitcommit: be2b23d847b9717224c5f31816594c8abda388a7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/18/2020
ms.locfileid: "106965226"
---
# <a name="ssl-certificates"></a>SSL 憑證

安全通訊端層 (SSL) （也稱為傳輸層安全性 (TLS) ）已成為保護網際網路連線的標準，可用來防止網路遭到竊聽。 SSL/TLS 通訊協定可讓用戶端和伺服器彼此驗證並協商加密演算法。

SSL 會使用加密金鑰和加密演算法來保護 HTTP 連接。 加密金鑰包含在用戶端和伺服器所使用的 SSL 憑證中。 憑證通常是 x.509 ([RFC 2459](https://www.ietf.org/rfc/rfc2459.txt)) 檔。 伺服器會提供會話的 SSL 憑證，並在交握階段將憑證傳送給用戶端。 用戶端只會在伺服器將要求傳送至憑證的用戶端時，才會將其憑證傳送至伺服器。 因此，用戶端一律會驗證服務器，但是伺服器也可以選擇是否要驗證用戶端。

伺服器憑證必須儲存在 HTTP 伺服器 API 的本機持續性儲存體中，以在每次建立安全連線時使用。 每個憑證存放區專案也包含伺服器的 IP 位址和埠、用來簽署訊息的憑證雜湊 () 和應用程式識別碼。 應用程式識別碼是用來識別擁有憑證的應用程式。

系統管理員可以使用設定 Api 來儲存 SSL 伺服器憑證資訊。 系統管理工具會呼叫 [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) 函數，並指定服務設定參數的 HttpServiceConfigSSLCertInfo 值，以設定 SSL 憑證的資訊。 電腦上的每個 IP 位址和通訊埠都只能設定一個伺服器憑證。 HTTP 伺服器 API 也提供 [**查詢**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) 和 [**刪除**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) 函數，以存取或刪除現有的憑證。

 

 




