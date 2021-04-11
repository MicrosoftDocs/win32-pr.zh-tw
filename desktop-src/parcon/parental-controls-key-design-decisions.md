---
description: 家長監護主要設計決策
ms.assetid: 0b41cf81-0770-4408-97a8-a178fae78d23
title: 家長監護主要設計決策
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39cb4be775a3380cb9fe7aa677362df31a2dc453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027464"
---
# <a name="parental-controls-key-design-decisions"></a>家長監護主要設計決策

開發 Windows Vista 家長監護的主要設計決策包括：

## <a name="essential-dependency-on-windows-vista-user-account-control-uac-feature"></a>Windows Vista 使用者帳戶控制 (UAC) 功能的必要相依性

Windows Vista 家長監護的一項重要決策，就是要依賴新的使用者帳戶控制 (UAC) 功能，來為受控制的使用者執行離線限制時特別需要的精簡許可權帳戶身分識別。 如需 UAC 的詳細資訊，請參閱 [Windows vista 和 Windows Server 2008 開發人員故事： Windows Vista 應用程式開發需求的使用者帳戶控制 (UAC) ](/previous-versions/aa905330(v=msdn.10))。 總而言之，具有系統管理員許可權的每個帳戶實際上都有許可權可執行流覽記錄資料和設定原則的父系或守護者角色。 家長監護只能設定在標準許可權的使用者上 (先前稱為最低許可權的使用者帳戶，或 LUAs) ，因為他們無法使用存取控制清單來改變記錄檔和設定， (Acl) 僅供系統管理員進行寫入。 換句話說：

-   父系或監護人身分識別會隱含地等於具有系統管理員許可權的帳戶。
-   Parentally 控制的使用者必須是標準使用者。

## <a name="nearly-all-settings-are-available-by-apis"></a>幾乎所有設定都可由 Api 取得

除了評等系統定義以外的專案之外，也可以透過公開的 Api 修改可由家長監護消費者介面操作的設定。 為了改變設定，程式必須有必要的許可權，才能變更設定，如上述的 UAC 所述。

## <a name="windows-vista-parental-controls-is-a-consumer-only-technology"></a>Windows Vista 家長監護控制項是一種僅取用者的技術

Windows Vista 家長監護不適合與網域帳戶搭配使用。 作為取用者技術，家長監護不會部署在 Windows Vista 的商務 Sku 中。 如果電腦已加入網域，則會隱藏家庭安全使用者介面連結。

系統會提供一種機制來公開已加入網域之案例的功能，但只有非網域的使用者帳戶可以使用家長監護來設定。

 

 
