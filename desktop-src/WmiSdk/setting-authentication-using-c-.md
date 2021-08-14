---
description: 適用于 WMI 的 IWbemLocator：： ConnectServer 的主要工作之一，是將指標傳回至 IWbemServices proxy。
ms.assetid: bbff43b7-79f8-4c7b-a772-d3d962cf3859
ms.tgt_platform: multiple
title: 使用 c + + 設定驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7b0ef3bcd1e9908815c94dacc3815fec77eaea33f2da48119dbe3178563eae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315615"
---
# <a name="setting-authentication-using-c"></a>使用 c + + 設定驗證

適用于 WMI 的 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) 的主要工作之一，是將指標傳回至 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy。 透過 **IWbemServices** proxy，您就可以存取 WMI 基礎結構的功能。 不過， **iwbemservices** proxy 的指標具有用戶端應用程式進程的身分識別，而不是 **iwbemservices** 進程的身分識別。 因此，如果您嘗試以指標存取 **IWbemServices** ，您可以收到拒絕存取的程式碼，例如 **E \_ ACCESSDENIED**。 若要避免拒絕存取的錯誤，您必須使用 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) 介面的呼叫來設定新指標的身分識別。

提供者可以設定命名空間的安全性，如此就不會傳回任何資料，除非您在與該命名空間的連接中使用封包隱私權 (**PktPrivacy**) 。 這可確保資料會在網路上進行加密。 如果您嘗試設定較低的驗證等級，您將會收到拒絕存取的訊息。 如需詳細資訊，請參閱 [設定命名空間安全描述項](setting-namespace-security-descriptors.md)。

如需有關在腳本中設定驗證的詳細資訊，請參閱 [使用 VBScript 設定預設進程安全性層級](setting-the-default-process-security-level-using-vbscript.md)。

## <a name="setting-security-on-a-remote-iunknown-interface"></a>在遠端 IUnknown 介面上設定安全性

在某些情況下，需要更多的伺服器存取權，而不只是 proxy 的指標。 有時，您可能需要對 proxy 的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面進行安全連線。 您可以使用 **IUnknown** 來查詢遠端系統，以取得介面和其他必要的技術。

當 proxy 位於遠端電腦上時，伺服器會將 proxy 的 [**iunknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面呼叫委派給 **iunknown** 介面。 例如，如果您在 proxy 上呼叫 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，而要求的介面不是 proxy 的一部分，則 proxy 會將呼叫傳送至遠端伺服器。 接著，遠端伺服器會檢查是否有適當的介面支援。 如果伺服器支援介面，COM 會將新的 proxy 封送處理回用戶端，讓應用程式能夠使用新的介面。

如果用戶端沒有遠端伺服器的存取權限，但使用的是使用者的認證，就會發生問題。 在此情況下，在遠端伺服器上存取 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 的任何嘗試都會失敗。 Proxy 的最終版本也會失敗，因為目前的使用者沒有遠端伺服器的存取權。 在用戶端應用程式失敗最終的 proxy 發行之前，會有一或兩秒延遲的徵兆。 發生失敗的原因是，COM 嘗試使用目前使用者的預設安全性設定來存取遠端伺服器，而該設定未包含先允許存取伺服器的修改過的認證。 如需詳細資訊，請參閱 [在 IWbemServices 和其他 proxy 上設定安全性](setting-the-security-on-iwbemservices-and-other-proxies.md)。

若要避免連線失敗，請使用 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) ，在從 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)傳回的指標上明確設定安全性驗證。 您可以使用 **CoSetProxyBlanket** 來確定遠端伺服器會收到正確的驗證身分識別。

下列程式碼範例顯示如何使用 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) 來存取遠端 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面。


```C++
SEC_WINNT_AUTH_IDENTITY_W* pAuthIdentity = 
   new SEC_WINNT_AUTH_IDENTITY_W;
ZeroMemory(pAuthIdentity, sizeof(SEC_WINNT_AUTH_IDENTITY_W));

pAuthIdentity->User = new WCHAR[32];
StringCbCopyW(pAuthIdentity->User,sizeof(L"MyUser"),L"MyUser");
pAuthIdentity->UserLength = wcslen(pAuthIdentity->User);

pAuthIdentity->Domain = new WCHAR[32];
StringCbCopyW(pAuthIdentity->Domain,sizeof(L"MyDomain"),L"MyDomain");
pAuthIdentity->DomainLength = wcslen(pAuthIdentity->Domain);

pAuthIdentity->Password = new WCHAR[32];
pAuthIdentity->Password[0] = NULL;
pAuthIdentity->PasswordLength = wcslen( pAuthIdentity->Password);

pAuthIdentity->Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;

IWbemServices* pWbemServices = 0;

// Set proxy security
hr = CoSetProxyBlanket(pWbemServices, 
                       RPC_C_AUTHN_DEFAULT, 
                       RPC_C_AUTHZ_NONE, 
                       COLE_DEFAULT_PRINCIPAL, 
                       RPC_C_AUTHN_LEVEL_DEFAULT, 
                       RPC_C_IMP_LEVEL_IMPERSONATE, 
                       pAuthIdentity, 
                       EOAC_NONE 
);
if (FAILED(hr))
{
   cout << "Count not set proxy blanket. Error code = 0x"
        << hex << hr << endl;
   pWbemServices->Release();
   return 1;
}

// Set IUnknown security
IUnknown*    pUnk = NULL;
pWbemServices->QueryInterface(IID_IUnknown, (void**) &pUnk);

hr = CoSetProxyBlanket(pUnk, 
                       RPC_C_AUTHN_DEFAULT, 
                       RPC_C_AUTHZ_NONE, 
                       COLE_DEFAULT_PRINCIPAL, 
                       RPC_C_AUTHN_LEVEL_DEFAULT, 
                       RPC_C_IMP_LEVEL_IMPERSONATE, 
                       pAuthIdentity, 
                       EOAC_NONE 
);
if (FAILED(hr))
{
   cout << "Count not set proxy blanket. Error code = 0x"
        << hex << hr << endl;
   pUnk->Release();
   pWbemServices->Release();
   delete [] pAuthIdentity->User;
   delete [] pAuthIdentity->Domain;
   delete [] pAuthIdentity->Password;
   delete pAuthIdentity;   
   return 1;
}

// cleanup IUnknown
pUnk->Release();

//
// Perform a bunch of operations
//

// Cleanup
pWbemServices->Release();

delete [] pAuthIdentity->User;
delete [] pAuthIdentity->Domain;
delete [] pAuthIdentity->Password;

delete pAuthIdentity;
```



> [!Note]  
> 當您在 proxy 的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面上設定安全性時，COM 會建立一份無法釋放的 proxy，直到您呼叫 [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)為止。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 WMI 中設定驗證](setting-authentication-in-wmi.md)
</dt> </dl>

 

 
