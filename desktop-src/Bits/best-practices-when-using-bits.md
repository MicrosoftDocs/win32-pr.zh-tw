---
title: 使用 BITS 的最佳作法
description: 本章節包含設計使用 BITS 的應用程式時應考慮的資訊。
ms.assetid: f4a09a80-2a85-4b59-b0fd-c23c128973f7
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: bbf69e75b99994eea3e8986d1be9920ff1a12bc5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931983"
---
# <a name="best-practices-when-using-bits"></a>使用 BITS 的最佳作法

本章節包含設計使用 BITS 的應用程式時應考慮的資訊。

## <a name="user-context-or-service-context"></a>使用者內容或服務內容

只有當作業的擁有者登入電腦 (使用者必須以互動方式登入) 時，BITS 才會傳送檔案。 BITS 不支援 **RunAs** 命令。 如需詳細資訊，請參閱 [使用者和網路連接](users-and-network-connections.md)。

如果您的應用程式不需要使用者的內容，請考慮改為以 LocalSystem、LocalService 或 NetworkService 的身分來撰寫服務。 這些系統帳戶一律會登入，因此傳送不會受限於使用者登出。 但是，如果您在建立作業時模擬使用者，則適用互動式登入規則。 如需詳細資訊，請參閱 [服務帳戶和 BITS](service-accounts-and-bits.md)。

## <a name="jobs-are-persistent"></a>作業是持續性的

作業會保留在佇列中，直到您呼叫 [**IBackgroundCopyJob：： Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) 或 [**IBackgroundCopyJob：： Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) 方法。 在您呼叫 **Complete** 之前，使用者無法使用作業中的檔案。 通常，您會在作業的狀態為 [ **bg \_ 作業 \_ 狀態 \_**] 時呼叫 [**完成**]，並在作業處於「 **Bg 作業」 \_ \_ 狀態 \_ 暫時性 \_ 錯誤** 或「 **Bg \_ 工作 \_ 狀態」 \_ 錯誤** 狀態且無法繼續進行時呼叫 **「取消」** 。

如果您未在90天內呼叫 [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) 方法或 [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) 方法 (預設 [JobInactivityTimeout](group-policies.md) 群組原則) ，則服務會取消作業。 您應該一律呼叫 **Complete** 或 **Cancel** 方法，而不是依賴 JobInactivityTimeout 原則來清除您的工作。 如果達到 MaxJobsPerUser 或 MaxJobsPerMachine 原則限制，佇列中剩餘的作業可能會讓使用者無法建立其他作業。

## <a name="when-to-use-foreground-or-background-priority"></a>使用前景或背景優先順序的時機

除非作業是時間緊迫的，或是使用者正在積極等候，否則您應該一律使用背景優先權。 不過，有時候您可能會想要從背景優先順序切換到前景優先順序，例如，當 proxy 或伺服器不支援內容約制標頭，或用戶端上的防毒軟體移除範圍標頭要求時。 切換為前景優先順序只適用于檔案大小小於 2 GB 的檔案。 如需範例，請參閱 [**IBackgroundCopyCallback：： JobError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) 方法的實作為。 另請注意，如果前景工作因為網路中斷連線或使用者登出而中斷，作業將會失敗，因為 BITS 會傳送範圍要求以嘗試從中斷的位置重新開機傳輸。

從 Windows 8 開始，您應該在目標伺服器不符合 [Bits 下載的 HTTP 需求](http-requirements-for-bits-downloads.md)時，設定以 **bits \_ 工作 \_ 屬性 \_ 動態 \_ 內容** 和 **BG \_ 作業 \_ 優先順序 \_ 前景** 的下載作業。 請記住，這會導致 BITS 必須從一開始 (就重新開機下載，例如，因為連線問題或系統重新開機) 。

如需可用優先順序和 BITS 如何使用優先權層級來排程工作的詳細資訊，請參閱 [**BG \_ 作業 \_ 優先順序**](/windows/desktop/api/Bits/ne-bits-bg_job_priority)。

## <a name="transient-and-fatal-errors"></a>暫時性和嚴重錯誤

有些錯誤是可復原的，有些則不是。 例如，「伺服器無法使用」錯誤是可復原的錯誤，且「拒絕存取」錯誤是嚴重錯誤。 BITS 可讓可復原的錯誤處於暫時性錯誤狀態，並在指定的間隔之後再次嘗試作業。 如果工作無法進行，BITS 會將作業移到嚴重的錯誤狀態。 使用 [**IBackgroundCopyJob：： SetMinimumRetryDelay**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay) 和 [**IBackgroundCopyJob：： SetNoProgressTimeout**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) 方法來控制 BITS 處理暫時性錯誤的方式。

針對前景工作，您應該限制讓作業保持暫時性錯誤狀態的時間量，並嘗試復原。 使用 [**SetNoProgressTimeout**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) 方法來限制作業停留在暫時性錯誤狀態的時間量，或強制工作進入嚴重錯誤狀態。 如果您讓作業嘗試復原，您應該使用 [**SetMinimumRetryDelay**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay) 方法，將重試延遲的最小值設定為60秒，或呼叫 [**IBackgroundCopyJob：： Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) 方法以重新開機作業。

如需詳細資訊，請參閱 [**BG \_ 工作 \_ 狀態**](/windows/desktop/api/Bits/ne-bits-bg_job_state)、 [BITS 作業的生命週期](life-cycle-of-a-bits-job.md)，以及 [處理錯誤](handling-errors.md)。

## <a name="measuring-network-bandwidth-usage"></a>測量網路頻寬使用量

BITS 可能會使用用戶端的網路介面卡來估計可用的網路頻寬。 因為 BITS 無法測量用戶端以外的頻寬，所以 BITS 可能會 congest WAN 連結。 若要減少 WAN 連結的擁塞，您可以使用 **MaxInternetBandwidth** 群組原則來限制用戶端所使用的頻寬量。 如需詳細資訊，請參閱 [網路頻寬](network-bandwidth.md) 和 [群組原則](group-policies.md)。

如果您撰寫的應用程式有許多用戶端將用來從指定的伺服器下載檔案，您應該考慮 staggers 下載要求的配置，這樣您就不會在要求中多載伺服器。

## <a name="setting-credentials-for-proxy-and-server-authentication"></a>設定 proxy 和伺服器驗證的認證

如果您預期 proxy 或伺服器需要使用者認證，您必須將認證提供給位。 若要指定認證，請呼叫 [**IBackgroundCopyJob2：： SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) 方法。 BITS 支援基本、摘要式、Negotiate、NTLM 和 Passport 驗證配置。

如需驗證的詳細資訊，請參閱 [驗證](authentication.md)。

## <a name="specifying-proxy-settings-for-user-accounts-and-service-accounts"></a>指定使用者帳戶和服務帳戶的 proxy 設定

依預設，BITS 會使用使用者的 Internet Explorer proxy 設定。 若要覆寫使用者的 Internet Explorer proxy 設定，請呼叫 [**IBackgroundCopyJob：： SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) 方法。

Internet Explorer 的 proxy 設定不適用於系統帳戶，因此除非採取其他設定步驟，否則預設 proxy 行為 (**BG \_ JOB \_ proxy \_ 使用方式 \_ PRECONFIG**) 將只能在 Web PROXY 自動探索通訊協定 (WPAD) 部署中正確運作。 如果您的應用程式是以 LocalSystem、LocalService 或 NetworkService 身分執行的服務，請考慮在 BITS 工作上設定協助程式權杖，或藉由呼叫 [**IBackgroundCopyJob：： SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) 與 **BG \_ 工作 \_ proxy 使用覆 \_ \_ 寫** 來明確設定正確的 proxy 設定。 或者，您可以使用 BitsAdmin.exe 的 **/Util/SetIEProxy** 交換器來設定 LocalSystem、LocalService 或 NetworkService 系統帳戶 Internet Explorer proxy 設定。 如需詳細資訊，請參閱 [BitsAdmin 工具](bitsadmin-tool.md)。

BITS 無法辨識使用 Proxycfg.exe 檔所設定的 proxy 設定。

從 Windows 10 2018 年10月更新 (10.0;組建 17763) ，BITS 會使用 WinHttp 與 AUTOMATIC_PROXY 搭配使用的相同 proxy 順序。 當指定 BG_JOB_PROXY_USAGE_PRECONFIG 時，BITS 會使用這個更相容的順序。 BG_JOB_PROXY_USAGE_PRECONFIG 是指定 HTTP PROXY 的預設值。

## <a name="specifying-user-specific-settings-for-authenticating-proxies"></a>指定驗證 proxy 的使用者特定設定

如果您在需要 proxy 驗證的環境中使用 BITS，但在電腦的網路網域中，以沒有可用 NTLM 或 Kerberos 認證的帳戶執行時，您必須採取額外的步驟，以使用在網域上具有認證的另一個使用者帳戶的認證來正確進行驗證。 當您的位程式碼以系統服務（如 LocalService、NetworkService 或 LocalSystem）執行時，這是常見的案例，因為這些帳戶沒有可用的 NTLM 或 Kerberos 認證。

如需有關驗證如何在此案例中運作的詳細資訊，請參閱 [驗證。](authentication.md)

## <a name="scalability"></a>延展性

如果佇列中有超過100個工作，根據作業的組成，效能可能會開始降低。 BITS 使用 [MaxJobsPerMachine](group-policies.md) 原則設定，對佇列中的作業數目強加硬性限制。 應用程式應該將其工作的數目限制為約10，如此一來，多個應用程式的機率將會降低超過 100-工作的指導方針。 通常，具有大量工作要提交的應用程式會先提交10個工作，然後在每個作業完成時一次提交一個工作。

作業中的檔案數目也應該限制為最多10個檔案。 如果您想要傳輸大量檔案來進行作業，請考慮改為建立包含所有檔案的封包檔。

## <a name="http-headers-can-be-in-any-case"></a>HTTP 標頭可以在任何情況下

HTTP 標準一直說過，HTTP 標頭必須被視為不區分大小寫 (RFC 7230 區段 3.2) 。 最新的 HTTP 標準（RFC 7540）會更進一步，並指出 HTTP/2 流量必須將標頭與不區分大小寫的標頭進行比較，且必須以小寫 6540 (的 8.1.2) 區段來呈現標頭。 即使以非案例標頭傳送流量，proxy 也可以選擇強制將標頭設為小寫。

## <a name="avoiding-personally-identifiable-information-pii"></a>避免個人識別資訊 (PII) 

具有系統管理員許可權的所有使用者都可以看到包含工作顯示名稱和描述和檔案名的 BITS 作業。 它們也可以新增至 Windows 遙測。 您應該避免將機密資料 (，例如在工作詳細資料中) 使用者的名稱。
