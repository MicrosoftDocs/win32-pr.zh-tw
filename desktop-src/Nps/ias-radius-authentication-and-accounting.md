---
title: RADIUS 驗證、授權和帳戶處理
description: NPS 完全支援 (RADIUS) 通訊協定遠端驗證撥入消費者服務。 RADIUS 通訊協定是遠端使用者驗證的標準標準，並記載于 RFC 2865 和 RFC 2866 中。
ms.assetid: 3e00d555-355c-4a4c-a389-ab44e9ed9ca9
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b0395b6bc147da4f78bb718cda714014b9b665f5a26a8d20fa29402ee8dec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063485"
---
# <a name="radius-authentication-authorization-and-accounting"></a>RADIUS 驗證、授權和帳戶處理

> [!Note]  
> 網際網路驗證服務 (IAS) 已重新命名網路原則伺服器 (NPS) 從 Windows Server 2008 開始。 本主題的內容適用于 IAS 和 NPS。 在整個文字中，NPS 是用來參考服務的所有版本，包括原本稱為 IAS 的版本。

 

NPS 完全支援 (RADIUS) 通訊協定遠端驗證撥入消費者服務。 RADIUS 通訊協定是遠端使用者驗證的標準標準，並記載于 [rfc 2865](https://www.ietf.org/rfc/rfc2865.txt) 和 [rfc 2866](https://www.ietf.org/rfc/rfc2866.txt)中。

## <a name="radius-authentication-and-authorization"></a>RADIUS 驗證與授權

下圖顯示驗證用戶端 ( 「使用者」 ) 使用點對點通訊協定 (PPP)  (PPP) ，透過撥號連線 (NAS) 連接到網路存取伺服器。 為了驗證使用者，NAS 會與執行 NPS 的遠端伺服器聯繫。 NAS 和 NPS 伺服器使用 RADIUS 通訊協定進行通訊。

![遠端使用者驗證](images/ias01.png)

NAS 會以支援 RADIUS 通訊協定的伺服器或伺服器用戶端的形式運作。 支援 RADIUS 通訊協定的伺服器通常稱為 RADIUS 伺服器。 RADIUS 用戶端（也就是 NAS）會將使用者的相關資訊傳遞給指定的 RADIUS 伺服器，然後對伺服器傳回的回應採取行動。 由 NAS 傳送至 RADIUS 伺服器以驗證使用者的要求通常稱為「驗證要求」。

如果 RADIUS 伺服器成功驗證使用者，RADIUS 伺服器會將設定資訊傳回到 NAS，讓它可以為使用者提供網路服務。 這項設定資訊是由「授權」所組成，其中包含了 NAS 可能提供給使用者 (例如 PPP 或 telnet) 的服務類型。

當 RADIUS 伺服器正在處理驗證要求時，它可以執行授權功能，例如驗證使用者的電話號碼，以及檢查使用者是否已經有進行中的會話。 RADIUS 伺服器可以藉由聯絡狀態伺服器，判斷使用者是否已經有進行中的會話。

如需 RADIUS 驗證和授權的詳細資訊，請參閱 [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt)。

## <a name="radius-accounting"></a>RADIUS 帳戶處理

RADIUS 伺服器也會收集 NAS 所傳送的各種資訊，這些資訊可用於帳戶處理和報告網路活動。 當使用者登入和登出時，RADIUS 用戶端會將資訊傳送給指定的 RADIUS 伺服器。 RADIUS 用戶端可能會在會話進行時定期傳送額外的使用量資訊。 用戶端傳送到伺服器以記錄登入/登出和使用資訊的要求通常稱為「會計要求」。

如需 RADIUS 帳戶處理的詳細資訊，請參閱 [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt)。

## <a name="radius-proxy"></a>RADIUS Proxy

RADIUS 伺服器可作為其他 RADIUS 伺服器的 proxy 用戶端。 在這些情況下，NAS 所聯繫的 RADIUS 伺服器會將驗證或帳戶處理要求傳遞至另一個實際執行驗證或帳戶處理工作的 RADIUS 伺服器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[網際網路驗證服務和網路原則伺服器](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[RADIUS 帳戶處理封包](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[使用狀態伺服器](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

 