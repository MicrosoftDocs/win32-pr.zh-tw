---
description: Schannel 支援傳輸層安全性 (TLS) 通訊協定的1.0、1.1 和1.2 版。
ms.assetid: af541a51-fabc-4abd-ae67-268bd984ab92
title: 傳輸層安全性通訊協定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bed6bc76b6a491105607c3110cda32723bbba75fdf55abe97f7667f397060209
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915590"
---
# <a name="transport-layer-security-protocol"></a>傳輸層安全性通訊協定

Schannel 支援 [*傳輸層安全性 (TLS) 通訊協定*](../secgloss/t-gly.md)的1.0、1.1 和1.2 版。 通訊協定是一種業界標準，旨在保護透過網際網路通訊的資訊隱私權。 TLS 假設連接導向傳輸（通常是 TCP）正在使用中。 TLS 通訊協定可讓用戶端/伺服器應用程式偵測下列安全性風險：

-   訊息篡改
-   訊息攔截
-   訊息偽造

您可以從 IETF 網站取得 TLS 通訊協定的完整規格： [https://www.ietf.org/rfc/rfc2246.txt](https://www.ietf.org/rfc/rfc2246.txt) 。

## <a name="organization-of-tls"></a>TLS 的組織

下列步驟牽涉到使用 TLS 進行用戶端/伺服器通訊：

 **使用 TLS 進行用戶端/伺服器通訊**

1.  交握和加密套件協商
2.  合作物件的驗證
3.  與金鑰相關的資訊交換
4.  應用程式資料交換

組成 TLS 的步驟分為兩種通訊協定，可同時提供連接安全性：

-   [TLS 交握通訊協定](tls-handshake-protocol.md)- (步驟1– 3) 
-   [TLS 記錄通訊協定](tls-record-protocol.md)- (步驟 4) 

## <a name="sspi-with-tls-implementations"></a>使用 TLS 的 SSPI

由於 TLS 沒有 GSSAPI 規格，因此 TLS 實施者可能不熟悉 SSPI 功能。 應用程式會呼叫 SSPI 函式來列舉可用的套件、建立及處理認證的控制碼、建立安全性內容，以及確保訊息完整性的隱私權。

若要支援使用者模式應用程式所使用的 SSPI 函式，TLS 實現（例如 schannel.dll）必須支援由 [使用者模式 SSP/ap 所執行](/windows/desktop/SecAuthN/authentication-functions) 之函式中所列的函式。

如需 SSPI 函數和 SSP 函數的詳細資訊，請參閱 [驗證](authentication-functions.md)函式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[TLS 加密套件](tls-cipher-suites.md)
</dt> <dt>

[TLS 與 SSL 的比較](tls-versus-ssl.md)
</dt> </dl>

 

 
