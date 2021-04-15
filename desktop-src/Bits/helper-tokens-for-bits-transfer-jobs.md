---
title: BITS 傳送工作的協助程式權杖
description: BITS 傳送工作的協助程式權杖
ms.assetid: f29f9870-e406-472b-9342-203def7453ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52925a6e0d5a9601e21848d514214bfb843f6246
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463684"
---
# <a name="helper-tokens-for-bits-transfer-jobs"></a>BITS 傳送工作的協助程式權杖

在 Windows Vista 中，背景智慧型傳送服務 (位) 服務可讓應用程式將單一安全性權杖與 BITS 傳送工作產生關聯。 BITS 傳送工作接著會使用此權杖進行驗證，以及存取本機和遠端資源。

在 Windows 7 中，BITS 服務會將額外的權杖與 BITS 傳送工作產生關聯。 您可以使用其他安全性權杖來設定 BITS 傳送作業，這是呼叫 BITS COM API 的應用程式所建立的模擬權杖。 此協助程式權杖模型可讓應用程式同時使用兩個不同的安全性權杖來存取本機檔案、用戶端憑證、遠端檔案和 proxy。 例如，會建立一個 BITS 傳送工作，將下載的資料寫入到特殊許可權的本機目錄，然後將低許可權網域身分識別提供給 HTTP 伺服器和 proxy 伺服器。

應用程式通常是 Windows 服務，會使用新的介面 [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)來指定協助程式權杖。 這個介面是由 BITS 工作物件所執行。 應用程式會呼叫 [**IBackgroundCopyJob：： QueryInterface**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) 以取得介面指標。 應用程式會模擬協助程式身分識別，並呼叫 [**IBitsTokenOptions：： SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) 將權杖傳遞給 BITS 服務。 然後，應用程式會使用 [**IBitsTokenOptions：： SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags)傳遞一組位旗標，以指定要套用權杖的資源。 應用程式會 (再次使用 **SetHelperTokenFlags** 來清除所有旗標，) 還原行為。 BITS 服務會將位旗標和權杖儲存在 BITS 傳送工作中。

當 BITS 傳送工作的擁有者登出時，BITS 服務會捨棄與傳送工作相關聯的任何協助程式權杖。 如果傳輸未完成，BITS 服務會將工作放在錯誤狀態，並以 **BG \_ E \_ 權杖 \_ 所需** 的錯誤碼來捨棄協助程式權杖。 用戶端應用程式可以藉由呼叫 [**IBitsTokenOptions：： SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) 來重新整理權杖，然後再繼續 BITS 傳送工作。 或者，用戶端應用程式可以使用 [**IBitsTokenOptions：： SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) 清除協助程式 token 旗標，然後繼續執行不含協助程式權杖的傳送作業。

同樣地，當終端機服務會話的擁有者登出時，BITS 服務必須捨棄該會話中的任何協助程式權杖，並將受影響的傳送工作放在錯誤狀態，並以 **BG \_ E \_ 權杖 \_ 所需** 的錯誤碼表示。

Helper 權杖模型需要變更 BITS 存取控制原則。 舊版的 BITS 會對每個方法呼叫執行存取檢查。 從 Windows 7 開始，必須在 [**IBackgroundCopyJob：： QueryInterface**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) 呼叫內執行存取檢查;否則，helper 權杖可能無法存取傳送工作。

> [!Note]  
> 較舊的執行實際上需要 BITS 使用者具有系統管理員許可權，才能設定協助程式權杖。 從 Windows 10 開始，版本1607、非系統管理員位的使用者可以使用 [**IBitsTokenOptions：： SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) ，在其所擁有的 BITS 工作上設定非系統管理員協助程式權杖。 這種變更可讓非系統管理員位使用者 (例如在 [NetworkService 帳戶](/windows/desktop/Services/networkservice-account) 下執行的背景下載程式服務) 來設定 helper 權杖。
>
> 明確地說，只要符合下列條件，就能讓沒有系統管理員許可權的使用者設定協助程式權杖：
>
> -   在 [**IBackgroundCopyJob：： QueryInterface**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) 呼叫期間，呼叫端的 THREAD'S token sid 與作業擁有者的使用者帳戶 sid 相同，而且
> -   當呼叫 [**IBitsTokenOptions：： SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) 時，helper 權杖沒有 (**網域 \_ 別名 \_ RID \_ 管理員**) 啟用的系統管理員 SID。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
</dt> </dl>

 

 