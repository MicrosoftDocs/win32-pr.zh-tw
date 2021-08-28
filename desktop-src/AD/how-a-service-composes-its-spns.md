---
title: 服務如何撰寫其 Spn
description: 服務可以使用兩個函式來撰寫其 Spn DsGetSpn 是用來撰寫 Spn 的一般用途函式，而 DsServerRegisterSpn 則是專門用來撰寫及註冊主機服務之簡單 Spn 的特殊函式。
ms.assetid: 8710409a-67b1-45e5-9cd7-5125443ab921
ms.tgt_platform: multiple
keywords:
- 服務主體名稱 AD，服務的組合方式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fb659eec3bb2d0f50fd109b39f356df1429535
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881401"
---
# <a name="how-a-service-composes-its-spns"></a>服務如何撰寫其 Spn

服務可以使用兩個函式來撰寫其 Spn： [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) 是用來撰寫 spn 的一般用途函式，而 [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) 則是專門用來撰寫和註冊主機服務之簡單 spn 的特殊函式。

服務安裝程式通常會使用 [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) 函式來撰寫 spn，然後使用 [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) 函數來註冊服務的登入帳戶。 **DsGetSpn** 可執行下列功能。

-   以 <service class> / &lt; 主機服務的「主機」格式建立簡單 SPN &gt; 。
-   建立包含可複製服務所使用之「服務名稱」元件的複雜 SPN， &lt; &gt; 或在 &lt; &gt; 單一主機上區分服務之多個實例的「埠」元件。
-   建立單一 SPN，並將 " &lt; host &gt; " 元件設定為指定主機的名稱，或預設為本機電腦的名稱。
-   針對將在整個樹系的多部主機上執行的多個服務實例，建立 Spn 的陣列。 每個 SPN 都會指定服務實例的主機名稱。
-   針對將在相同主機上執行的多個服務實例，建立 Spn 的陣列。 每個 SPN 都會指定主機的名稱，以及服務實例的埠號碼。

[**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna)傳回的名稱陣列必須藉由呼叫 [**DsFreeSpnArray**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya)函數來釋出。

請注意， [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna)、 [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)和 [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) 函式不會驗證 spn 是否是唯一的。 因為如果用戶端出示的 SPN 不是唯一的，所以相互驗證會失敗，請在註冊 SPN 之前確認唯一性。 若要這樣做，請針對符合您 SPN 的 **servicePrincipalName** 屬性，搜尋通用類別目錄 (GC) 。 如需有關搜尋 GC 的詳細資訊，請參閱 [搜尋通用類別目錄](searching-global-catalog-contents.md)。

 

 




