---
description: Windows 安全性模型可讓核心交易管理員的呼叫端 (KTM) 控制交易、交易管理員、資源管理員和登錄物件的存取權。
ms.assetid: c9d51d4d-9f07-44d6-a2e1-4a47367cc4ae
title: KTM 安全性與存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed4e42c9aaf8498ff16ebd1d32f539fef5b54b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975874"
---
# <a name="ktm-security-and-access-rights"></a>KTM 安全性與存取權限

Windows 安全性模型可讓核心交易管理員的呼叫端 (KTM) 控制交易、交易管理員、資源管理員和登錄物件的存取權。 如需詳細資訊，請參閱 [存取控制模型](/windows/desktop/SecAuthZ/access-control-model)。 對於不在意安全性的應用程式，可以使用寬鬆的存取控制清單來建立交易 (Acl) ，讓任何資源管理員都能在交易上登記。

## <a name="transactions"></a>交易

當用戶端使用 [**OpenTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction) 函式時，系統會針對交易對象的安全描述項，檢查要求的存取權限。

交易對象的有效存取權限包括查詢和設定資訊、登錄和各種交易作業，以及 [標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights)的能力。 [**交易存取遮罩**](transaction-access-masks.md) 會列出交易的特定存取權限。

因為交易具有持久狀態，所以與 KTM 互動的 RMs 和 Tm 必須符合其復原的義務。 若無法履行這些義務，可能會導致資源流失（即使系統重新開機也不會清除）。 請考慮造成 KTM 取用核心資源的持續性洩漏或惡意程式碼的影響，直到導致系統失敗為止;在產生的重新開機之後，KTM 會讀取其記錄並重新建立所有的持續性物件，可能會導致相同的系統失敗重複發生。 以配額為基礎的節流將可防止來自 rogue 或行為不良的 RM 的持續性資源。 最後，您必須建立系統管理機制，才能偵測和更正這類持續性流失。

## <a name="transaction-managers"></a>交易管理員

當用戶端使用 [**OpenTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager) 函式時，系統會根據資源管理員物件的安全描述項來檢查要求的存取權限。

交易管理員物件的有效存取權限包括查詢和設定資訊、建立 RMs、復原和重新命名作業以及 [標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights)的能力。 [**交易管理員存取遮罩**](transaction-manager-access-masks.md) 會列出交易管理員的特定存取權限。

資源管理員可以使用嚴格的 Acl 來建立自己的交易管理員物件，以限制哪些資源管理員可以參與使用該交易管理員記錄的交易。

## <a name="resource-managers"></a>資源管理員

當用戶端使用 [**OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager) 函式時，系統會根據資源管理員物件的安全描述項來檢查要求的存取權限。

資源管理員物件的有效存取權限包括查詢和設定資訊、復原、登錄、註冊作業、傳播和復原作業，以及 [標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights)的能力。 [**Resource Manager 存取遮罩**](resource-manager-access-masks.md) 會列出資源管理員的特定存取權限。

如果您想要防止惡意程式碼攔截通知或強制執行特定交易結果，則資源管理員可以建立具有嚴格 Acl 的資源管理員物件。

## <a name="enlistments"></a>登記

當用戶端使用 [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) 函式時，系統會針對登錄物件的安全描述項，檢查要求的存取權限。

登錄物件的有效存取權限包括查詢和設定資訊、復原作業以及 [標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights)的能力。 [**登記存取遮罩**](enlistment-access-masks.md) 會列出登記的特定存取權限。

 

 
