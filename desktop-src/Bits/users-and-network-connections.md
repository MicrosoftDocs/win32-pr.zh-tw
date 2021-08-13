---
title: 使用者和網路連接
description: 只有當作業擁有者已登入且已建立網路連線時，BITS 才會傳送檔案。
ms.assetid: b31fc04f-8fa8-407f-9380-ca6b09589c46
keywords:
- 網路連接位
- 轉移工作位，擁有權
- 傳送作業位、擁有權、使用者帳戶
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 54e346590cac90b8d896a9a45c86aee5ae241d7d299bb055cf9ff55db88b8668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118679880"
---
# <a name="users-and-network-connections"></a>使用者和網路連接

只有當作業擁有者已登入且已建立網路連線時，BITS 才會傳送檔案。 BITS 會使用作業擁有者的安全性內容來處理傳送作業。 建立作業的使用者會被視為作業的擁有者。 不過，具有系統管理員許可權的使用者可以取得其他使用者工作的 [**擁有權**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) 。

當擁有者登出或網路連線遺失 (BITS 不會強制) 的網路連線時，BITS 會暫停工作。 當擁有者重新登入並建立網路連線時，BITS 會繼續執行作業。 建立網路連線之後，在 BITS 開始傳送資料之前，可能會有短暫的延遲。

如果遺失網路連線，其狀態為 [**bg \_ 作業 \_ 狀態 \_**](/windows/desktop/api/Bits/ne-bits-bg_job_state) 為 [已佇列] 或 [ **bg \_ 工作 \_ 狀態 \_ ]** 的所有工作都會移至 [bg] **\_ 工作 \_ 狀態 \_ 暫時性 \_ 錯誤** 狀態，並出現「 [bg \_ E \_ 網路 \_ 中斷](bits-return-values.md) 連線」錯誤碼。 建立網路連線時， **BG \_ 工作 \_ 狀態 \_ 暫時性 \_ 錯誤** 狀態中的所有工作（可能包含任何錯誤碼）都會移至 **bg \_ 工作 \_ 狀態 \_ 佇列** 狀態。

若要讓 BITS 偵測到使用者已登入，使用者必須使用下列其中一個互動式登入選項：

-   透過歡迎畫面登入。
-   登入終端機 [服務](../termserv/terminal-services-portal.md) 用戶端。
-   使用 [快速切換使用者](../shell/fast-user-switching.md)。
-   從 Windows 10 1607 版開始，請使用遠端 Powershell 從其他裝置登入。 如需詳細資訊，請參閱 [管理 PowerShell 遠端會話](using-windows-powershell-to-create-bits-transfer-jobs.md) 。

使用 **RunAs** 命令) 以另一位 (使用者的身分執行應用程式，並不是互動式登入;BITS 不會執行與指定使用者相關聯的工作。

LocalSystem、LocalService 和 NetworkService 系統帳戶一律會登入;因此，使用這些帳戶的服務所提交的作業一律會執行。 如需使用服務帳戶的相關資訊和限制，請參閱 [服務帳戶和 BITS](service-accounts-and-bits.md)。

作業擁有者可以提供協助程式權杖，以便在需要多個權杖才能完成傳輸的情況下使用，例如用於遠端主機的驗證。 如需詳細資訊，請參閱 [BITS 傳送工作的協助程式權杖](helper-tokens-for-bits-transfer-jobs.md) 。 在舊版 Windows 中，作業擁有者實際上必須擁有系統管理員許可權，才能啟動使用 helper 權杖的工作。 在 Windows 10 1607 版中，只要協助程式權杖沒有系統管理員功能，BITS 作業擁有者就可以在不是系統管理員的情況下設定 helper 權杖。 這將能透過讓背景下載或更新工具在具有較低權限的 NetworkService 帳戶 (而非具有系統管理員權限的帳戶) 下執行，來降低背景下載或更新工具的弱點數量。

具有 [受限制權杖](../secauthz/restricted-tokens.md) 的使用者 (包含限制 sid 的權杖) 無法建立或修改作業。
 

 