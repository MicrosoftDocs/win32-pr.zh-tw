---
description: 原則模組是接收來自憑證服務之要求、評估這些要求，以及指定用來填滿這些要求之憑證的選擇性屬性的程式。
ms.assetid: 23d920ea-af62-42ce-ad48-c7a03ab55fc9
title: 原則模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6781a88ab714c402ea1670ac8c18ae4d80eb776e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945131"
---
# <a name="policy-modules"></a>原則模組

原則模組是接收來自憑證服務之要求、評估這些要求，以及指定用來填滿這些要求之憑證的選擇性屬性的程式。 原則模組會實作為 [*動態連結程式庫*](../secgloss/d-gly.md) ， (DLL) 。 原則模組可以使用 [ICertServerPolicy](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) 介面與憑證服務進行通訊。 憑證服務會透過直接 COM 呼叫來與原則模組進行通訊，或者，如果此模組不支援透過自動化的直接 COM 呼叫。

原則模組可查看現有的憑證屬性和擴充功能，也可能會查看要求屬性和屬性。 此外，原則模組可能會設定或修改憑證延伸和 "NotBefore" 和 "NotAfter" 屬性，以及憑證主體 (RDN) 的 [*相對辨別名稱*](../secgloss/r-gly.md) （受限於特定限制）。 原則模組最後會發出或拒絕 [*憑證要求*](../secgloss/c-gly.md) ，或將其保留為擱置中。

撰寫自訂原則模組之前，請考慮使用其中一個預設原則模組。 憑證服務企業 [*憑證授權單位*](../secgloss/c-gly.md) 單位 (CA) 和獨立 CA 都會隨附適當的預設原則模組。 企業和獨立的預設原則模組都會發出憑證要求 (雖然獨立的預設原則是將憑證擱置，直到系統管理員以手動方式發出) 為止。 企業憑證授權單位單位只能使用 Microsoft 提供的企業原則模組。

企業 CA 需要 Active Directory。 預設原則模組的其他功能包括憑證範本、 [*存取控制清單*](../secgloss/a-gly.md) (ACL) 安全性的憑證範本，以確保只會將要求發給已授權、預先定義的延伸模組新增至已發行的憑證，以及支援智慧卡網域登入憑證。

預設的獨立 CA 原則模組並不支援預設 enterprise 模組的許多功能，但它支援發行智慧卡憑證。 如需特定詳細資料，以及預設原則模組的最新功能，請參閱產品檔。

針對預設原則模組無法接受的安裝，憑證服務允許自訂原則模組。 如需詳細資訊，請參閱 [撰寫自訂原則模組](writing-custom-modules.md)。

 

 
