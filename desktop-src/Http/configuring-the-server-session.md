---
title: 設定伺服器會話
description: .
ms.assetid: 1e4e9440-8d70-44df-90a7-2d5e25b2f680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcf069b22992fa178798c7f28545e30217d0dada
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967187"
---
# <a name="configuring-the-server-session"></a>設定伺服器會話

伺服器會話識別碼會使用 [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) 函式建立，並用於 [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)的呼叫中。 *PPropertyInformation* 參數指向設定之屬性類型的設定結構。 *PropertyInformationLength* 參數會指定設定結構的大小（以位元組為單位）。 例如，在設定 **HttpServerTimeoutsProperty** 時， **pPropertyInformation** 參數必須指向至少為 [**HTTP \_ TIMEOUT \_ 限制 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) 結構大小的緩衝區。

HTTP 應用程式通常會建立單一伺服器會話，而且可能會設定整個應用程式的屬性，例如全域頻寬節流限制，或啟用此伺服器會話的集中式記錄。 [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) 會覆寫呼叫應用程式的 HTTP 伺服器 API 設定;它不會影響 HTTP 伺服器 API 範圍的屬性。 藉由呼叫 [**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)來查詢伺服器會話設定。

 

 




