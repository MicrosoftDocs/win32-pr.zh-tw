---
description: COM + CRM 安全性考慮
ms.assetid: e212c847-b43b-43be-b089-82336551b89a
title: COM + CRM 安全性考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1052f9e8cf4f23dd80e2b4706b7e13c0f39a2aedd9b9a985da2d41101118467d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638728"
---
# <a name="com-crm-security-considerations"></a>COM + CRM 安全性考慮

CRM 記錄檔可能包含必須受到保護的機密資訊。 基於這個理由，如果在第一次建立 CRM 記錄檔時，伺服器應用程式是在互動式使用者以外的任何身分識別下執行，則 CRM 記錄檔只會受限於該使用者的安全性。 這項功能僅適用于 NTFS 檔案系統。 如果後續變更伺服器應用程式的身分識別，則不會自動變更 CRM 記錄檔的安全性資訊。 您可以使用現有的 Windows 管理工具，以手動方式進行變更。 替代方法是在 CRM 記錄檔處於「乾淨」狀態時刪除 CRM 記錄檔， (在伺服器應用程式) 的控制項關機之後，這是預期的情況。

在正常操作中，COM + 會建立 CRM 補償器元件，並呼叫 [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) 介面。 不過，擁有建立 CRM 補償器許可權的使用者可以在不適當的時間呼叫 **ICrmCompensator** 介面，可能會造成系統安全性問題。 為了協助防止這些安全性問題，系統管理員可以使用以角色為基礎的安全性，將 CRM 補償器元件限制為只有執行它的伺服器應用程式的身分識別。 如果元件是在程式庫應用程式中執行，則會包含伺服器應用程式的所有身分識別。

> [!Note]  
> 從 Windows server 2003 開始，為了協助防止從伺服器應用程式外部啟用，您可以藉由將 CRM 補償器元件標示為私用，進一步確保系統的安全。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 補償 Resource Manager 概念](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



