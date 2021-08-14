---
description: 提供機制來控制安全物件的存取。
ms.assetid: 5923cb4c-f663-40d2-989a-07d71ac475db
title: 認證相符控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac1a39cfc1d1ab819181e37c17328d6015a884f9ae1cce546643480351341b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117781491"
---
# <a name="mandatory-integrity-control"></a>認證相符控制

認證相符控制 (MIC) 提供一種機制來控制安全物件的存取。 這項機制除了任意存取控制之外，還會評估存取權，然後再對物件的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) 進行存取檢查， (DACL) 會進行評估。

MIC 使用完整性層級和強制性原則來評估存取權。 [*安全性主體*](/windows/desktop/SecGloss/s-gly) 和安全物件會被指派完整性層級，以決定其保護或存取層級。 例如，低完整性層級的主體無法寫入具有中度完整性層級的物件，即使該物件的 DACL 允許主體的寫入存取權也一樣。

Windows 定義四個完整性層級：低、中、高和系統。 標準使用者會收到中高許可權的使用者。 如果可執行檔的層級很低，您所建立的進程和您所建立的物件會收到您的完整性層級 (中或高) 或低;系統服務接收系統完整性。 系統會將缺少完整性標籤的物件視為「中」，這可防止低完整性程式碼修改未標記的物件。 此外，Windows 可確保以低完整性層級執行的進程無法取得與應用程式容器相關聯之進程的存取權。

## <a name="integrity-labels"></a>完整性標籤

完整性標籤會指定安全物件和安全性主體的完整性層級。 完整性標籤會以 [*完整性 sid*](/windows/desktop/SecGloss/i-gly)表示。 安全物件的完整性 SID 會儲存在其 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly) 中， (SACL) 。 SACL 包含 [**系統 \_ 強制 \_ 標籤 \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-system_mandatory_label_ace) [*存取控制專案*](/windows/desktop/SecGloss/a-gly) (ACE) ，其中包含完整性 SID。 任何沒有完整性 SID 的物件都會被視為具有中完整性。

安全性主體的完整性 SID 會儲存在其存取權杖中。 存取權杖可包含一或多個完整性 Sid。

如需有關已定義完整性 Sid 的詳細資訊，請參閱 [知名的 sid](well-known-sids.md)。

## <a name="process-creation"></a>處理序建立

當使用者嘗試啟動可執行檔時，系統會建立新的進程，並以最少的使用者完整性層級和檔案完整性層級建立。 這表示新的進程絕對不會以比可執行檔更高的完整性執行。 如果系統管理員使用者執行低完整性程式，則新進程的權杖會在低完整性層級執行。 這有助於保護從該程式碼所執行的惡意行為啟動不信任程式碼的使用者。 使用者資料（在一般的使用者完整性層級）是針對這個新進程進行寫入保護。

## <a name="mandatory-policy"></a>強制原則

安全物件之 SACL 中的 [**系統 \_ 強制 \_ 標籤 \_ ace**](/windows/desktop/api/Winnt/ns-winnt-system_mandatory_label_ace) ace 包含存取遮罩，可指定授與具有低於物件之完整性層級的主體存取權。 針對此存取遮罩定義的值為「 **系統 \_ 強制 \_ 標籤 \_ 否 \_ 寫入 \_**」、「 **系統 \_ 強制 \_ 標籤 \_ 否 \_ 讀取 \_**」和「 **系統 \_ 強制 \_ 標籤 \_ 不 \_ 執行 \_**」。 根據預設，系統會建立每個具有「 **系統 \_ 強制 \_ 標籤 \_ 無 \_ 寫入 \_**」存取遮罩的物件。

每個存取權杖也會指定在建立權杖時，由 [*本地安全機構*](/windows/desktop/SecGloss/l-gly) (LSA) 所設定的強制原則。 此原則是由與權杖相關聯的 [**權杖 \_ 強制 \_ 原則**](/windows/desktop/api/Winnt/ns-winnt-token_mandatory_policy) 結構所指定。 藉由呼叫 [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) 函數，並將 *TokenInformationClass* 參數的值設定為 **TokenMandatoryPolicy**，即可查詢此結構。

 

 
