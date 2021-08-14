---
title: 用戶端如何撰寫服務的 SPN
description: 若要驗證服務，用戶端應用程式會針對它必須連接的服務實例撰寫 SPN。
ms.assetid: cf6c491a-d84d-4c9c-bd69-1f2264f395b6
ms.tgt_platform: multiple
keywords:
- 用戶端如何撰寫服務的 SPN AD
- 服務主體名稱 AD，用戶端如何撰寫服務的 SPN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06c3531ac329af1a4c4fa7721b5d575ce762d86f15767278ad9a348e7956cfa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188183"
---
# <a name="how-clients-compose-a-services-spn"></a>用戶端如何撰寫服務的 SPN

若要驗證服務，用戶端應用程式會針對它必須連接的服務實例撰寫 SPN。 用戶端應用程式可以使用 [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) 函數來撰寫 SPN。 用戶端會使用已知資料或從服務本身以外的來源抓取的資料，來指定 SPN 的元件。

SPN 的表單如下所示：


```C++
<service class>/<host>:<port>/<service name>
```



在此格式中， &lt; 需要 "service class &gt; " 和 " &lt; host &gt; "。 「 &lt; 埠」 &gt; 和「 &lt; 服務名稱」是 &gt; 選擇性的。

一般而言，用戶端會辨識名稱的 " &lt; service class &gt; " 部分，並辨識要包含在 SPN 中的選擇性元件。 用戶端可以從服務連接點 (SCP) 或使用者輸入等來源，取得 SPN 的元件。 例如，用戶端可以讀取服務 SCP 的 **serviceDNSName** 屬性來取得「 &lt; 主機」 &gt; 元件。 **ServiceDNSName** 屬性包含服務實例執行所在之伺服器的 dns 名稱，或包含服務複本之主機資料的 SRV 記錄的 dns 名稱。 「 &lt; 服務名稱」 &gt; 元件只用于可複寫的服務，可以是服務 SCP 的分辨名稱、服務所服務之網域的 dns 名稱，或是 SRV 或 MX 記錄的 dns 名稱。

如需詳細資訊和用來撰寫服務 SPN 的程式碼範例，請參閱[用戶端如何驗證以 SCP 為基礎的 Windows 通訊端服務](how-a-client-authenticates-an-scp-based-windows-sockets-service.md)。

如需 SPN 元件的詳細資訊和描述，請參閱 [唯一 spn 的名稱格式](name-formats-for-unique-spns.md)。

 

 




