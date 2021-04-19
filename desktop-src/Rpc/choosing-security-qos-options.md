---
title: 選擇安全性 QOS 選項
description: 安全性 QOS 選項會做為 SecurityQOS 參數的一部分傳遞給 RpcBindingSetAuthInfoEx 函數。 使用下列最佳做法。
ms.assetid: 43befe3d-079a-4389-a1ff-6bda90935769
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c286b516438eae78117ef8d73939c3b4bed396d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968114"
---
# <a name="choosing-security-qos-options"></a>選擇安全性 QOS 選項

安全性 QOS 選項會做為 *SecurityQOS* 參數的一部分傳遞給 [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) 函數。 使用下列最佳做法。

## <a name="use-mutual-authentication"></a>使用相互驗證

只有特定的安全性提供者才能使用真正的相互驗證：協商 (當協調 Kerberos) 、Kerberos 和 Schannel 時。 NTLM 不支援相互驗證。 使用相互驗證需要提供格式正確的伺服器主體名稱。 許多開發人員使用下列錯誤的安全性作法：系統會呼叫伺服器來要求其主體名稱 ([**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname)) ，然後使用該主體名稱盲目地要求相互驗證。 這種方法會打破相互驗證的整個概念;相互驗證的概念是，只會呼叫特定的伺服器，因為它們受信任可以剖析和處理您的資料。 使用剛剛所述的錯誤安全性作法，開發人員將其資料提供給任何聰明的人，以傳回其名稱。

例如，如果用戶端軟體應該只呼叫 Joe、Pete 或 Alice 帳戶下執行的伺服器，就應該呼叫 [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname) 函式，並檢查傳回的名稱。 如果是 Joe、Pete 或 Alice，應使用其伺服器主體名稱要求相互驗證。 這可確保兩個交談的一半都會移至相同的主體。

如果用戶端軟體應該只呼叫 Joe 帳戶下執行的服務，請直接撰寫 Joe 的伺服器主體名稱並進行呼叫。 如果伺服器不是 Joe，則呼叫會失敗。

許多時候，服務都是以 Windows 系統服務的方式執行，這表示它們是在電腦帳戶下執行。 仍建議使用相互驗證和建立伺服器主體名稱。

## <a name="use-the-lowest-impersonationtype-that-allows-the-call-to-go-through"></a>使用可讓呼叫進入的最低 ImpersonationType

這項最佳作法很容易理解。 即使使用相互驗證，請勿授與伺服器比所需更多的許可權;合法的伺服器可能已遭入侵，即使您傳送的資料在這種情況下遇到錯誤的情況，至少伺服器也不能代表您存取網路上的其他資料。 有些伺服器將會拒絕沒有足夠資訊的呼叫，以判斷呼叫端，也可能模擬呼叫端。 此外，請注意，某些通訊協定順序支援傳輸層級安全性 ([**ncacn \_ np**](/windows/desktop/Midl/ncacn-np) 和 [**ncalrpc**](/windows/desktop/Midl/ncalrpc)) 。 在這種情況下，如果您在建立系結控制碼時，透過 *NetworkOptions* 參數指定夠高的模擬等級，伺服器一律會模擬您。

最後，某些安全性提供者或傳輸可能會以透明方式將 ImpersonationType 與指定的層級相較之下。 開發程式時，請確定您嘗試使用預期的 ImpersonationType 進行呼叫，並檢查您是否在伺服器上取得較高的 ImpersonationType。

 

 