---
title: 設定伺服器會話
description: 設定伺服器會話
ms.assetid: 1e4e9440-8d70-44df-90a7-2d5e25b2f680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 321d2710a0d9a0f7f3c70ad6de84336d382ae161b938ee2e22f20ddde5012604
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746588"
---
# <a name="configuring-the-server-session"></a>設定伺服器會話

伺服器會話識別碼會使用 [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) 函式建立，並用於 [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)的呼叫中。 *PPropertyInformation* 參數指向設定之屬性類型的設定結構。 *PropertyInformationLength* 參數會指定設定結構的大小（以位元組為單位）。 例如，在設定 **HttpServerTimeoutsProperty** 時， **pPropertyInformation** 參數必須指向至少為 [**HTTP \_ TIMEOUT \_ 限制 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) 結構大小的緩衝區。

HTTP 應用程式通常會建立單一伺服器會話，而且可能會設定整個應用程式的屬性，例如全域頻寬節流限制，或啟用此伺服器會話的集中式記錄。 [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) 會覆寫呼叫應用程式的 HTTP 伺服器 API 設定;它不會影響 HTTP 伺服器 API 範圍的屬性。 藉由呼叫 [**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)來查詢伺服器會話設定。

 

 




