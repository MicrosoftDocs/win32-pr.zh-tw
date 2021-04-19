---
title: NTLMSSP
description: NTLMSSP
ms.assetid: ae434165-4429-4ef0-b083-60abdfc50de0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706c788f103d3d616b5a3087522b5f06b417e972
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106984946"
---
# <a name="ntlmssp"></a>NTLMSSP

NTLMSSP （其驗證服務識別碼是 RPC \_ C \_ 驗證 \_ WINNT）是所有 DCOM 版本都提供的安全性支援提供者。 它會使用 NTLM 通訊協定進行驗證。 NTLM 永遠不會在驗證期間將使用者的密碼傳送至伺服器。 因此，在模擬期間，伺服器無法使用密碼來存取使用者可存取的網路資源。 只能存取本機資源。

NTLM 可在本機和跨電腦運作。 也就是說，如果用戶端和伺服器位於不同的電腦上，則 NTLM 仍然可以確保用戶端是其宣稱的身分。

使用 NTLM 時，用戶端的身分識別會以功能變數名稱、使用者名稱及密碼或權杖來表示。 當伺服器呼叫 [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket)時，會傳回用戶端的功能變數名稱和使用者名稱。 不過，當伺服器呼叫 [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)時，會傳回用戶端的權杖。 如果用戶端與伺服器之間沒有信任關係，而且伺服器具有與用戶端相同名稱和密碼的本機帳戶，則該帳戶將用來代表用戶端。

NTLM 支援跨執行緒和跨進程的相互驗證 (只能在本機) 。 如果用戶端在 \\ 呼叫 [**IClientSecurity：： SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)的情況下，以網域使用者的形式指定伺服器的主體名稱，則伺服器的身分識別必須符合該主體名稱，否則呼叫將會失敗。 如果用戶端指定 **Null**，則不會檢查伺服器的身分識別。

NTLM 另外支援在本機) 的委派模擬層級跨執行緒和跨進程 (。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 和安全性封裝](com-and-security-packages.md)
</dt> </dl>

 

 